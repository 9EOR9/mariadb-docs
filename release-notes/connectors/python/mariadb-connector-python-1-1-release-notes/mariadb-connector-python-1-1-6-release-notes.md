# Connector/Python 1.1.6 Release Notes

{% include "../../../.gitbook/includes/latest-python.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="mariadb-connector-python-1-1-6-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-1-1-6-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 1 Mar 2023

This is a [_**stable**_](../../../mariadb-release-criteria.md) release of MariaDB Connector/Python.

**For a description of this library see the** [**MariaDB Connector/Python documentation**](https://mariadb-corporation.github.io/mariadb-connector-python/index.html) **.**

MariaDB Connector/Python enables python programs to access MariaDB and MySQL databases, using an API which is compliant with the Python DB API 2.0 (PEP-249). It is written in C and uses MariaDB Connector/C client library for client server communication.

## Notable changes

* [CONPY-247](https://jira.mariadb.org/browse/CONPY-247): Added optional parameter "pool\_invalidation\_interval", which specifies the validation interval in milliseconds after which the status of a connection requested from the pool is checked. The default values is 500 milliseconds, a value of 0 means that the status will always be checked.

## Bug fixes

* [CONPY-251](https://jira.mariadb.org/browse/CONPY-251): Check if stmt was already initialized in cursor nextset() method.
* [CONPY-250](https://jira.mariadb.org/browse/CONPY-250): Fixed calculation of connection pool size
* [CONPY-248](https://jira.mariadb.org/browse/CONPY-248): Replace broken connections in connection pool
* [CONPY-246](https://jira.mariadb.org/browse/CONPY-246): Rollback transaction if connection pool was created without pool\_reset\_connection option.
* [CONPY-245](https://jira.mariadb.org/browse/CONPY-245): Implementation of LRU cache in connection pool.
* [CONPY-240](https://jira.mariadb.org/browse/CONPY-240): Don't overwrite errormessage/stacktrace if an exception was generated during module initialization.

## Installation

MariaDB Connector/Python 1.1.6 can be obtained from central python repository:

```bash
pip3 install mariadb
```

or to upgrade to the most recent version

```bash
pip3 install --upgrade mariadb
```

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-1-1-6-changelog.md).

## Links:

* [Documentation](https://mariadb-corporation.github.io/mariadb-connector-python/index.htmli)
* [Bug tracker](https://jira.mariadb.org)
* Sources are hosted on [Github](https://github.com/mariadb-corporation/mariadb-connector-python)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
