# MariaDB 5.1.47 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.1.47) | **Release Notes** | [Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5147-changelog.md) |[Overview of 5.1](changes-improvements-in-mariadb-5-1.md)

**Release date:** 01 Jun 2010

For a list of every change made in this release, see the[changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5147-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

In addition to the differences noted in previous[release notes](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/release-notes/README.md) and [changelogs](../../../connectors/odbc/changelogs/), the main\
differences between MariaDB and MySQL are:

## Includes MySQL 5.1.47

For [MariaDB 5.1.47](mariadb-5147-release-notes.md) we have merged in all of the upstream changes from MySQL\
5.1.45, 5.1.46, and 5.1.47. The MySQL[5.1.45](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-45.html),[5.1.46](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-46.html), and[5.1.47](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-47.html) release notes\
have details of what changes were made upstream by MySQL since 5.1.44.

## Includes [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) 1.0.6-10

We have included XtraDB 1.0.6-10 in this version of MariaDB. The[XtraDB 1.0.6-10 release notes](https://www.percona.com/docs/wiki/percona-server:release_notes_51#release_106-10)\
page has details of the changes made to XtraDB since version 1.0.6-9 (the\
version included since [MariaDB 5.1.42](mariadb-5142-release-notes.md)).

## Includes [PBXT](https://github.com/mariadb-corporation/docs-release-notes/blob/test/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/pbxt-storage-engine/README.md) 1.0.11

We have included PBXT 1.0.11 in this version of MariaDB. The[PBXT ChangeLog](https://www.primebase.org/download/ChangeLog) has a list of\
all of the changes made since PBXT 1.0.09f (the version included in MariaDB\
since 5.1.41).

Also included is the `xtstat` program. `xtstat` can be\
used to monitor all internal activity of [PBXT](https://github.com/mariadb-corporation/docs-release-notes/blob/test/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/pbxt-storage-engine/README.md).\
See [xtstat](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/xtstat) for information on this utility.

## Windows build improvements

Several steps were taken during the development of [MariaDB 5.1.47](mariadb-5147-release-notes.md) to improve\
our Windows builds. Steps included the creation of new Windows build slaves,\
fixes for Windows compiler errors, and better Windows build automation. Windows\
builds should now be included with every MariaDB release.

## Ubuntu Fixes

A few Ubuntu-specific fixes are included with [MariaDB 5.1.47](mariadb-5147-release-notes.md):

1. A fix for a dependency problem with Ubuntu 10.04 Lucid packages.
2. We now build against the full 10.04 release (we used to build against an\
   alpha version of Ubuntu 10.04).
3. A fix for an Ubuntu issue that appeared when using libmyodbc with mariadb\
   packages.

## Improved Repositories

We've fixed some process issues with the Debian, Ubuntu, and CentOS\
repositories provided by Open Query. These issues were delaying the latest\
release from appearing in the repositories. Now releases should show up in the\
repositories at around the same time a release shows up on the mirrors.

## Fewer warnings and bugs

In [MariaDB 5.1.47](mariadb-5147-release-notes.md) we've continued to fix bugs and compiler warnings, including\
bugs in MySQL 5.1.47. The [changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5147-changelog.md) has links to\
several of the bugs that we have fixed.

## Test Suite improvements

We have also continued our work in improving the test suite.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formid="4316" formId="4316" %}
