# Connector/ODBC 3.1.18 Release Notes

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](mariadb-connector-odbc-3-1-18-release-notes.md)[Changelog](../changelogs/mariadb-connector-odbc-31-changelogs/mariadb-connector-odbc-3-1-18-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-odbc/README.md)

**Release date:** 13 Apr 2023

This is a [Stable (GA)](../../../community-server/about/release-criteria.md) release of MariaDB Connector/ODBC 3.1.

MariaDB Connector/ODBC 3.1.18 is built on top of [MariaDB Connector/C v.3.3.2](../../c/mariadb-connector-c-33-release-notes/mariadb-connector-c-332-release-notes.md).

## Notable Changes

* Authentication plugins are now all static(compiled in) on Windows. That is also true for named pipe pvio plugin ([ODBC-384](https://jira.mariadb.org/browse/ODBC-384))

## Bug Fixes

* [ODBC-313](https://jira.mariadb.org/browse/ODBC-313) - Redundant SQLPrimaryKeys calls in applications created with Embarcadero
* [ODBC-374](https://jira.mariadb.org/browse/ODBC-374) - SQL\_C\_FLOAT should be mapped to SQLREAL, and not to SQLFLOAT
* [ODBC-375](https://jira.mariadb.org/browse/ODBC-375) - Connector can crash, if one of queries in the batch returns error on result storing
* [ODBC-377](https://jira.mariadb.org/browse/ODBC-377) - Timeouts set via ODBC do nothing
* [ODBC-378](https://jira.mariadb.org/browse/ODBC-378) - OPTIMIZE TABLE returns no resultset
* [ODBC-380](https://jira.mariadb.org/browse/ODBC-380) - Memory leak if connected with multistatement option
* [ODBC-385](https://jira.mariadb.org/browse/ODBC-385) - Wrong documentation for named pipes
* [ODBC-386](https://jira.mariadb.org/browse/ODBC-386) - Optimizing empty tables corrupts the MariaDB connection via ODBC
* [ODBC-387](https://jira.mariadb.org/browse/ODBC-387) - Connection string superseded by default settings

## Changelog

For a complete list of every change made in this release, with links to\
detailed information on each push, see the [changelog](../changelogs/mariadb-connector-odbc-31-changelogs/mariadb-connector-odbc-3-1-18-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
