# MariaDB 5.2.2 Release Notes

The most recent release in the [MariaDB 5.2 series](changes-improvements-in-mariadb-5-2.md) is:[**MariaDB 5.2.14**](mariadb-5214-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.2.2-gamma) | **Release Notes** | [Changelog](../../../changelogs/changelogs-mariadb-52-series/mariadb-522-changelog.md) |[Overview of 5.2](changes-improvements-in-mariadb-5-2.md)

**Release date:** 28 Sep 2010

This is a [gamma release](../../../mariadb-release-criteria.md). In general this means we believe the code is ready for general usage (based on bug inflow), but we want more testing before calling it stable. For a list of every change made in this release, see the[Changelog](../../../changelogs/changelogs-mariadb-52-series/mariadb-522-changelog.md). For a description of this release see the [MariaDB 5.1 overview](../release-notes-mariadb-5-1-series/changes-improvements-in-mariadb-5-1.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

In addition to the differences noted in previous[release notes](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/release-notes/README.md) and[changelogs](../../../connectors/odbc/changelogs/), the main new things in this version of [MariaDB 5.2](changes-improvements-in-mariadb-5-2.md) are:

## Includes [MariaDB 5.1.50](../release-notes-mariadb-5-1-series/mariadb-5150-release-notes.md)

For [MariaDB 5.2.2](mariadb-522-release-notes.md) we have merged in all of the changes from [MariaDB 5.1](../release-notes-mariadb-5-1-series/changes-improvements-in-mariadb-5-1.md), which included[MariaDB 5.1.50](../release-notes-mariadb-5-1-series/mariadb-5150-release-notes.md) + some new bug fixes which will be in [MariaDB 5.1.51](../release-notes-mariadb-5-1-series/mariadb-5151-release-notes.md), and MySQL 5.1.51. The [MariaDB 5.1.50 release notes](../release-notes-mariadb-5-1-series/mariadb-5150-release-notes.md) have details of what changes were made.

## Maria Storage Engine Renamed to Aria

In this version of [MariaDB 5.2](changes-improvements-in-mariadb-5-2.md) the Maria Storage Engine has been renamed to[Aria](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/aria/aria-storage-engine).

## SphinxSE

The Sphinx Storage Engine has been added to MariaDB. It is built as a dynamically loadable .so plugin, so use it you need to perform a one-time `[INSTALL PLUGIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/install-plugin)`. See the [SphinxSE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/sphinx-storage-engine) page for more details.

## Bug Fixes

The main drive for this version of [MariaDB 5.2](changes-improvements-in-mariadb-5-2.md) (compared to the previous two\
beta releases) was to fix bugs and otherwise prepare for a stable release of[MariaDB 5.2](changes-improvements-in-mariadb-5-2.md). So, as in [previous releases](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/release-notes/README.md), in [MariaDB 5.2.2](mariadb-522-release-notes.md)\
many bug fixes and other improvements were made. See the[Changelog](../../../changelogs/changelogs-mariadb-52-series/mariadb-522-changelog.md) for details and links to the bugs that were\
fixed.

CC BY-SA / Gnu FDL

{% @marketo/form formid="4316" formId="4316" %}
