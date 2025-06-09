# MariaDB 5.5.28a Release Notes

The most recent release in the [MariaDB 5.5](broken-reference) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.28a) | **Release Notes** | [Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5528a-changelog.md) |[Overview of 5.5](broken-reference)

**Release date:** 29 Nov 2012

[MariaDB 5.5.28](mariadb-5528-release-notes.md)a is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_\
release. In general this means that there are no known serious bugs,\
except for those marked as feature requests, that no bugs were fixed\
since last release that caused a notable code changes, and that we\
believe the code is ready for general usage (based on bug inflow).

**For a description of** [**MariaDB 5.5**](broken-reference) **see the**[**What is MariaDB 5.5**](broken-reference) **page.**

For a list of changes made in [MariaDB 5.5.28](mariadb-5528-release-notes.md)a, with links to detailed\
information on each push, see the[MariaDB 5.5.28a Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5528a-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Important Security Fix for a Buffer Overflow Bug

[MariaDB 5.5.28](mariadb-5528-release-notes.md)a includes a fix for [CVE-2012-5611](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5611), a vulnerability that allowed an authenticated user to crash MariaDB server or to execute arbitrary code with the privileges of the `mysqld` process. **This is a serious security issue.** We recommend upgrading from older versions as soon as possible.

Thanks, and enjoy MariaDB!

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.
