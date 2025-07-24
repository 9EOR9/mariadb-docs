# Connector/ODBC 3.1.19 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-19-release-notes.md)[Changelog](mariadb-connector-odbc-3-1-19-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 7 Jul 2023

For the highlights of this release, see the [release notes](../../mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-19-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #08da03f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/08da03f)\
  2023-06-10 21:58:33 +0200
  * Overriding the problem with c/c requires C99 with older GCC
* [Revision #fc52d66](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/fc52d66)\
  2023-06-10 12:42:29 +0200
  * [ODBC-392](https://jira.mariadb.org/browse/ODBC-392) The fix and the testcase
* [Revision #a210bfa](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a210bfa)\
  2023-06-05 12:44:14 +0200
  * [ODBC-391](https://jira.mariadb.org/browse/ODBC-391) Only the fix as lower\_case\_table\_names can't be changed for session. i.e. the test has been added, but to server has to be in lower\_case\_table\_names=2 mode to test the fix, otherwise it ensures that the fix doesn't break catalog functions against server in "normaler" mode. The fix adds reading of the lower\_case\_table\_names, and if it's 2, then it compares table name case insensitively where case sensitive comparison would be used otherwise. The problem actually affects not ony SQLStatistics, but almost all catalog functions, that take catalog and/or table parameter as ordinary argument.
* [Revision #60a5bd6](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/60a5bd6)\
  2023-06-02 14:03:09 +0200
  * [ODBC-350](https://jira.mariadb.org/browse/ODBC-350) The fix and the testcase
* [Revision #9b96270](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9b96270)\
  2023-05-17 10:28:42 +0200
  * Fix of potential issue found with ASAN
* [Revision #2eb9877](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2eb9877)\
  2023-05-15 10:16:55 +0200
  * Added WITH\_ASAN, WITH\_UBSAN and WITH\_MSAN cmake option to enable
* [Revision #c0d989b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c0d989b)\
  2023-04-28 12:34:59 +0200
  * [ODBC-390](https://jira.mariadb.org/browse/ODBC-390) Using SQL\_ATTR\_QUERY\_TIMEOUT leaks memory
* [Revision #313102f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/313102f)\
  2023-04-13 13:47:37 -0400
  * bump the VERSION

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
