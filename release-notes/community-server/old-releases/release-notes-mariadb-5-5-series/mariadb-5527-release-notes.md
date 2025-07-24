# MariaDB 5.5.27 Release Notes

The most recent release in the [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.27) |**Release Notes** |[Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5527-changelog.md) |[Overview of 5.5](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md)

**Release date:** 07 Sep 2012

[MariaDB 5.5.27](mariadb-5527-release-notes.md) is a [_**Stable**_](../../about/release-criteria.md) _**(GA)**_\
release. In general this means that there are no known serious bugs,\
except for those marked as feature requests, that no bugs were fixed\
since last release that caused a notable code changes, and that we\
believe the code is ready for general usage (based on bug inflow).

**For a description of** [**MariaDB 5.5**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **see the**[**What is MariaDB 5.5**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **page.**

For a list of changes made in [MariaDB 5.5.27](mariadb-5527-release-notes.md), with links to detailed\
information on each push, see the [MariaDB 5.5.27 Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5527-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Includes [MariaDB 5.3.8](../release-notes-mariadb-5-3-series/mariadb-538-release-notes.md) and MySQL 5.5.27

[MariaDB 5.5.27](mariadb-5527-release-notes.md) includes [MariaDB 5.3.8](../release-notes-mariadb-5-3-series/mariadb-538-release-notes.md) and MySQL 5.5.27. See the [MariaDB 5.3.8](../release-notes-mariadb-5-3-series/mariadb-538-release-notes.md)[Release Notes](../release-notes-mariadb-5-3-series/mariadb-538-release-notes.md) and [Changelog](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) for more information on the changes in [MariaDB 5.3.8](../release-notes-mariadb-5-3-series/mariadb-538-release-notes.md). See [Changes in MySQL 5.5.27](https://dev.mysql.com/doc/refman/5.5/en/news-5-5-27.html)\
for what changed between this and previous MySQL versions.

## Includes XtraDB from Percona-Server-5.5.27-rel28.1

For [MariaDB 5.5.27](mariadb-5527-release-notes.md), we've merged in XtraDB from Percona Server Percona-Server-5.5.27-rel28.0 and 5.5.27-rel28.1. See the Percona Server [5.5.27-28.0](https://www.percona.com/doc/percona-server/5.5/release-notes/Percona-Server-5.5.27-28.0.html) and [5.5.27-28.1](https://www.percona.com/doc/percona-server/5.5/release-notes/Percona-Server-5.5.27-28.1.html) release notes for more information.

## Alternative Linux binaries

In this version of MariaDB we are starting to provide alternative Linux binaries built on a different build machine with a different build toolchain. Binaries created on this box require at least GLIBC\_2.14. For continuity, we are still providing binaries built with the same toolchain as previous releases. The alternative binaries have a "(GLIBC\_2.14)" label to distinguish them from the others.

## Fixes and Performance Enhancements

This release includes fixes for the following security vulnerabilities:

* [CVE-2012-3163](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3163)
* [CVE-2012-3158](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3158)
* [CVE-2012-3177](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3177)
* [CVE-2012-3150](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3150)
* [CVE-2012-3197](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3197)
* [CVE-2013-1548](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1548)
* [CVE-2012-3166](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3166)
* [CVE-2012-3173](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3173)
* [CVE-2012-3167](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3167)

This release fixes numerous cases of the incorrect identifier quoting in the replication code. They were open [SQL injection](https://en.wikipedia.org/wiki/SQL_injection) vulnerabilities, that allowed, to a certain extent, to bypass the database privilege system and modify the data, that one was granted no access to. See [MDEV-382](https://jira.mariadb.org/browse/MDEV-382) for details. ([CVE-2012-4414](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-4414))

Additionally, 5.5.27 includes several other bug fixes and\
performance enhancements.

See the [MariaDB 5.5.27 Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5527-changelog.md) for full details.

Thanks, and enjoy MariaDB!

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
