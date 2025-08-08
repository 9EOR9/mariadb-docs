# MariaDB 10.1.48 Release Notes

[Download](https://downloads.mariadb.org/mariadb/10.1.48/) | [Release Notes](mariadb-10148-release-notes.md) | [Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10148-changelog.md) | [Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 3 Nov 2020

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.48](mariadb-10148-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) updated to 25.3.31
* [BLACKHOLE Storage Engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/blackhole) maximum index size increased from 1000 to 3500 bytes ([MDEV-24017](https://jira.mariadb.org/browse/MDEV-24017))
* [Calculating (auto rounding)](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/variables-and-modes/server-system-variables#div_precision_increment) issue ([MDEV-23702](https://jira.mariadb.org/browse/MDEV-23702))
* Temporary tables can no longer overwrite existing files. Instead an error is returned should a conflict occur ([MDEV-23569](https://jira.mariadb.org/browse/MDEV-23569))
* Binlog checksum verification at recovery time ([MDEV-23832](https://jira.mariadb.org/browse/MDEV-23832))
* Verbose print-out of [Geometry types](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/geometry/geometry-types) by [mysqlbinlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog) ([MDEV-22330](https://jira.mariadb.org/browse/MDEV-22330))
* [SHOW BINLOG EVENTS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-binlog-events) from validates when binlog checksummed ([MDEV-21839](https://jira.mariadb.org/browse/MDEV-21839))
* Freeing memory of [replicate\_do\_table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#replicate_do_table) ([MDEV-23534](https://jira.mariadb.org/browse/MDEV-23534))
* Corrected verbose [mysqlbinlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog) output for multi-record Rows-log-event ([MDEV-16372](https://jira.mariadb.org/browse/MDEV-16372))
* [SET GLOBAL replicate\_do\_db = DEFAULT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#replicate_do_db) no longer causes crash ([MDEV-20744](https://jira.mariadb.org/browse/MDEV-20744))
* [User killed queries](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/kill) that were running an index condition pushdown in InnoDB/XtraDB will now return an error ([MDEV-23938](https://jira.mariadb.org/browse/MDEV-23938))
* As per the [MariaDB Deprecation Policy](../../about/platform-deprecation-policy.md), this will be the last release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) for CentOS/RHEL 6.x
* As per the [MariaDB Maintenance Policy](https://mariadb.org/about/#maintenance-policy), this will be the final release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md)
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2020-14812](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14812)
  * [CVE-2020-14765](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14765)
  * [CVE-2020-28912](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-28912) ([MDEV-24040](https://jira.mariadb.org/browse/MDEV-24040))

## Changelog

For a complete list of changes made in [MariaDB 10.1.48](mariadb-10148-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10148-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.1.48](mariadb-10148-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-10-10-3-20-10-2-29-and-10-1-46-now-available/).

A file format compatibility bug that was introduced in [MariaDB 10.1.0](mariadb-10-1-0-release-notes.md) was fixed in [MariaDB 10.1.21](mariadb-10121-release-notes.md).\
Using [page\_compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression) or non-default [innodb\_page\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) created files that were incompatible with [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) or MySQL 5.6. [MariaDB 10.1.21](mariadb-10121-release-notes.md) and higher will convert affected files from earlier [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) releases to a compatible format.**This prevents a downgrade to earlier** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **versions.**[See the commit for details.](https://github.com/MariaDB/server/commit/ab1e6fefd869242d962cb91a006f37bb9ad534a7)

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
