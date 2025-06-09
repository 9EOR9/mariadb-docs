# MariaDB Connector/ODBC 2.0.11 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/2.0.11)[Release Notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2011-release-notes.md)[Changelog](mariadb-connector-odbc-2011-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 9 Jun 2016

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2011-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #34cf2a3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/34cf2a3)\
  2016-06-07 17:37:26 +0200
  * Fix for the bug [ODBC-44](https://jira.mariadb.org/browse/ODBC-44) - incorrect binding of TIMESTAMP to TIME type(affected work with MS Access, if table has time and auto\_increment fields) Changed existing testcase(t\_tstotime) to cover this case as well.
* [Revision #5436e8a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5436e8a)\
  2016-06-03 10:32:46 +0200
  * Fix of memleak with multistatement - 1 MYSQL\_STMT structure had been being lost.
* [Revision #e05a6c7](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e05a6c7)\
  2016-06-02 19:33:33 +0200
  * Small testcase to ensure that ';' in string in query does not confuse the connector
* [Revision #c301508](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c301508)\
  2016-06-02 00:02:54 +0200
  * Fix for [ODBC-41](https://jira.mariadb.org/browse/ODBC-41) - basically ensuring that number of columns(counter in descriptor) is reset before issuing new query. Fixed possible memory leak with multistatement
* [Revision #23ae3e3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/23ae3e3)\
  2016-05-26 23:38:08 +0200
  * Fix for [ODBC-38](https://jira.mariadb.org/browse/ODBC-38) - SQLColumns(and some others along with it) returned ODBC3 SQL types, while MS Access is ODBC2. Along with it, catalog test suite was split into 2 suites,and 2 tests there were un-skipped. One happens to pass now, for 2nd one issue is fixed by this revision - connector could crash on "CREATE FUNCTION". But there are some more problems with it.
* [Revision #f347cea](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f347cea)\
  2016-05-24 16:30:32 +0200
  * Fixed small bug - SQLGetInfo returned a bit wrong value for SQL\_DRIVER\_NAME info type. And completely wrong on \*nix
* [Revision #fbd517e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/fbd517e)\
  2016-05-20 00:00:15 +0200
  * Some changes to make WiX build using last built configuration.
* [Revision #65b26b2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/65b26b2)\
  2016-05-12 00:34:34 +0200
  * Fixed testcase t\_sqltables in catalog - it misbehaved and dropped/re-created user's test database. Which is not particularly good as for a test.
* [Revision #cf5ce78](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cf5ce78)\
  2016-05-10 19:09:10 +0200
  * Fix of warnings on 64bit. Many of them were clearly bugs in fact, but most of those were harmless on LE machine. Some were real bugs. As part of this, changed some internal functions parameter and/or return types. Also changed types of properties in some structures. e.g. in descriptor header's Count is SQLSMALLINT now(according to specs), InternalLength in records is now "unsigned long" as it is used in MYSQL\_BIND for length.
* [Revision #4a1a196](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4a1a196)\
  2016-05-03 19:54:48 +0200
  * ([ODBC-37](https://jira.mariadb.org/browse/ODBC-37)) Variable used for length in bind structure in SQLGetData was bigger than "unsigned long" on 64bit machines. And it wasn't initialized. Application could eventually get garbage as a length. Also fixed tests in multistatement - there were also pointed variable length problems on 64bit.
* [Revision #6eefff8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6eefff8)\
  2016-05-03 13:33:20 +0200
  * SQLColAttribute wrote to numeric pointer(if it was supplied) even if string attribute had been requested
* [Revision #9a00acc](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9a00acc)\
  2016-04-27 22:49:19 +0200
  * Un-skipped the testcase for bit field. And fixed conversion of bit fields to numeric types(unfortunately for binds only) Structured SQLFetch a bit. Added updating of ird data to SQLMoreResults. We probably had bugs because of that.
* [Revision #ac9147e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ac9147e)\
  2016-04-11 17:42:33 +0200
  * Version bump -> 2.0.11
