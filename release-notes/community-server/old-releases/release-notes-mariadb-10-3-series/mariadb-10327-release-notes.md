# MariaDB 10.3.27 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download 10.3.27](https://downloads.mariadb.org/mariadb/10.3.27/) | [Release Notes](mariadb-10327-release-notes.md) | [Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10327-changelog.md) | [Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 11 Nov 2020

[MariaDB 10.3](what-is-mariadb-103.md) is the previous stable series of MariaDB, and an evolution of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else and\
with backported and reimplemented features from MySQL.

[MariaDB 10.3.27](mariadb-10327-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* Out-of-cycle release to fix regressions in [MariaDB 10.3.26](mariadb-10326-release-notes.md)
* Follow up to [MDEV-19838](https://jira.mariadb.org/browse/MDEV-19838) to alter protocol checks to support the following implementations (which add garbage to the end of some packets):
  * PHP PDO (all versions) ([MDEV-24121](https://jira.mariadb.org/browse/MDEV-24121))
  * mysqlnd (from PHP < 7.3) ([MDEV-24121](https://jira.mariadb.org/browse/MDEV-24121))
  * mysql-connector-python (all versions) ([MDEV-24134](https://jira.mariadb.org/browse/MDEV-24134))
  * and mysql-connector-java (all versions)
* The query optimizer consumed a lot of memory when handling construct in form of `key_column [NOT] IN (large-list-of constants)` ([MDEV-24117](https://jira.mariadb.org/browse/MDEV-24117))
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-`-``#`

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.27](mariadb-10327-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10327-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.27](mariadb-10327-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-8-10-4-17-10-3-27-and-10-2-36-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
