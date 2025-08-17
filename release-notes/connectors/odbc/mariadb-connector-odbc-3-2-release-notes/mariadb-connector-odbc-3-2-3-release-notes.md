# Connector/ODBC 3.2.3 Release Notes

{% include "../../../.gitbook/includes/latest-odbc.md" %}

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector/) | [Release Notes](mariadb-connector-odbc-3-2-3-release-notes.md) | [Changelog](../changelogs/mariadb-connector-odbc-3-2-changelogs/mariadb-connector-odbc-3-2-3-changelog.md) | [About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-odbc/README.md)

**Release date:** 26 Aug 2024

This is a [Stable (GA)](../../../community-server/about/release-criteria.md) release of MariaDB Connector/ODBC 3.2.

MariaDB Connector/ODBC 3.2.3 is built on top of [MariaDB Connector/C v.3.4.1](../../c/mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-1-release-notes.md).

## Issues Fixed

* [ODBC-424](https://jira.mariadb.org/browse/ODBC-424) - Can't open connection from .NET application to MySQL 8.4
* [ODBC-426](https://jira.mariadb.org/browse/ODBC-426) - SQLForeignKeys call may result in error with MySQL server
* [ODBC-427](https://jira.mariadb.org/browse/ODBC-427) - Out parameters won't be written to parameter buffers with MySQL server
* [ODBC-429](https://jira.mariadb.org/browse/ODBC-429) - AccessViolationException when executing a SELECT on a non existing table
* [ODBC-430](https://jira.mariadb.org/browse/ODBC-430) - Wrong reported max size for VARCHAR and VARBINARY
* [ODBC-431](https://jira.mariadb.org/browse/ODBC-431) - Result-set streaming doesn't work with binary results
* [ODBC-432](https://jira.mariadb.org/browse/ODBC-432) - Driver fails to cache multiple results
* [ODBC-433](https://jira.mariadb.org/browse/ODBC-433) - SQLMoreResults may pick other statement's results
* [ODBC-435](https://jira.mariadb.org/browse/ODBC-435) - SQLPrimaryKeys call returns incorrect KEY\_SEQ field

## Changelog

For a complete list of every change made in this release, with links to\
detailed information on each push, see the [changelog](../changelogs/mariadb-connector-odbc-3-2-changelogs/mariadb-connector-odbc-3-2-2-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
