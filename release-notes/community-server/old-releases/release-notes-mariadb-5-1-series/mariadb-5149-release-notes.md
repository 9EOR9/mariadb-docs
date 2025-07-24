# MariaDB 5.1.49 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.1.49) | **Release Notes** | [Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5149-changelog.md) |[Overview of 5.1](changes-improvements-in-mariadb-5-1.md)

**Release date:** 09 Aug 2010

For a list of every change made in this release, see the [Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5149-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

In addition to the differences noted in previous [release notes](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/release-notes/README.md) and [changelogs](../../../connectors/odbc/changelogs/), the main differences\
between MariaDB and MySQL are:

## Includes MySQL 5.1.49

For [MariaDB 5.1.49](mariadb-5149-release-notes.md) we have merged in all of the upstream changes from MySQL\
5.1.48 and 5.1.49. The MySQL [5.1.48](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-48.html), and [5.1.49](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-49.html) release\
notes have details of what changes were made upstream by MySQL since 5.1.47.

## Includes [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) 5.1.47-11.2

We have included XtraDB from Percona Server 5.1.47-11.2 in this version of\
MariaDB. The [XtraDB 5.1.47-11.2 release notes](https://www.percona.com/docs/wiki/percona-server:release_notes_51#release_5147-112)\
page has details of the changes made to XtraDB since version 1.0.6-10 (the\
version included in [MariaDB 5.1.47](mariadb-5147-release-notes.md)).

## Aria Engine Fixes and Enhancements

In this version of MariaDB we have fixed several recovery and other bugs in the\
Aria engine. See the [changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5149-changelog.md) for more details and\
links to the individual bug reports.

## Windows Installer

An installer for Windows has been included in this version of MariaDB. The\
installer allows choosing which parts of MariaDB to install (devel headers,\
client libraries, and etc...), setting the install directory, and optionally\
installing MariaDB as a Windows service.

The win32 zip file contains both a release and a debug build, and just unzips\
to a directory. For this reason, the installer is recommended for regular use\
while the zip file is better for special-purpose installations for power users.

## New Location for Release Notes and Changelogs

For this release of MariaDB the Release Notes and Changelog are located at the\
new [Askmonty.org Knowledgebase](https://kb.askmonty.org). Over time, the\
Knowledgebase will become the primary source of MariaDB documentation and\
release information. Documentation, Changelogs, Release Notes for previous\
versions of MariaDB will be migrated here over the next few months. Redirects\
will be created for items as they are moved from the [wiki](https://askmonty.org/wiki), so any bookmarks will continue to work after\
a page has been moved.

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
