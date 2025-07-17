# Connector/ODBC 2.0.17 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/2.0.17)[Release Notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2017-release-notes.md)[Changelog](mariadb-connector-odbc-2017-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 12 Jun 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2017-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #1303def](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1303def)\
  2018-06-08 01:36:11 +0200
  * Windows build fix
* [Revision #9c6ad40](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9c6ad40)\
  2018-06-05 20:03:20 +0200
  * In the cmake config, moved compiler flags processing above C/C inclusion
* [Revision #7e10afd](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7e10afd)\
  2018-05-30 19:46:00 +0200
  * \[[ODBC-146](https://jira.mariadb.org/browse/ODBC-146)] The fix and the testscase. Wrong decimal value (0) when after longtext field in select clause (using ADO, client side cursor)
* [Revision #c34cf79](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c34cf79)\
  2018-05-28 16:26:26 +0200
  * \[test] removing plugins from server test build. server test build can be build with plugins according to build options. This patch permit will not install those plugins (particulary mariadb-plugin-cracklib-password-check)
* [Revision #28ace4f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/28ace4f)\
  2018-05-04 11:39:45 +0200
  * \[TODO-1299] Testing connector against last server build on travis. Those tests permit to check early regression and might failed, so tagged as "Allowed Failures" on travis
* [Revision #6d05b62](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6d05b62)\
  2018-04-09 17:52:03 +0900
  * Fetching Multiple Result Set Crash - completion of [ODBC-126](https://jira.mariadb.org/browse/ODBC-126) fix
* [Revision #505bd33](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/505bd33)\
  2018-05-28 17:41:20 +0300
  * Added version-script for non-windows platform
* [Revision #1e3037d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1e3037d)\
  2018-05-15 00:50:27 +0200
  * \[[ODBC-141](https://jira.mariadb.org/browse/ODBC-141)] The fix and the testcase.
* [Revision #4ce7c26](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4ce7c26)\
  2018-05-03 20:05:35 +0200
  * \[[ODBC-143](https://jira.mariadb.org/browse/ODBC-143)] Wrong SQL\_IDENTIFIER\_QUOTE\_CHAR info in case of ANSI\_QUOTES
* [Revision #f6acdad](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f6acdad)\
  2017-01-18 08:11:10 +0100
  * Build Connector/ODBC with git subproject Connector/C.
* [Revision #dce6451](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/dce6451)\
  2018-03-27 16:54:19 +0200
  * Final version of [ODBC-133](https://jira.mariadb.org/browse/ODBC-133) fix and extended testcase
* [Revision #4cd0642](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4cd0642)\
  2018-03-25 19:47:30 +0200
  * \[[ODBC-133](https://jira.mariadb.org/browse/ODBC-133)] Wrong values for bound as NUMERIC type
* [Revision #2d4fce5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2d4fce5)\
  2018-03-22 12:41:19 +0100
  * \[[ODBC-137](https://jira.mariadb.org/browse/ODBC-137)] fix variant. 133 and 139 testcases
* [Revision #b68cc3d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b68cc3d)\
  2018-02-20 05:02:56 +0100
  * \[[ODBC-91](https://jira.mariadb.org/browse/ODBC-91)] The fix and the testcase. If the connection handles was reused, the connector would try to use default database from previous connection (and if there wasn't such database the connect would fail). That happened because connector copied database name form connection string to the structure field where SQL\_ATTR\_CURRENT\_CATALOG attribute is stored, if it wasn't set.
* [Revision #d6cc40c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d6cc40c)\
  2018-02-14 18:56:33 +0100
  * Version bump -> 2.0.17

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
