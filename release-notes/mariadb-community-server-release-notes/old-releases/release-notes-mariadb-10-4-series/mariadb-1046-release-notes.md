# MariaDB 10.4.6 Release Notes

The most recent release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download](https://downloads.mariadb.org/mariadb/10.4.6/)[Release Notes](mariadb-1046-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-1046-changelog.md)[Overview of 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104)

**Release date:** 18 Jun 2019

With this release, [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is now the current _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.6](mariadb-1046-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) **see the**[**What is MariaDB 10.4?**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

Notable changes of this release include:

* MariaDB Server is now statically linked with the bundled wolfSSL library in MSI and ZIP packages on Windows, as well as in .deb packages provided by Debian's and Ubuntu's default repositories ([MDEV-18531](https://jira.mariadb.org/browse/MDEV-18531)).
  * See [TLS and Cryptography Libraries Used by MariaDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/securing-mariadb-encryption/tls-and-cryptography-libraries-used-by-mariadb) for more details.
* MariaDB Named Commands ([MDEV-17591](https://jira.mariadb.org/browse/MDEV-17591))
* System-versioned tables: [MDEV-19486](https://jira.mariadb.org/browse/MDEV-19486)
* Galera: [MDEV-17458](https://jira.mariadb.org/browse/MDEV-17458)
* Virtual columns: [MDEV-19027](https://jira.mariadb.org/browse/MDEV-19027), [MDEV-19602](https://jira.mariadb.org/browse/MDEV-19602)
* Recovery: [MDEV-19541](https://jira.mariadb.org/browse/MDEV-19541), [MDEV-19587](https://jira.mariadb.org/browse/MDEV-19587), [MDEV-19435](https://jira.mariadb.org/browse/MDEV-19435)
* Encryption: [MDEV-19509](https://jira.mariadb.org/browse/MDEV-19509), [MDEV-19695](https://jira.mariadb.org/browse/MDEV-19695)
* Other:
  * [MDEV-19614](https://jira.mariadb.org/browse/MDEV-19614) - SET GLOBAL innodb\_ deadlock due to LOCK\_global\_system\_variables
  * [MDEV-19725](https://jira.mariadb.org/browse/MDEV-19725) - Incorrect error handling in ALTER TABLE
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 10.4.6](mariadb-1046-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-1046-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.6](mariadb-1046-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-6-first-stable-10-4-release-and-mariadb-connector-j-2-4-2-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
