# Connector/ODBC 3.1.22 Release Notes

{% include "../../../.gitbook/includes/latest-odbc.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector" class="button primary">Download</a> <a href="mariadb-connectorodbc-3-1-22-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/mariadb-connector-odbc-31-changelogs/mariadb-connector-odbc-3.1.22-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-odbc" class="button secondary">About MariaDB Connector/ODBC</a>

**Release date:**

This is a [Stable (GA)](../../../community-server/about/release-criteria.md) release of MariaDB Connector/ODBC 3.1.

MariaDB Connector/ODBC 3.1.22 is built on top of [MariaDB Connector/C v.3.3.15](../../c/mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-15-release-notes.md).

## Bug Fixes

* [ODBC-458](https://jira.mariadb.org/browse/ODBC-458) - MS Access won't work with the linked table if best row id is BIGINT
* [ODBC-459](https://jira.mariadb.org/browse/ODBC-459) - MS Access shows record with AUTO\_INCREMENT primary key as #Deleted after insert that does not specify that field value
* [ODBC-464](https://jira.mariadb.org/browse/ODBC-464) - Multiple issues with current implementation of SQLCancel
* [ODBC-466](https://jira.mariadb.org/browse/ODBC-466) - SQLCancel could run on already dropped statement due to race condition

## New Feature

* [ODBC-457](https://jira.mariadb.org/browse/ODBC-457) - Introduced option TRUNCDT to skip time truncation error. Setting it to non-zero value makes connector not to return error on date/time type parameter value truncation. These are when value for SQL\_TIME contains fractional part, or for SQL\_DATE contains non-zero time. In particular, that permits to insert value with fractional part into TIME field which in MariaDB can have fractional part as ODBC SQL\_TIME type.

## Changelog

For a complete list of every change made in this release, with links to\
detailed information on each push, see the [changelog](https://github.com/mariadb-corporation/docs-release-notes/blob/test/connectors/odbc/mariadb-connector-odbc-3-1-release-notes/mariadb-connector-odbc-3-1-22-changelog/README.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
