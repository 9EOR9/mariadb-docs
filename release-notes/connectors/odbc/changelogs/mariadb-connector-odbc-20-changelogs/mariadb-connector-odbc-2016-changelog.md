# MariaDB Connector/ODBC 2.0.16 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/2.0.16)[Release Notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2016-release-notes.md)[Changelog](mariadb-connector-odbc-2016-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 8 Feb 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2016-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #d93b0b8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d93b0b8)\
  2018-02-04 23:01:24 +0100
  * \[[ODBC-134](https://jira.mariadb.org/browse/ODBC-134)] The fix and the test-case. Fetch would fail, if unbound column contained NULL, and for that column some arbitrary descriptor field was set by application(but not value/len/ind buffer ptrs). The bug affected ADO, as that is something it can do with CursorLocation adUseClient in some cases
* [Revision #d506530](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d506530)\
  2018-02-01 10:20:13 +0100
  * For the info type SQL\_SCHEMA\_TERM/SQL\_OWNER\_TERM the connector returned wrong length. Or more exactly - did not write anything into application's length buffer. The fix and the test-case. Possibly fixes [ODBC-109](https://jira.mariadb.org/browse/ODBC-109).
* [Revision #e7e12ae](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e7e12ae)\
  2018-01-28 23:21:04 +0100
  * \[[ODBC-119](https://jira.mariadb.org/browse/ODBC-119)] The fix and the test-case. The connector ordered SQLStatistics results using wrong columns. That could cause MS Access to pick wrong column as a unique index. And that, in its turn, could cause mangled data shown for the linked table. Fix of the test-case in catalog2 that failed against 10.3 due to new privilege. Added test of SQL\_GROUP\_BY info to [ODBC-123](https://jira.mariadb.org/browse/ODBC-123) test-case. It had similar problem(and tested in similar way) Fixed build in VS2017
* [Revision #ce44b4d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ce44b4d)\
  2018-01-17 14:48:56 +0100
  * Small fix of the testcase for SQLProcedureColumns - reference values for RADIX field were wrong for 2 parameters. Has to be 10(or theoretically 2) for numeric types
* [Revision #8f34a4e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8f34a4e)\
  2018-01-26 16:21:06 +0100
  * Fix bug in ABI analogous to \[[ODBC-123](https://jira.mariadb.org/browse/ODBC-123)]
* [Revision #dbc6409](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/dbc6409)\
  2018-01-21 23:38:16 +0100
  * \[[ODBC-131](https://jira.mariadb.org/browse/ODBC-131)] The fix and the test-case. While linking a table, MS Access threw the error when it received unexpected length for SQLSMALLINT and SQLINTEGER columns from SQLColumns resultset. New graphic images for the installer on Windows.
* [Revision #e84bdcc](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e84bdcc)\
  2018-01-13 18:02:15 +0100
  * Temporary turned off tests atainst MaxScale in Travis
* [Revision #4f8bdb9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4f8bdb9)\
  2018-01-12 17:50:40 -0500
  * Addition to the fix of [ODBC-123](https://jira.mariadb.org/browse/ODBC-123) and the testcase for that problem - for SQL\_CATALOG\_LOCATION info type the connector incorrectly wrote to the buffer SQLUINTEGER, while it has to be SQLUSMALLINT
* [Revision #a22bf42](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a22bf42)\
  2018-01-10 20:54:38 +0100
  * \[[ODBC-126](https://jira.mariadb.org/browse/ODBC-126)] The fix and testcases. Some of internal structures weren't reallocated in accordance with the next resultset fields count. Beyond the case described in the report, they cover the case of statements batch. It had similar and own problems. Removed unused property from the statement structure.
* [Revision #b085030](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b085030)\
  2017-12-27 21:46:48 +0100
  * \[[ODBC-123](https://jira.mariadb.org/browse/ODBC-123)] The fix and the test-case. LibreOffice sets SQL\_ATTR\_USE\_BOOKMARKS attribute, but does not actually use bookmarks. The connector was not ready for that, and would throw wrongly error, and then crash. Fixed a number of compilation warnings.
* [Revision #99ccc9e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/99ccc9e)\
  2017-12-13 12:07:27 +0000
  * Don't space pad parameters with non-zero scale
* [Revision #528df54](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/528df54)\
  2017-12-19 19:16:55 +0100
  * Fix of waring from recent pull request
* [Revision #4ab2f82](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4ab2f82)\
  2017-12-13 10:49:18 +0000
  * Return correct scale for SQL\_C\_NUMERIC
* [Revision #7c445fb](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7c445fb)\
  2017-12-06 23:56:35 +0100
  * Addition for the fix of [ODBC-120](https://jira.mariadb.org/browse/ODBC-120) - optimization only used for FORWARD\_ONLY cursors in this branch. Correction of merge error - tests detected Travis in wrong way
* [Revision #c077544](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c077544)\
  2017-11-17 18:40:02 +0100
  * Fixed connection procedure call in couple of tests, since 1 parameter type was changed in previous commit, and these references were overlooked. Skipping connstring in Travis. Fixed SQL\_API SQLTablePrivilegesW - it would always return empty resultset if CatalogName is NULL. That was not intended, and its ANSI counterpart doesn't behave like that.
* [Revision #d9c0ff4](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d9c0ff4)\
  2017-12-03 16:25:51 +0100
  * Adding [MariaDB 5.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5) server to Travis tests. Skipping one tests with 5.5 servers(and MySQL <5.7), since it doesn't make sense there.
* [Revision #27daadc](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/27daadc)\
  2017-11-27 22:32:02 +0100
  * Fixing remaining issues in Travis Made (most of) tests framework global variables static, as one of them clashed with variable in connector's env, and that caused problems in some cases. Also fixed few tests in connstring, that expected test connection to use password. Skipped one of tests there(in connstring) on travis.
* [Revision #0f69c54](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0f69c54)\
  2017-11-23 01:30:48 +0100
  * \[[ODBC-120](https://jira.mariadb.org/browse/ODBC-120)] Fix of the performance issue. We did redundant calls of mysql\_stmt\_data\_seek. They are needed for different type of cursors, positioned operation, array fetch etc. But in forward\_only cursor it only significantly slows down execution.
* [Revision #553bc88](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/553bc88)\
  2017-11-14 13:02:13 +0200
  * Fix of testcases failing in Travis. Mostly that is adding cursor closing, as older UnixODBC versions require it even there it is not really required. One test in catalog2(bug50195) was expecting, that db server is on the same host with tests(that is not the case in Travis). Added Travis detection in the tests framework.
* [Revision #714acf9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/714acf9)\
  2017-11-09 13:48:59 +0200
  * Changed DSN parsing/saving/reading tests(connstring.c) in order they do not fail with unixODBC. UnixODBC has buggy ini cache(which seemingly will be fixed in 2.3.5): if dsn is changed, and then read again, application will get old cached value. That doesn't occur if unixODBC is built with `--enable-inicaching=no` Thus tests have been changed to create and use individual DSN's, rather then one common for all tests DSN.
* [Revision #514a892](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/514a892)\
  2017-10-19 15:51:54 +0200
  * Initial Travis setup
* [Revision #20c43cc](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/20c43cc)\
  2017-10-09 19:58:56 +0300
  * Fixed one small memory leak - SQLSetCursorNameW leaked recoded (into ANSI or utf8 encoding) name. Added freeing of allocated memory in a couple of tests, so they don't create noise in valgrind. Enabled test of "where current of" - it was skipped with misleading "unsupported" message, and it doesn't fail.
* [Revision #e475a3d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e475a3d)\
  2017-10-09 16:54:20 +0300
  * Enabled test of updateable cursor (SQLSetPos with SQL\_UPDATE), it was skipped with misleading "unsupported" message, and it doesn't fail.
* [Revision #9ea9f21](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9ea9f21)\
  2017-10-06 21:17:19 +0200
  * Fix of the memory leak. It could occur if prepare, or direct execution in case of 10.2, failed, and Stmt handler is reused. Also removed unused field from Stmt struct and its references (was only freed in few places).
* [Revision #bb86bf1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bb86bf1)\
  2017-10-04 23:48:52 +0200
  * \[[ODBC-115](https://jira.mariadb.org/browse/ODBC-115)] The fix and the testcase. Fix and the testcase. Wrong rc and sqlstate for numeric overflow (but not for fractional truncation). Now the connector returns 22003 and SQL\_ERROR. Also changed int SQLFetch couple of switches to switch on Concise\_Type, and not Type, that was seemingly wrong. Changed logo in the READMC.md
* [Revision #33116e2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/33116e2)\
  2017-08-28 12:27:17 +0200
  * \[[ODBC-110](https://jira.mariadb.org/browse/ODBC-110)] The Fix and the testcase of the crash in case of columns unbinding after stmt execution and before fetching data. The reason was freeing of 2 internal arrays that are allocated during execution and reset at each fetch. SQLFreeStmt(SQL\_UNBIND) just shouldn't free them.
* [Revision #064a189](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/064a189)\
  2017-07-31 02:30:34 +0200
  * \[[ODBC-105](https://jira.mariadb.org/browse/ODBC-105)] Starting from v. 10.2.7, server encloses COLUMN\_DEFAULT in the INFORMATION\_SCHEMA.COLUMNS table, in single quotes for literal strings. Connector now considers the server version, when constructing the query for SQLColumns.
* [Revision #ab661fb](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ab661fb)\
  2017-06-22 16:56:39 +0200
  * Merge pull request #15 from jacquesg/include-guard
* [Revision #cd24ea5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cd24ea5)\
  2017-06-22 14:12:19 +0200
  * correct include guard

{% @marketo/form formid="4316" formId="4316" %}
