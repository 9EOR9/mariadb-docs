# Connector/ODBC 3.2.2 Changelog

{% include "../../../../../.gitbook/includes/latest-odbc.md" %}

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector/) | [Release Notes](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-2-release-notes.md) | [Changelog](mariadb-connector-odbc-3-2-2-changelog.md) | [About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 18 Jun 2024

For the highlights of this release, see the [release notes](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-2-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #97115b8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/97115b8)\
  2024-06-12 23:44:19 +0200
  * Fix of issues found with ASAN - memleaks and read past end of buffer
* [Revision #378e053](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/378e053)\
  2024-06-10 13:22:11 +0200
  * [ODBC-163](https://jira.mariadb.org/browse/ODBC-163) Small amendment in one callback
* [Revision #aa9b2b1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/aa9b2b1)\
  2024-06-07 14:19:27 +0200
  * [ODBC-421](https://jira.mariadb.org/browse/ODBC-421) amendment and workaround of the problem caused by move to C/C 3.4
* [Revision #4a2089e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4a2089e)\
  2024-06-03 00:55:16 +0200
  * Changes to add SSLVERIFY option to generated testing environments
* [Revision #968123d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/968123d)\
  2024-06-01 17:28:25 +0200
  * [ODBC-421](https://jira.mariadb.org/browse/ODBC-421) C/C is moved to 3.4 branch at the v3.4.0 tag
* [Revision #33524e9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/33524e9)\
  2024-05-16 15:43:42 +0200
  * [ODBC-405](https://jira.mariadb.org/browse/ODBC-405) Error on reading server decimal variable in ADO
* [Revision #b80852b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b80852b)\
  2024-05-13 13:51:55 +0200
  * Removed [ODBC-419](https://jira.mariadb.org/browse/ODBC-419) - query timeout control
* [Revision #96d93d6](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/96d93d6)\
  2024-05-13 09:57:33 +0200
  * [ODBC-418](https://jira.mariadb.org/browse/ODBC-418) Widechar gets truncated if contains NULL character
* [Revision #778530f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/778530f)\
  2024-05-03 16:17:42 +0200
  * Merge 3.1 branch into 3.2
* [Revision #a9b5b13](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a9b5b13)\
  2024-03-27 17:50:03 +0000
  * \[[ODBC-411](https://jira.mariadb.org/browse/ODBC-411)] Fix test failure on s390x
* [Revision #3a07ef1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3a07ef1)\
  2024-05-03 12:40:27 +0200
  * \[misc] correcting travis global environment setting
* [Revision #36d553b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/36d553b)\
  2024-05-03 12:15:11 +0200
  * Merge branch 'master'(3.1) into develop(3.2)
* [Revision #907de1c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/907de1c)\
  2024-02-22 09:26:34 +0000
  * test/types.c: fix build on `gcc-14`
* [Revision #8f3bee5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8f3bee5)\
  2023-12-04 09:48:03 -0500
  * bump the VERSION
* [Revision #9241fb8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9241fb8)\
  2023-12-01 11:15:36 +0100
  * Fix of SQLCanclel testcase, that would fail in case of RS streaming
* [Revision #cdb2990](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cdb2990)\
  2023-11-30 21:04:58 +0100
  * [ODBC-399](https://jira.mariadb.org/browse/ODBC-399) Error on the query consisting from the comment only
* [Revision #9b117a1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9b117a1)\
  2023-11-30 14:39:27 +0100
  * [ODBC-404](https://jira.mariadb.org/browse/ODBC-404) Use SET STATEMENT only with servers, that support it
* [Revision #5ef91f2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5ef91f2)\
  2023-11-29 12:28:46 +0100
  * libmariadb submodule has been updated to v3.3.8
* [Revision #d99a261](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d99a261)\
  2023-11-27 22:14:22 +0100
  * Fixes for MacOS/iOdbc
* [Revision #5f1fbdf](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5f1fbdf)\
  2023-11-29 01:02:31 +0100
  * [ODBC-402](https://jira.mariadb.org/browse/ODBC-402) Support of NO\_BIGINT option with testcase
* [Revision #014e86b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/014e86b)\
  2023-11-22 17:30:10 +0100
  * [ODBC-399](https://jira.mariadb.org/browse/ODBC-399) The testcase, as it appears now
* [Revision #314a1c2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/314a1c2)\
  2023-11-22 10:43:04 +0100
  * [ODBC-401](https://jira.mariadb.org/browse/ODBC-401) SQLCancel fix
* [Revision #497c64c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/497c64c)\
  2024-04-30 15:14:41 +0200
  * Some rather cosmetic changes in tests
* [Revision #d87ebe1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d87ebe1)\
  2024-04-29 14:20:17 +0200
  * [ODBC-419](https://jira.mariadb.org/browse/ODBC-419) Conenction string option controlling use of query timeout
* [Revision #2124cb5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2124cb5)\
  2024-04-29 00:36:05 +0200
  * [ODBC-410](https://jira.mariadb.org/browse/ODBC-410) Optimization of the SQLForeignKeys
* [Revision #7439cac](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7439cac)\
  2024-04-15 12:30:57 +0200
  * [ODBC-163](https://jira.mariadb.org/browse/ODBC-163) Use of C/C callbacks
* [Revision #5f597fb](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5f597fb)\
  2024-04-15 12:25:08 +0200
  * [ODBC-163](https://jira.mariadb.org/browse/ODBC-163) Support of callbacks
* [Revision #e3e648f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e3e648f)\
  2023-12-12 16:07:55 +0100
  * \[misc] using common default servers test suite
* [Revision #2d8ed06](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2d8ed06)\
  2023-12-01 10:00:03 -0500
  * bump the VERSION

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
