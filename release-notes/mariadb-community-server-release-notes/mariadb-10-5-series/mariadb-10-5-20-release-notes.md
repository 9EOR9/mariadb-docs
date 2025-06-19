# MariaDB 10.5.20 Release Notes

The most recent release of [MariaDB 10.5](what-is-mariadb-105.md) is:[**MariaDB 10.5.28**](mariadb-10-5-28-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.5.28/)

[Download 10.5.20](https://downloads.mariadb.org/mariadb/10.5.20/)[Release Notes](mariadb-10-5-20-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-10-5-20-changelog.md)[Overview of 10.5](what-is-mariadb-105.md)

**Release date:** 10 May 2023

[MariaDB 10.5](what-is-mariadb-105.md) is a previous _stable_ series of MariaDB, [maintained until](https://mariadb.org/about/#maintenance-policy) June 2025. It is an evolution of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/mariadb-10-5-series/broken-reference/README.md) with several entirely new features not found anywhere else and with backported and reimplemented features from MySQL.

[MariaDB 10.5.20](mariadb-10-5-20-release-notes.md) is a [_**Stable (GA)**_](https://app.gitbook.com/o/diTpXxF5WsbHqTReoBsS/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-release-criteria) release.

**For an overview of** [**MariaDB 10.5**](what-is-mariadb-105.md) **see the**[**What is MariaDB 10.5?**](what-is-mariadb-105.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### InnoDB

* Crash on [ROLLBACK](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/transactions/rollback) in a [ROW\_FORMAT=COMPRESSED](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-row-formats/innodb-compressed-row-format) table ([MDEV-30882](https://jira.mariadb.org/browse/MDEV-30882))
* UNIQUE USING HASH accepts duplicate entries for tricky collations ([MDEV-30034](https://jira.mariadb.org/browse/MDEV-30034))
* rec\_get\_offsets() is not optimal ([MDEV-30567](https://jira.mariadb.org/browse/MDEV-30567))
* Performance regression in fil\_space\_t::try\_to\_close() introduced in [MDEV-23855](https://jira.mariadb.org/browse/MDEV-23855) ([MDEV-30775](https://jira.mariadb.org/browse/MDEV-30775))
* InnoDB recovery hangs when buffer pool ran out of memory ([MDEV-30551](https://jira.mariadb.org/browse/MDEV-30551))
* InnoDB undo log truncation fails to wait for purge of history ([MDEV-30671](https://jira.mariadb.org/browse/MDEV-30671)
* Fix miscount of doublewrites by [Innodb\_data\_written](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#innodb_data_written) ([MDEV-31124](https://jira.mariadb.org/browse/MDEV-31124))

## Backup

* mariadb-backup doesn't utilise innodb-undo-log-directory (if specified as a relative path) during copy-back operation ([MDEV-28187](https://jira.mariadb.org/browse/MDEV-28187))
* mariabackup issues error messages during InnoDB tablespaces export on partial backup preparing ([MDEV-29050](https://jira.mariadb.org/browse/MDEV-29050))
* mariadb-backup does not copy Aria logs if aria\_log\_dir\_path is used ([MDEV-30968](https://jira.mariadb.org/browse/MDEV-30968))
* Race condition between buffer pool flush and log file deletion in mariadb-backup --prepare ([MDEV-30860](https://jira.mariadb.org/browse/MDEV-30860))

### Replication

* Fixed a deadlock on parallel slave involving full image Write event on the sequence engine ([MDEV-29621](https://jira.mariadb.org/browse/MDEV-29621))
* Fixed an attempted out-of-order binlogging error on slave involving ALTER on the sequence engine ([MDEV-31077](https://jira.mariadb.org/browse/MDEV-31077))
* Corrected non-versioned master to versioned slave replication on no-unique attribute table ([MDEV-30430](https://jira.mariadb.org/browse/MDEV-30430))
* Mended encrypted binlog master to error out to gtid-mode slave when master could not decrypt a binlog file ([MDEV-28798](https://jira.mariadb.org/browse/MDEV-28798))
* Refined optimistic parallel slave to error-exit without any hang ([MDEV-30780](https://jira.mariadb.org/browse/MDEV-30780))
* Ensured SHOW-SLAVE-STATUS is processed on the parallel slave having a necessary mutex always intialized ([MDEV-30620](https://jira.mariadb.org/browse/MDEV-30620))
* Fixed the slave applier to report a correct error when gtid\_slave\_pos insert fails for some (engine) reasons ([MDEV-31038](https://jira.mariadb.org/browse/MDEV-31038))

### Optimizer

* [Split Materialized](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/optimizations-for-derived-tables/lateral-derived-optimization) optimization is improved to re-fill the materialized table only if necessary. The fewer number of table refills is taken into account when choosing query plan, too ([MDEV-26301](https://jira.mariadb.org/browse/MDEV-26301)).
* Queries using `SELECT DISTINCT some_expression(aggregate_function())` could produce wrong query result. ([MDEV-20057](https://jira.mariadb.org/browse/MDEV-20057))
* A GROUP BY query with `MIN(primary_key)` in select list and `primary_key<>const` in the WHERE could produce wrong result when executed with "Using index for group-by" strategy ([MDEV-30605](https://jira.mariadb.org/browse/MDEV-30605))
* EXPLAIN could erroneously report that [Rowid Filter optimization](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/rowid-filtering-optimization) is used for partitioned tables. Partitioned tables do not support it. ([MDEV-30596](https://jira.mariadb.org/browse/MDEV-30596))
* A bug in selectivity computations for SINGLE/DOUBLE\_PREC\_HB histograms could cause wrong estimates to be produced. This could cause the optimizer to pick sub-optimal query plans ([MDEV-31067](https://jira.mariadb.org/browse/MDEV-31067)).

### Docker Official Images

* Add replication setup to containers contributed by Md Sahil ([MDEV-29762](https://jira.mariadb.org/browse/MDEV-29762))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2022-47015](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-47015)

## Changelog

For a complete list of changes made in [MariaDB 10.5.20](mariadb-10-5-20-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-10-5-20-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.5.20](mariadb-10-5-20-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-11-3-10-10-4-10-9-6-10-8-8-10-6-13-10-5-20-10-4-29-and-10-3-39-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
