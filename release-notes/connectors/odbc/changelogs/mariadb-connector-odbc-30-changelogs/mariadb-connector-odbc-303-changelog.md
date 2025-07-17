# Connector/ODBC 3.0.3 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/3.0.3)[Release Notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-303-release-notes.md)[Changelog](mariadb-connector-odbc-303-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-odbc/README.md)

**Release date:** 8 Feb 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-303-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #ed35eb6](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ed35eb6)\
  2018-02-06 12:55:20 +0100
  * Added missing dependency in windows build(version.lib is needed by C/C)
* [Revision #ed92516](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ed92516)\
  2018-02-04 23:01:24 +0100
  * \[[ODBC-134](https://jira.mariadb.org/browse/ODBC-134)] The fix and the test-case. Fetch would fail, if unbound column contained NULL, and for that column some arbitrary descriptor field was set by application(but not value/len/ind buffer ptrs). The bug affected ADO, as that is something it can do in some cases with CursorLocation adUseClient
* [Revision #b7520af](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b7520af)\
  2018-02-01 10:20:13 +0100
  * For the info type SQL\_SCHEMA\_TERM/SQL\_OWNER\_TERM the connector returned wrong length. Or more exactly - did not write anything into application's length buffer. The fix and the test-case. Possibly fixes [ODBC-109](https://jira.mariadb.org/browse/ODBC-109).
* [Revision #740c862](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/740c862)\
  2018-01-28 23:21:04 +0100
  * \[[ODBC-119](https://jira.mariadb.org/browse/ODBC-119)] The fix and the test-case. The connector ordered SQLStatistics results using wrong columns. That could cause MS Access to pick wrong column as a unique index. And that, in its turn, could cause mangled data shown for the linked table. Fix of the test-case in catalog2 that failed against 10.3 due to new privilege. Added test of SQL\_GROUP\_BY info to [ODBC-123](https://jira.mariadb.org/browse/ODBC-123) test-case. It had similar problem(and tested in similar way) Fixed build in VS2017
* [Revision #256bf8d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/256bf8d)\
  2018-01-26 16:21:06 +0100
  * Fix bug in ABI analogous to \[[ODBC-123](https://jira.mariadb.org/browse/ODBC-123)]
* [Revision #1c97fd9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1c97fd9)\
  2018-01-21 23:38:16 +0100
  * \[[ODBC-131](https://jira.mariadb.org/browse/ODBC-131)] The fix and the test-case. While linking a table, MS Access threw the error when it received unexpected length for SQLSMALLINT and SQLINTEGER columns from SQLColumns resultset. New graphic images for the installer on Windows.
* [Revision #4b507cd](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4b507cd)\
  2018-01-17 14:48:56 +0100
  * Small fix of the testcase for SQLProcedureColumns - reference values for RADIX field were wrong for 2 parameters. Has to be 10(or theoretically 2) for numeric types
* [Revision #cfb8e53](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cfb8e53)\
  2018-01-12 17:50:40 -0500
  * Addition to the fix of [ODBC-123](https://jira.mariadb.org/browse/ODBC-123) and the testcase for that problem - for SQL\_CATALOG\_LOCATION info type the connector incorrectly wrote to the buffer as SQLUINTEGER, while it has to be SQLUSMALLINT
* [Revision #acdd5cd](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/acdd5cd)\
  2018-01-10 20:54:38 +0100
  * \[[ODBC-126](https://jira.mariadb.org/browse/ODBC-126)] The fix and testcases. Some of internal structures weren't reallocated in accordance with the next resultset fields count. Beyond the case described in the report, they cover the case of statements batch. It had similar and own problems. Removed unused property from the statement structure.
* [Revision #a1e8995](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a1e8995)\
  2017-12-27 21:46:48 +0100
  * \[[ODBC-123](https://jira.mariadb.org/browse/ODBC-123)] The fix and the test-case. LibreOffice sets SQL\_ATTR\_USE\_BOOKMARKS attribute, but does not actually use bookmarks. The connector was not ready for that, and would throw wrongly error, and then crash. Fixed a number of compilation warnings.
* [Revision #9f9ca38](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9f9ca38)\
  2017-12-13 12:07:27 +0000
  * Don't space pad parameters with non-zero scale
* [Revision #4300efe](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4300efe)\
  2017-06-22 14:12:19 +0200
  * correct include guard
* [Revision #7d5f4fa](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7d5f4fa)\
  2017-12-03 16:25:51 +0100
  * Adding [MariaDB 5.5](../../../../community-server/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md) server to Travis tests. Skipping one test with 5.5 servers(and MySQL <5.7), since it doesn't make sense there.
* [Revision #050ebc8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/050ebc8)\
  2017-12-19 19:16:55 +0100
  * Fix of warning from recent pull request
* [Revision #740206f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/740206f)\
  2017-12-13 10:49:18 +0000
  * Return correct scale for SQL\_C\_NUMERIC
* [Revision #c7059c4](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c7059c4)\
  2017-11-27 22:32:02 +0100
  * Fixing remaining issues in Travis Made (most of) testframework global variables static, as one of them clashed with variable in connector's env, and that caused problems in some cases. Also fixed few tests in connstring, that expected test connection to use password. Skipped one of tests there(in connstring) on travis.
* [Revision #d0523b2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d0523b2)\
  2017-11-23 01:30:48 +0100
  * \[[ODBC-120](https://jira.mariadb.org/browse/ODBC-120)] Fix of the performance issue. We did redundant calls of mysql\_stmt\_data\_seek. They are needed for different type of cursors, positioned operation, array fetch etc. But in forward\_only cursor it only significantly slows down execution.
* [Revision #c5659d5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c5659d5)\
  2017-11-17 18:40:02 +0100
  * Fixed connection procedure call in couple of tests, since 1 parameter type was changed in previous commit, and these references were overlooked. Skipping connstring in Travis. Fixed SQL\_API SQLTablePrivilegesW - it would always return empty resultset if CatalogName is NULL. That was not intended, and its ANSI counterpart doesn't behave like that.
* [Revision #cae4d21](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cae4d21)\
  2017-11-14 13:02:13 +0200
  * Fix of testcases failing in Travis. Mostly that is adding cursor closing, as older UnixODBC versions require it even there it is not really required. One test in catalog2(bug50195) was expecting, that db server is on the same host with tests(that is not the case in Travis). Added Travis detection in the tests framework.
* [Revision #4aae120](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4aae120)\
  2017-11-09 13:48:59 +0200
  * Changed DSN parsing/saving/reading tests(connstring.c) in order they do not fail with unixODBC. UnixODBC has buggy ini cache(which seemingly will be fixed in 2.3.5): if dsn is changed, and then read again, application will get old cached value. That doesn't occur if unixODBC is built with `--enable-inicaching=no` Thus tests have been changed to create and use individual DSN's, rather then one common for all tests DSN.
* [Revision #d31b4b0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d31b4b0)\
  2017-10-19 15:51:54 +0200
  * Initial Travis setup

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
