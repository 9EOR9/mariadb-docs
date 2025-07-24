# Connector/ODBC 3.2.2 Release Notes

The most recent [_**Stable**_](../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector/)[Release Notes](mariadb-connector-odbc-3-2-2-release-notes.md)[Changelog](../changelogs/mariadb-connector-odbc-3-2-changelogs/mariadb-connector-odbc-3-2-2-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 18 Jun 2024

This is a [Stable (GA)](../../../community-server/about/release-criteria.md) release of MariaDB Connector/ODBC 3.2.

MariaDB Connector/ODBC 3.2.2 is built on top of [MariaDB Connector/C v.3.4.0](../../c/mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-0-release-notes.md).

## Notable Changes

* [ODBC-421](https://jira.mariadb.org/browse/ODBC-421) - The driver has been moved to use Connector/C 3.4 series driver. The most important change implied by that, is that certificate verification option (`SSLVERIFY`) is now by default on if encrypted connection is requested by the application.
* [ODBC-163](https://jira.mariadb.org/browse/ODBC-163) - Support of new C/C callback system for custom data type conversion. There are 2 types of callbacks - for parameters and result.
  * Parameter callbacks are used for bulk operations and allow to minimize memory use required for data type conversions. Their use controlled by the connection string option `PCALLBACK`, which is `on` by default.
  * Result callbacks are designed to make certain types of conversions faster and also reduce memory use, as they can write directly to application buffers and do not allocate intermediate buffers normally required for conversion. The option to turn on result callbacks is `RCALLBACK` and it is `off` by default.
* [ODBC-410](https://jira.mariadb.org/browse/ODBC-410) - `SQLForeignKeys` performance optimization. The function could be noticeably slow in the case of a large number of schemas in the database. The optimization makes it significantly faster in such cases.

## Issues Fixed

* [ODBC-399](https://jira.mariadb.org/browse/ODBC-399) - Executable Comment Syntax which results in empty command gives `'You have an error in your SQL syntax'`
* [ODBC-403](https://jira.mariadb.org/browse/ODBC-403) - Setting query timeout could cause error with older server versions `"Unknown system variable 'STATEMENT'"`
* [ODBC-405](https://jira.mariadb.org/browse/ODBC-405) - can't read DECIMAL values with error:

```
Multiple-step OLE DB operation generated errors. Check each OLE DB status value, if available. No work was done.
```

* [ODBC-418](https://jira.mariadb.org/browse/ODBC-418) - Widechar string data gets truncated if it contains a `NULL` character

## Changelog

For a complete list of every change made in this release, with links to\
detailed information on each push, see the [changelog](../changelogs/mariadb-connector-odbc-3-2-changelogs/mariadb-connector-odbc-3-2-2-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
