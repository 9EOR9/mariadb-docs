# Connector/Python 1.1.2 GA Release Notes

{% include "../../../.gitbook/includes/latest-python.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="mariadb-connector-python-1-1-2-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-112-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 27 Jun 2022

This is a [_**stable**_](../../../community-server/about/release-criteria.md) release of MariaDB Connector/Python.

**For a description of this library see the** [**MariaDB Connector/Python documentation**](https://mariadb-corporation.github.io/mariadb-connector-python/index.html) **.**

MariaDB Connector/Python enables python programs to access MariaDB and MySQL databases, using an API which is compliant with the Python DB API 2.0 (PEP-249). It is written in C and uses MariaDB Connector/C client library for client server communication.

## Notable changes

* [CONPY-203](https://jira.mariadb.org/browse/CONPY-203): Error constants added
* [CONPY-204](https://jira.mariadb.org/browse/CONPY-204): New connection method dump\_debug\_info()

## Bug fixes

* [CONPY-194](https://jira.mariadb.org/browse/CONPY-194): Support for INSERT RETURNING in executemany() method.
* Removed utf8 part of internal parser and use binary objects for parameter substitution
* [CONPY-205](https://jira.mariadb.org/browse/CONPY-205): Fixed inconsistent exceptions:
  * All parameter exceptions are returned as ProgrammingError
  * A dictionary now might contain more keys than specified in SQL statement
* Fixed memory leak when using decimal parameters
* [CONPY-201](https://jira.mariadb.org/browse/CONPY-201): Fixed build issues with Python 3.11 beta

## Installation

MariaDB Connector/Python 1.1.2 can be obtained from central python repository:

```bash
pip3 install mariadb
```

or to upgrade to the most recent version

```bash
pip3 install --upgrade mariadb
```

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-112-changelog.md).

## Links:

* [Documentation](https://mariadb-corporation.github.io/mariadb-connector-python/index.htmli)
* [Bug tracker](https://jira.mariadb.org)
* Sources are hosted on [Github](https://github.com/mariadb-corporation/mariadb-connector-python)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
