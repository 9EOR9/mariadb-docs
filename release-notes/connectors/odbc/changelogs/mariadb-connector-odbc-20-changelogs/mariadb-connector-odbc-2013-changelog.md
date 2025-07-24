# Connector/ODBC 2.0.13 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/2.0.13)[Release Notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2013-release-notes.md)[Changelog](mariadb-connector-odbc-2013-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 31 Oct 2016

For the highlights of this release, see the [release notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2013-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #ebf0132](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ebf0132)\
  2016-10-26 01:36:14 +0200
  * Changed type of BindType in descriptor header to SQLULEN(as in specs) SQL\_ATTR\_PARAMSET\_SIZE stmt attribute now sets correct descriptor field. Corrected (long time depricated) SQLParamOptions, which people seem to be still using. SQLExecute does not do mysql\_stmt\_store\_result if Out parameters have been fetched already.
* [Revision #cd32260](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cd32260)\
  2016-10-25 23:51:26 +0200
  * Added check of mysql\_stmt\_store\_result result
* [Revision #7fadd77](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7fadd77)\
  2016-10-16 00:51:29 +0200
  * Fix for [ODBC-61](https://jira.mariadb.org/browse/ODBC-61)/tdf#103077 (LibreOffice)
* [Revision #f7d9200](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f7d9200)\
  2016-10-17 00:41:41 +0200
  * The testcase for [ODBC-61](https://jira.mariadb.org/browse/ODBC-61)
* [Revision #4705b82](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4705b82)\
  2016-10-15 19:55:19 +0200
  * Fix some cppcheck reports: (#11)
* [Revision #8b2f543](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8b2f543)\
  2016-10-02 18:04:03 +0200
  * Testcase for [ODBC-58](https://jira.mariadb.org/browse/ODBC-58). The bug is in C/C, thus no fix will follow.
* [Revision #1889f32](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1889f32)\
  2016-09-27 00:15:24 +0200
  * [ODBC-56](https://jira.mariadb.org/browse/ODBC-56) Fix of wrong calculation of StLen ptr in case of columnwise binding. Change in 2 tests in relative and in dyn\_cursor to cover this case. Also similar bugs was fixed in other places, mostly affecting all sorts of position commands

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
