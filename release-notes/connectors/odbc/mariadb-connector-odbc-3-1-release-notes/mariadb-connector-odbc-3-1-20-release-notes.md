# Connector/ODBC 3.1.20 Release Notes

The most recent [_**Stable**_](../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector)[Release Notes](mariadb-connector-odbc-3-1-20-release-notes.md)[Changelog](../changelogs/mariadb-connector-odbc-31-changelogs/mariadb-connector-odbc-3-1-20-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 4 Dec 2023

This is a [Stable (GA)](../../../community-server/about/release-criteria.md) release of MariaDB Connector/ODBC 3.1.

MariaDB Connector/ODBC 3.1.20 is built on top of [MariaDB Connector/C v.3.3.8](../../c/mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-8-release-notes.md).

## Notable Changes

* Connector/ODBC is now available as RPM and DEB packages for selected platforms(RHEL, Ubuntu, Debian)

## Bug Fixes

* [ODBC-394](https://jira.mariadb.org/browse/ODBC-394) - Transaction Isolataion with 11.1.1 server
* [ODBC-395](https://jira.mariadb.org/browse/ODBC-395) - Tansaction Isolation Level is not applied if set before connect
* [ODBC-399](https://jira.mariadb.org/browse/ODBC-399) - Executable Comment Syntax which results in empty command gives 'You have an error in your SQL syntax'
* [ODBC-401](https://jira.mariadb.org/browse/ODBC-401) - SQLCancel won't work in case of encrypted connection, and in some other cases
* [ODBC-403](https://jira.mariadb.org/browse/ODBC-403) - Unknown system variable 'STATEMENT'

## New Feature

* [ODBC-402](https://jira.mariadb.org/browse/ODBC-402) - Add support of MADB\_OPT\_FLAG\_NO\_BIGINT option. Some classic applications do not support SQLBIGINT option. This option makes the column that normally would be of SQLBIGINT type to look like it is of SQLINTEGER type

## Changelog

For a complete list of every change made in this release, with links to\
detailed information on each push, see the [changelog](../changelogs/mariadb-connector-odbc-31-changelogs/mariadb-connector-odbc-3-1-20-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
