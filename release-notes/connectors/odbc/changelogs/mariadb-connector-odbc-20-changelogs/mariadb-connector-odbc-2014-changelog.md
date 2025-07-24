# Connector/ODBC 2.0.14 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/2.0.14)[Release Notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2014-release-notes.md)[Changelog](mariadb-connector-odbc-2014-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-odbc/README.md)

**Release date:** 7 Apr 2017

For the highlights of this release, see the [release notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2014-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #2c5a9a0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2c5a9a0)\
  2017-04-05 15:40:38 +0200
  * Fix of the error in computation of returned ParameterValuePtr in SQLParamData on 64bit linux.
* [Revision #0d1fdac](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0d1fdac)\
  2017-04-04 23:25:13 +0200
  * Cherry-picking from 3.0 - fixed (not) closing of MYSQL\_STMT handles, and optimized some exessive close/init of them. Fix of possible memory leak in case of preparing of a multistatement query, and not executing it.
* [Revision #817ec5e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/817ec5e)\
  2017-04-03 21:14:05 +0200
  * To mitigate ODBC limitations causing [ODBC-83](https://jira.mariadb.org/browse/ODBC-83), added support of hour\_to\_minute/second interval types. It allows to insert/fetch time values > 23:59:59(or < -23:59:59)
* [Revision #d94541b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d94541b)\
  2017-03-17 21:28:22 +0100
  * \[[ODBC-90](https://jira.mariadb.org/browse/ODBC-90)] Fix and the testcase. We inserted default values for ignored columns. In case of the timestamp that is a function, and that does not work with prepared statements. The patch does not include ignored columns in the query. Also it fixes SQLCopyDesc - InternalBuffer pointers are not copied, since that can cause them to be freed twice.
* [Revision #939c888](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/939c888)\
  2017-03-11 23:18:25 +0100
  * Fix and tests for [ODBC-62](https://jira.mariadb.org/browse/ODBC-62). Export from MS Access did not work mainly because we returned wrong values in CREATE\_PARAMS column of the SQLGetTypeInfo, and that caused MS Access to generate bad CREATE TABLE queries.
* [Revision #3a77b1a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3a77b1a)\
  2017-03-08 00:50:33 +0100
  * Removed last traces of 'def' catalog. Still were in some catalog funcions
* [Revision #b0e0d7c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b0e0d7c)\
  2017-03-06 02:02:27 +0100
  * \[[ODBC-73](https://jira.mariadb.org/browse/ODBC-73)]Fix and testcase. The connector relied on the field's BINARY\_FLAG flag to establish the fact whether the field it binary or not. But that flag would be set if any binary collation is selected for any char field. And that is not right. The patch is changing that to check only, if field's charset is binary charset(63)
* [Revision #168ea7b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/168ea7b)\
  2017-03-03 20:34:50 +0100
  * Version bump -> 2.0.14 Added charset conversion processing for WCHAR in SQLGetData
* [Revision #3f3ec84](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3f3ec84)\
  2017-03-03 00:37:35 +0100
  * \[[ODBC-72](https://jira.mariadb.org/browse/ODBC-72)] Fix and testcase. Fixing the case, when while getting WCHAR data in parts, surrogate pair gets divided into different chunks, i.e first SQLWCHAR of the pair falls on the end of buffer.
* [Revision #8c998ae](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8c998ae)\
  2017-03-01 01:00:22 +0100
  * Fixes and testcases more around [ODBC-70](https://jira.mariadb.org/browse/ODBC-70) AND [ODBC-83](https://jira.mariadb.org/browse/ODBC-83) - connector now checks if date/time are valid ODBC date/time, and returns errors, if they are not. Fixed bug in SQLSetStmtAttr - SQL\_ATTR\_ROW\_OPERATION\_PTR and SQL\_ATTR\_ROW\_STATUS\_PTR were setting fields in wrong descriptors. Fixed many things around row status, return code for rowset fetch.
* [Revision #677f3c9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/677f3c9)\
  2017-02-25 21:35:38 +0100
  * Fix building ODBC connector on OSX/macOS (#13)
* [Revision #bf947c0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bf947c0)\
  2017-02-25 18:05:45 +0100
  * \[[ODBC-71](https://jira.mariadb.org/browse/ODBC-71)] Fix and testcase for the problems causing issue and around. These include: errors in SQLCopyDesc, that could cause a crash, support of missing (odbc2) info types(SQL\_POS\_OPERATIONS, SQL\_STATIC\_SENSITIVITY, SQL\_LOCK\_TYPES, SQL\_SCROLL\_CONCURRENCY), support of SQL\_DESC\_SEARCHABLE and SQL\_DESC\_SCHEMA\_NAME thru SQLColAttribute.
* [Revision #6ccf03c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6ccf03c)\
  2017-02-23 12:03:57 +0100
  * Setting Connection->mariadb to NULL, after mysql\_close'ing it. Reportedly that helps to avoid certain problems in some applications.
* [Revision #8d85958](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8d85958)\
  2017-02-23 00:46:41 +0100
  * Added locks around all mysql\_stmt\_init, since they modify list inside MYSQL structure.
* [Revision #06b5e6a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/06b5e6a)\
  2017-02-22 15:21:06 +0100
  * \[[ODBC-69](https://jira.mariadb.org/browse/ODBC-69)] Fix and testcase - charset name is case-insensitive now
* [Revision #4d2c342](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4d2c342)\
  2017-02-22 00:19:12 +0100
  * \[[ODBC-84](https://jira.mariadb.org/browse/ODBC-84)] The fix ant the testcase. SQLGetTypeInfo returned SQL\_ERROR for SQL\_WCHAR and other wchar types.
* [Revision #f185440](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f185440)\
  2017-02-21 16:49:20 +0100
  * \[[ODBC-78](https://jira.mariadb.org/browse/ODBC-78)] Fix and testcase. Besides described in the report case, the fix also take care of fixed length types - specs say also to return SQL\_NO\_DATA for subsequent calls of SQLGetData for such columns. Also had to introduce some changes, since the fix affected SQLSetPos, that calls same function to get values required to construct queries, and (fix affected) some tests.
* [Revision #4fe4e64](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4fe4e64)\
  2017-02-02 07:36:02 +0100
  * \[[ODBC-77](https://jira.mariadb.org/browse/ODBC-77)] Fix and the testcase. Connector did not recognize ANALYZE TABLE as query returning result. SImilar error fixed for EXPLAIN.
* [Revision #3de37aa](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3de37aa)\
  2017-01-31 00:19:25 +0100
  * \[[ODBC-74](https://jira.mariadb.org/browse/ODBC-74)] Fix and testcase. The problem was in errors in query parsing, while splitting the batch to single statements. The patch also fixes other parsing errors with comments and quotes in a query.
* [Revision #572bdb1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/572bdb1)\
  2016-10-27 19:44:59 +0200
  * Fix and testcase for the [ODBC-57](https://jira.mariadb.org/browse/ODBC-57). The problem was in MS Access adding parenthesis around each SELECT in the UNION. And the function determining query type wasn't ready for that. Now it skips query string characters till first alpha.

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
