# MariaDB Connector/ODBC 3.1.21 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector)[Release Notes](../../mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-21-release-notes.md)[Changelog](mariadb-connector-odbc-3-1-21-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 24 Feb 2025

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-21-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #da56c19](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/da56c19)\
  2025-02-11 14:44:08 +0100
  * Fixed in tests SQL statements there schema name was not in quotes
* [Revision #974041b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/974041b)\
  2025-02-11 14:15:18 +0100
  * Fix of buffer overflow found by ASAN
* [Revision #8c01caa](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8c01caa)\
  2025-02-10 12:45:17 +0100
  * Increased the required cmake version to 3.5.1 to match C/C requirement
* [Revision #4d4cec9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4d4cec9)\
  2025-02-06 16:09:58 +0100
  * [ODBC-446](https://jira.mariadb.org/browse/ODBC-446) deb packages name follow the common pattern with other products
* [Revision #5df9be3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5df9be3)\
  2025-02-07 11:34:14 +0100
  * Connector/C submodule has been updated to v3.3.14
* [Revision #d10cab7](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d10cab7)\
  2025-01-08 22:05:05 +0100
  * [ODBC-435](https://jira.mariadb.org/browse/ODBC-435) The testcase. The fix has been cherry-picked in one of previous
* [Revision #0e7533e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0e7533e)\
  2025-01-08 14:04:18 +0100
  * Testcase for [ODBC-429](https://jira.mariadb.org/browse/ODBC-429). Not present in 3.1
* [Revision #e872c8c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e872c8c)\
  2024-12-31 23:50:53 +0100
  * Updated travis to use unified base config(as in 3.2 and other)
* [Revision #81ca310](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/81ca310)\
  2024-07-07 18:36:44 +0200
  * [ODBC-430](https://jira.mariadb.org/browse/ODBC-430) Wrong max size for SQL\_VARCHAR/BINARY types in SQLGetTypeInfo
* [Revision #a59ca60](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a59ca60)\
  2024-12-27 19:16:58 +0100
  * Cherrypick from 3.2 - fixes in catalog functions for MySQL server
* [Revision #1003f85](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1003f85)\
  2024-12-27 17:05:54 +0100
  * [ODBC-405](https://jira.mariadb.org/browse/ODBC-405) Error on reading server decimal variable in ADO
* [Revision #be98828](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/be98828)\
  2024-12-27 14:58:36 +0100
  * [ODBC-418](https://jira.mariadb.org/browse/ODBC-418) Widechar gets truncated if contains NULL character
* [Revision #74e98ed](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/74e98ed)\
  2024-12-23 12:40:56 +0100
  * [ODBC-448](https://jira.mariadb.org/browse/ODBC-448) Converting int fields to double should not cause error
* [Revision #512d8e1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/512d8e1)\
  2024-05-31 22:47:00 +0200
  * C/C has been updated to v3.3.10
* [Revision #a9b5b13](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a9b5b13)\
  2024-03-27 17:50:03 +0000
  * \[[ODBC-411](https://jira.mariadb.org/browse/ODBC-411)] Fix test failure on s390x
* [Revision #907de1c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/907de1c)\
  2024-02-22 09:26:34 +0000
  * test/types.c: fix build on `gcc-14`
* [Revision #8f3bee5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8f3bee5)\
  2023-12-04 09:48:03 -0500
  * bump the VERSION

{% @marketo/form formid="4316" formId="4316" %}
