# MariaDB Connector/ODBC 2.0.18 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/2.0.18)[Release Notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2018-release-notes.md)[Changelog](mariadb-connector-odbc-2018-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 8 Sep 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2018-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #e7cd90b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e7cd90b)\
  2018-09-07 19:51:38 +0200
  * [ODBC-178](https://jira.mariadb.org/browse/ODBC-178) Optimization for some long queries\
    Optimization is only used for queries longer than 32K. And it skips most of\
    parsing job in case if connector is sure that the query is not a multistatement, and\
    does not have parameters.
* [Revision #a3da3ab](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a3da3ab)\
  2018-09-07 01:24:15 +0200
  * [ODBC-177](https://jira.mariadb.org/browse/ODBC-177) The fix and the testcase.\
    In case of SP call, if one of its queries resulted in error, connector\
    would not return the error on corresponding result fetch, but would\
    return it as SQL\_NO\_DATA.\
    Moreover, instead of the last result with SP execution status, connector\
    would also do the same. Thus, for example, application could not get\
    affected rows count.
* [Revision #b0b5620](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b0b5620)\
  2018-08-11 04:18:19 +0200
  * [ODBC-171](https://jira.mariadb.org/browse/ODBC-171) Adding BUILD.md file with build instructions
* [Revision #c21b408](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c21b408)\
  2018-08-09 23:27:28 +0200
  * Fixed genertaion source package with git.\
    It uses now .gitattributes file, and does not incude libmariadb, test,\
    travis and git files
* [Revision #baf2287](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/baf2287)\
  2018-07-31 23:23:29 +0200
  * Fix of memory leaks in the driver. Query structure delete routine was called in the wrong place for\
    SQL\_DROP, and thus wasn't invoked for single statement queries.\
    Other leak would only occur in case of multistatement query preparing,\
    and batches were not allowed for the connection.\
    One more leak would occur if a batch of statements was optimized to be\
    executed via text protocol.\
    Also the fix of the memory leak in tests. Not really a problem, but created noise in valgrind output.
* [Revision #91ea64d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/91ea64d)\
  2018-07-31 13:39:02 +0200
  * Update of libmariabd module to v3.0.6
* [Revision #d888051](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d888051)\
  2018-07-27 17:35:33 +0200
  * [ODBC-159](https://jira.mariadb.org/browse/ODBC-159) The fix and the testcase. In case if the query is a multistatement, connector splitted it into\
    individual statements, prepare one by one, and then execute one by one.\
    In case if one of statements depends on execution of one of previous statements,\
    application can get error(think of tmp table creation with\
    select from it) or incorrect results. We can't do anything in case of\
    SQLPrepare + SQLExecute. The patch fixes that for SQLExecDirect. Now\
    connector prepares and immediately executes each statement in the batch.
* [Revision #8f14569](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8f14569)\
  2018-07-24 18:22:34 +0200
  * [ODBC-166](https://jira.mariadb.org/browse/ODBC-166) Wrong display size for decimal fields.
* [Revision #145f157](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/145f157)\
  2018-07-23 15:17:00 +0200
  * [ODBC-164](https://jira.mariadb.org/browse/ODBC-164) Not including libmariadb into source package
* [Revision #8912f9f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8912f9f)\
  2018-07-19 12:49:41 +0200
  * [ODBC-161](https://jira.mariadb.org/browse/ODBC-161) FileDSN creation - fix and testcase
* [Revision #f0cd063](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f0cd063)\
  2018-07-17 14:31:11 +0200
  * [ODBC-162](https://jira.mariadb.org/browse/ODBC-162) The fix and the testcase. Connector does some query parsing, in particular to know the type of\
    the query. Mostly it is interested if query returns result. It didn't\
    evaluate WITH correctly
* [Revision #91f7d86](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/91f7d86)\
  2018-07-13 01:02:18 +0200
  * [ODBC-158](https://jira.mariadb.org/browse/ODBC-158) The fix and the testcase. Those aggregate functions, that caused error, returned LONGLONG value,\
    and Access was getting it as SQL\_C\_LONG. The problem was that connector\
    returned length of the data as 8(field's size), and not 4(requested\
    C-type size), as specs prescribe.
* [Revision #fe2dc81](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/fe2dc81)\
  2018-07-11 17:05:28 +0200
  * [ODBC-160](https://jira.mariadb.org/browse/ODBC-160) The fix and the testcase. Connector did not return length of string returned for SQL\_IDENTIFIER\_QUOTE\_CHAR info type.
* [Revision #02b7565](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/02b7565)\
  2018-07-10 12:50:27 +0200
  * Changed version to 3.0 in README files.
* [Revision #c6085eb](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c6085eb)\
  2018-07-09 12:47:04 +0200
  * [ODBC-157](https://jira.mariadb.org/browse/ODBC-157) The fix and the testcase. Display and column length did notinclude fractional part for (date)time\
    types. Also octet length for those types was length of they string\
    representation, while specs say it should be size of corresponding ODBC data\
    structs.
* [Revision #6d526c1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6d526c1)\
  2018-07-04 18:06:26 +0200
  * [ODBC-154](https://jira.mariadb.org/browse/ODBC-154) Fix of build with dynamic C/C linking
* [Revision #da0c41c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/da0c41c)\
  2018-07-03 01:05:41 +0200
  * [ODBC-155](https://jira.mariadb.org/browse/ODBC-155) Scale(DecimalDigits) IRD field wasn't set for (date)time/timestamp fields with second fractional part. Thus SQLDescribeCol retulrned 0 in DegitalDigitsPtr
* [Revision #1273ebd](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1273ebd)\
  2018-07-02 01:19:59 +0200
  * [ODBC-149](https://jira.mariadb.org/browse/ODBC-149) The fix and the testcase. Date(time) types had numerous issues with bulk operations. We provided array of buffers, and C/C expects array of pointers to buffers.
* [Revision #468d5a3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/468d5a3)\
  2018-06-27 00:51:56 +0200
  * [ODBC-151](https://jira.mariadb.org/browse/ODBC-151) The fix and the testcase. For fixed length types SQL\_DESC\_OCTET\_LENGTH initialized by type length, rather than by BufferLength parameter value.
* [Revision #6afe9ee](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6afe9ee)\
  2018-06-25 14:11:34 +0200
  * [ODBC-150](https://jira.mariadb.org/browse/ODBC-150) The fix and extended old testcase. DESC statement caused error with the connector.
* [Revision #7a1a226](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7a1a226)\
  2018-06-18 14:36:35 +0200
  * [ODBC-148](https://jira.mariadb.org/browse/ODBC-148) the testcase and some amendments to the fix. Used OctetLengthPtr, since IndicatorPtr may be different from length ptr\
    Version bump -> 3.0.6
* [Revision #cd5c619](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cd5c619)\
  2018-06-14 21:33:01 -0400
  * [ODBC-148](https://jira.mariadb.org/browse/ODBC-148) The field length is not set for DATE, TIME, or DATETIME values assigned during SQLFetch calls. Without the length set, Crystal Reports interprets all DATE, TIME, and DATETIME values as NULL. Setting \*ArdRecord->IndicatorPtr to the size of the appropriate data structure in MADB\_CopyMadbTimestamp.
