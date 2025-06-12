# MariaDB 5.5.32 Release Notes

The most recent release in the [MariaDB 5.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.32) | **Release Notes** | [Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5532-changelog.md) | [Overview of 5.5](broken-reference)

**Release date:** 18 Jul 2013

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release. In general this\
means that there are no known serious bugs, except for those marked as feature\
requests, that no bugs were fixed since last release that caused a notable code\
changes, and that we believe the code is ready for general usage (based on bug\
inflow).

**For a description of** [**MariaDB 5.5**](broken-reference) **see the**[**What is MariaDB 5.5?**](broken-reference) **page.**

For a list of changes made in this release, with links to detailed\
information on each push, see the[MariaDB 5.5.32 Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5532-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

This is primarily a bug-fix release.

## Includes [MariaDB 5.3.12](../release-notes-mariadb-5-3-series/mariadb-5312-release-notes.md) and MySQL 5.5.32

This release includes [MariaDB 5.3.12](../release-notes-mariadb-5-3-series/mariadb-5312-release-notes.md) and MySQL 5.5.32. See[Changes in MySQL 5.5.32](https://dev.mysql.com/doc/relnotes/mysql/5.5/en/news-5-5-32.html)\
for what changed in MySQL.

## Security fixes

This release includes fixes for the following security vulnerabilities:

* [CVE-2013-1861](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1861)
* [CVE-2013-3809](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-3809)
* [CVE-2013-3793](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-3793)
* [CVE-2013-3802](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-3802)
* [CVE-2013-3804](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-3804)
* [CVE-2013-3783](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-3783)
* [CVE-2013-3812](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-3812)
* [CVE-2016-0502](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0502)

## Other Notable Information

* Includes [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) from Percona Server-5.5.32-rel31.0
* As long as XtraDB is used, [MariaDB 5.5.32](mariadb-5532-release-notes.md) is not affected by [MySQL Bug #69623](https://bugs.mysql.com/bug.php?id=69623) (multi-file tablespaces do not work after an upgrade).

Thanks, and enjoy MariaDB!

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
