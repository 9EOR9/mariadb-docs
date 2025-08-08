# MariaDB 10.1.38 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.38) | [Release Notes](mariadb-10138-release-notes.md) | [Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10138-changelog.md) | [Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 6 Feb 2019

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.38](mariadb-10138-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 9.5
* [MDEV-17475](https://jira.mariadb.org/browse/MDEV-17475): Maximum value of [table\_definition\_cache](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/variables-and-modes/server-system-variables#table_definition_cache) is now `2097152`
* [MDEV-13671](https://jira.mariadb.org/browse/MDEV-13671): InnoDB should use case-insensitive column name comparisons like the rest of the server
* ALTER TABLE fixes: [MDEV-17230](https://jira.mariadb.org/browse/MDEV-17230), [MDEV-16499](https://jira.mariadb.org/browse/MDEV-16499), [MDEV-17904](https://jira.mariadb.org/browse/MDEV-17904), [MDEV-17833](https://jira.mariadb.org/browse/MDEV-17833),[MDEV-17470](https://jira.mariadb.org/browse/MDEV-17470), [MDEV-18237](https://jira.mariadb.org/browse/MDEV-18237), [MDEV-18016](https://jira.mariadb.org/browse/MDEV-18016)
* Improvements to InnoDB page checksum, recovery, and mariadb-backup: [MDEV-17957](https://jira.mariadb.org/browse/MDEV-17957),[MDEV-12112](https://jira.mariadb.org/browse/MDEV-12112), [MDEV-18025](https://jira.mariadb.org/browse/MDEV-18025), [MDEV-18279](https://jira.mariadb.org/browse/MDEV-18279), [MDEV-18183](https://jira.mariadb.org/browse/MDEV-18183)
* Galera
  * [MDEV-15740](https://jira.mariadb.org/browse/MDEV-15740): Galera durability fix
  * New configuration variable `wsrep_certification_rules`, used for\
    controlling whether to use new/optimized\
    (`--wsrep_certification_rules=optimized`) certification rules or the\
    old/classic ones (`--wsrep_certification_rules=strict`). Setting the\
    variable to `strict` can cause more certification failures.
* Debian has stopped supporting the ppc64el architecture for Debian 8\
  Jessie and so this is the last release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) on Jessie for that\
  architecture
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2019-2537](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2537)
  * [CVE-2019-2529](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2529)

## Changelog

For a complete list of changes made in [MariaDB 10.1.38](mariadb-10138-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10138-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.1.38](mariadb-10138-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-1-38-now-available/).

A file format compatibility bug that was introduced in [MariaDB 10.1.0](mariadb-10-1-0-release-notes.md) was fixed in [MariaDB 10.1.21](mariadb-10121-release-notes.md).\
Using [page\_compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression) or non-default [innodb\_page\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) created files that were incompatible with [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) or MySQL 5.6. [MariaDB 10.1.21](mariadb-10121-release-notes.md) and higher will convert affected files from earlier [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) releases to a compatible format.**This prevents a downgrade to earlier** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **versions.**[See the commit for details.](https://github.com/MariaDB/server/commit/ab1e6fefd869242d962cb91a006f37bb9ad534a7)

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
