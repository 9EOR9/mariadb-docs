# MariaDB 10.1.41 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.41/)[Release Notes](mariadb-10141-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10141-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 31 Jul 2019

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.41](mariadb-10141-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-19922](https://jira.mariadb.org/browse/MDEV-19922): [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 10.2
* [MDEV-18328](https://jira.mariadb.org/browse/MDEV-18328): [Disks Plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/disks-plugin) is now stable and requires the [FILE privilege](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant).
* Update InnoDB/XtraDB from MySQL 5.6.45 and Percona Server 5.6.44-86.0
* ALTER TABLE: [MDEV-16060](https://jira.mariadb.org/browse/MDEV-16060)
* FULLTEXT INDEX: [MDEV-14154](https://jira.mariadb.org/browse/MDEV-14154), [MDEV-18220](https://jira.mariadb.org/browse/MDEV-18220), [MDEV-19441](https://jira.mariadb.org/browse/MDEV-19441), [MDEV-19445](https://jira.mariadb.org/browse/MDEV-19445)
* Encryption: [MDEV-13983](https://jira.mariadb.org/browse/MDEV-13983), [MDEV-16866](https://jira.mariadb.org/browse/MDEV-16866)
* Galera + FOREIGN KEY: [MDEV-19660](https://jira.mariadb.org/browse/MDEV-19660)
* Recovery & mariadb-backup: [MDEV-19978](https://jira.mariadb.org/browse/MDEV-19978)
* Other: [MDEV-19614](https://jira.mariadb.org/browse/MDEV-19614), [MDEV-20102](https://jira.mariadb.org/browse/MDEV-20102)
* [MDEV-20091](https://jira.mariadb.org/browse/MDEV-20091): DROP TEMPORARY table is logged despite no CREATE was logged
* [MDEV-19491](https://jira.mariadb.org/browse/MDEV-19491): update query stopped working after mariadb upgrade
* [MDEV-20110](https://jira.mariadb.org/browse/MDEV-20110): don't try to load client plugins with invalid names
* [MDEV-19427](https://jira.mariadb.org/browse/MDEV-19427): mysql\_upgrade\_service throws exception upgrading from 10.0 to 10.3
* As per the [MariaDB Deprecation Policy](../../about/platform-deprecation-policy.md), this will be the last release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) for OpenSUSE 42.3 and Ubuntu 18.10 "Cosmic"
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2019-2805](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2805)
  * [CVE-2019-2740](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2740)
  * [CVE-2019-2739](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2739)
  * [CVE-2019-2737](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2737)
  * [CVE-2020-2922](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2922)
  * [CVE-2021-2007](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2007)

## Changelog

For a complete list of changes made in [MariaDB 10.1.41](mariadb-10141-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10141-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.1.41](mariadb-10141-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-7-10-3-17-10-2-26-10-1-41-and-5-5-65-now-available/).

A file format compatibility bug that was introduced in [MariaDB 10.1.0](mariadb-10-1-0-release-notes.md) was fixed in [MariaDB 10.1.21](mariadb-10121-release-notes.md).\
Using [page\_compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression) or non-default [innodb\_page\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) created files that were incompatible with [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) or MySQL 5.6. [MariaDB 10.1.21](mariadb-10121-release-notes.md) and higher will convert affected files from earlier [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) releases to a compatible format.**This prevents a downgrade to earlier** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **versions.**[See the commit for details.](https://github.com/MariaDB/server/commit/ab1e6fefd869242d962cb91a006f37bb9ad534a7)

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
