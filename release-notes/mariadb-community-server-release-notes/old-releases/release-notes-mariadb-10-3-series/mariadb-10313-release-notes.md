# MariaDB 10.3.13 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.13/)[Release Notes](mariadb-10313-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10313-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 21 Feb 2019

[MariaDB 10.3](what-is-mariadb-103.md) is an evolution\
of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.3.13](mariadb-10313-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-18254](https://jira.mariadb.org/browse/MDEV-18254): [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 9.5
* [MDEV-17475](https://jira.mariadb.org/browse/MDEV-17475): Maximum value of [table\_definition\_cache](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#table_definition_cache) is now `2097152`.
* mariadb-backup fixes: [MDEV-18185](https://jira.mariadb.org/browse/MDEV-18185), [MDEV-18201](https://jira.mariadb.org/browse/MDEV-18201), [MDEV-18194](https://jira.mariadb.org/browse/MDEV-18194), [MDEV-18415](https://jira.mariadb.org/browse/MDEV-18415), [MDEV-18611](https://jira.mariadb.org/browse/MDEV-18611)
* InnoDB ALTER TABLE fixes: [MDEV-17441](https://jira.mariadb.org/browse/MDEV-17441), [MDEV-18237](https://jira.mariadb.org/browse/MDEV-18237), [MDEV-17823](https://jira.mariadb.org/browse/MDEV-17823), [MDEV-18152](https://jira.mariadb.org/browse/MDEV-18152), [MDEV-17821](https://jira.mariadb.org/browse/MDEV-17821), [MDEV-18222](https://jira.mariadb.org/browse/MDEV-18222), [MDEV-18256](https://jira.mariadb.org/browse/MDEV-18256), [MDEV-18016](https://jira.mariadb.org/browse/MDEV-18016), [MDEV-18295](https://jira.mariadb.org/browse/MDEV-18295)
* InnoDB crash recovery fixes: [MDEV-18183](https://jira.mariadb.org/browse/MDEV-18183), [MDEV-18279](https://jira.mariadb.org/browse/MDEV-18279), [MDEV-18349](https://jira.mariadb.org/browse/MDEV-18349)
* Galera crash recovery fixes: [MDEV-15740](https://jira.mariadb.org/browse/MDEV-15740)
* [MDEV-18281](https://jira.mariadb.org/browse/MDEV-18281): COM\_RESET\_CONNECTION changes the connection encoding
* binlog fixes: [MDEV-10963](https://jira.mariadb.org/browse/MDEV-10963) & [MDEV-10963](https://jira.mariadb.org/browse/MDEV-10963)
* [Spider](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider) updated to 3.3.14
* Fixed some crashes and a few wrong results with Spider
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2019-2510](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2510)
  * [CVE-2019-2537](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2537)

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.13](mariadb-10313-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10313-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.13](mariadb-10313-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-3-13-and-mariadb-connector-c-3-0-9-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
