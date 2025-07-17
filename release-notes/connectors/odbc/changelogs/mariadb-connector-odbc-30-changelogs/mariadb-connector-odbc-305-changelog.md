# Connector/ODBC 3.0.5 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/3.0.5)[Release Notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-305-release-notes.md)[Changelog](mariadb-connector-odbc-305-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 12 Jun 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-305-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #a17d984](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a17d984)\
  2018-06-07 00:08:08 +0200
  * Windows build fix
* [Revision #a6621de](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a6621de)\
  2018-05-31 00:01:05 +0200
  * Version bump -> 3.0.5
* [Revision #62545da](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/62545da)\
  2018-05-30 19:46:00 +0200
  * \[[ODBC-146](https://jira.mariadb.org/browse/ODBC-146)] The fix and the testscase. Wrong decimal value (0) when after longtext field in select clause (using ADO, client side cursor)
* [Revision #8a15bdc](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8a15bdc)\
  2018-05-30 00:26:03 +0200
  * Fixed dynamic linking against C/C
* [Revision #cfb393b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cfb393b)\
  2018-05-28 16:26:26 +0200
  * \[test] removing plugins from server test build. server test build can be build with plugins according to build options. This patch permit will not install those plugins (particulary mariadb-plugin-cracklib-password-check)
* [Revision #ea7a519](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ea7a519)\
  2018-05-28 17:41:20 +0300
  * Added version-script for non-windows platform
* [Revision #e674bd6](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e674bd6)\
  2018-05-22 14:46:39 +0200
  * Small test enhancement to check if correct length
* [Revision #0719af3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0719af3)\
  2018-05-04 11:39:45 +0200
  * \[TODO-1299] testing connector against last server build. Those tests permit to check early regression and might failed, so tagged as "Allowed Failures" on travis
* [Revision #7da0dbb](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7da0dbb)\
  2018-04-09 17:52:03 +0900
  * Fetching Multiple Result Set Crash - completion of [ODBC-126](https://jira.mariadb.org/browse/ODBC-126) fix
* [Revision #860c985](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/860c985)\
  2018-05-15 00:50:27 +0200
  * \[[ODBC-141](https://jira.mariadb.org/browse/ODBC-141)] The fix and the testcase.
* [Revision #ad6dbb5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ad6dbb5)\
  2018-05-03 20:05:35 +0200
  * \[[ODBC-143](https://jira.mariadb.org/browse/ODBC-143)] Wrong SQL\_IDENTIFIER\_QUOTE\_CHAR info in case of ANSI\_QUOTES
* [Revision #2e46189](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2e46189)\
  2018-04-04 13:14:12 +0200
  * Travis change for C/C as a subproject Subproject update to latest commit Fix of CTest configuration with new executable names
* [Revision #c0070c3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c0070c3)\
  2017-01-18 08:54:34 -0800
  * Windows build fixes
* [Revision #cc0f481](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cc0f481)\
  2017-01-18 16:11:56 +0100
  * Add Connector/C plugins into package
* [Revision #1560f9d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1560f9d)\
  2017-01-18 08:52:30 +0100
  * use tag v3.0.1-beta for Connector/C
* [Revision #4860a43](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4860a43)\
  2017-01-18 08:30:35 +0100
  * Added helper script for retrieving connector/c sources
* [Revision #76a37b7](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/76a37b7)\
  2017-01-18 08:11:10 +0100
  * Build Connector/ODBC with git subproject Connector/C. Connector/C will be installed in libmariadb
* [Revision #025978c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/025978c)\
  2018-03-27 16:54:19 +0200
  * Final version of [ODBC-133](https://jira.mariadb.org/browse/ODBC-133) fix and expended test
* [Revision #16b9541](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/16b9541)\
  2018-03-25 19:47:30 +0200
  * \[[ODBC-133](https://jira.mariadb.org/browse/ODBC-133)] Wrong values for bound as NUMERIC type
* [Revision #d86a5ca](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d86a5ca)\
  2018-03-22 12:41:19 +0100
  * \[[ODBC-137](https://jira.mariadb.org/browse/ODBC-137)] fix variant. 133 and 139 testcases
* [Revision #f07b8ff](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f07b8ff)\
  2018-02-20 05:02:56 +0100
  * \[[ODBC-91](https://jira.mariadb.org/browse/ODBC-91)] The fix and the testcase. If the connection handles was reused, the connector would try to use default database from previous connection (and if there wasn't such database the connect would fail). That happened because connector copied database name form connection string to the structure field where SQL\_ATTR\_CURRENT\_CATALOG attribute is stored, if it wasn't set.
* [Revision #e0be887](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e0be887)\
  2018-02-14 18:51:30 +0100
  * Version bump -> 3.0.4
* [Revision #8cf710f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8cf710f)\
  2018-02-10 19:15:46 +0100
  * Merge pull request #21 from FaramosCZ/mschorm\_1
* [Revision #8b84d59](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8b84d59)\
  2018-02-10 18:41:05 +0100
  * Fix FSF address

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
