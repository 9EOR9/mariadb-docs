# MariaDB Connector/ODBC 3.0.7 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/3.0.7/)[Release Notes](mariadb-connector-odbc-307-release-notes.md)[Changelog](../changelogs/mariadb-connector-odbc-30-changelogs/mariadb-connector-odbc-307-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 14 Nov 2018

This is a [Stable (GA)](../../../mariadb-release-criteria.md) release of MariaDB Connector/ODBC 3.0.

MariaDB Connector/ODBC 3.0.7 is built on top of[MariaDB Connector/C v.3.0.7](../../c/mariadb-connector-c-30-release-notes/mariadb-connector-c-307-release-notes.md).

## Bug Fixes

* [ODBC-43](https://jira.mariadb.org/browse/ODBC-43) - If string parameter bound as date/time sql type, overflow errors are not detected
* [ODBC-198](https://jira.mariadb.org/browse/ODBC-198) - Incorrect second fraction number if string field is fetched into TIMESTAMP struct
* [ODBC-199](https://jira.mariadb.org/browse/ODBC-199) - If time parameter is bound as timestamp, date fields should be set to current date values
* [ODBC-194](https://jira.mariadb.org/browse/ODBC-194) - SQLGetData does not return SQL\_NULL\_DATA for datetime types in some cases
* [ODBC-197](https://jira.mariadb.org/browse/ODBC-197) - If Time value is fetched as Timestamp, the fraction part should be 0
* [ODBC-192](https://jira.mariadb.org/browse/ODBC-192) - ODBC 3.0.6 VBA Error on Query
* [ODBC-188](https://jira.mariadb.org/browse/ODBC-188) - Adding Windows ODBC DSN from command line via odbcconf.exe fails
* [ODBC-190](https://jira.mariadb.org/browse/ODBC-190) - Remove C/C auth plugins from packages
* [ODBC-70](https://jira.mariadb.org/browse/ODBC-70) - Last part - caring of 0-date passed in the string
* [ODBC-152](https://jira.mariadb.org/browse/ODBC-152) - Problem with SQLColumns / SQLFetch
* [ODBC-186](https://jira.mariadb.org/browse/ODBC-186) - Several problems with SQLColumns and SQLProcedureColumns
* [ODBC-169](https://jira.mariadb.org/browse/ODBC-169) - Empty results or error if executing mutliple selects in a batch
* [ODBC-183](https://jira.mariadb.org/browse/ODBC-183) - Connector reports incorrect number of affected rows for statements in batch
* [ODBC-182](https://jira.mariadb.org/browse/ODBC-182) - Wrong data inserted into TIME field if bound as TIMESTAMP, and date fields contain data
* [ODBC-181](https://jira.mariadb.org/browse/ODBC-181) - Insert query error decimal + longtext
* [ODBC-178](https://jira.mariadb.org/browse/ODBC-178) - Performance Drop on Long Queries
* [ODBC-177](https://jira.mariadb.org/browse/ODBC-177) - Deadlock error not reported correctly back to client application when using Connector/ODBC
* [ODBC-171](https://jira.mariadb.org/browse/ODBC-171) - Adding BUILD.md file with build instructions

## Changelog

For a complete list of every change made in this release, with links to\
detailed information on each push, see the[changelog](../changelogs/mariadb-connector-odbc-30-changelogs/mariadb-connector-odbc-307-changelog.md).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
