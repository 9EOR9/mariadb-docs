# Connector/Python 1.1.8 Release Notes

{% include "../../../.gitbook/includes/latest-python.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="mariadb-connector-python-1-1-8-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-1-1-8-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 16 Oct 2023

This is a [_**stable**_](../../../community-server/about/release-criteria.md) release of MariaDB Connector/Python.

**For a description of this library see the** [**MariaDB Connector/Python documentation**](https://mariadb-corporation.github.io/mariadb-connector-python/index.html) **.**

MariaDB Connector/Python enables python programs to access MariaDB and MySQL databases, using an API which is compliant with the Python DB API 2.0 (PEP-249). It is written in C and uses MariaDB Connector/C client library for client server communication.

## Notable changes

* [CONPY-271](https://jira.mariadb.org/browse/CONPY-271): Cusor object provides now a metadata attribute, which returns resultset metadata as a dictionary. metadata attribute also contains information about extended field types like JSON, UUID, INET4/6 and geometry types.
* Added new constants mariadb.constants.EXT\_FIELD\_TYPE which describe extended field types..

## Bug fixes

* [CONPY-270](https://jira.mariadb.org/browse/CONPY-270): Data will be converted to Binary only if the character set is binary, the BINARY\_FLAG will be ignored.
* [CONPY-269](https://jira.mariadb.org/browse/CONPY-269): If cursors rowcount attribute will be retrieved after the cursor was closed, rowcount now returns -1 instead of raising an exception. This is a workaround for a pandas bug.

## Installation

MariaDB Connector/Python 1.1.8 can be obtained from central python repository:

```bash
pip3 install mariadb
```

or to upgrade to the most recent version

```bash
pip3 install --upgrade mariadb
```

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-1-1-8-changelog.md).

## Links:

* [Documentation](https://mariadb-corporation.github.io/mariadb-connector-python/index.htmli)
* [Bug tracker](https://jira.mariadb.org)
* Sources are hosted on [Github](https://github.com/mariadb-corporation/mariadb-connector-python)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
