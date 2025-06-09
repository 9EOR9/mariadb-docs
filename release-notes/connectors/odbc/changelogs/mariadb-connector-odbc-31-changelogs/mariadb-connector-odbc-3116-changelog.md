# MariaDB Connector/ODBC 3.1.16 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-16-release-notes.md)[Changelog](mariadb-connector-odbc-3116-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 22 Jun 2022

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-16-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #47a57b9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/47a57b9)\
  2022-06-18 16:13:14 +0200
  * [ODBC-346](https://jira.mariadb.org/browse/ODBC-346) returned static linking of C/C lib as default on MacOS
* [Revision #530929a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/530929a)\
  2022-06-18 14:53:43 +0200
  * [ODBC-366](https://jira.mariadb.org/browse/ODBC-366) Here is only the testcase as it only takes to move libmariadb to the 3.3 branch
* [Revision #d4afdd0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d4afdd0)\
  2022-06-17 18:48:12 +0200
  * Fix of the textcase in catalog2 failing on 32b Windows
* [Revision #1346a82](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1346a82)\
  2022-06-13 15:32:35 +0200
  * [ODBC-365](https://jira.mariadb.org/browse/ODBC-365) The fix only(the testcase of [ODBC-359](https://jira.mariadb.org/browse/ODBC-359) covers it)
* [Revision #12ebbdf](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/12ebbdf)\
  2022-05-30 14:49:18 +0200
  * [ODBC-361](https://jira.mariadb.org/browse/ODBC-361) Unique indexes with nullable (part) column were returned by
* [Revision #d021e22](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d021e22)\
  2022-05-09 12:46:08 +0200
  * Unit test case for [ODBC-359](https://jira.mariadb.org/browse/ODBC-359) calling SQLBindCol with no target buffer / only a length buffer
* [Revision #baafb25](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/baafb25)\
  2022-05-09 11:19:14 +0200
  * [ODBC-359](https://jira.mariadb.org/browse/ODBC-359) add NULL check to buffer in MADB\_FixFetchedValues case SQL\_C\_WCHAR
* [Revision #d2a96c4](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d2a96c4)\
  2022-04-21 18:36:09 +0200
  * [ODBC-356](https://jira.mariadb.org/browse/ODBC-356) Fixed support of unique indexes for positioned operations
* [Revision #852f634](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/852f634)\
  2022-02-13 22:05:54 +0100
  * [ODBC-298](https://jira.mariadb.org/browse/ODBC-298) Added NULLISCURRENT connection string option
* [Revision #7826a9b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7826a9b)\
  2022-02-12 21:21:10 +0100
  * [ODBC-352](https://jira.mariadb.org/browse/ODBC-352) Fix of the tarballs structure
* [Revision #37f16f7](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/37f16f7)\
  2022-01-29 15:45:44 +0100
  * [ODBC-328](https://jira.mariadb.org/browse/ODBC-328) Fix for the connection error to older MySQL servers
* [Revision #2dfce7f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2dfce7f)\
  2022-01-10 12:30:09 +0100
  * [ODBC-347](https://jira.mariadb.org/browse/ODBC-347) Added option to disable LOAD DATA LOCAL INFILE
* [Revision #6b3c369](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6b3c369)\
  2021-11-18 15:57:07 -0500
  * bump the VERSION

{% @marketo/form formid="4316" formId="4316" %}
