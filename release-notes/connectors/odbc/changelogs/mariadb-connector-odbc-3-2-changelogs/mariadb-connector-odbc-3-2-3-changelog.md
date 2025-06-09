# MariaDB Connector/ODBC 3.2.3 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector/)[Release Notes](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-3-release-notes.md)[Changelog](mariadb-connector-odbc-3-2-3-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 26 Aug 2024

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-3-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #4aacd69](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4aacd69)\
  2024-08-23 14:49:51 +0200
  * Workaround of the bug in C/C cmake failing in case of static plugins
* [Revision #64dffc4](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/64dffc4)\
  2024-08-21 23:04:11 +0200
  * C/C has been update to v3.4.1
* [Revision #1a3157b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1a3157b)\
  2024-08-15 17:52:04 +0200
  * [ODBC-436](https://jira.mariadb.org/browse/ODBC-436) SQLPrimaryKeys returns fields in wrong order with wrong SEQ\_NUM
* [Revision #3afdb55](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3afdb55)\
  2024-08-14 22:43:06 +0200
  * [ODBC-432](https://jira.mariadb.org/browse/ODBC-432),[ODBC-433](https://jira.mariadb.org/browse/ODBC-433) Caching of multiple RS,SQLMoreResults could "steal" RS
* [Revision #ca84e49](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ca84e49)\
  2024-07-31 14:03:20 +0200
  * [ODBC-432](https://jira.mariadb.org/browse/ODBC-432) Driver would not cache multiple results for new incoming query
* [Revision #8c13551](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8c13551)\
  2024-07-29 13:46:43 +0200
  * [ODBC-431](https://jira.mariadb.org/browse/ODBC-431) Caching of streamed binary result would not work
* [Revision #03f34d8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/03f34d8)\
  2024-07-29 10:05:58 +0200
  * [ODBC-430](https://jira.mariadb.org/browse/ODBC-430) Wrong max size for SQL\_VARCHAR/BINARY types in SQLGetTypeInfo
* [Revision #6100932](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6100932)\
  2024-07-29 00:44:26 +0200
  * Fixes in driver and tests aroung result streaming
* [Revision #d92de86](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d92de86)\
  2024-07-22 14:17:04 +0200
  * [ODBC-429](https://jira.mariadb.org/browse/ODBC-429) Crash in SQLMoreResults if called after error. Fix\&test
* [Revision #3bc6293](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3bc6293)\
  2024-07-22 10:33:38 +0200
  * [ODBC-427](https://jira.mariadb.org/browse/ODBC-427) Out parameters wasn't written with MySQL server
* [Revision #c07684f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c07684f)\
  2024-07-07 18:36:44 +0200
  * Fixes in tests for MySQL server
* [Revision #5c3bad9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5c3bad9)\
  2024-07-07 18:18:59 +0200
  * [ODBC-426](https://jira.mariadb.org/browse/ODBC-426) SQLForeignKeys won't work with MySQL with some parameter
* [Revision #3469b35](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3469b35)\
  2024-07-07 18:10:02 +0200
  * [ODBC-424](https://jira.mariadb.org/browse/ODBC-424) 3.2.2 won't connect to MySQL server on Windows
* [Revision #299b910](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/299b910)\
  2024-06-17 10:34:38 -0400
  * bump the VERSION
