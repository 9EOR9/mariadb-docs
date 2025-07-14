# Connector/Python 1.1.0 Beta1 Release Notes

{% include "../../../.gitbook/includes/latest-python.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="mariadb-connector-python-1-1-0-beta1-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-110-beta1-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 27 Sep 2021

This is a [_**beta**_](../../../mariadb-release-criteria.md) release of MariaDB Connector/Python and not intended for production use.

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

**For a description of this library see the**[**MariaDB Connector/Python documentation**](https://mariadb-corporation.github.io/mariadb-connector-python/index.html) **.**

MariaDB Connector/Python enables python programs to access MariaDB and MySQL databases, using an API which is compliant with the Python DB API 2.0 (PEP-249). It is written in C and uses MariaDB Connector/C client library for client server communication.

## Notable changes

* [CONPY-162](https://jira.mariadb.org/browse/CONPY-162): Added attributes for obtaining version of MariaDB Connector/C library:
  * mariadb.client\_version returns an integer, describing the version in the following format: MAJOR\_VERSION \* 10000 + MINOR\_VERSION \* 1000 + PATCH\_VERSION
  * mariadb\_client\_version\_info returns client version in tuple format

## Bug fixes

* [CONPY-159](https://jira.mariadb.org/browse/CONPY-159): Parse integer instead of short integer when retrieving server status
* [CONPY-160](https://jira.mariadb.org/browse/CONPY-160): ConnectionPool.get\_connection might return None due to low precision of time.monotonic()
* [CONPY-161](https://jira.mariadb.org/browse/CONPY-161): ConnectionPool.connection\_count returns list of connections instead of a numeric value

## Installation

MariaDB Connector/Python 1.1.0-beta1 can be obtained from central python repository:

```bash
pip3 install --pre mariadb
```

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-110-beta1-changelog.md).

## Links:

* [Documentation](https://github.com/mariadb-corporation/mariadb-connector-python/wiki)
* [Bug tracker](https://jira.mariadb.org)
* Sources are hosted on [Github](https://github.com/mariadb-corporation/mariadb-connector-python)

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
