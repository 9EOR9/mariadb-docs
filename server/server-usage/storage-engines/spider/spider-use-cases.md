# Spider Use Cases

## Introduction

This article will cover simple working examples for some standard use cases for Spider. The example will be illustrated using a sales opportunities table to be consistent throughout. In some cases the actual examples will be contrived but are used to illustrate the varying syntax options.

## Basic setup

Have 3 or more servers available and Install MariaDB on each of these servers:

* spider server which will act as the front end server hosting the spider storage engine.
* backend1 which will act as a backed server storing data
* backend2 which will act as a second backend server storing data

Follow the instructions [here](spider-storage-engine-overview.md#installing) to enable the Spider storage engine on the spider server:

```sql
INSTALL SONAME 'ha_spider';
```

### Setting the SUPER privilege for the Spider user on data nodes or alternatives to avoid privilege issues

When explicitly setting the [spider\_internal\_sql\_log\_off](spider-system-variables.md#spider_internal_sql_log_off) system variable, please note that Spider will execute matching [SET SQL\_LOG\_OFF](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#sql_log_off) statements on each of the data nodes. It will attempt to do this on the data nodes using the [SUPER](../../../reference/sql-statements/account-management-sql-statements/grant.md#super) privilege, which thus requires one to grant this privilege to the Spider user on the data nodes.

If the Spider user on the data note is not configured with the SUPER privilege, you may encounter issues when working with Spider tables like ERROR 1227 (42000): Access denied for the missing SUPER privilege. To avoid this, don't explicitly set spider\_internal\_sql\_log\_off, or set it to -1, or grant the SUPER privilege to the Spider user on the data node.

### Create accounts for spider to connect with on backend servers

Spider needs a remote connection to the backend server to actually perform the remote query. So this should be setup on each backend server. In this case 172.21.21.2 is the ip address of the spider node limiting access to just that server.

```
backend1> mysql
grant all on test.* to spider@'172.21.21.2' identified by 'spider';
backend2> mysql
grant all on test.* to spider@'172.21.21.2' identified by 'spider';
```

Now verify that these connections can be used from the spider node (here 172.21.21.3 = backend1 and 172.21.21.4 = backend2):

```
spider> mysql -u spider -p -h 172.21.21.3 test
spider> mysql -u spider -p -h 172.21.21.4 test
```

### Create table on backend servers

The table definition should be created in the test database on both backend1 and backend2 servers:

```sql
create table opportunities (
id int,
accountName varchar(20),
name varchar(128),
owner varchar(7),
amount decimal(10,2),
closeDate date,
stageName varchar(11),
primary key (id),
key (accountName)
) engine=InnoDB;
```

### Create server entries on spider server

While the connection information can also be specified inline in the comment or (from [MariaDB 10.8.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-8-series/mariadb-1081-release-notes)) as table options, it is cleaner to define a server object representing each remote backend server connection:

```sql
create server backend1 foreign data wrapper mysql options 
(host '172.21.21.3', database 'test', user 'spider', password 'spider', port 3306);
create server backend2 foreign data wrapper mysql options 
(host '172.21.21.4', database 'test', user 'spider', password 'spider', port 3306);
```

#### Unable to Connect Errors

Bear in mind, if you ever need to remove, recreate or otherwise modify the server definition for any reason, you need to also execute a [FLUSH TABLES](../../../reference/sql-statements/administrative-sql-statements/flush-commands/flush.md) statement. Otherwise, Spider continues to use the old server definition, which can result in queries raising the error

```sql
Error 1429: Unable to connect to foreign data source
```

If you encounter this error when querying Spider tables, issue a [FLUSH TABLES](../../../reference/sql-statements/administrative-sql-statements/flush-commands/flush.md) statement to update the server definitions.

```
FLUSH TABLES;
```

## Use case 1: remote table

In this case, a spider table is created to allow remote access to the opportunities table hosted on backend1. This then allows for queries and remote dml into the backend1 server from the spider server:

```sql
create table opportunities (
id int,
accountName varchar(20),
name varchar(128),
owner varchar(7),
amount decimal(10,2),
closeDate date,
stageName varchar(11),
primary key (id),
key (accountName)
) engine=spider comment='wrapper "mysql", srv "backend1" , table "opportunities"';
```

## Use case 2: sharding by hash

See also `[hash-partitioning-type](../../../server-management/partitioning-tables/partitioning-types/hash-partitioning-type.md)`.

In this case a spider table is created to distribute data across backend1 and backend2 by hashing the id column. Since the id column is an incrementing numeric value the hashing will ensure even distribution across the 2 nodes.

```sql
create table opportunities (
id int,
accountName varchar(20),
name varchar(128),
owner varchar(7),
amount decimal(10,2),
closeDate date,
stageName varchar(11),
primary key (id),
key (accountName)
) engine=spider COMMENT='wrapper "mysql", table "opportunities"'
 PARTITION BY HASH (id)
(
 PARTITION pt1 COMMENT = 'srv "backend1"',
 PARTITION pt2 COMMENT = 'srv "backend2"'
) ;
```

## Use case 3: sharding by range

See also `[range-partitioning-type](../../../server-management/partitioning-tables/partitioning-types/range-partitioning-type.md)`.

In this case a spider table is created to distribute data across backend1 and backend2 based on the first letter of the accountName field. All accountNames that start with the letter L and prior will be stored in backend1 and all other values stored in backend2. Note that the accountName column must be added to the primary key which is a requirement of MariaDB partitioning:

```sql
create table opportunities (
id int,
accountName varchar(20),
name varchar(128),
owner varchar(7),
amount decimal(10,2),
closeDate date,
stageName varchar(11),
primary key (id, accountName),
key(accountName)
) engine=spider COMMENT='wrapper "mysql", table "opportunities"'
 PARTITION BY range columns (accountName)
(
 PARTITION pt1 values less than ('M') COMMENT = 'srv "backend1"',
 PARTITION pt2 values less than (maxvalue) COMMENT = 'srv "backend2"'
) ;
```

## Use case 4: sharding by list

See also `[list-partitioning-type](../../../server-management/partitioning-tables/partitioning-types/list-partitioning-type.md)`.

In this case a spider table is created to distribute data across backend1 and backend2 based on specific values in the owner field. Bill, Bob, and Chris will be stored in backend1 and Maria and Olivier stored in backend2. Note that the owner column must be added to the primary key which is a requirement of MariaDB partitioning:

```sql
create table opportunities (
id int,
accountName varchar(20),
name varchar(128),
owner varchar(7),
amount decimal(10,2),
closeDate date,
stageName varchar(11),
primary key (id, owner),
key(accountName)
) engine=spider COMMENT='wrapper "mysql", table "opportunities"'
 PARTITION BY list columns (owner)
(
 PARTITION pt1 values in ('Bill', 'Bob', 'Chris') COMMENT = 'srv "backend1"',
 PARTITION pt2 values in ('Maria', 'Olivier') COMMENT = 'srv "backend2"'
) ;
```

With [MariaDB 10.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/what-is-mariadb-102) the following partition clause can be used to specify a default partition for all other values, however this must be a distinct partition / shard:

```sql
PARTITION partition_name DEFAULT
```

For a complete list of partition types, see `[partitioning-types](../../../server-management/partitioning-tables/partitioning-types/README.md)`.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
