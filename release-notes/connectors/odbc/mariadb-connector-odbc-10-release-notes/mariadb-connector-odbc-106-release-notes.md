# Connector/ODBC 1.0.6 Release Notes

The most recent [_**Stable**_](../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/1.0.6)[Release Notes](mariadb-connector-odbc-106-release-notes.md)[Changelog](../changelogs/mariadb-connector-odbc-10-changelogs/mariadb-connector-odbc-106-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 11 Apr 2016

This is a [_**Stable**_](../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB\
Connector/ODBC.

MariaDB Connector/ODBC 1.0.6 is built on top of MariaDB Connector/C 2.2 and\
uses the binary prepared statement protocol.

This is expected to be the final release in the MariaDB Connector/ODBC 1.0 series.

## Bug Fixes

* [ODBC-23](https://jira.mariadb.org/browse/ODBC-23) - Added missing functionality to let application to point to C/C plugins location
* [ODBC-26](https://jira.mariadb.org/browse/ODBC-26) - Duplicate characters when added new row in MS Access
* [ODBC-27](https://jira.mariadb.org/browse/ODBC-27) - In SQLDriverConnect out connection ctring wasn't copied in case of prompting
* [ODBC-29](https://jira.mariadb.org/browse/ODBC-29) - Fixed one of issues from there - error in case of leading blank characters
* [ODBC-30](https://jira.mariadb.org/browse/ODBC-30) - Connection string options did not take precedence of values from the DSN
* [ODBC-32](https://jira.mariadb.org/browse/ODBC-32) - An attempt to set SQL\_ATTR\_PACKET\_SIZE led to connection failure
* Fixed several memory leaks

## Changelog

For a complete list of every change made in this release, with links to\
detailed information on each push, see the [changelog](../changelogs/mariadb-connector-odbc-10-changelogs/mariadb-connector-odbc-106-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
