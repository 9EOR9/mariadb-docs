
# Moving from MySQL to MariaDB in Debian 9

[MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) is now the default mysql server in Debian 9 "Stretch". This page provides information on this change and instructions to help with upgrading your Debian 8 "Jessie" version of MySQL or MariaDB to [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) in Debian 9 "Stretch".


## Background information


The version of MySQL in Debian 8 "Jessie" is 5.5. When installing, most users will install the `mysql-server` package, which depends on the `mysql-server-5.5 package`. In Debian 9 "Stretch" the `mysql-server` package depends on a new package called `default-mysql-server`. This package in turn depends on `mariadb-server-10.1`. There is no `default-mysql-server` package in Jessie.


In both Jessie and Stretch there is also a `mariadb-server` package which is a MariaDB-specific analog to the `mysql-server` package. In Jessie this package depends on `mariadb-server-10.0` and in Stretch this package depends on `mariadb-server-10.1` (the same as the `default-mysql-server` package).


So, the main repository difference in Debian 9 "Stretch" is that when you install the `mysql-server` package on Stretch you will get [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) instead of MySQL, like you would with previous versions of Debian. Note that `mysql-server` is just an empty transitional meta-package and users are encouraged to install MariaDB using the actual package `mariadb-server`.


All apps and tools, such as the popular LAMP stack, in the repositories that depend on the `mysql-server` package will continue to work using MariaDB as the database. For new installs there is nothing different that needs to be done when installing the mysql-server or mariadb-server packages.


## Before you upgrade


If you are currently running MySQL 5.5 on Debian 8 "Jessie" and are planning an upgrade to [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) on Debian 9 "Stretch", there are some things to keep in mind:


### Backup before you begin


This is a major upgrade, and so complete database backups are strongly suggested before you begin. [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) is compatible on disk and wire with MySQL 5.5, and the MariaDB developer team has done extensive development and testing to make upgrades as painless and trouble-free as possible. Even so, it's always a good idea to do regular backups, especially before an upgrade. As the database has to shutdown anyway for the upgrade, this is a good opportunity to do a backup!


### Changed, renamed, and removed options


Some default values have been changed, some have been renamed, and others have been removed between MySQL 5.5 and [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1). The following sections detail them.


#### Options with changed default values


Most of the following options have increased a bit in value to give better
performance. They should not use much additional memory, but some of them do
use a bit more disk space.[[1](#_note-0)]



| Option | Old default value | New default value |
| --- | --- | --- |
| Option | Old default value | New default value |
| [aria-sort-buffer-size](../../../../reference/storage-engines/aria/aria-system-variables.md#aria_sort_buffer_size) | 128M | 256M |
| [back_log](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#back_log) | 50 | 150 |
| [innodb-concurrency-tickets](../../../../reference/storage-engines/innodb/innodb-system-variables.md) | 500 | 5000 |
| [innodb-log-file-size](../../../../reference/storage-engines/innodb/innodb-system-variables.md) | 5M | 48M |
| [innodb_log_compressed_pages](../../../../reference/storage-engines/innodb/innodb-system-variables.md) | ON | OFF |
| [innodb-old-blocks-time](../../../../reference/storage-engines/innodb/innodb-system-variables.md) | 0 | 1000 |
| [innodb-open-files](../../../../reference/storage-engines/innodb/innodb-system-variables.md) | 300 | 400 [[2]](#_note-1) |
| [innodb-purge-batch-size](../../../../reference/storage-engines/innodb/innodb-system-variables.md) | 20 | 300 |
| [innodb-undo-logs](../../../../reference/storage-engines/innodb/innodb-system-variables.md) | ON | 20 |
| [join_buffer_size](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#join_buffer_size) | 128K | 256K |
| [max_allowed_packet](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#max_allowed_packet) | 1M | 4M |
| [max-connect-errors](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#max_connect_errors) | 10 | 100 |
| [max-relay-log-size](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#max_relay_log_size) | 0 | 1024M |
| [myisam-sort-buffer-size](../../../../reference/storage-engines/myisam-storage-engine/myisam-system-variables.md) | 8M | 128M |
| [optimizer-switch](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#optimizer_switch) | ... | Added extended_keys=on, exists_to_in=on |
| [query_alloc_block_size](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#query_alloc_block_size) | 8192 | 16384 |
| [query_cache_size](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#query_cache_size) | 0 | 1M |
| [query_cache_type](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#query_cache_type) | ON | OFF |
| [query_prealloc_size](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#query_prealloc_size) | 8192 | 24576 |
| [secure_auth](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#secure_auth) | OFF | ON |
| [sql_log_bin](../../../../server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables.md) |  | No longer affects replication of events in a Galera cluster. |
| [sql_mode](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#sql_mode) | empty | NO_AUTO_CREATE_USER, NO_ENGINE_SUBSTITUTION |
| [sync_master_info](../../../../server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables.md) | 0 | 10000 |
| [sync_relay_log](../../../../server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables.md) | 0 | 10000 |
| [sync_relay_log_info](../../../../server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables.md) | 0 | 10000 |
| [table_open_cache](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#table_open_cache) | 400 | 2000 |
| [thread_pool_max_threads](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#thread_pool_max_threads) | 500 | 1000 |



#### Options that have been removed or renamed


The following options should be removed or renamed if you use them in your
config files:



| Option | Reason |
| --- | --- |
| Option | Reason |
| engine-condition-pushdown | Replaced with [set optimizer_switch='engine_condition_pushdown=on'](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/query-optimizations/index-condition-pushdown.md) |
| innodb-adaptive-flushing-method | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-autoextend-increment | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-blocking-buffer-pool-restore | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-buffer-pool-pages | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-buffer-pool-pages-blob | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-buffer-pool-pages-index | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-buffer-pool-restore-at-startup | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-buffer-pool-shm-checksum | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-buffer-pool-shm-key | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-checkpoint-age-target | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-dict-size-limit | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-doublewrite-file | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-fast-checksum | Renamed to [innodb-checksum-algorithm](../../../../reference/storage-engines/innodb/innodb-system-variables.md) |
| innodb-flush-neighbor-pages | Renamed to [innodb-flush-neighbors](../../../../reference/storage-engines/innodb/innodb-system-variables.md) |
| innodb-ibuf-accel-rate | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-ibuf-active-contract | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-ibuf-max-size | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-import-table-from-xtrabackup | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-index-stats | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-lazy-drop-table | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-merge-sort-block-size | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-persistent-stats-root-page | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-read-ahead | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-recovery-stats | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-recovery-update-relay-log | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-stats-auto-update | Renamed to innodb-stats-auto-recalc |
| innodb-stats-update-need-lock | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-sys-stats | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-table-stats | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-thread-concurrency-timer-based | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| innodb-use-sys-stats-table | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |
| [rpl_recovery_rank](../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#rpl_recovery_rank) | Unused in 10.0+ |
| xtradb-admin-command | Removed by [XtraDB](../../../../reference/storage-engines/innodb/README.md) |



### Suggested upgrade procedure for replication


If you have a [master-slave setup](../../../../server-usage/replication-cluster-multi-master/standard-replication/README.md), the normal procedure is to first upgrade your slaves to MariaDB, then move one of your slaves to be the master and then upgrade your original master. In this scenario you can upgrade from MySQL to MariaDB or upgrade later to a new version of MariaDB without any downtime.


### Other resources to consult before beginning your upgrade


It may also be useful to check out the [Upgrading MariaDB](../../upgrading/README.md) section. It contains several articles on upgrading from MySQL to MariaDB and from one version of MariaDB to another. For upgrade purposes, MySQL 5.5 and [MariaDB 5.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5) are very similar. In particular, see the [Upgrading from MariaDB 5.5 to MariaDB 10.0](../../upgrading/upgrading-from-mariadb-10-4-to-mariadb-10-5.md) and [Upgrading from MariaDB 10.0 to MariaDB 10.1](../../upgrading/upgrading-to-unmaintained-mariadb-releases/upgrading-from-mariadb-100-to-mariadb-101.md) articles.


If you need help with upgrading or setting up replication, you can always [contact the MariaDB corporation](https://mariadb.com/contact) to find experts to help you with this.


## Upgrading to [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) from MySQL 5.5


The suggested upgrade procedure is:


1. Set [innodb_fast_shutdown](../../../../reference/storage-engines/innodb/innodb-system-variables.md) to `0`. This is to ensure that if you make a backup as part of the upgrade, all data is written to the InnoDB data files, which simplifies any restore in the future.
1. Shutdown MySQL 5.5
1. Take a [backup](../../../backing-up-and-restoring-databases/backup-and-restore-overview.md)

  * when the server is shut down is the perfect time to take a backup of your databases
  * store a copy of the backup on external media or a different machine for safety
1. Perform the upgrade from Debian 8 to Debian 9
1. During the upgrade, the [mysql_upgrade](../../../../clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade.md) script will be run automatically; this script does two things:

  1. Upgrades the permission tables in the `mysql` database with some new fields
  1. Does a very quick check of all tables and marks them as compatible with [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1)

    * In most cases this should be a fast operation (depending of course on the number of tables)
1. Add new options to [my.cnf](../../configuring-mariadb-with-option-files.md) to enable features

  * If you change `my.cnf` then you need to restart `mysqld` with e.g. `sudo service mysql restart` or `sudo service mariadb restart`.


## Upgrading to [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) from an older version of MariaDB


If you have installed [MariaDB 5.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5) or [MariaDB 10.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0) on your Debian 8 "Jessie" machine from the MariaDB repositories you will need to upgrade to [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) when upgrading to Debian 9 "Stretch". You can choose to continue using the MariaDB repositories or move to using the Debian repositories.


If you want to continue using the MariaDB repositories edit the MariaDB entry in your sources.list and change every instance of 5.5 or 10.0 to 10.1. Then upgrade as suggested [above](#upgrading-to-mariadb-101-from-mysql-55).


If you want to move to using [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) from the Debian repositories, delete or comment out the MariaDB entries in your sources.list file. Then upgrade as suggested [above](#upgrading-to-mariadb-101-from-mysql-55).


If you are already using [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) on your Debian 8 "Jessie" machine, you can choose to continue to use the MariaDB repositories or move to using the Debian repositories as with [MariaDB 5.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5) and 10.0. In either case, the upgrade will at most be just a minor upgrade from one version of [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) to a newer version. In the case that you are already on the current version of MariaDB that exists in the Debian repositories or a newer one) MariaDB will not be upgraded during the system upgrade but will be upgraded when future versions of MariaDB are released.


You should always perform a compete backup of your data prior to performing any major system upgrade, even if MariaDB itself is not being upgraded!


## MariaDB Galera Cluster


If you have been using MariaDB Galera Cluster 5.5 or 10.0 on Debian 8 "Jessie" it is worth mentioning that [Galera Cluster](/en/galera/) is included by default in [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1), there is no longer a need to install a separate `mariadb-galera-server` package.


## Configuration options for advanced database users


To get better performance from MariaDB used in production environments, here are some suggested additions to [your configuration file](../../configuring-mariadb-with-option-files.md) which in Debian is at `/etc/mysql/mariadb.d/my.cnf`:


```
[[mysqld]]
# Cache for disk based temporary files
aria_pagecache_buffer_size=128M
# If you are not using MyISAM tables directly (most people are using InnoDB)
key_buffer_size=64K
```

The reason for the above change is that MariaDB is using the newer [Aria](../../../../reference/storage-engines/aria/aria-storage-engine.md) storage engine for disk based temporary files instead of MyISAM. The main benefit of Aria is that it can cache both indexes and rows and thus gives better performance than MyISAM for large queries.


## Secure passwordless root accounts only on new installs


Unlike the old MySQL packages in Debian, [MariaDB 10.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0) onwards in Debian uses unix socket authentication on new installs to avoid root password management issues and thus be more secure and easier to use with provision systems of the cloud age.


This only affects new installs. Upgrades from old versions will continue to use whatever authentication and user accounts already existed. This is however good to know, because it can affect upgrades of dependant systems, typically e.g. require users to rewrite their Ansible scripts and similar tasks. The new feature is much easier than the old, so adjusting for it requires little work.


## See also


* [Differences in MariaDB in Debian (and Ubuntu)](differences-in-mariadb-in-debian-and-ubuntu.md)
* [Configuring MariaDB for optimal performance](../../mariadb-performance-advanced-configurations/configuring-mariadb-for-optimal-performance.md)
* [New features in MariaDB you should considering using](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/compatibility-and-differences/mariadb-vs-mysql-features)
* [What is MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1)
* [General instructions for upgrading from MySQL to MariaDB](../../migrating-to-mariadb/moving-from-mysql/upgrading-from-mysql-to-mariadb.md)


## Comments and suggestions


If you have comments or suggestions on things we can add or change to improve this page. Please add them as comments below.


## Notes


1. [↑](#_ref-0) The `innodb-open-files` variable defaults to the value of `table-open-cache` (`400` is the default) if it is set to any value less than `10` so long as `innodb-file-per-table` is set to `1` or `TRUE` (the default). If `innodb_file_per_table` is set to `0` or `FALSE` and `innodb-open-files` is set to a value less than `10`, the default is `300`


CC BY-SA / Gnu FDL

