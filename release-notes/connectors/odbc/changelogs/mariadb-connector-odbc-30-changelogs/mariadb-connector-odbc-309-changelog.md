# MariaDB Connector/ODBC 3.0.9 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-309-release-notes.md)[Changelog](mariadb-connector-odbc-309-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 3 May 2019

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-309-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more\
details of the revision and view diffs of the code modified in that revision.

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
