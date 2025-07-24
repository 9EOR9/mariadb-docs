# Connector/ODBC 2.0.12 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/2.0.12)[Release Notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2012-release-notes.md)[Changelog](mariadb-connector-odbc-2012-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 15 Sep 2016

For the highlights of this release, see the [release notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2012-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #48d7ae1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/48d7ae1)\
  2016-09-13 15:32:26 +0200
  * Partial fix for [ODBC-45](https://jira.mariadb.org/browse/ODBC-45) - conversion of SQL\_C\_CHAR parameters to SQL\_BIT has been corrected
* [Revision #05206c8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/05206c8)\
  2016-09-07 18:25:13 +0200
  * Some amendments to [ODBC-51](https://jira.mariadb.org/browse/ODBC-51) patch on \*nix. Also connector returned 0 as available string length in case if application did not provide buffer for it - that has been fixed.
* [Revision #6b41841](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6b41841)\
  2016-09-07 00:29:19 +0200
  * Fix and testcase for the bug [ODBC-51](https://jira.mariadb.org/browse/ODBC-51)(and [ODBC-52](https://jira.mariadb.org/browse/ODBC-52), that is in fact duplicate). Connector returned error when had to convert empty string to SQL\_C\_WCHAR.
* [Revision #5b72458](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5b72458)\
  2016-08-18 01:51:58 +0200
  * Fix and the testcase for [ODBC-48](https://jira.mariadb.org/browse/ODBC-48) - dealing with ISO format of for procedure call. We simply remove pair of curly brackets to make it possible for server to parse the query.
* [Revision #cfa6634](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cfa6634)\
  2016-08-16 02:50:11 +0200
  * Fixed bugs in DAE with SQLSetPos update. One of them probably could affect parameter arrays.
* [Revision #6b0d283](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6b0d283)\
  2016-08-16 01:02:24 +0200
  * Fixed some bugs in SQLSetPos with SQL\_COLUMN\_IGNORE - we had failing test in cursor.c Also fixed error it returns if there were errors on some of updated rows.
* [Revision #1f33c14](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1f33c14)\
  2016-07-25 23:01:24 +0200
  * The testcase for [ODBC-47](https://jira.mariadb.org/browse/ODBC-47)(The bug itself has been fixed in the Connector/C)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
