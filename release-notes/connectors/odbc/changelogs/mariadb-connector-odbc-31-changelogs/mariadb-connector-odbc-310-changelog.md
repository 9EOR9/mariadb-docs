# MariaDB Connector/ODBC 3.1.0 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/?showall=1\&tab=connectors\&group=mariadbconnectors\&product=ODBC%20connector\&version=3.1.0)[Release Notes](../../mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-0-release-notes.md)[Changelog](mariadb-connector-odbc-310-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-odbc/README.md)

**Release date:** 29 Jan 2019

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-0-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #bd783e5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bd783e5)\
  2019-01-28 20:42:11 +0100
  * Changed connector quality to RC.
* [Revision #83f9b26](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/83f9b26)\
  2019-01-23 23:51:27 +0100
  * Some more test fixes, making them work on OSX
* [Revision #07f6b00](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/07f6b00)\
  2019-01-23 23:19:34 +0100
  * [ODBC-212](https://jira.mariadb.org/browse/ODBC-212) The fix and the testcase\
    Wrong Input/Output parameter type when mapping SQLBindParam to SQLBindParameter
* [Revision #7d8dc44](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7d8dc44)\
  2019-01-23 21:50:15 +0100
  * Merge branch '`odbc-3.0`' into develop
* [Revision #646803f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/646803f)\
  2019-01-23 21:28:59 +0100
  * [ODBC-213](https://jira.mariadb.org/browse/ODBC-213) The fix and the testcase\
    SQL\_DESC\_PARAMETER\_TYPE is SQLSMALLINT, but if application tried to read it into SQLSMALLINT buffer, memory would be corrupted, and application would crash. Also, this field should exist only in IPD. While it was accessible also in IRD.
* [Revision #6dd7bc4](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6dd7bc4)\
  2019-01-22 23:23:30 +0100
  * Fix of few tests in blob.c and bulk.c
* [Revision #45e4669](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/45e4669)\
  2019-01-20 23:27:49 +0100
  * Changed in Travis compiler for OS X to gcc
* [Revision #8ce8fd5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8ce8fd5)\
  2019-01-18 00:19:10 +0100
  * [ODBC-210](https://jira.mariadb.org/browse/ODBC-210) Warnings fix on OSX
* [Revision #df99372](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/df99372)\
  2019-01-16 19:11:55 +0100
  * [ODBC-209](https://jira.mariadb.org/browse/ODBC-209) Added dependencies on C/C plugins into MSI project
* [Revision #2b6ec8c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2b6ec8c)\
  2019-01-14 09:51:31 +0200
  * Speed up Mac build on Travis by not updating brew
* [Revision #ad991a2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ad991a2)\
  2019-01-11 00:22:00 +0100
  * Merge of local 3.1 version with repo version
* [Revision #aa867c8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/aa867c8)\
  2019-01-08 14:17:32 +0200
  * Merge pull request #32 from rasmushoj/develop
* [Revision #787ae97](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/787ae97)\
  2019-01-08 14:08:22 +0200
  * appveyor conf cleaning and addition of artifacts
* [Revision #7ea9d17](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7ea9d17)\
  2019-01-07 16:34:16 +0200
  * Update ODBC driver name to correspond with new version
* [Revision #bffb234](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bffb234)\
  2018-12-20 10:45:22 +0000
  * Appveyor configuration MariaDB Server 10.3.11 will be downloaded and tests run against it DSN is set up directly in Windows registry.
* [Revision #976a667](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/976a667)\
  2019-01-11 00:21:42 +0100
  * Fix of the connector and testcases to make them work
* [Revision #3111b4f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3111b4f)\
  2019-01-04 02:22:16 +0100
  * Merge branch '`master`' into 'develop'
* [Revision #636d21c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/636d21c)\
  2018-12-21 00:45:35 +0100
  * [ODBC-206](https://jira.mariadb.org/browse/ODBC-206) and [ODBC-193](https://jira.mariadb.org/browse/ODBC-193) utf8mb4 has been made the default charset
* [Revision #97a6f1c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/97a6f1c)\
  2018-12-20 16:22:17 +0200
  * iODBC testing on Mac OSX (#28)
* [Revision #3a23170](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3a23170)\
  2018-12-14 01:27:19 +0100
  * [ODBC-193](https://jira.mariadb.org/browse/ODBC-193) Mores tests changes for iOdbc
* [Revision #8c22413](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8c22413)\
  2018-12-11 01:05:22 +0100
  * Merge branch '`master`' into develop
* [Revision #f400be2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f400be2)\
  2018-12-05 01:12:50 +0100
  * Mostly testcase fixes for iODBC and for UnixODBC
* [Revision #56865a6](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/56865a6)\
  2018-12-04 23:19:14 +0100
  * Merge with '`master`', updated C/C to latest commit
* [Revision #12cec4b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/12cec4b)\
  2018-11-15 17:17:17 +0100
  * [ODBC-193](https://jira.mariadb.org/browse/ODBC-193) Enabling connect and most of operations
* [Revision #bb8c6b8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bb8c6b8)\
  2018-11-14 23:35:54 +0100
  * [ODBC-193](https://jira.mariadb.org/browse/ODBC-193) Enabling build with iODBC
* [Revision #dde33ab](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/dde33ab)\
  2018-11-06 12:06:17 +0100
  * Build fix on systems other than Windows.
* [Revision #e9a0b40](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e9a0b40)\
  2018-11-05 23:59:15 +0100
  * Merge branch '`master`' into develop
* [Revision #894d718](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/894d718)\
  2018-10-11 00:45:02 +0200
  * [ODBC-189](https://jira.mariadb.org/browse/ODBC-189) Made install lib dir name configurable
* [Revision #077f001](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/077f001)\
  2018-10-09 00:36:07 +0200
  * [ODBC-23](https://jira.mariadb.org/browse/ODBC-23) C/C authentication plugins have been added to the MSI package.
* [Revision #10b5dda](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/10b5dda)\
  2018-10-02 12:54:09 +0200
  * Merge branch '`master`' into develop
* [Revision #b74e5dc](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b74e5dc)\
  2018-09-27 19:47:01 +0200
  * Version bump -> 3.1alpha
* [Revision #547589c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/547589c)\
  2018-09-27 19:38:55 +0200
  * Merge branch '`master`' into develop
* [Revision #768b94f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/768b94f)\
  2018-09-20 15:58:05 +0200
  * [ODBC-185](https://jira.mariadb.org/browse/ODBC-185) The fix and the testcase. Char fields type returned by SQLColums in case of the Unicode connection
