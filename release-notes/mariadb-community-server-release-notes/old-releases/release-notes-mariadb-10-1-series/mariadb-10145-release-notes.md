# MariaDB 10.1.45 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.45/)[Release Notes](mariadb-10145-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10145-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 12 May 2020

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.45](mariadb-10145-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 11.0 ([MDEV-22032](https://jira.mariadb.org/browse/MDEV-22032))
* InnoDB ALTER TABLE fixes ([MDEV-21564](https://jira.mariadb.org/browse/MDEV-21564), [MDEV-19092](https://jira.mariadb.org/browse/MDEV-19092), [MDEV-21549](https://jira.mariadb.org/browse/MDEV-21549))
* InnoDB FULLTEXT INDEX fixes ([MDEV-21563](https://jira.mariadb.org/browse/MDEV-21563))
* Corruption for `SET GLOBAL innodb_` string variables ([MDEV-22393](https://jira.mariadb.org/browse/MDEV-22393))
* wsrep performance optimization ([MDEV-7962](https://jira.mariadb.org/browse/MDEV-7962))
* Test suite, Add JUnit support to MTR to generate XML test result ([MDEV-22176](https://jira.mariadb.org/browse/MDEV-22176))
* [mysqldump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysqldump) parameter, `--ignore-table-data`, added ([MDEV-22037](https://jira.mariadb.org/browse/MDEV-22037))
* Refactored `MYSQL_BIN_LOG::xid_count_per_binlog` to satisfy UBSAN enabled build ([MDEV-20923](https://jira.mariadb.org/browse/MDEV-20923))
* Unregister of slave threads disconnected before COM\_BINLOG\_DUMP (Bug#29915479)
* Server can fail while replicating conditional comments (Bug#28388217)
* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) updated to 25.3.29
* Added the `xml-report` option to [mysql-test-run](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/testing-tools/mariadb-test/mariadb-test-run-pl-options) ([MDEV-22176](https://jira.mariadb.org/browse/MDEV-22176))
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) for Debian 8 "Jessie"
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2020-2752](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2752)
  * [CVE-2020-2812](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2812)
  * [CVE-2020-2814](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2814)

## Changelog

For a complete list of changes made in [MariaDB 10.1.45](mariadb-10145-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10145-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.1.45](mariadb-10145-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-13-10-3-23-10-2-32-10-1-45-and-5-5-68-now-available).\
Thanks, and enjoy MariaDB!

A file format compatibility bug that was introduced in [MariaDB 10.1.0](mariadb-10-1-0-release-notes.md) was fixed in [MariaDB 10.1.21](mariadb-10121-release-notes.md).\
Using [page\_compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression) or non-default [innodb\_page\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) created files that were incompatible with [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) or MySQL 5.6. [MariaDB 10.1.21](mariadb-10121-release-notes.md) and higher will convert affected files from earlier [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) releases to a compatible format.**This prevents a downgrade to earlier** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **versions.**[See the commit for details.](https://github.com/MariaDB/server/commit/ab1e6fefd869242d962cb91a006f37bb9ad534a7)

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
