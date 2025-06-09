# MariaDB Connector/ODBC 1.0.0 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/1.0.0)[Release Notes](mariadb-connector-odbc-100-release-notes.md)[Changelog](../changelogs/mariadb-connector-odbc-10-changelogs/mariadb-connector-odbc-100-changelog.md)[Overview of MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-the-mariadb-odbc-driver/README.md)

**Release date:** 29 Jan 2015

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of the MariaDB Connector/ODBC.\
In general, marking this release as _stable_ means that\
there are no known serious bugs, except for those marked as feature requests,\
that no bugs were fixed since last release that caused a notable code changes,\
and that we believe the code is ready for general usage (based on bug inflow).

MariaDB Connector/ODBC 1.0.0 is built on top of the MariaDB Connector/C 2.1\
and uses the binary prepared statement protocol.

## Bug fixes

* The connector now can be tested with odbcte32. Added support for SQL\_ODBC\_API\_CONFORMANCE and SQL\_ODBC\_SQL\_CONFORMANCE info types. ([ODBC-17](https://jira.mariadb.org/browse/ODBC-17))
* Fixed a number of memory leaks in the connector
* Change in build. FindMariaDB now uses mariadb\_config to determine include and library path.
* Removed memory leak in allocated statement (was not properly freed) and possible buffer overrun in some internal functions (MADB\_KeyTypeCount and MADB\_StmtGetData)
* Applications running certain sequences of query types(in particular when query batches were involved) on long run made server reach max\_prepared\_stmt\_count, causing application error and/or crash. ([ODBC-16](https://jira.mariadb.org/browse/ODBC-16))
* SQLGetInfo did not support deprecated info type SQL\_ODBC\_API\_CONFORMANCE ([ODBC-15](https://jira.mariadb.org/browse/ODBC-15))
* Fixed processing of IPD SQL\_DESC\_UNNAMED field update by application. ([ODBC-14](https://jira.mariadb.org/browse/ODBC-14))
* SQL\_UNNAMED value is now allowed, SQL\_NAMED causes HY092 error. The error prevented use of queries with parameters in ADO
* Fixed DS setup dialog prompting ([ODBC-13](https://jira.mariadb.org/browse/ODBC-13))
* Fixed length calculation for SQL\_C\_CHAR
* Fixed length calculation if both OctetLength and IndicatorPtr (== SQL\_NTS) was specified
* Fix for WCHAR fetch: terminating zero character was not converted.
* Fixed length calculation for array\_binding if SQL\_NTS was specified.
* Due to server bug [MDEV-5273](https://jira.mariadb.org/browse/MDEV-5273) we can't get result set metadata after prepare for each statement. Statements like SHOW or CALL procedure name will return metadata after execute. In latter case the number of columns after execute will change and we need to set the ird metadata. ([ODBC-11](https://jira.mariadb.org/browse/ODBC-11))
* Fixed string lengths for unicode conversion
* Fixed length calculation for SQLWCHAR for Fetch and Execute ([ODBC-10](https://jira.mariadb.org/browse/ODBC-10))
* Fixed buffer overflow during conversion from char\* to SQL\_NUMERIC\_TYPE ([ODBC-9](https://jira.mariadb.org/browse/ODBC-9))
* Map FieldIdentifier in SQLColAttributes to ODBC 3.0 compliant values ([ODBC-8](https://jira.mariadb.org/browse/ODBC-8))
* Return SQL\_VARCHAR instead of SQL\_UNKNOWN\_TYPE for NULL fields ([ODBC-7](https://jira.mariadb.org/browse/ODBC-7))
* Application fails with the following exception when sending data as parameters. System.Data.Odbc.OdbcException: ERROR \[HY000] Illegal mix of collations (latin1\_swedish\_ci,IMPLICIT) and (utf8\_general\_ci,COERCIBLE) for operation '=' ([ODBC-6](https://jira.mariadb.org/browse/ODBC-6))
* When using MariaDB ODBC Connector with ODBC Driver Manager 3.81, the Driver Manager returns errror IM001 (The driver doesn't support this function) for SQLExecute, SQLExecDirect or SQLBindCol. ([ODBC-5](https://jira.mariadb.org/browse/ODBC-5))
* Fixed typecasts for CURSOR\_BEHAVIOR constants in SQLGetInfo
* Fix for SQLCursor: If ODBC version is < 3.0 SQLCloseCursor should not return an error in no cursor is open.
* Fixed bug in the msi-installer: The GUID for the driver components was undefined. ([ODBC-4](https://jira.mariadb.org/browse/ODBC-4))
* Uninstallation of prior versions require manual deletion of the MariaDB ODBC driver directory
* SQLBindCol should ignore column index if the statement doesn't return a result set ([ODBC-3](https://jira.mariadb.org/browse/ODBC-3))

For a complete\
list and description please check the[Jira bug system](https://jira.mariadb.org/browse/ODBC)

## Changelog

For a list of changes made in this release, with links to detailed\
information on each push, see the[changelog](../changelogs/mariadb-connector-odbc-10-changelogs/mariadb-connector-odbc-100-changelog.md).
