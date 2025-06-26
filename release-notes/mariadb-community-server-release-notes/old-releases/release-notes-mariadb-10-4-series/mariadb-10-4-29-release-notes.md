# MariaDB 10.4.29 Release Notes

The most recent release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download 10.4.29](https://downloads.mariadb.org/mariadb/10.4.29/)[Release Notes](mariadb-10-4-29-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10-4-29-changelog.md)[Overview of 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104)

**Release date:** 10 May 2023

[MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is a previous _stable_ series of MariaDB, [maintained until](https://mariadb.org/about/#maintenance-policy) June 2024. It is an evolution of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else and with backported and reimplemented features from MySQL.

[MariaDB 10.4.29](mariadb-10-4-29-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **see the**[**What is MariaDB 10.4?**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### InnoDB

* Crash on [ROLLBACK](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/transactions/rollback) in a [ROW\_FORMAT=COMPRESSED](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-row-formats/innodb-compressed-row-format) table ([MDEV-30882](https://jira.mariadb.org/browse/MDEV-30882))
* UNIQUE USING HASH accepts duplicate entries for tricky collations ([MDEV-30034](https://jira.mariadb.org/browse/MDEV-30034))
* rec\_get\_offsets() is not optimal ([MDEV-30567](https://jira.mariadb.org/browse/MDEV-30567))

## Backup

* mariadb-backup doesn't utilise innodb-undo-log-directory (if specified as a relative path) during copy-back operation ([MDEV-28187](https://jira.mariadb.org/browse/MDEV-28187))
* mariadb-backup issues error messages during InnoDB tablespaces export on partial backup preparing ([MDEV-29050](https://jira.mariadb.org/browse/MDEV-29050))
* mariadb-backup does not copy Aria logs if aria\_log\_dir\_path is used ([MDEV-30968](https://jira.mariadb.org/browse/MDEV-30968))

### Replication

* Fixed a deadlock on parallel slave involving full image Write event on the sequence engine ([MDEV-29621](https://jira.mariadb.org/browse/MDEV-29621))
* Fixed an attempted out-of-order binlogging error on slave involving ALTER on the sequence engine ([MDEV-31077](https://jira.mariadb.org/browse/MDEV-31077))
* Corrected non-versioned master to versioned slave replication on no-unique attribute table ([MDEV-30430](https://jira.mariadb.org/browse/MDEV-30430))
* Mended encrypted binlog master to error out to gtid-mode slave when master could not decrypt a binlog file ([MDEV-28798](https://jira.mariadb.org/browse/MDEV-28798))
* Refined optimistic parallel slave to error-exit without any hang ([MDEV-30780](https://jira.mariadb.org/browse/MDEV-30780))

### Optimizer

* [Split Materialized](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/optimizations-for-derived-tables/lateral-derived-optimization) optimization is improved to re-fill the materialized table only if necessary. The fewer number of table refills is taken into account when choosing query plan, too ([MDEV-26301](https://jira.mariadb.org/browse/MDEV-26301)).
* Queries using `SELECT DISTINCT some_expression(aggregate_function())` could produce wrong query result. ([MDEV-20057](https://jira.mariadb.org/browse/MDEV-20057))
* EXPLAIN could erroneously report that [Rowid Filter optimization](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/rowid-filtering-optimization) is used for partitioned tables. Partitioned tables do not support it. ([MDEV-30596](https://jira.mariadb.org/browse/MDEV-30596))
* A bug in selectivity computations for SINGLE/DOUBLE\_PREC\_HB histograms could cause wrong estimates to be produced. This could cause the optimizer to pick sub-optimal query plans ([MDEV-31067](https://jira.mariadb.org/browse/MDEV-31067)).

### Docker Official Images

* Add replication setup to containers contributed by Md Sahil ([MDEV-29762](https://jira.mariadb.org/browse/MDEV-29762))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2022-47015](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-47015)

## Changelog

For a complete list of changes made in [MariaDB 10.4.29](mariadb-10-4-29-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10-4-29-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.29](mariadb-10-4-29-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-11-3-10-10-4-10-9-6-10-8-8-10-6-13-10-5-20-10-4-29-and-10-3-39-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
