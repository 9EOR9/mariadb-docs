# MariaDB 5.2.7 Release Notes

The most recent release in the [MariaDB 5.2 series](changes-improvements-in-mariadb-5-2.md) is:[**MariaDB 5.2.14**](mariadb-5214-release-notes.md)

[Download](https://downloads.askmonty.org/mariadb/5.2.7) |**Release Notes** |[Changelog](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-2-series/broken-reference/README.md) |[Overview of 5.2](changes-improvements-in-mariadb-5-2.md)

**Release date:** 14 Jun 2011

[MariaDB 5.2.7](mariadb-527-release-notes.md) is a [Stable release](../../../mariadb-release-criteria.md). In general this means\
there are no known serious bugs and we believe the code is ready for general\
usage. A "stable" MariaDB release is equivalent to a MySQL "GA" release.

For a high-level description of [MariaDB 5.2.7](mariadb-527-release-notes.md) see the[What is MariaDB 5.2](changes-improvements-in-mariadb-5-2.md) page.

For a list of every change made in [MariaDB 5.2.7](mariadb-527-release-notes.md), including the various bugs\
that were fixed and links to detailed information on each push, see the[MariaDB 5.2.7 Changelog](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-2-series/broken-reference/README.md). See previous[release notes](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/release-notes/README.md) and [changelogs](../../../connectors/odbc/changelogs/) for changes made in previous\
versions of MariaDB.

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

Be notified of new releases automatically by adding the[releases rss feed](https://montyprogram.com/news/feed/mariadb_releases) to\
your favorite feed reader or by [subscribing](https://mariadb.org) to the\
announce 'at' mariadb.org announcement list (this is a low traffic,\
announce-only list).

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

[MariaDB 5.2.7](mariadb-527-release-notes.md) contains the following changes:

## Faster Internal Temporary Tables

In [MariaDB 5.2.7](mariadb-527-release-notes.md) we've added some improvements and optimizations which result\
in faster internal temporary tables for some edge cases (when using GROUP BY\
without summary functions).

## HeidiSQL GUI client now included in Windows MSI package

Beginning with [MariaDB 5.2.7](mariadb-527-release-notes.md), the GPLv2 licensed [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) graphical client is now included in the\
Windows MSI installer package. A big thanks to Ansgar Becker for helping make\
this happen.

## Red Hat Enterprise Linux (RHEL) 5 RPMs

Starting with [MariaDB 5.2.7](mariadb-527-release-notes.md), we are now building Red Hat Enterprise Linux\
(RHEL) 5 RPM packages. This is in addition to our CentOS 5 packages, which we\
will continue to provide.

## Other fixes and enhancements

* Fixed problem with wrong priority (nice -19) on mysqld server
* Fixed crash with partitioned archive tables where there were too few file\
  descriptors
* Lots of small fixes for easier windows builds

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
