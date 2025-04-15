
# Upgrading Between Major MariaDB Versions

MariaDB is designed to allow easy upgrades. You should be able to trivially upgrade from ANY earlier
MariaDB version to the latest one (for example [MariaDB 10.3](../../../../release-notes/mariadb-community-server/what-is-mariadb-103.md).x to [MariaDB 10.11](../../../../release-notes/mariadb-community-server/what-is-mariadb-1011.md).x), usually in a few seconds. This is also mainly true for any MySQL version < 8.0 to [MariaDB 10.4](../../../../release-notes/mariadb-community-server/what-is-mariadb-104.md) and up.


Upgrades are normally easy because:


* All MariaDB table data files are backward compatible
* The MariaDB connection protocol is backward compatible. You don't normally need to upgrade any of your old clients to be able to connect to a newer MariaDB version.
* The MariaDB replica can be of any newer version than the primary.


MariaDB Corporation regularly runs tests to check that one can upgrade from [MariaDB 5.5](../../../../release-notes/mariadb-community-server/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md) to the latest MariaDB version without any trouble. All older versions should work too (as long as the storage engines you were using are still around).


Note that if you are using [MariaDB Galera Cluster](../../../server-usage/replication-cluster-multi-master/galera-cluster/galera-cluster-status-variables.md), you have to follow the [Galera upgrading instructions](../../../server-usage/replication-cluster-multi-master/galera-cluster/upgrading-galera-cluster/README.md)!


## Requirements for Doing an Upgrade Between Major Versions


* Go through the individual version upgrade notes (listed below) to look for any major changes or configuration options that have changed.
* Ensure that the target MariaDB version supports the storage engines you are using. For example, in 10.5 [TokuDB](../../../reference/storage-engines/tokudb/tokudb-resources.md) is not supported.
* Back up the database (just in case). At least, take a copy of the `<code class="fixed" style="white-space:pre-wrap">mysql</code>` system database directory under the data directory with [mariadb-dump --add-drop-table mysql](../../../clients-and-utilities/backup-restore-and-import-clients/mariadb-dump.md) (called mysqldump in [MariaDB 10.3](../../../../release-notes/mariadb-community-server/what-is-mariadb-103.md) and earlier) as most of the upgrade changes are done there (adding new fields and new system tables etc).
* Cleanly shutdown the server. This is necessary because even if data files are compatible between versions, recovery logs may not be.

  * Ensure that the [innodb_fast_shutdown](../../../reference/storage-engines/innodb/innodb-system-variables.md#innodb_fast_shutdown) variable is not 2 (fast crash shutdown). The default of this variable is 1.
  * [innodb_force_recovery](../../../reference/storage-engines/innodb/innodb-system-variables.md#innodb_force_recovery) must be less than `<code>3</code>`.


Note that rpms don't support upgrading between major versions, only minor like 10.4.1 to 10.4.2. If you are using rpms, you should de-install the old MariaDB rpms and install the new MariaDB rpms before running [mariadb-upgrade](../../../clients-and-utilities/mariadb-upgrade.md). Note that when installing the new rpms, [mariadb-upgrade](../../../clients-and-utilities/mariadb-upgrade.md) may be run automatically. There is no problem with running [mariadb-upgrade](../../../clients-and-utilities/mariadb-upgrade.md) many times.


## Recommended Steps


* If you have a [primary-replica setup](../../../server-usage/replication-cluster-multi-master/standard-replication/README.md), first upgrade one replica and when you have verified that the replica works well, upgrade the rest of the replicas (if any). Then [upgrade one replica to primary](../../../server-usage/replication-cluster-multi-master/standard-replication/changing-a-replica-to-become-the-primary.md), upgrade the primary, and change the replica to a primary.


* If you don't have a primary-replica setup, then [take a backup](../../backing-up-and-restoring-databases/mariabackup/mariabackup-and-backup-stage-commands.md), [shutdown MariaDB](../../../clients-and-utilities/legacy-clients-and-utilities/mysqladmin.md) and do the upgrade.


### Step by Step Instructions for Upgrades


* Upgrade MariaDB binaries and libraries, preferably without starting MariaDB.
* If the MariaDB server process, [mariadbd](../starting-and-stopping-mariadb/mariadbd-options.md) was not started as part of the upgrade, start it by executing `<code class="fixed" style="white-space:pre-wrap">mariadbd --skip-grant-tables</code>`. This may produce some warnings about some system tables not being up to date, but you can ignore these for now as [mariadb-upgrade](../../../clients-and-utilities/mariadb-upgrade.md) will fix that.
* Run [mariadb-upgrade](../../../clients-and-utilities/mariadb-upgrade.md)
* Restart MariaDB server.


## Work Done by mariadb-upgrade


The main work done when upgrading is done by running [mariadb-upgrade](../../../clients-and-utilities/mariadb-upgrade.md). The main things it does are:


* Updating the system tables in the `<code class="fixed" style="white-space:pre-wrap">mysql</code>` database to the newest version. This is very quick.
* [mariadb-upgrade](../../../clients-and-utilities/mariadb-upgrade.md) also runs [mariadb-check --check-upgrade](../../../clients-and-utilities/mariadb-check.md) to check if there have been any collation changes between the major versions. This recreates indexes in old tables that are using any of the changed collations. This can take a bit of time if there are a lot of tables or there are many tables which used the changed collation. The last time a collation changed was in MariaDB/MySQL 5.1.23.


## Post Upgrade Work


Check the [MariaDB error log](../../server-monitoring-logs/error-log.md) for any problems during upgrade. If there are any warnings in the log files, do your best to get rid of them!


The common warnings/errors are:


* Using obsolete options. If this is the case, remove them from your [my.cnf files](../configuring-mariadb-with-option-files.md).


* Check the manual for [new features](../../../../columnstore/mariadb-columnstore-columnstore/mariadb-columnstore-10-upgrades/upgrading-mariadb-columnstore-from-103-to-104.md) that have been added since your last MariaDB version.
* Test that your application works as before. The main difference from before is that because of optimizer improvements your application should work better than before, but in some rare cases the optimizer may get something wrong. In this case, you can try to use [explain](../../../../general-resources/learning-and-training/training-and-tutorials/advanced-mariadb-articles/development-articles/outdated-pages/explain-formatjson-in-mysql.md), [optimizer trace](../../../reference/mariadb-internals/mariadb-internals-documentation-query-optimizer/mariadb-internals-documentation-optimizer-trace/README.md) or [optimizer_switch](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/query-optimizations/optimizer-switch.md) to fix the queries.


## If Something Goes Wrong


* First, check the [MariaDB error log](../../server-monitoring-logs/error-log.md) to see if you are using configure options that are not supported anymore.
* Check the upgrade notices for the MariaDB release that you are upgrading to.
* File an issue in the [MariaDB bug tracker](../../../reference/bug-tracking/README.md) so that we know about the issue and can provide a fix to make upgrades even better.
* Add a comment to this manual entry for how we can improve it.


### Disaster Recovery


In the unlikely event something goes wrong, you can try the following:


* Remove the InnoDB tables from the `<code class="fixed" style="white-space:pre-wrap">mysql</code>` data directory. They are:

  * gtid_slave_pos
  * innodb_table_stats
  * innodb_index_stats
  * transaction_registry
* Move the `<code class="fixed" style="white-space:pre-wrap">mysql</code>` data directory to `<code class="fixed" style="white-space:pre-wrap">mysql-old</code>` and run [mariadb-install-db](../mariadb-install-db-exe.md) to generate a new one.
* After the above, you have to add back your old users.
* When done, delete the `<code class="fixed" style="white-space:pre-wrap">mysql-old</code>` data directory.


## Downgrading


MariaDB server is not designed for downgrading. That said, in most cases, as long as you haven't run any [ALTER TABLE](../../../reference/sql-statements-and-structure/sql-statements/data-definition/alter/alter-tablespace.md) or [CREATE TABLE](../../../reference/sql-statements-and-structure/vectors/create-table-with-vectors.md) statements and you have a [mariadb-dump](../../../clients-and-utilities/backup-restore-and-import-clients/mariadb-dump.md) of your old `<code class="fixed" style="white-space:pre-wrap">mysql</code>` database , you should be able to downgrade to your previous version by doing the following:


* Do a clean shutdown. For this special case you have to set [innodb_fast_shutdown](../../../reference/storage-engines/innodb/innodb-system-variables.md#innodb_fast_shutdown) to 0,before taking down the new MariaDB server, to ensure there are no redo or undo logs that need to be applied on the downgraded server.
* Delete the tables in the `<code class="fixed" style="white-space:pre-wrap">mysql</code>` database (if you didn't use the option `<code class="fixed" style="white-space:pre-wrap">--add-drop-table</code>` to [mariadb-dump](../../../clients-and-utilities/backup-restore-and-import-clients/mariadb-dump.md))
* Delete the new MariaDB installation
* Install the old MariaDB version
* Start the server with [mariadbd --skip-grant-tables](../starting-and-stopping-mariadb/mariadbd-options.md#-skip-grant-tables)
* Install the old `<code class="fixed" style="white-space:pre-wrap">mysql</code>` database
* Execute in the [mariadb client](../../../clients-and-utilities/mariadb-client/README.md) [FLUSH PRIVILEGES](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/flush-commands/flush-tables-for-export.md)


## See Also


* [Upgrading from MySQL to MariaDB](../migrating-to-mariadb/moving-from-mysql/upgrading-from-mysql-to-mariadb.md)
* [Upgrading from MariaDB 10.11 to MariaDB 11.4](upgrading-from-mariadb-10-11-to-mariadb-11-4.md)
* [Upgrading from MariaDB 10.6 to MariaDB 10.11](upgrading-from-mariadb-10-6-to-mariadb-10-11.md)
* [Upgrading from MariaDB 10.6 to MariaDB 10.7](upgrading-to-unmaintained-mariadb-releases/upgrading-from-mariadb-10-6-to-mariadb-10-7.md)
* [Upgrading from MariaDB 10.5 to MariaDB 10.6](upgrading-from-mariadb-10-5-to-mariadb-10-6.md)
* [Upgrading from MariaDB 10.4 to MariaDB 10.5](upgrading-from-mariadb-10-4-to-mariadb-10-5.md)


* [Galera upgrading instructions](../../../server-usage/replication-cluster-multi-master/galera-cluster/upgrading-galera-cluster/README.md)
* [innodb_fast_shutdown](../../../reference/storage-engines/innodb/innodb-system-variables.md#innodb_fast_shutdown)

