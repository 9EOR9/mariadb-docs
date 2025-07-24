# Connector/ODBC 3.0.7 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/3.0.7/)[Release Notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-307-release-notes.md)[Changelog](mariadb-connector-odbc-307-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-odbc/README.md)

**Release date:** 14 Nov 2018

For the highlights of this release, see the [release notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-307-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #3eed852](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3eed852)\
  2018-11-13 00:01:24 +0100
  * Version bump -> 3.0.7\
    Also, the fix of one compilation warning and of the memory leak introduced by one of fixes in this release
* [Revision #a94af40](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a94af40)\
  2018-11-09 01:07:26 +0100
  * [ODBC-43](https://jira.mariadb.org/browse/ODBC-43), [ODBC-198](https://jira.mariadb.org/browse/ODBC-198) and [ODBC-199](https://jira.mariadb.org/browse/ODBC-199) fixes\
    These are all date/time types related issues.\
    Correct errors, fractional part, type conversions.[ODBC-43](https://jira.mariadb.org/browse/ODBC-43)(overflow errors detection and reporting) was partly done earlier.[ODBC-198](https://jira.mariadb.org/browse/ODBC-198) is mostly fix in C/C, but added similar changes to similar function in c/odbc, and added the testcase.
* [Revision #ae8467a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ae8467a)\
  2018-11-05 23:44:43 +0100
  * [ODBC-194](https://jira.mariadb.org/browse/ODBC-194) and [ODBC-197](https://jira.mariadb.org/browse/ODBC-197) - fixes and testcases\
    Connector would not return NULL for 0000-00-00 datetime values in case of SQLGetData call, while doing that in SQLFetch.\
    Also it would not do that in case of empty string conversion to date/time types.\
    If time field fetched as timestamp type, fractional part is set to 0.\
    The patch makes SQLFetch and SQLGetData to use the same function to copy data to application buffers and process erroneous values.
* [Revision #351c1aa](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/351c1aa)\
  2018-10-31 15:13:35 +0100
  * [ODBC-192](https://jira.mariadb.org/browse/ODBC-192) The fix and the testcase + [ODBC-194](https://jira.mariadb.org/browse/ODBC-194) test\
    The problem was incorrect buffer address calculation for the TIMESTAMP type in case of row-based columns binding. That caused the error in ADO, and could cause a crash.\
    Some issues were fixed along the way. Like caring of the case when value buffer is not provided for the field, or if Indicator and StrLen (for the column) have different buffers.
* [Revision #1e3184f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1e3184f)\
  2018-10-18 00:52:16 +0200
  * [ODBC-188](https://jira.mariadb.org/browse/ODBC-188) The fix and testcases\
    The main issue was incorrect processing of the connect string with\
    NULL-separated key=value pairs. But also there were found and fixed many\
    issues with ConfigDSN use. Like no dialogs/message boxes should be showed if the\
    parent window handle isn't provided. Extended dsn\_test to test ConfigDSN\
    more thoroughly in the interactive mode.
* [Revision #63fcf15](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/63fcf15)\
  2018-10-13 00:03:03 +0200
  * [ODBC-186](https://jira.mariadb.org/browse/ODBC-186) Improved the SQLProcedureColumns testcase\
    It would fail if connection charset was not a single-byte
* [Revision #9ed4a7a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9ed4a7a)\
  2018-10-10 00:43:37 +0200
  * [ODBC-190](https://jira.mariadb.org/browse/ODBC-190) Removing C/C auth plugins from packages
* [Revision #bc32db6](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bc32db6)\
  2018-10-03 00:41:59 +0200
  * [ODBC-70](https://jira.mariadb.org/browse/ODBC-70) Last part. Caring of 0-date in the string\
    Enforcing of the constraint on date/time values in case they are passed as a string. Enhanced the testcase for [ODBC-70](https://jira.mariadb.org/browse/ODBC-70)\
    Fixed calculation of the SQL type from the concise type - it didn't consider ODBCv3 types.
* [Revision #d49df3d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d49df3d)\
  2018-10-01 14:31:21 +0200
  * [ODBC-152](https://jira.mariadb.org/browse/ODBC-152) The fix and the testcase\
    The fix has been accidentally lost in previous commit. In case if\
    SQL\_DATA\_TYPE value was fetched in the bound buffer, the truncation error would occur.\
    The fix is casting the column in the query to SIGNED type
* [Revision #fa081fb](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/fa081fb)\
  2018-09-20 15:58:05 +0200
  * [ODBC-186](https://jira.mariadb.org/browse/ODBC-186) The fix and testcases\
    This is fixes several issues with SQLColumns and SQLProcedureColumns,\
    as they share good part of SQL queries. Most of issues are rather minor.
* [Revision #a9e55d1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a9e55d1)\
  2018-09-18 17:58:38 +0200
  * Change requested in [ODBC-152](https://jira.mariadb.org/browse/ODBC-152) - SQL\_DATA\_TYPE value casted to SIGNED in SQLColumns query. Otherwise its type(returned by server) is MEDIUM\_BLOB. Even though at the moment it's not quite clear\
    what is the problem, the change looks reasonable.
* [Revision #bfb78c0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bfb78c0)\
  2018-09-13 17:48:26 +0200
  * [ODBC-169](https://jira.mariadb.org/browse/ODBC-169) The fix and the testcase.\
    If data was fetched using SQLGetData, with batches of SELECTS that would fail like described int the bug - empty values or even the program crash. The reason was that in such case one of structures involved in the data fetching was not reset on move to the new resultset.\
    Also the patch fixes SQLRowsCount for batches of upserts or other statements generating affected rows count
* [Revision #79efd0e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/79efd0e)\
  2018-09-12 11:34:19 +0200
  * [ODBC-182](https://jira.mariadb.org/browse/ODBC-182) The fix and the testcase\
    If SQL\_TIME field was bound as SQL\_C\_TIMESTAMP, and the day field\
    was not zero, the inserted time value would be different from the value\
    in time fields of the parameter(server would add total number of hours in those days to the time). The patch makes connector to copy only time fields for the parameter.\
    Also, the patch enforces time and date validity checks for such parameters, as the specs require.
* [Revision #548db71](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/548db71)\
  2018-09-11 20:17:54 +0200
  * [ODBC-181](https://jira.mariadb.org/browse/ODBC-181) The fix + the testcase\
    The crash or error could be caused by error in the (client side) query parsing in case of a dash followed by a string containing newline character and semicolon
* [Revision #0960f5d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0960f5d)\
  2018-09-07 19:51:38 +0200
  * [ODBC-178](https://jira.mariadb.org/browse/ODBC-178) Optimization for some long queries\
    Optimization is only used for queries longer than 32K. And it skips most of\
    parsing job in case if connector is sure that the query is not a multistatement, and\
    does not have parameters.
* [Revision #45d0868](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/45d0868)\
  2018-09-07 01:24:15 +0200
  * [ODBC-177](https://jira.mariadb.org/browse/ODBC-177) The fix and the testcase.\
    In case of SP call, if one of its queries resulted in error, connector\
    would not return the error on corresponding result fetch, but would\
    return it as SQL\_NO\_DATA.\
    Moreover, instead of last result with SP execution status, connector\
    would also do the same. Thus, for example, application could not get\
    affected rows count.
* [Revision #a9b6e76](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a9b6e76)\
  2018-08-11 04:18:19 +0200
  * [ODBC-171](https://jira.mariadb.org/browse/ODBC-171) Adding BUILD.md file with build instructions
* [Revision #32f3601](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/32f3601)\
  2018-08-09 23:27:28 +0200
  * Fixed generation of the source package with git.

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
