# MariaDB Connector/ODBC 1.0.0 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/1.0.0)[Release Notes](../../mariadb-connector-odbc-10-release-notes/mariadb-connector-odbc-100-release-notes.md)[Changelog](mariadb-connector-odbc-100-changelog.md)[Overview of MariaDB Connector/ODBC](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-odbc/mariadb-connector-odbc-guide)

**Release date:** 29 Jan 2015

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-10-release-notes/mariadb-connector-odbc-100-release-notes.md).

The revision number links will take you to the revision's page on Launchpad. On\
Launchpad you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #55](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/55)\
  Wed 2015-01-28 13:41:50 +0100
  * Fixed outdated dependencies of msi installer
* [Revision #54](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/54)\
  Tue 2015-01-27 16:49:10 +0100
  * Ignore Visual Studio files in source package
* [Revision #53](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/53)\
  Tue 2015-01-27 13:09:17 +0100
  * Added readne and license information Added support for creating source package: soure packages can be created by cpack --target package\_source
* [Revision #52](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/52)\
  Thu 2015-01-15 15:02:08 +0100
  * Fixed package name
* [Revision #51](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/51)\
  Thu 2015-01-15 08:57:24 +0100
  * Removed beta in msi package name Bumped version number to 1.0.0 (GA)
* [Revision #50](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/50)\
  Wed 2015-01-14 16:32:16 +0100
  * Partial fix for [ODBC-17](https://jira.mariadb.org/browse/ODBC-17) Now odbcte32 can use the connector. Added support for SQL\_ODBC\_API\_CONFORMANCE and SQL\_ODBC\_SQL\_CONFORMANCE info types.
* [Revision #49](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/49)\
  Wed 2015-01-07 13:37:45 +0100
  * Fixed bug in FindMariaDB.cmake Bumped version number
* [Revision #48](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/48)\
  Tue 2015-01-06 00:42:05 +0100
  * Some amendments to the previous patch fixing memoryleaks
* [Revision #47](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/47)\
  Mon 2015-01-05 12:13:51 +0100
  * Fix of memory leaks in the connector
* [Revision #46](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/46)\
  Fri 2014-12-19 17:45:05 +0100
  * Fixes for posix build.
* [Revision #45](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/45)\
  Wed 2014-11-19 13:22:48 +0100
  * Version bump(patch 5->6)
* [Revision #44](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/44)\
  Tue 2014-11-11 22:19:50 +0100
  * Change for the [ODBC-16](https://jira.mariadb.org/browse/ODBC-16) patch: If previously prepared query was not a batch of statements, Stmt->stmt is closed only if new query is the batch. Much more optiomal, and fixes regressions caused by original patch.
* [Revision #43](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/43)\
  Mon 2014-11-10 16:27:17 +0100\
  \*
  1. Removed memory leak in MADB\_KeyTypeCount - alocated statement was not properly freed 2) Fixed possible buffer overrun in MADB\_StmtGetData 3) Changed in all testcase assert to IS - using not overloaded assert was a bad idea for automated tests. 4) Changed testing framework output to be more in accordance with TAP specs - for failed tests now printed "not ok" instead of "fail" 5) Extended framework with meand to set/get server variables/status. Helper function setting variables. remembers original value, and that value is restored after end of test
* [Revision #42](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/42)\
  Thu 2014-10-23 11:04:44 +0200
  * bump patch version number
* [Revision #41](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/41)\
  Wed 2014-10-22 20:00:44 +0200
  * The fix for [ODBC-16](https://jira.mariadb.org/browse/ODBC-16). It's adding missing mysql\_stmt\_close calls. The most important one is in MADB\_StmtPrepare(called by both SQLPrepare and SQLExecDirect) closing previosly opened by this STMT object prepared statements
* [Revision #40](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/40)\
  Tue 2014-10-21 14:19:00 +0200
  * Fix and the testcase for the bug [ODBC-15](https://jira.mariadb.org/browse/ODBC-15) - SQLGetInfo did not support one deprecated info type(SQL\_ODBC\_API\_CONFORMANCE)
* [Revision #39](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/39)\
  Fri 2014-09-19 17:36:50 +0200
  * Fix and the testcase for [ODBC-14](https://jira.mariadb.org/browse/ODBC-14) - fixed processing of IPD SQL\_DESC\_UNNAMED field update by appliction. SQL\_UNNAMED value is now allowed, SQL\_NAMED causes HY092 error. The error prevented use of queries with parameters in ADO
* [Revision #38](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/38)\
  Fri 2014-09-19 16:47:42 +0200
  * bumped minor version
* [Revision #37](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/37)\
  Thu 2014-08-14 17:46:37 +0300
  * Something that builds on \*nix. DM libs/headers are neither looked for, nor reported they are not found
* [Revision #36](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/36)\
  Tue 2014-08-12 17:26:47 +0300
  * Changed all occurrences of SUCCEEDED macro definition use, to more appropriate and more portable, as for a ODBC driver, SQL\_SUCCEEDED macro
* [Revision #35](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/35)\
  Sun 2014-08-10 02:28:09 +0300
  * Small change for better portability - u\_int64 types use changed to int64\_t
* [Revision #34](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/34)\
  Fri 2014-08-08 21:41:11 +0300
  * Fix for the bug [ODBC-13](https://jira.mariadb.org/browse/ODBC-13) - everything to make prompting work.
* [Revision #33](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/33)\
  Sun 2014-07-13 17:17:53 +0300\
  \*
  1. Made tests to read values from environment as well. Command line parameters override values from the environment variables. Names of variables are: TEST\_DSN TEST\_DRIVER TEST\_SERVER TEST\_UID TEST\_PASSWORD TEST\_SCHEMA TEST\_PORT 2) Added some more name templates to .bzrignore
* [Revision #32](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/32)\
  Tue 2014-07-01 01:24:51 +0300
  * Mostly fixes of warnings on Windows. 1) rc files could not be compiled with express version of VS because of "afxres.h" inclusion. That header belongs to MFC that does not come with express version. 2) Big number of changes is making data types casts explicit or changing type of variables(to avoid casts), removing of not referenced variables, changed ++/-- from postfix to prefix form. 3) Changed one helper function(MADB\_SetString) parameter type to eliminate signed/unsigned values comparing warnings. 4) Also there are some fixes of existing casts. Some of them look bad enough to had been able to cause problems. 5) Now fixes in tests. Some macros were duplicated - removed copies. In many places positions of parameters of macros were switched. Renamed IS\_NUM to is\_num because it clashed with other macro in some windows header. 6) Tests did not respect some of command line parameters. Also I added processing of the case when connection to the server could not be established - some tests were crashing. 7) Introduced .bzrignore file
* [Revision #31](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/31)\
  Mon 2014-06-23 16:22:18 +0300
  * Recoded rc files from utf16(le) to ansi to let bzr see diff in it
* [Revision #30](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/30)\
  Thu 2014-06-26 06:15:57 +0200
  * Fix length calculation for SQL\_C\_CHAR
* [Revision #29](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/29)\
  Wed 2014-06-25 14:53:11 +0200\
  \*
  * Fixed length calculation if both OctetLength and IndicatorPtr (== SQL\_NTS) was specified. - Bump patch version ------------- Ths lin and the following will be ignored --------------
* [Revision #28](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/28)\
  Tue 2014-06-24 19:15:21 +0200
  * Fix for WCHAR fetch: We need to convert the terminating zero charater too.
* [Revision #27](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/27)\
  Fri 2014-06-20 16:15:50 +0200
  * Fixed length calculation for array\_binding if SQL\_NT was specified.
* [Revision #26](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/26)\
  Thu 2014-06-12 06:57:41 +0200
  * Fix for [ODBC-11](https://jira.mariadb.org/browse/ODBC-11): Due to server bug [MDEV-5273](https://jira.mariadb.org/browse/MDEV-5273) we can't get result set metadata after prepare for each statement. Statements like SHOW or CALL procedure name will return metadata after execute. In latter case the number of columns after execute will change and we need to set the ird metadata.
* [Revision #25](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/25)\
  Mon 2014-06-02 08:29:21 +0200
  * Fixed string lengths for unicode conversion
* [Revision #24](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/24)\
  Thu 2014-05-29 15:22:32 +0200
  * Fix for [ODBC-10](https://jira.mariadb.org/browse/ODBC-10): Fixed length calculation for SQLWCHAR for Fetch and Execute
* [Revision #23](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/23)\
  Wed 2014-05-28 08:35:57 +0200
  * Fix for [ODBC-9](https://jira.mariadb.org/browse/ODBC-9): buffer overflow during conversion from char\* to SQL\_NUMERIC\_TYPE
* [Revision #22](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/22)\
  Mon 2014-05-26 12:58:05 +0200
  * Fix for [ODBC-8](https://jira.mariadb.org/browse/ODBC-8): Map FieldIdentifier in SQLColAttributes to ODBC 3.0 compliant values
* [Revision #21](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/21)\
  Mon 2014-05-19 11:46:21 +0200
  * °Fix for [ODBC-6](https://jira.mariadb.org/browse/ODBC-6) and [ODBC-7](https://jira.mariadb.org/browse/ODBC-7) Also includes fix for ADO crash (wrong binding)
* [Revision #20](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/20)\
  Thu 2014-05-15 16:28:35 +0200
  * Fix for CONO7: Return SQL\_VARCHAR instead of SQL\_UNKNOWN\_TYPE for NULL fields
* [Revision #19](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/19)\
  Wed 2014-05-14 08:29:42 +0200
  * Fix for [ODBC-6](https://jira.mariadb.org/browse/ODBC-6): Fixed length attribute for SQLWCHAR parameters if the string isn't null terminated (SqlLen\_or\_IndPtr != SQL\_NTS)
* [Revision #18](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/18)\
  Wed 2014-04-23 09:32:53 +0200
  * Fixed typecasts for CURSOR\_BEHAVIOR constants in SQLGetInfo
* [Revision #17](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/17)\
  Thu 2014-04-10 19:00:45 +0200
  * Fix for SQLCursor: If ODBC version is < 3.0 SQLCloseCursor should not return an error in no cursor is open.
* [Revision #16](https://bazaar.launchpad.net/~jplindst/maria/10.0-FusionIO/revision/16)\
  Thu 2014-04-10 11:44:31 +0200
  * Fixed bug in the msi-installer: The GUID for the driver components was undefined. Uninstallation of prior versions require manual deletion of the MariaDB ODBC driver directory

{% @marketo/form formid="4316" formId="4316" %}
