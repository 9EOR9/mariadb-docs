# MariaDB 10.5.2 Release Notes

The most recent release of [MariaDB 10.5](what-is-mariadb-105.md) is:[**MariaDB 10.5.28**](mariadb-10-5-28-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.5.28/)

[Download](https://downloads.mariadb.org/mariadb/10.5.2/)[Release Notes](mariadb-1052-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-1052-changelog.md)[Overview of 10.5](what-is-mariadb-105.md)

**Release date:** 26 Mar 2020

[MariaDB 10.5](what-is-mariadb-105.md) is the current _development_ series of MariaDB. It is an evolution\
of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/mariadb-10-5-series/broken-reference/README.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.5.2](mariadb-1052-release-notes.md) is a [_**Beta**_](../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

**For an overview of** [**MariaDB 10.5**](what-is-mariadb-105.md) **see the**[**What is MariaDB 10.5?**](what-is-mariadb-105.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the second beta release in the [MariaDB 10.5](what-is-mariadb-105.md) series.

Notable changes of this release include:

### Syntax

* [RELEASE\_ALL\_LOCKS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/miscellaneous-functions/release_all_locks) ([MDEV-10569](https://jira.mariadb.org/browse/MDEV-10569))
* [ALTER TABLE ... RENAME INDEX / KEY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table#rename-indexkey) ([MDEV-7318](https://jira.mariadb.org/browse/MDEV-7318))
* [ALTER TABLE ... RENAME COLUMN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table#rename-column) ([MDEV-16290](https://jira.mariadb.org/browse/MDEV-16290))
* Recursive [CTE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/common-table-expressions) cycle detection using CYCLE clause ([MDEV-20632](https://jira.mariadb.org/browse/MDEV-20632))
* [ALTER TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table) and [RENAME TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/rename-table) now support `IF EXISTS`.

### Privileges

* Split SUPER [privilege](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant) to smaller privileges ([MDEV-21743](https://jira.mariadb.org/browse/MDEV-21743)). New privileges were added so that more fine grained tuning of what each user can do can be applied:
  * [BINLOG ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#binlog-admin)
  * [BINLOG REPLAY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#binlog-replay)
  * [CONNECTION ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#connection-admin)
  * [FEDERATED ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#federated-admin)
  * [READ\_ONLY ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#read_only-admin)
  * [REPLICATION MASTER ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-master-admin)
  * [REPLICATION SLAVE ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-slave-admin)
  * [SET USER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#set-user)
* The [REPLICATION CLIENT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-client) privilege was renamed to [BINLOG MONITOR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#binlog-monitor). The old syntax is understood for compatibility ([MDEV-21743](https://jira.mariadb.org/browse/MDEV-21743)).
* The [SHOW MASTER STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-binlog-status) statement was renamed to [SHOW BINLOG STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-binlog-status) ([MDEV-21743](https://jira.mariadb.org/browse/MDEV-21743)). The old syntax is understood for compatibility.
* A number of statements changed the privileges that they require. The old privileges were historically inappropriately chosen in the upstream. 10.5.2 fixes this problem. Note, these changes are incompatible to previous versions. A number of GRANT commands might be needed after upgrade.
  * [SHOW BINLOG EVENTS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-binlog-events) now requires the [BINLOG MONITOR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#binlog-monitor) privilege (required [REPLICATION SLAVE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-slave) prior to 10.5.2).
  * [SHOW SLAVE HOSTS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-replica-hosts) now requires the [REPLICATION MASTER ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-master-admin) privilege (required [REPLICATION SLAVE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-slave) prior to 10.5.2).
  * [SHOW SLAVE STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-replica-status) now requires the [REPLICATION SLAVE ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-slave-admin) or the [SUPER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#super) privilege (required [REPLICATION CLIENT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-client) or [SUPER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#super) prior to 10.5.2).
  * [SHOW RELAYLOG EVENTS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-relaylog-events) now requires the [REPLICATION SLAVE ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-slave-admin) privilege (required [REPLICATION SLAVE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-slave) prior to 10.5.2).
* In order to help the server understand which version a privilege record was written by, the [mysql.global\_priv.priv](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-global_priv-table) field contains a new JSON field, `version_id` ([MDEV-21704](https://jira.mariadb.org/browse/MDEV-21704))
* [SHOW PRIVILEGES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-privileges) now correctly lists the `Delete history` privilege, rather than displaying it as `Delete versioning rows`. ([MDEV-20382](https://jira.mariadb.org/browse/MDEV-20382))

### InnoDB

* An upgrade will only be possible after a clean shutdown. mariabackup --prepare will not work with backups taken before version 10.5.2.
* Efficient InnoDB redo log record format ([MDEV-12353](https://jira.mariadb.org/browse/MDEV-12353))
* Deprecate and ignore [innodb\_scrub\_log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_scrub_log) and [innodb\_scrub\_log\_speed](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_scrub_log_speed) ([MDEV-21870](https://jira.mariadb.org/browse/MDEV-21870))
* Remove [INFORMATION\_SCHEMA.INNODB\_TABLESPACES\_SCRUBBING](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-innodb-tables/information-schema-innodb_tablespaces_scrubbing-table) table and deprecate and ignore [innodb-background-scrub-data-uncompressed](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_background_scrub_data_uncompressed), [innodb-background-scrub-data-compressed](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_background_scrub_data_compressed), [innodb-background-scrub-data-interval](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_background_scrub_data_interval) and [innodb-background-scrub-data-check-interval](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_background_scrub_data_check_interval) ([MDEV-15528](https://jira.mariadb.org/browse/MDEV-15528))
* Deprecate and ignore [innodb\_log\_files\_in\_group](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_log_files_in_group) ([MDEV-14425](https://jira.mariadb.org/browse/MDEV-14425))
* Do not acquire InnoDB record locks when covering table locks exist ([MDEV-14479](https://jira.mariadb.org/browse/MDEV-14479))
* Issue a message on changing deprecated innodb\_log\_files\_in\_group ([MDEV-21990](https://jira.mariadb.org/browse/MDEV-21990))
* Optimize append only files for NVDIMM ([MDEV-17084](https://jira.mariadb.org/browse/MDEV-17084))
* Improve innodb redo log group commit performance ([MDEV-21534](https://jira.mariadb.org/browse/MDEV-21534))
* Punch holes when pages are freed ([MDEV-15528](https://jira.mariadb.org/browse/MDEV-15528))

### Optimizer

* Allow packed sort keys in sort buffer ([MDEV-21580](https://jira.mariadb.org/browse/MDEV-21580))

### Performance Schema

* Merge 5.7 P\_S transaction instrumentation and tables ([MDEV-16435](https://jira.mariadb.org/browse/MDEV-16435))
* Merge 5.7 P\_S memory instrumentation and tables ([MDEV-16431](https://jira.mariadb.org/browse/MDEV-16431))
* Merge 5.7 P\_S mdl instrumentation and tables ([MDEV-16432](https://jira.mariadb.org/browse/MDEV-16432))
* Merge 5.7 P\_S sxlocks instrumentation and tables ([MDEV-16436](https://jira.mariadb.org/browse/MDEV-16436))
* Merge 5.7 P\_S user variables instrumentation and tables ([MDEV-16439](https://jira.mariadb.org/browse/MDEV-16439))
* Merge 5.7 P\_S \[show] status instrumentation and tables ([MDEV-16438](https://jira.mariadb.org/browse/MDEV-16438))
* Merge 5.7 P\_S ps instrumentation and tables ([MDEV-16433](https://jira.mariadb.org/browse/MDEV-16433))
* Merge 5.7 P\_S sp instrumentation and tables ([MDEV-16434](https://jira.mariadb.org/browse/MDEV-16434))

### Replication

* `ENFORCE` option for [slave\_run\_triggers\_for\_rbr](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#slave_run_triggers_for_rbr) ([MDEV-21833](https://jira.mariadb.org/browse/MDEV-21833))

### ANALYZE FORMAT=JSON

* Add information about packed addon fields in [ANALYZE FORMAT=JSON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/analyze-and-explain-statements/analyze-format-json) ([MDEV-21838](https://jira.mariadb.org/browse/MDEV-21838))

### Binaries

* All binaries previously beginning with `mysql` now begin with `mariadb`, with symlinks for the corresponding `mysql` command. ([MDEV-21303](https://jira.mariadb.org/browse/MDEV-21303))

### Galera

* [Galera wsrep library](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/readme/mariadb-galera-cluster-guide) updated to 26.4.4
* Galera Cluster Node During IST gets stuck going from "Synced" to "Joining:..." ([MDEV-21002](https://jira.mariadb.org/browse/MDEV-21002))

### Other

* [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 11.0 ([MDEV-22032](https://jira.mariadb.org/browse/MDEV-22032))
* [require\_secure\_transport](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#require_secure_transport) system variable, for rejecting connections attempted using insecure transport ([MDEV-13362](https://jira.mariadb.org/browse/MDEV-13362))
* [sql\_if\_exists](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#sql_if_exists) session system variable, which adds an implicit IF EXISTS to ALTER, RENAME and DROP of TABLES, VIEWS, FUNCTIONS and PACKAGES. ([MDEV-19964](https://jira.mariadb.org/browse/MDEV-19964))
* [XA PREPARE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/transactions/xa-transactions#syntax) transactions must survive client disconnection ([MDEV-742](https://jira.mariadb.org/browse/MDEV-742))
* Binary tarball size has been reduced ([MDEV-21943](https://jira.mariadb.org/browse/MDEV-21943))

## Changelog

For a complete list of changes made in [MariaDB 10.5.2](mariadb-1052-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-1052-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.5.2](mariadb-1052-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-2-now-available/).

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
