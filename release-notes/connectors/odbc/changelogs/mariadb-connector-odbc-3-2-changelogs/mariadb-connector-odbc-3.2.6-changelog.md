# MariaDB Connector/ODBC 3.2.6 Changelog

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector" class="button primary">Download</a> <a href="../../mariadb-connector-odbc-3-2-release-notes/mariadb-connectorodbc-3-2-6-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-connector-odbc-3.2.6-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-odbc" class="button secondary">About MariaDB Connector/ODBC</a>

**Release date:** ?

For the highlights of this release, see the [release notes](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connectorodbc-3-2-6-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #7942b8a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7942b8a) 2025-05-27 00:05:55 +0200
  * Fix of the last merge.
* [Revision #e61572c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e61572c) 2025-05-26 13:39:55 +0200
  * [ODBC-457](https://jira.mariadb.org/browse/ODBC-457) Fix of the possible crash in SQLCancelHandle(SQL\_HANDLE\_DBC)
* [Revision #d040629](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d040629) 2025-05-26 13:17:11 +0200
  * Merge branch '[ODBC-3](https://jira.mariadb.org/browse/ODBC-3).1'
* [Revision #bc65180](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bc65180) 2025-05-26 11:24:24 +0200
  * [ODBC-464](https://jira.mariadb.org/browse/ODBC-464) Amendment to the fix
* [Revision #e5827f4](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e5827f4) 2025-05-26 04:18:36 +0200
  * [ODBC-466](https://jira.mariadb.org/browse/ODBC-466) Making sure that SQLCancel does not run on freed statement
* [Revision #7aad503](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7aad503) 2025-05-22 10:14:57 +0200
  * Update README.md
* [Revision #431b6cd](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/431b6cd) 2025-05-22 10:16:46 +0200
  * Update README.md
* [Revision #79a26ca](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/79a26ca) 2025-05-19 13:51:49 +0200
  * Merge branch '[ODBC-3](https://jira.mariadb.org/browse/ODBC-3).1'
* [Revision #6f6079d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6f6079d) 2025-05-19 00:38:37 +0200
  * [ODBC-464](https://jira.mariadb.org/browse/ODBC-464) Removing possible race conditions in SQLCancel
* [Revision #17f6850](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/17f6850) 2025-05-11 22:57:03 +0200
  * Small correction for the [ODBC-462](https://jira.mariadb.org/browse/ODBC-462) fix - driver sent extra byte for some
* [Revision #16ff1ef](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/16ff1ef) 2025-05-05 03:51:15 +0200
  * [ODBC-461](https://jira.mariadb.org/browse/ODBC-461) The destructor releasing serve side PS could throw
* [Revision #2db9d58](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2db9d58) 2025-05-05 02:34:54 +0200
  * [ODBC-462](https://jira.mariadb.org/browse/ODBC-462) Client side batch did not respect if multistatement disallowed
* [Revision #cd0ad90](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cd0ad90) 2025-04-27 23:09:24 +0200
  * Merge branch '[ODBC-3](https://jira.mariadb.org/browse/ODBC-3).1' into master(3.2)
* [Revision #5b3040a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5b3040a) 2025-04-27 14:36:40 +0200
  * Small impovement in SQLStatistics - got rid off sprintf's
* [Revision #589a263](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/589a263) 2025-04-27 13:04:32 +0200
  * Updated C/C to v3.3.15
* [Revision #fdf6b99](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/fdf6b99) 2025-03-24 13:18:19 +0100
  * [ODBC-459](https://jira.mariadb.org/browse/ODBC-459) MS Access shows record with auto\_increment as deleted
* [Revision #db807a9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/db807a9) 2025-03-28 18:25:25 +0100
  * [ODBC-458](https://jira.mariadb.org/browse/ODBC-458) Fix of working with bigint auto\_increment field in MSAccess
* [Revision #7a6f0a3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7a6f0a3) 2025-03-24 00:24:07 +0100
  * [ODBC-458](https://jira.mariadb.org/browse/ODBC-458) part1, and possibly the last for now. Fixing NOBIGINT option
* [Revision #8ee1f7b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8ee1f7b) 2025-04-26 00:38:52 +0200
  * The checkbox for EDSERVER option was missing in the DSN dialog
* [Revision #66a063e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/66a063e) 2025-04-25 22:15:24 +0200
  * [ODBC-460](https://jira.mariadb.org/browse/ODBC-460) Crash in SQLExecDirect on UPDATE statement with paramset
* [Revision #167468a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/167468a) 2025-04-25 11:29:02 +0200
  * Updated C/C to the v3.4.5
* [Revision #dd67939](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/dd67939) 2025-03-06 04:29:43 +0100
  * Merge branch '[ODBC-3](https://jira.mariadb.org/browse/ODBC-3).1'
* [Revision #a8fd0a9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a8fd0a9) 2025-03-05 04:32:48 +0100
  * [ODBC-457](https://jira.mariadb.org/browse/ODBC-457) New option permitting to skip date/time parameter overflow
* [Revision #d0edbc1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d0edbc1) 2025-02-24 14:00:28 -0500
  * bump the VERSION
* [Revision #da56c19](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/da56c19) 2025-02-11 14:44:08 +0100
  * Fixed in tests SQL staements there schemaname was not in quotes
* [Revision #974041b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/974041b) 2025-02-11 14:15:18 +0100
  * Fix of buffer overflow found by ASAN
* [Revision #8c01caa](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8c01caa) 2025-02-10 12:45:17 +0100
  * Increased the required cmake version to 3.5.1 to match C/C requirement
* [Revision #4d4cec9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4d4cec9) 2025-02-06 16:09:58 +0100
  * [ODBC-446](https://jira.mariadb.org/browse/ODBC-446) deb packages name follow the common pattern with other products
* [Revision #5df9be3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5df9be3) 2025-02-07 11:34:14 +0100
  * Connector/C submodule has been updated to v3.3.14
* [Revision #d10cab7](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d10cab7) 2025-01-08 22:05:05 +0100
  * [ODBC-435](https://jira.mariadb.org/browse/ODBC-435) The testcase. The fix has been cherry-picked in one of previous
* [Revision #0e7533e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0e7533e) 2025-01-08 14:04:18 +0100
  * Testcase for [ODBC-429](https://jira.mariadb.org/browse/ODBC-429). Not present in 3.1
* [Revision #e872c8c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e872c8c) 2024-12-31 23:50:53 +0100
  * Updated travis to use unified base config(as in 3.2 and other)
* [Revision #81ca310](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/81ca310) 2024-07-07 18:36:44 +0200
  * [ODBC-430](https://jira.mariadb.org/browse/ODBC-430) Wrong max size for SQL\_VARCHAR/BINARY types in SQLGetTypeInfo
* [Revision #a59ca60](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a59ca60) 2024-12-27 19:16:58 +0100
  * Cherrypick from 3.2 - fixes in catalog functions for MySQL server
* [Revision #1003f85](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1003f85) 2024-12-27 17:05:54 +0100
  * [ODBC-405](https://jira.mariadb.org/browse/ODBC-405) Error on reading server decimal variable in ADO
* [Revision #be98828](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/be98828) 2024-12-27 14:58:36 +0100
  * [ODBC-418](https://jira.mariadb.org/browse/ODBC-418) Widechar gets truncated if contains NULL character
* [Revision #74e98ed](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/74e98ed) 2024-12-23 12:40:56 +0100
  * [ODBC-448](https://jira.mariadb.org/browse/ODBC-448) Converting int fields to double should not cause error
* [Revision #512d8e1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/512d8e1) 2024-05-31 22:47:00 +0200
  * C/C has been updated to v3.3.10
* [Revision #659e385](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/659e385) 2025-02-24 14:03:23 -0500
  * bump the VERSION

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
