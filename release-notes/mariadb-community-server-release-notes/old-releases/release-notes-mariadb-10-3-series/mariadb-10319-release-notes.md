# MariaDB 10.3.19 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

After an upgrade MariaDB Server can crash if InnoDB tables exist with a `FULLTEXT INDEX` and a `FOREIGN KEY` constraint attached to them. We got reports that the crash already will be encountered on startup, but a crash is also possible at a later stage. See [MDEV-20987](https://jira.mariadb.org/browse/MDEV-20987) for more details.**Do not download or use this release.**

[Download](https://mariadb.com/downloads/)[Release Notes](mariadb-10319-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10319-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.3.19/)

**Release date:** 5 Nov 2019

[MariaDB 10.3](what-is-mariadb-103.md) is the previous stable series of MariaDB, and an evolution of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features\
not found anywhere else and with backported and reimplemented features from\
MySQL.

[MariaDB 10.3.19](mariadb-10319-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-20864](https://jira.mariadb.org/browse/MDEV-20864): Debug-only option [innodb\_change\_buffer\_dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_change_buffer_dump) for dumping the contents of the InnoDB change buffer to the server error log at startup.
* mariadb-backup:
  * [MDEV-18438](https://jira.mariadb.org/browse/MDEV-18438): mbstream recreates xtrabackup\_info on same directory as backup file
  * [MDEV-20703](https://jira.mariadb.org/browse/MDEV-20703): mariadb-backup creates binlog files in server binlog directory on --prepare --export step
* Read-only replicas
  * Issues related to read only replicas are fixed:
  * [CREATE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-table), [DROP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/drop/drop-table), [ALTER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table), [INSERT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/inserting-loading-data/insert) and [DELETE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/delete) of temporary tables are not logged to binary log, even in [statement](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log/binary-log-formats#statement-based-logging) or [mixed](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log/binary-log-formats#mixed-logging) mode. With earlier MariaDB versions, one can avoid the problem with temporary tables by using [binlog\_format=ROW](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log/binary-log-formats#row-based-logging) in which cases temporary tables are never logged.
  * Changes to temporary tables created during `read_only` will not be logged even after `read_only` mode is disabled (for example if the replica is promoted to a primary).
  * The Admin statements [ANALYZE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/analyze-table), [OPTIMIZE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimizing-tables/optimize-table) and [REPAIR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/repair-table) will not be logged to the binary log under read-only.
* FULLTEXT INDEX:
  * [MDEV-19647](https://jira.mariadb.org/browse/MDEV-19647): Server hangs after dropping full text indexes and restart
  * [MDEV-19529](https://jira.mariadb.org/browse/MDEV-19529): InnoDB hang on `DROP FULLTEXT INDEX`
  * [MDEV-19073](https://jira.mariadb.org/browse/MDEV-19073): FTS row mismatch after crash recovery
  * [MDEV-20621](https://jira.mariadb.org/browse/MDEV-20621): FULLTEXT INDEX activity causes InnoDB hang
* [MDEV-20927](https://jira.mariadb.org/browse/MDEV-20927): Duplicate key with auto increment
* ALTER TABLE:
  * [MDEV-20799](https://jira.mariadb.org/browse/MDEV-20799): DROP Virtual Column crash
  * [MDEV-20852](https://jira.mariadb.org/browse/MDEV-20852): BtrBulk is unnecessarily holding `dict_index_t::lock`
* System-Versioned Tables:
  * [MDEV-16210](https://jira.mariadb.org/browse/MDEV-16210): FK constraints on versioned tables use historical rows, which may cause constraint violation
  * [MDEV-20812](https://jira.mariadb.org/browse/MDEV-20812): Unexpected `ER_ROW_IS_REFERENCED_2` or server crash in `row_ins_foreign_report_err` upon DELETE from versioned table with FK
* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) updated to 25.3.28
* Packages for Ubuntu 19.10 Eoan have been added in this release
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2019-2974](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2974)
  * [CVE-2019-2938](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2938)
  * [CVE-2020-2780](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2780)
  * [CVE-2021-2144](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2144)

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.19](mariadb-10319-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10319-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.19](mariadb-10319-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-9-10-3-19-and-10-2-28-10-1-42-and-5-5-66-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
