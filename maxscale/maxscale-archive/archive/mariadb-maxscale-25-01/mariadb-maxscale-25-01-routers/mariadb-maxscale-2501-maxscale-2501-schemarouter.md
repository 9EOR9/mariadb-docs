# MaxScale 25.01 SchemaRouter

## SchemaRouter

The SchemaRouter provides an easy and manageable sharding solution by\
building a single logical database server from multiple separate ones. Each\
database is shown to the client and queries targeting unique databases are\
routed to their respective servers. In addition to providing simple\
database-based sharding, the schemarouter also enables cross-node\
session variable usage by routing all queries that modify the session to all\
nodes.

By default the SchemaRouter assumes that each database and table is only located\
on one server. If it finds the same database or table on multiple servers, it\
will close the session with the following error:

```
ERROR 5000 (DUPDB): Error: duplicate tables found on two different shards.
```

The exception to this rule are the system tables `mysql`, `information_schema`,`performance_schema`, `sys` that are never treated as duplicates.

If duplicate tables are expected, use the[ignore\_tables\_regex](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#ignore_tables_regex) parameter to control which\
duplicate tables are allowed. To disable the duplicate database detection, use`ignore_tables_regex=.*`. Starting with MaxScale 25.01, the detection of\
duplicate tables can be turned off with `allow_duplicates=true`.

Schemarouter compares table and database names case-insensitively. This means\
that the tables `test.t1` and `test.T1` are assumed to refer to the same table.

The main limitation of SchemaRouter is that aside from session variable writes\
and some specific queries, a query can only target one server. This means that\
queries which depend on results from multiple servers give incorrect results.\
See [Limitations](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#limitations) for more information.

From 2.3.0 onwards, SchemaRouter is capable of limited table family sharding.

Older versions of MaxScale required that the `auth_all_servers` parameter was\
enabled in order for the schemarouter services to load the authentication data\
from all servers instead of just one server. Starting with MaxScale 24.02, the\
schemarouter automatically fetches the authentication data from all servers and\
joins it together. At the same time, the `auth_all_servers` parameter has been\
deprecated and is ignored if present in the configuration.

* [SchemaRouter](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#schemarouter)
  * [Routing Logic](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#routing-logic)
    * [Custom SQL Commands](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#custom-sql-commands)
    * [Database Mapping](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#database-mapping)
  * [Configuration](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#configuration)
  * [Settings](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#settings)
    * [allow\_duplicates](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#allow_duplicates)
    * [ignore\_tables](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#ignore_tables)
    * [ignore\_tables\_regex](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#ignore_tables_regex)
    * [max\_sescmd\_history](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#max_sescmd_history)
    * [disable\_sescmd\_history](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#disable_sescmd_history)
    * [refresh\_databases](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#refresh_databases)
    * [refresh\_interval](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#refresh_interval)
    * [max\_staleness](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#max_staleness)
  * [Table Family Sharding](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#table-family-sharding)
  * [Router Diagnostics](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#router-diagnostics)
  * [Module commands](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#module-commands)
    * [invalidate SERVICE](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#invalidate-service)
    * [clear SERVICE](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#clear-service)
  * [Limitations](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#limitations)
  * [Examples](mariadb-maxscale-2501-maxscale-2501-schemarouter.md#examples)

### Routing Logic

* If a command modifies the session state by modifying any session or user\
  variables, the query is routed to all nodes. These statements include `SET`\
  statements as well as any other statements that modify the behavior of the\
  client.
* If a client changes the default database after connecting, either with a `USE <db>` query or a `COM_INIT_DB` command, the query is routed to all servers\
  that contain the database. This same logic applies when a client connects with\
  a default database: the default database is set only on servers that actually\
  contain it.
* If a query targets one or more tables that the schemarouter has discovered\
  during the database mapping phase, the query is only routed if a server is\
  found that contains all of the tables that the query uses. If no such server\
  is found, the query is routed to the server that was previously used or to the\
  first available backend if none have been used. If a query uses a table but\
  doesn't define the database it is in, it is assumed to be located on the\
  default database of the connection.
* If a query targets a table or a database that is present on all nodes\
  (e.g. `information_schema`) and the connection is using a default database,\
  the query is routed based on the default database. This makes it possible to\
  control where queries that do match a specific node are routed. If the\
  connection is not using a default database, the query is routed based solely\
  on the tables it contains.
* If a query uses a table that is unknown to the schemarouter or executes a\
  command that doesn't target a table, the query is routed to a server contains\
  the current active default database. If the connection does not have a default\
  database, the query is routed to the backend that was last used or to the\
  first available backend if none have been used. If the query contains a\
  routing hint that directs it to a server, the query is routed there.

This means that all administrative commands, replication related command as\
well as certain transaction control statements (XA transaction) are routed to\
the first available server in certain cases. To avoid problems, use routing\
hints to direct where these statements should go.

* Starting with MaxScale 6.4.5, transaction control commands (`BEGIN`, `COMMIT`\
  and `ROLLBACK`) are routed to all nodes. Older versions of MaxScale routed the\
  queries to the first available backend. This means that cross-shard\
  transactions are technically possible but, without external synchronization,\
  the transactions are not guaranteed to be globally consistent.
* `LOAD DATA LOCAL INFILE` commands are routed to the first available server\
  that contains the tables listed in the query.

#### Custom SQL Commands

To check how databases and tables map to servers, execute the special query`SHOW SHARDS`. The query does not support any modifiers such as `LIKE`.

```
show shards;

Database |Server       |
---------|-------------|
db1.t1   |MyServer1    |
db1.t2   |MyServer1    |
db2.t1   |MyServer2    |
```

The schemarouter will also intercept the `SHOW DATABASES` command and generate\
it based on its internal data. This means that newly created databases will not\
show up immediately and will only be visible when the cached data has been\
updated.

#### Database Mapping

The schemarouter maps each of the servers to know where each database and table\
is located. As each user has access to a different set of tables and databases,\
the result is unique to the username and the set of servers that the service\
uses. These results are cached by the schemarouter. The lifetime of the cached\
result is controlled by the `refresh_interval` parameter.

When a server needs to be mapped, the schemarouter will route a query to each of\
the servers using the client's credentials. While this query is being executed,\
all other sessions that would otherwise share the cached result will wait for\
the update to complete. This waiting functionality was added in MaxScale 2.4.19,\
older versions did not wait for existing updates to finish and would perform\
parallel database mapping queries.

### Configuration

Here is an example configuration of the schemarouter:

```
[Shard-Router]
type=service
router=schemarouter
servers=server1,server2
user=myuser
password=mypwd
```

The module generates the list of databases based on the servers parameter\
using the connecting client's credentials. The user and password parameters\
define the credentials that are used to fetch the authentication data from\
the database servers. The credentials used only require the same grants as\
mentioned in the configuration documentation.

The list of databases is built by sending a SHOW DATABASES query to all the\
servers. This requires the user to have at least USAGE and SELECT grants on\
the databases that need be sharded.

If you are connecting directly to a database or have different users on some\
of the servers, you need to get the authentication data from all the\
servers. You can control this with the `auth_all_servers` parameter. With\
this parameter, MariaDB MaxScale forms a union of all the users and their\
grants from all the servers. By default, the schemarouter will fetch the\
authentication data from all servers.

For example, if two servers have the database `shard` and the following\
rights are granted only on one server, all queries targeting the database`shard` would be routed to the server where the grants were given.

```
# Execute this on both servers
CREATE USER 'john'@'%' IDENTIFIED BY 'password';

# Execute this only on the server where you want the queries to go
GRANT SELECT,USAGE ON shard.* TO 'john'@'%';
```

This would in effect allow the user 'john' to only see the database 'shard'\
on this server. Take notice that these grants are matched against MariaDB\
MaxScale's hostname instead of the client's hostname. Only user\
authentication uses the client's hostname and all other grants use MariaDB\
MaxScale's hostname.

### Settings

#### `allow_duplicates`

* Type: [boolean](../mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-configuration-guide.md)
* Mandatory: No
* Dynamic: Yes
* Default: false

If enabled, the detection of duplicated tables on shards is not done.

This parameter was added in MaxScale 25.01 and it is a more convenient and\
efficient way to disable the duplicate table detection that previously was only\
possible with `ignore_tables_regex=.*`.

#### `ignore_tables`

* Type: stringlist
* Mandatory: No
* Dynamic: Yes
* Default: `""`

List of full table names (e.g. db1.t1) to ignore when checking for duplicate\
tables. By default no tables are ignored.

This parameter was once called `ignore_databases`.

#### `ignore_tables_regex`

* Type: [regex](../mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-configuration-guide.md)
* Mandatory: No
* Dynamic: No
* Default: `""`

A [PCRE2 regular expression](../mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-configuration-guide.md)\
that is matched against database names when checking for duplicate databases.\
By default no tables are ignored.

The following configuration ignores duplicate tables in the databases `db1` and `db2`,\
and all tables starting with "t" in `db3`.

```
[Shard-Router]
type=service
router=schemarouter
servers=server1,server2
user=myuser
password=mypwd
ignore_tables_regex=^db1|^db2|^db3\.t
```

This parameter was once called `ignore_databases_regex`.

#### `max_sescmd_history`

This parameter has been moved to[the MaxScale core](../mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-configuration-guide.md)\
in MaxScale 6.0.

#### `disable_sescmd_history`

This parameter has been moved to[the MaxScale core](../mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-configuration-guide.md)\
in MaxScale 6.0.

#### `refresh_databases`

* Type: [boolean](../mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-configuration-guide.md)
* Mandatory: No
* Dynamic: No
* Default: `false`

Enable database map refreshing mid-session. These are triggered by a failure to\
change the database i.e. `USE ...` queries. This feature is disabled by default.

Before MaxScale 6.2.0, this parameter did nothing. Starting with the 6.2.0\
release of MaxScale this parameter now works again but it is disabled by default\
to retain the same behavior as in older releases.

#### `refresh_interval`

* Type: [duration](../mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-configuration-guide.md)
* Mandatory: No
* Dynamic: Yes
* Default: `300s`

The minimum interval between database map refreshes in seconds. The default\
value is 300 seconds.

The interval is specified as documented[here](../mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-configuration-guide.md). If no explicit unit\
is provided, the value is interpreted as seconds in MaxScale 2.4. In subsequent\
versions a value without a unit may be rejected. Note that since the granularity\
of the intervaltimeout is seconds, a timeout specified in milliseconds will be rejected,\
even if the duration is longer than a second.

#### `max_staleness`

* Type: [duration](../mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-configuration-guide.md)
* Mandatory: No
* Dynamic: Yes
* Default: 150s

The time how long stale database map entries can be used while an update is in\
progress. When a database map entry goes stale, the next connection to be\
created will start an update of the database map. While this update is ongoing,\
other connections can use the stale entry for up to `max_staleness` seconds. If\
this limit is exceeded and the update still hasn't completed, new connections\
will instead block and wait for the update to finish.

This feature was added in MaxScale 23.08.0. Older versions of MaxScale\
always waited for the update to complete when the database map entry\
went stale.

### Table Family Sharding

This functionality was introduced in 2.3.0.

If the same database exists on multiple servers, but the database contains different\
tables in each server, SchemaRouter is capable of routing queries to the right server,\
depending on which table is being addressed.

As an example, suppose the database `db` exists on servers _server1_ and _server2_, but\
that the database on _server1_ contains the table `tbl1` and on _server2_ contains the\
table `tbl2`. The query `SELECT * FROM db.tbl1` will be routed to _server1_ and the query`SELECT * FROM db.tbl2` will be routed to _server2_. As in the example queries, the table\
names must be qualified with the database names for table-level sharding to work.\
Specifically, the query series below is not supported.

```
USE db;
SELECT * FROM tbl1; // May be routed to an incorrect backend if using table sharding.
```

### Router Diagnostics

The `router_diagnostics` output for a schemarouter service contains the\
following fields.

* `shard_map_hits`: Cache hits for the shard map cache.
* `shard_map_misses`: Cache misses for the shard map cache.

In MaxScale 24.02, the `queries` `sescmd_percentage`, `longest_sescmd_chain`,`times_sescmd_limit_exceeded`, `longest_session`, `shortest_session` and`average_session` statistics have been replaced by core service statistics.

### Module commands

Read [Module Commands](../mariadb-maxscale-25-01-reference/mariadb-maxscale-2501-maxscale-2501-module-commands.md) documentation for\
details about module commands.

The schemarouter supports the following module commands.

#### `invalidate SERVICE`

Invalidates the database map cache of the given service. This can be used to schedule\
the updates to the database maps to happen at off-peak hours by configuring a\
high value for `refresh_interval` and invalidating the cache externally.

#### `clear SERVICE`

Clears the database map cache of the given service. This forces new connections\
to use a freshly retrieved entry.

If the set of databases and tables in each shard is very large, the update can\
take some time. If there are stale cache entries and `max_staleness` is\
configured to be higher than the time it takes to update the database map, the\
invalidation will only slow down one client connection that ends up doing the\
update. When the cache is cleared completely, all clients will have to wait for\
the update to complete. In general, cache invalidation should be preferred over\
cache clearing.

### Limitations

* Cross-database queries (e.g. `SELECT column FROM database1.table UNION select column FROM database2.table`) are not properly supported. Such queries are routed either to the\
  first explicit database in the query, the current database in use or to the first\
  available database, depending on which succeeds.
* Without a default database, queries that do not use fully qualified table\
  names and which do not modify the session state (e.g. `SELECT * FROM t1`) will\
  be routed to the first available server. This includes queries such as explicit\
  transaction commands (`BEGIN`, `COMMIT`, `ROLLBACK`), all non-table `CREATE`\
  commands (`CREATE DATABASE`, `CREATE SEQUENCE`) as well as any `SELECT`\
  statements that do not directly refer to a table. `CREATE` commands should be\
  done directly on the node or the router should be equipped with the hint filter\
  and a routing hint should be used. Queries that modify the session state\
  (e.g. `SET autocommit=1`) will be routed to all servers regardless of the\
  default database. For explicit transactions, the recommended way is to use `SET autocommit=0` to start a transaction and `SET autocommit=1` to commit it,\
  otherwise routing hints are required to correctly route the transaction control\
  commands. [MXS-4467](https://jira.mariadb.org/browse/MXS-4467) changed the\
  routing of transaction control commands to route them to all servers used by the\
  schemarouter.
* SELECT queries that modify session variables are not supported because uniform results\
  cannot be guaranteed. If such a query is executed, the behavior of the router is\
  undefined. To work around this limitation, the query must be executed in separate parts.
* If a query targets a database the SchemaRouter has not mapped to a server, the\
  query will be routed to the first available server. This possibly returns an\
  error about database rights instead of a missing database.
* Prepared statement support is limited. PREPARE, EXECUTE and DEALLOCATE are routed to the\
  correct backend if the statement is known and only requires one backend server. EXECUTE\
  IMMEDIATE is not supported and is routed to the first available backend and may give\
  wrong results. Similarly, preparing a statement from a variable (e.g. `PREPARE stmt FROM @a`) is not supported and may be routed wrong.
* `SHOW DATABASES` is handled by the router instead of routed to a server. The router only\
  answers correctly to the basic version of the query. Any modifiers such as `LIKE` are\
  ignored. Starting with MaxScale 22.08, the database names will always be in lowercase.
* `SHOW TABLES` is routed to the server with the current database. If using\
  table-level sharding, the results will be incomplete. Similarly, `SHOW TABLES FROM db1` is routed to the server with database `db1`, ignoring table\
  sharding. Use `SHOW SHARDS` to get results from the router itself. Starting with\
  MaxScale 22.08, the database names will always be in lowercase.
* `USE db1` is routed to the server with `db1`. If the database is divided to multiple\
  servers, only one server will get the command.

### Examples

[Here](../mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-schemarouter-simple-sharding-with-two-servers.md) is a small tutorial on how\
to set up a sharded database.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
