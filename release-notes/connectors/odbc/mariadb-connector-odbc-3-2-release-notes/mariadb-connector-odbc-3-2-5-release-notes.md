# MariaDB Connector/ODBC 3.2.5 Release Notes

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector/)[Release Notes](mariadb-connector-odbc-3-2-5-release-notes.md)[Changelog](../changelogs/mariadb-connector-odbc-3-2-changelogs/mariadb-connector-odbc-3-2-5-changelog.md)[About MariaDB Connector/ODBC](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-odbc/mariadb-connector-odbc-guide)

**Release date:** 24 Feb 2025

This is a [Stable (GA)](../../../mariadb-release-criteria.md) release of MariaDB Connector/ODBC 3.2.

* MariaDB Connector/ODBC 3.2.5 is built on top of [MariaDB Connector/C v.3.4.4](../../c/mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-4-release-notes.md).

## Notable Changes

MariaDB ODBC drivers of 3.2 series can use both text and binary protocol, i.e. prepare statements on the client or on the server side, with text protocol being the default for direct execution(SQLExecDirect() function) and binary protocol for prepared statements(SQLPrepare()+SQLExecute() functions). This release provides applications more control on what protocol to be used

* [ODBC-451](https://jira.mariadb.org/browse/ODBC-451) - Introduced connection string option `EDSERVER` to force SQLExecDirect to use server side prepared statements(SSPS)/binary protocol. This option compliments introduced earlier `PREPONCLIENT` option making SQLPrepare+SQLExecute to prepare query on the client side
* [ODBC-452](https://jira.mariadb.org/browse/ODBC-452) - Added statement and connection attributes to control where queries are prepared by SQLExecDirect and SQLPrepare. These attributes are MariaDB specific, i.e. they will be ignored by other ODBC drivers. The attribute type values are `SQL_ATTR_EXECDIRECT_ON_SERVER`=`25100` and `SQL_ATTR_PREPARE_ON_CLIENT`=`25101`. Setting of connection attributes are equivalent of using of connection string options mentioned above. Statement attributes allow to do the same at the statement level. You can read more at [dedicated section](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-odbc/mariadb-connector-odbc-guide#data-source-specific-attributes) of the article [about MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

## Issues Fixed

* [ODBC-446](https://jira.mariadb.org/browse/ODBC-446) - Wrong naming pattern for deb packages assembled by cpack
* [ODBC-447](https://jira.mariadb.org/browse/ODBC-447) - When trying to use ODBC command FillSchema I get a crash every time / module faulting
* [ODBC-449](https://jira.mariadb.org/browse/ODBC-449) - Milliseconds are truncated
* [ODBC-450](https://jira.mariadb.org/browse/ODBC-450) - GPF on modifying VarChar-Field with more than 4001 Bytes after calling any Stored Procedure
* [ODBC-454](https://jira.mariadb.org/browse/ODBC-454) - SQLForeignKeys reports error

## Changelog

For a complete list of every change made in this release, with links to\
detailed information on each push, see the[changelog](../changelogs/mariadb-connector-odbc-3-2-changelogs/mariadb-connector-odbc-3-2-5-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
