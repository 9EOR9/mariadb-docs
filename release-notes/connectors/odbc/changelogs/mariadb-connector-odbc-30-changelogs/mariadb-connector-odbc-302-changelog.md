# MariaDB Connector/ODBC 3.0.2 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/3.0.2)[Release Notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-302-release-notes.md)[Changelog](mariadb-connector-odbc-302-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 12 Oct 2017

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-302-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #743255a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/743255a)\
  2017-10-09 19:58:56 +0300
  * Fixed one small memory leak - SQLSetCursorNameW leaked recoded (into ANSI or utf8 encoding) name. Added freeing of allocated memory in a couple of tests, so they don't create noise in valgrind.\
    Enabled test of "where current of" - it was skipped with misleading "unsupported" message, and it doesn't fail.
* [Revision #6a61dc6](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6a61dc6)\
  2017-10-09 16:54:20 +0300
  * Enabled test of updateable cursor (SQLSetPos with SQL\_UPDATE), it was skipped with misleading "unsupported" message, and it doesn't fail.
* [Revision #9069741](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9069741)\
  2017-10-06 21:17:19 +0200
  * Fix of the memory leak. It could occur if prepare, or direct execution in case of 10.2, failed, and Stmt handler is reused. Also removed unused field from Stmt struct and its references (was only freed in few places).
* [Revision #6265daf](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6265daf)\
  2017-10-04 23:48:52 +0200
  * [ODBC-115](https://jira.mariadb.org/browse/ODBC-115) Fix and the testcase. Wrong rc and sqlstate for numeric overflow (but not for fractional truncation). Now the connector returns 22003 and SQL\_ERROR. Also changed int SQLFetch couple of switches to switch on Concise\_Type, and not Type, that was seemingly wrong. Changed logo in the READMC.md
* [Revision #f673843](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f673843)\
  2017-10-03 23:44:16 +0200
  * [ODBC-114](https://jira.mariadb.org/browse/ODBC-114) Some optimizations for bulk operations - length arrays are not allocated and filled for fixed length types.
* [Revision #193c7b0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/193c7b0)\
  2017-09-30 01:53:34 +0200
  * [ODBC-113](https://jira.mariadb.org/browse/ODBC-113) and [ODBC-117](https://jira.mariadb.org/browse/ODBC-117) - We don't copy useful arrays data to smaller arrays if there are rows to skip (113), and we don't use PS bulk operations for statements other than INSERT and UPDATE(117). For the former we set a corresponding indicator value in one of the columns. For the latter we now store the query type in the Stmt structure.
* [Revision #2aaa286](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2aaa286)\
  2017-09-29 13:46:57 +0200
  * [ODBC-117](https://jira.mariadb.org/browse/ODBC-117) Testcase: server doesn't support bulk operations for DELETE.
* [Revision #860e7f8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/860e7f8)\
  2017-08-28 12:27:17 +0200
  * [ODBC-110](https://jira.mariadb.org/browse/ODBC-110) Fix and testcase of the crash in case of columns unbinding after stmt execution and before fetching data. The reason was freeing of 2 internal arrays that are allocated during execution and reset at each fetch. SQLFreeStmt(SQL\_UNBIND) just shouldn't free them.
* [Revision #2569534](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2569534)\
  2017-08-24 22:54:07 +0200
  * [ODBC-55](https://jira.mariadb.org/browse/ODBC-55) Making possible to link C/C dynamically. Cmake option MARIADB\_LINK\_DYNAMIC tells cmake to look for and configure to link against dynamic library. Fixed all remaining uses of not exported C/C symbols.

{% @marketo/form formid="4316" formId="4316" %}
