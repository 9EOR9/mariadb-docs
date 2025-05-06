
# Upgrading from MySQL to MariaDB

For [all practical purposes](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/compatibility-and-differences/mariadb-vs-mysql-compatibility), you can view MariaDB as an upgrade of MySQL:


* Before upgrading, please [check if there are any known incompatibilities](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/compatibility-and-differences/mariadb-vs-mysql-compatibility) between your MySQL release and the MariaDB release you want to move to.
* In particular, note that the [JSON type](../../../../reference/data-types/string-data-types/json.md) in MariaDB is a LONGTEXT, while in MySQL it's a binary type. See [Making MariaDB understand MySQL JSON](https://mariadb.org/making-mariadb-understand-mysql-json/).
* If you are using MySQL 8.0 or above, you have to use [mysqldump](../../../../clients-and-utilities/legacy-clients-and-utilities/mysqldump.md) to move your database to MariaDB.
* For upgrading from very old MySQL versions, see [Upgrading to MariaDB from MySQL 5.0 (or older version)](migrating-to-mariadb-from-mysql-obsolete-articles/upgrading-to-mariadb-from-mysql-50-or-older.md).
* Within the same base version (for example MySQL 5.5 -> [MariaDB 5.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5), MySQL 5.6 -> [MariaDB 10.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0) and MySQL 5.7 -> [MariaDB 10.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/what-is-mariadb-102)) you can in most cases just uninstall MySQL and install MariaDB and you are good to go. There is no need to dump and restore databases. As with any upgrade, we recommend making a backup of your data beforehand.
* You should run [mariadb-upgrade](../../../../clients-and-utilities/mariadb-upgrade.md) (as you would with `mysql_upgrade` in MySQL) to finish the upgrade. This is needed to ensure that your mysql privilege and event tables are updated with the new fields MariaDB uses. Note that if you use a MariaDB package, `mariadb-upgrade` is usually run automatically.
* All your old clients and connectors (PHP, Perl, Python, Java, etc.) will work
 unchanged (no need to recompile). This works because MariaDB and MySQL use
 the same client protocol and the client libraries are binary compatible. You can also use your old MySQL connector packages with MariaDB if you want.


## Upgrading from MySQL 5.6 or MySQL 5.7


### Prerequisites


Check the values of the following server variables:


* [innodb_file_per_table](../../../../reference/storage-engines/innodb/innodb-system-variables.md#innodb_file_per_table)
* [innodb_fast_shutdown](../../../../reference/storage-engines/innodb/innodb-system-variables.md#innodb_fast_shutdown)


```
select @@Innodb_file_per_table,@@Innodb_fast_shutdown\G
```

[innodb_file_per_table](../../../../reference/storage-engines/innodb/innodb-system-variables.md#innodb_file_per_table) should be 1. This is the default setting for MySQL and MariaDB. If not, one should use [mysqldump](../../../../clients-and-utilities/legacy-clients-and-utilities/mysqldump.md) for migration as some of the following recommendations will not work.


[innodb_fast_shutdown](../../../../reference/storage-engines/innodb/innodb-system-variables.md#innodb_fast_shutdown) should be 0 (at least on the migrated server during shutdown, to ensure that a full shutdown is done when taking server down). This is required when upgrading between major versions of both MySQL and MariaDB as the format of the undo or redo files can change between major versions. This variable can be set just before doing the shutdown.


If your distribution allows it, install the MariaDB packages or the MariaDB tar distribution on the database server. Do not start MariaDB yet! This will decrease the downtime while doing the migration.


### MySQL `caching_sha256_password` Authentication


MariaDB does not yet support the `caching_sha256_password`
authentication protocol as it's cumbersome and not secure for in-house attacks. (clear text password is available inside the server).


* [MDEV-9804](https://jira.mariadb.org/browse/MDEV-9804) / Implement a `caching_sha256_password` plugin


You can check which MySQL users are using SHA-256 or `caching_sha256_password` by executing:


```
SELECT user, plugin FROM mysql.user where plugin like "%sha%";
```

You can change the user/s to use a protocol compatible with both MySQL and
MariaDB with:


```
ALTER USER user_name IDENTIFIED WITH mysql_native_password BY  'new_password';
```

### JSON


MariaDB stores JSON differently than MySQL. Normally you do not have to do anything when migrating JSON data, except if you are using replication or Galera. If this is the case, then you should convert your JSON columns to TEXT to ensure that all data is stored identically in MySQL and MariaDB:


If you are using JSON columns and want to upgrade to MariaDB, use the [mysql_json](../../../../reference/plugins/other-plugins/mysql_json.md) plugin to automatically convert MySQL JSON to TEXT.


Alternatively you need to either convert them to TEXT or use [mysqldump](../../../../clients-and-utilities/legacy-clients-and-utilities/mysqldump.md) to copy these tables to MariaDB.


You can check if you are have tables that uses the MySQL JSON type with:


```
select table_schema, table_name from information_schema.COLUMNS where
data_type="JSON";
```

You can convert the JSON column to text with:


```
ALTER TABLE table_name MODIFY json_column LONGTEXT;
```

### XA


When doing a backup, ensure that there are no active XA transactions in the backup, as these transactions needs to be committed/rolled back before the migration.


### Encryption and Compression


Encryption and compression are very different in MySQL and MariaDB.


Encrypted/compressed tables need to be de-encrypted/de-compressed before starting the conversion, and then encrypted/compressed again afterwards.


Detect compressed tables with the following query:


```
select table_name, create_options from information_schema.TABLES where
create_options like "%comp%";
```

### Config Files


* Create config files for MariaDB that match the MySQL cluster option files
* There are some configuration options that differ. See [System Variable Differences between MariaDB and MySQL](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/compatibility-and-differences/system-variable-differences-between-mariadb-and-mysql/).
* You can use `[mariadb]` or `[mariadb-x.y.z]` (for the specific version) in the current config files for MariaDB-specific options.
* You can also place MySQL-specific options inside a `[mysqld-5.7]` section. This includes all options that use mysql-specific directories for logging or replication (on other words, paths with `mysql` as part of the path).
* With a combination of these, it's easy to create a config file that will work with both MariaDB and MySQL, no matter what options are present.
* See also [MDEV-32745](https://jira.mariadb.org/browse/MDEV-32745) for an upcoming tool to automatically detect incompatible options.


#### Audit plugin


* MariaDB does not have the audit_log_plugin. Rather, MariaDB uses the server_audit plugin, which takes different options.


### Common Steps


* Perform all the prerequisite steps (SHA-256) on the MySQL Server.
* If replication is used, do these steps also on the primary.
* Take a backup.
* Install the MariaB packages or MariaDB tar distribution.
* Fix the my.cnf file to work with both MariaDB and MySQL.
* When MariaDB is installed, you can test your config files with `mariadbd --help --verbose > /tmp/log 2>&1` which will display all unsupported config options. It's also possible to use the script at [MDEV-32745](https://jira.mariadb.org/browse/MDEV-32745) to find all unsupported options.
* Check the log for `ERROR` and fix the config files if needed.


### Sample Steps for Single Instance MySQL Server


In the shell:


```
shell> mysql --user=root ...##
```

In MySQL:


```
set @@global.innodb_fast_shutdown=0;
quit
```

* Take down the node with `mysqladmin shutdown` or `sudo service mysqld stop`:


```
shell> mysqladmin --user=root shutdown
```

* Drop the MySQL packages:


```
shell> yum -y remove Percona-Server*
```

or


```
shell> rpm -q -a | grep Percona | xargs rpm -e --nodeps
```

or


```
shell> rpm -q -a | grep -i mysql | xargs rpm -e --nodeps
```

* This can also be done later if one has both MySQL and MariaDB installed at the same time)
* Remove the unsupported auditlog (Only relevant with Percona server):


```
shell> mv /etc/my.cnf.d/auditlog.cnf /etc/my.cnf.d/auditlog.cnf-backup
```

* Install MariaDB if not already installed from the [download site](https://mariadb.org/download/)
* Using the repo is recommended, or


```
shell> yum install MariaDB-server MariaDB-client
```

* Start mariadbd on the node data


```
systemctl start mariadb.service
```

* If it does not start, check the error file. Remove all unsupported options from the config files and try again.
* run [mariadb-upgrade](../../../../clients-and-utilities/mariadb-upgrade.md):


```
mariadb-upgrade
```

* If there were problems with a plugin that does not work or is not supported, you can disable it with:


```
mariadb mysql
```

* Then, from the MariaDB client:


```
select * from mysql.plugin
```

* and then for each unsupported plugin:


```
UNINSTALL PLUGIN IF EXISTS #plugin_name#;
```

* Test your new server
* As long as one does not create new tables or alter tables, it should be possible to go back to MySQL by:
* Dropping all tables in the 'mysql' database


```
set @@global.innodb_fast_shutdown=0;
SHUTDOWN
```

* Start MySQL server with --skip-grants
* Install the backup of the 'mysql' database with:


```
shell> mysql mysql < /tmp/mysql-dump.txt
shell> mysqladmin flush-privileges
```

### MySQL replication setup


In case of replication you can either convert one of the existing nodes directly to MariaDB or create a new node, convert that to MariaDB and then delete the old MySQL node after testing.


* Do all the "Prerequisite steps" on the to-be-converted node.
* Follow the [Single instance MySQL server](#sample-steps-for-single-instance-mysql-server) instructions for the node.
* Start MariaDB as a replica to MySQL.
* Test that the new node works as expected.
* Note that a MariaDB replica will work with replication positions, not with MySQL GTID.
* Repeat with all other nodes.
* Switch one of the MariaDB nodes to be the primary.
* Convert the old primary according to the above instructions.
* Add the old primary as a replica.


## [Upgrading on Windows](../../upgrading/upgrading-mariadb-on-windows.md)


On Windows, you should not uninstall MySQL and install MariaDB, this would not work, the existing database will not be found.


Thus On Windows, just install MariaDB and use the upgrade wizard which is part of installer package and is launched by MSI installer. Or, in case you prefer command line, use `mysql_upgrade_service <service_name>` on the command line.


## Upgrading my.cnf


All the options in your original MySQL [my.cnf file](../../mariadbd-configuration-files-and-groups.md) should work fine for MariaDB.


However as MariaDB has more features than MySQL, there are a few things that you should consider changing in your `my.cnf` file.


* MariaDB uses the [Aria storage engine](../../../../reference/storage-engines/aria/aria-storage-engine.md) by default for internal temporary files, instead of MyISAM. If you have a lot of temporary files, you should add and set `[aria-pagecache-buffer-size](../../../../reference/storage-engines/aria/aria-system-variables.md#aria_pagecache_buffer_size)` to the same value as you have for `[key-buffer-size](../../../../reference/storage-engines/myisam-storage-engine/myisam-system-variables.md#key_buffer_size)`.
* If you don't use MyISAM tables, you can set [key-buffer-size](../../../../reference/storage-engines/myisam-storage-engine/myisam-system-variables.md#key_buffer_size) to a very low value, like 64K.
* If you have a LOT of connections (> 100) that mostly run short running queries, you should consider using the [thread pool](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/buffers-caches-and-threads/thread-pool/thread-pool-in-mariadb.md). For example using : [thread_handling=pool-of-threads](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#thread_handling) and [thread_pool_size=128](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#thread_pool_size) could give a notable performance boost in this case. Where the `thread_pool_size` should be about `2 * number of cores on your machine`.


## Other Things to Think About


* MariaDB has LGPL versions of the [C connector](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/) and [Java Client](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-j/). If you are shipping an application that supports MariaDB or MySQL, you should consider using these!
* You should consider trying out the [MyRocks storage engine](../../../../reference/storage-engines/myrocks/README.md) or some of the other [new storage engines](../../../../reference/storage-engines/README.md) that MariaDB provides.


## See Also


* MariaDB has a lot of [new features](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/compatibility-and-differences/mariadb-vs-mysql-features) that you should know about.
* [MariaDB versus MySQL - Compatibility](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/compatibility-and-differences/mariadb-vs-mysql-compatibility)
* [Migrating to MariaDB](../README.md)
* You can find general upgrading informations on the [MariaDB installation page](../../README.md).
* There is a [Screencast for upgrading MySQL to MariaDB](migrating-to-mariadb-from-mysql-obsolete-articles/screencast-for-upgrading-mysql-to-mariadb-obsolete.md).
* [Upgrading to MariaDB in Debian 9](../../troubleshooting-installation-issues/installation-issues-on-debian-and-ubuntu/moving-from-mysql-to-mariadb-in-debian-9.md)


CC BY-SA / Gnu FDL

