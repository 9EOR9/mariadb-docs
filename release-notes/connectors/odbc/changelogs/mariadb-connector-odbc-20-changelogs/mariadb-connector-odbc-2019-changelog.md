# MariaDB Connector/ODBC 2.0.19 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2019-release-notes.md)[Changelog](mariadb-connector-odbc-2019-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-odbc/README.md)

**Release date:** 5 Jun 2019

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-2019-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #d42d88f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d42d88f)\
  2019-05-27 18:06:30 +0200
  * Merge of latest 3.0 changes(3.0.7-3.0.9) into 2.0
* [Revision #832360f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/832360f)\
  2019-05-02 20:21:24 +0200
  * [ODBC-211](https://jira.mariadb.org/browse/ODBC-211) The fix and the testcase
    * Also fixed precision, octet length, and display size calculation in case of\
      unsigned decimal field and/or 0 scale.
* [Revision #38e4205](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/38e4205)\
  2019-04-26 00:12:16 +0200
  * [ODBC-225](https://jira.mariadb.org/browse/ODBC-225) The fix and updated testcases
    * The driver treated NULL values as empty strings when checked if the\
      SQLTables call is special case for the databases list return.
    * Also contains fixes for [ODBC-245](https://jira.mariadb.org/browse/ODBC-245) and [ODBC-246](https://jira.mariadb.org/browse/ODBC-246)
* [Revision #1e633f8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1e633f8)\
  2019-04-09 00:47:36 +0200
  * [ODBC-238](https://jira.mariadb.org/browse/ODBC-238) Added FORCETLS connection string option
    * This is for implementation of the C/C MYSQL\_OPT\_SSL\_ENFORCE option, which\
      enables forcing TLS use
* [Revision #9d1d94b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9d1d94b)\
  2019-04-08 15:30:40 +0200
  * [ODBC-239](https://jira.mariadb.org/browse/ODBC-239) Changed mysql\_options calls as it's deprecated
* [Revision #3b39fe0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3b39fe0)\
  2019-04-04 19:28:45 +0200
  * Version bump -> 3.0.9
* [Revision #031e0ac](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/031e0ac)\
  2019-03-23 16:30:52 +0100
  * Making sure SSL options are not empty strings and not white spaces only.\
    That shouldn't normally happen, as the connector trims dsn field values, and\
    does not store empty strings. But better to be safe.
* [Revision #fb0ac79](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/fb0ac79)\
  2019-03-21 23:18:47 +0100
  * [ODBC-232](https://jira.mariadb.org/browse/ODBC-232) The fix and the testcase
    * This bug boils down to a crash in SQLGetData if an application unbinds\
      result buffers after execution, i.e. calls SQLFreeStmt(SQL\_UNBIND). That\
      happened because SQL\_UNBIND freed columns metadata along with freeing bind\
      buffers.
* [Revision #172c399](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/172c399)\
  2019-03-21 15:36:41 +0100
  * [ODBC-228](https://jira.mariadb.org/browse/ODBC-228) Added connection string option TLSVERSION
    * This option can be used to enforce MARIADB\_OPT\_TLS\_VERSION C/C option to\
      limit allowed for the connection TLS versions.
    * The value can be either a bitmap, where bit 1 corresponds to TLSv1.1,\
      bit 2 - TLSv1.2, and 4 - to TLSv1.3, or it can be set as combination of\
      string names TLSv1.1, TLSv1.2 and TLSv1.3.
    * Checkbox group has been added to the Windows setup dialog. If no\
      checkbox is checked there means all versions are allowed.
    * The testcase tests only correct connection string parsing/storing
    * The file win/ma\_odbc\_setup.h has been moved to 'dsn' directory, as there\
      was already the file with the same name, that wasn't used. 'win'\
      directory has been removed, since that was the only file there
* [Revision #21864d5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/21864d5)\
  2019-03-19 22:13:05 +0100
  * [ODBC-229](https://jira.mariadb.org/browse/ODBC-229) Added option for reading section in my.cnf
    * Connection string option is USE\_MYCNF. OPTIONS bit 65536 may also be used.
    * The checkbox for the option has been added to Windows setup dialog. Removed some garbage from rc file along the way. Test of the option has been added to connstring.
* [Revision #1aad919](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1aad919)\
  2019-03-18 14:57:46 +0100
  * [ODBC-234](https://jira.mariadb.org/browse/ODBC-234) The fix only - not new tests needed
    * [ODBC-233](https://jira.mariadb.org/browse/ODBC-233) will enable tests for this bug
* [Revision #553c71f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/553c71f)\
  2019-03-17 23:25:49 +0100
  * [ODBC-231](https://jira.mariadb.org/browse/ODBC-231) The fix and the testcase.
    * The bug is actually in SSIS. It binds column size as signed int, but the\
      value for LONGTEXT is max unsigned int. Connector was returning truncation\
      error on the row fetch. And that is probably not quite right. The patch\
      makes connector not to return truncation error in case if truncation is\
      caused solely by sign-ness of the field/buffer.
* [Revision #5165a90](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5165a90)\
  2019-03-14 21:20:01 +0100
  * The fix of the build in travis with latest C/C release
* [Revision #35f9e5d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/35f9e5d)\
  2019-03-13 20:55:57 +0100
  * [ODBC-219](https://jira.mariadb.org/browse/ODBC-219) The fix and the testcase.
    * This bug boils down to not reporting correct columns count in case of a\
      query with multiple results(stored procedure or statements batch) if the\
      result with affected rows count followed a resultset.
    * In case of stored procedure(like in the bug report) this is always the\
      case, if SP returns a result set.
    * The bug occured becaule IRD was not reset in the SQLMoreResults in the\
      described case.
    * Fixed mistake in previous commit(for [ODBC-216](https://jira.mariadb.org/browse/ODBC-216)) - lost statement handler\
      reinitialization in one place.
* [Revision #8d22a84](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8d22a84)\
  2019-02-28 23:41:21 +0100
  * [ODBC-216](https://jira.mariadb.org/browse/ODBC-216) The fix and the testcase.
    * Connector returned wrong value for SQL\_DESC\_FIXED\_PREC\_SCALE. In the report\
      it was going about bigint type, but in fact for many other types SQL\_TRUE\
      was returned, where it shouldn't be. Since definition of\
      SQL\_DESC\_FIXED\_PREC\_SCALE is not clear, we checked what SQL Server driver\
      returns for different types for reference. Only for (small)money types\
      SQL\_TRUE is returned. For types that has counterparts in MariaDB, SQL\_FALSE\
      is always returned. Thus, SQL\_FALSE has been made a default value for all\
      types for the SQL\_DESC\_FIXED\_PREC\_SCALE field.
* [Revision #aaba291](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/aaba291)\
  2019-01-24 15:54:55 +0100
  * Fix of error made in tests framework by previous commit
* [Revision #646803f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/646803f)\
  2019-01-23 21:28:59 +0100
  * [ODBC-213](https://jira.mariadb.org/browse/ODBC-213) The fix and the testcase
    * SQL\_DESC\_PARAMETER\_TYPE was returned in wrong type - integer instead of\
      small integer. Also, application could get it not only from Ipd descriptor,\
      but also from Ird.
* [Revision #7b463c1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7b463c1)\
  2018-12-20 16:42:02 -0700
  * [ODBC-207](https://jira.mariadb.org/browse/ODBC-207) Fix multi-statement param realloc.\
    Example use case:\
    Prepare the following SQL statement:\
    "INSERT INTO tbl (a,b) VALUES (?,?); SELECT 1 FROM tbl WHERE c = ?"\
    First execution of prepared statement will work, second execution will segfault or cause memory corruption.
* [Revision #99a8ac0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/99a8ac0)\
  2019-01-03 19:15:48 +0100
  * Merge branch 'master' into [ODBC-3](https://jira.mariadb.org/browse/ODBC-3).0
* [Revision #5d5ec8e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5d5ec8e)\
  2018-10-17 12:39:33 +0100
  * Add SQL\_OUTER\_JOINS support to SQLGetInfo\
    This is an older attribute that is largely superseded by\
    the newer SQL\_OJ\_CAPABILITIES attribute but some software\
    checks it first and only uses SQL\_OJ\_CAPABILITIES to get\
    more details if SQL\_OUTER\_JOINS says they are supported.
* [Revision #5916978](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5916978)\
  2019-01-02 13:31:26 +0100
  * Updating libmariadb to the 3.0.8 release tag
* [Revision #cb5b7ce](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/cb5b7ce)\
  2018-12-10 18:16:41 +0100
  * [ODBC-205](https://jira.mariadb.org/browse/ODBC-205) The patch moves string to date/time types conversion from C/C on C/ODBC\
    side to better meet ODBC requirements.
* [Revision #20e0a50](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/20e0a50)\
  2018-12-02 22:31:37 +0100
  * [ODBC-203](https://jira.mariadb.org/browse/ODBC-203) The fix and the testcase.\
    The problem occurred only with data fetched as SQL\_C\_WCHAR. That\
    happened because for statement handles after 1st one, there wasn't STMT\_ATTR\_UPDATE\_MAX\_LENGTH attribute set, and getting data as a widestring depends on max\_length.
* [Revision #f1e0cd2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f1e0cd2)\
  2018-11-30 01:16:37 +0100
  * [ODBC-204](https://jira.mariadb.org/browse/ODBC-204) SQLGetData did not return empty wide string
* [Revision #92699ab](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/92699ab)\
  2018-11-28 01:33:13 +0100
  * odbc\*.ini files were generated in CMAKE\_SOURCE\_DIR, instead of CMAKE\_BINARY\_DIR. That probably is not right, and they have to be along with tests binaries
* [Revision #07381cc](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/07381cc)\
  2018-11-16 12:06:49 +0100
  * The new logo in README.md
* [Revision #3eed852](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3eed852)\
  2018-11-13 00:01:24 +0100
  * The fix of one compilation warning and of the memory leak introduced by one of fixes in this release
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
* [Revision #79efd0e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/79efd0e)\
  2018-09-12 11:34:19 +0200
  * [ODBC-182](https://jira.mariadb.org/browse/ODBC-182) The fix and the testcase
* [Revision #548db71](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/548db71)\
  2018-09-11 20:17:54 +0200
  * [ODBC-181](https://jira.mariadb.org/browse/ODBC-181) The fix + the testcase\
    The crash or error could be caused by error in the (client side) query parsing in case of a dash followed by a string containing newline character and semicolon
* [Revision #21f200a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/21f200a)\
  2018-09-10 14:41:08 +0200
  * Version bump -> 2.0.19

{% @marketo/form formid="4316" formId="4316" %}
