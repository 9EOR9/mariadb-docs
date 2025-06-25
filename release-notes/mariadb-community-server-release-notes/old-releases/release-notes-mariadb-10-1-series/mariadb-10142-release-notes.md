# MariaDB 10.1.42 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

After an upgrade MariaDB Server can crash if InnoDB tables exist with a `FULLTEXT INDEX` and a `FOREIGN KEY` constraint attached to them. We got reports that the crash already will be encountered on startup, but a crash is also possible at a later stage. See [MDEV-20987](https://jira.mariadb.org/browse/MDEV-20987) for more details.**Do not download or use this release.**

[Download](https://mariadb.com/downloads/)[Release Notes](mariadb-10142-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10142-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.1.42/)

**Release date:** 5 Nov 2019

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.42](mariadb-10142-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-17638](https://jira.mariadb.org/browse/MDEV-17638): Improved `innochecksum` error messages
* [MDEV-20247](https://jira.mariadb.org/browse/MDEV-20247): Replication hangs with "`preparing`" and never starts
* FULLTEXT INDEX:
  * [MDEV-19647](https://jira.mariadb.org/browse/MDEV-19647): Server hangs after dropping full text indexes and restart
  * [MDEV-19529](https://jira.mariadb.org/browse/MDEV-19529): InnoDB hang on `DROP FULLTEXT INDEX`
  * [MDEV-19073](https://jira.mariadb.org/browse/MDEV-19073): FTS row mismatch after crash recovery
  * [MDEV-20621](https://jira.mariadb.org/browse/MDEV-20621): FULLTEXT INDEX activity causes InnoDB hang
* [MDEV-20927](https://jira.mariadb.org/browse/MDEV-20927): Duplicate key with auto increment
* [MDEV-19376](https://jira.mariadb.org/browse/MDEV-19376): Repl\_semi\_sync\_master::commit\_trx assertion
* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) updated to 25.3.28
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2019-2974](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2974)
  * [CVE-2020-2780](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2780)
  * [CVE-2021-2144](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2144)

## Changelog

For a complete list of changes made in [MariaDB 10.1.42](mariadb-10142-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10142-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.1.42](mariadb-10142-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-9-10-3-19-and-10-2-28-10-1-42-and-5-5-66-now-available/).

A file format compatibility bug that was introduced in [MariaDB 10.1.0](mariadb-10-1-0-release-notes.md) was fixed in [MariaDB 10.1.21](mariadb-10121-release-notes.md).\
Using [page\_compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression) or non-default [innodb\_page\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) created files that were incompatible with [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) or MySQL 5.6. [MariaDB 10.1.21](mariadb-10121-release-notes.md) and higher will convert affected files from earlier [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) releases to a compatible format.**This prevents a downgrade to earlier** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **versions.**[See the commit for details.](https://github.com/MariaDB/server/commit/ab1e6fefd869242d962cb91a006f37bb9ad534a7)

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
