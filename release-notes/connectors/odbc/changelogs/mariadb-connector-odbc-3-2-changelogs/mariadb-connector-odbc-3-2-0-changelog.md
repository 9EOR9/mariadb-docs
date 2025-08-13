# Connector/ODBC 3.2.0 Changelog

{% include "../../../../../.gitbook/includes/latest-odbc.md" %}

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector/) | [Release Notes](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-0-release-notes.md) | [Changelog](mariadb-connector-odbc-3-2-0-changelog.md) | [About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-odbc/README.md)

**Release date:** 21 Apr 2023

For the highlights of this release, see the [release notes](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-0-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #2f4a21b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2f4a21b)\
  2023-04-14 17:36:22 +0200
  * [ODBC-298](https://jira.mariadb.org/browse/ODBC-298) Making NULL catalog means current a default behavior
* [Revision #2eca650](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2eca650)\
  2023-04-13 14:53:42 +0200
  * C/C has been moved to v3.3.4 & fix of the build with xcode
* [Revision #162e5af](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/162e5af)\
  2023-04-12 20:41:49 +0200
  * Fix of 32b build on Windows
* [Revision #6011a4f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6011a4f)\
  2023-04-11 17:12:08 +0200
  * Fix of conversion of string to MYSQL\_TIME structure, and of SQLErrorW
* [Revision #80cdf03](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/80cdf03)\
  2023-04-11 16:25:06 +0200
  * [ODBC-388](https://jira.mariadb.org/browse/ODBC-388) Change of value-less attribute treatment
* [Revision #d78064e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d78064e)\
  2023-04-11 14:21:10 +0200
  * Connstring option PREPONCLIENT to prepare on client by default
* [Revision #7c8aba4](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7c8aba4)\
  2023-04-09 23:51:48 +0200
  * [ODBC-388](https://jira.mariadb.org/browse/ODBC-388) Support of perfschema connection attrimutes
* [Revision #e15062d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e15062d)\
  2023-03-30 02:17:04 +0200
  * Updated C/C to v3.3.4
* [Revision #2fb8781](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2fb8781)\
  2023-03-28 22:28:59 +0200
  * gcc compilation warning fix
* [Revision #b72749f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b72749f)\
  2023-03-24 17:01:30 +0100
  * Build fix on Linux
* [Revision #eaf9c33](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/eaf9c33)\
  2023-03-24 00:55:34 +0100
  * Merge branch 'master' into develop(3.1 into 3.2)
* [Revision #e4b7741](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e4b7741)\
  2023-03-21 15:00:16 +0100
  * [ODBC-313](https://jira.mariadb.org/browse/ODBC-313) The testcase for the fix, that has been already committed
* [Revision #2168db0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2168db0)\
  2023-03-20 23:48:28 +0100
  * Moved C/C subproject to v3.3.4
* [Revision #c7b3644](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c7b3644)\
  2023-03-17 20:55:13 +0100
  * [ODBC-313](https://jira.mariadb.org/browse/ODBC-313) Embarcadero had unnecesssary SQLPrimaryKeys calls
* [Revision #1253aa4](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1253aa4)\
  2023-03-12 22:50:23 +0100
  * [ODBC-377](https://jira.mariadb.org/browse/ODBC-377) Timeouts set via ODB attributes did nothing
* [Revision #855667c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/855667c)\
  2023-03-08 23:36:33 +0100
  * [ODBC-385](https://jira.mariadb.org/browse/ODBC-385) Fixes in the setup dilog to comply updated docs
* [Revision #9b1fa2d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9b1fa2d)\
  2023-03-08 14:34:49 +0100
  * [ODBC-384](https://jira.mariadb.org/browse/ODBC-384) Named pipe pvio plugin was missing - the fix with the testcase
* [Revision #854ecfe](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/854ecfe)\
  2023-02-18 11:27:50 +0100
  * [ODBC-378](https://jira.mariadb.org/browse/ODBC-378) The fix and the testcase
* [Revision #5379a12](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5379a12)\
  2023-01-20 01:12:29 +0100
  * [ODBC-380](https://jira.mariadb.org/browse/ODBC-380) Memory leak during connect if multistatement option selected
* [Revision #8fc8d33](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8fc8d33)\
  2022-12-11 21:04:06 +0100
  * Changed in 2 places, where connector accessed data in C/C handles
* [Revision #539a3a9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/539a3a9)\
  2022-12-03 18:19:57 +0100
  * Small optimization not to run extra strlen on query text
* [Revision #2574487](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2574487)\
  2022-11-29 20:10:01 +0100
  * [ODBC-375](https://jira.mariadb.org/browse/ODBC-375) Connector crash if one of queires in the batch returns error on
* [Revision #a315872](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a315872)\
  2022-11-23 20:40:15 +0100
  * Fix of possible crash in config dialog in connection test function
* [Revision #bf86c4c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bf86c4c)\
  2022-11-21 14:59:00 +0100
  * Adopting new style travis config using connectors-test-machine
* [Revision #159ea70](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/159ea70)\
  2022-11-19 00:03:27 +0100
  * [ODBC-374](https://jira.mariadb.org/browse/ODBC-374) The fix and the testcase. Wrong mapping of SQL\_C\_FLOAT could
* [Revision #66c21a2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/66c21a2)\
  2023-01-31 14:24:04 +0100
  * Introducing client side statemnt preparing
* [Revision #42b581e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/42b581e)\
  2022-11-03 17:36:14 +0100
  * Merge branch 'master'(3.1) into develop(3.2)
* [Revision #1088d97](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1088d97)\
  2022-08-30 12:49:11 -0400
  * bump the VERSION
* [Revision #c9887da](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c9887da)\
  2020-12-15 23:56:09 +0100
  * Some initial changes to make the connector C++ internally.
* [Revision #9939f16](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9939f16)\
  2019-05-11 00:02:53 +0200
  * Starting 3.2.0 alpha

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
