# MariaDB Connector/C 3.0.6 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.6)[Release Notes](mariadb-connector-c-306-release-notes.md)[Changelog](../changelogs/mariadb-connector-c-30-changelogs/mariadb-connector-c-306-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 2 Aug 2018

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of the MariaDB\
Connector/C, formerly known as MariaDB Client Library for C.

**For a description of this library see the**[**MariaDB Connector/C**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c) **page.**

## Notable Bug fixes

* [MDEV-15263](https://jira.mariadb.org/browse/MDEV-15263): FIx IS\_NUM() macro
* Coverity scan bug fixes
* [CONC-297](https://jira.mariadb.org/browse/CONC-297): local infile parameter must be unsigned int instead of my\_bool
* [CONC-329](https://jira.mariadb.org/browse/CONC-329): change return value of internal socket functions from my\_bool to int (Thanks to Daniel Black for his contribution)
* [CONC-332](https://jira.mariadb.org/browse/CONC-332): my\_auth doesn't read/update server ok packet
* [CONC-344](https://jira.mariadb.org/browse/CONC-344): reset internal row counter
* [CONC-345](https://jira.mariadb.org/browse/CONC-345): invalid heap use after free
* [CONC-346](https://jira.mariadb.org/browse/CONC-346): Remove old cmake policies
* [ODBC-154](https://jira.mariadb.org/browse/ODBC-154): Fixed build layout when building Connector/C as subproject in Connector/ODBC (Thanks to Lawrin Novitsky for his contribution)
* fixed crash in mysql\_select\_db if NULL parameter was provided
* Debian layout changes/fixes (Thanks to Otto Kekäläinen)

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-c-30-changelogs/mariadb-connector-c-306-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
