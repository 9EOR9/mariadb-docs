# MariaDB Connector/Python 1.1.7 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/Python is:[**MariaDB Connector/Python 1.1.12**](mariadb-connector-python-1-1-12-release-notes.md)

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/)[Release Notes](mariadb-connector-python-1-1-7-release-notes.md)[Changelog](../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-1-1-7-changelog.md)[Connector/Python Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb-connector-python/README.md)

**Release date:** 10 Jul 2023

This is a [_**stable**_](../../../mariadb-release-criteria.md) release of the MariaDB\
Connector/Python.

**For a description of this library see the**[**MariaDB Connector/Python documentation**](https://mariadb-corporation.github.io/mariadb-connector-python/index.html) **.**

MariaDB Connector/Python enables python programs to access MariaDB and MySQL databases, using an API which is compliant with the Python DB API 2.0 (PEP-249). It is written in C and uses MariaDB Connector/C client library for client server communication.

## Notable changes

* [CONPY-253](https://jira.mariadb.org/browse/CONPY-253): The connection method now offers the option of specifying the version of the TLS protocol using tls\_version.

## Bug fixes

* [CONPY-258](https://jira.mariadb.org/browse/CONPY-258): Fixed ValueError exception if ZEROFILL flag is defined
* [CONPY-255](https://jira.mariadb.org/browse/CONPY-255): If all connections from a pool are in use, pool.get\_connection now returns None instead of raising an exception.
* [CONPY-256](https://jira.mariadb.org/browse/CONPY-256): Fix indexing when moving a free connection to used connections to avoid returning the same connection twice. Kudos and thanks to G.Mech for reporting this bug and providing the fix.

## Installation

MariaDB Connector/Python 1.1.7 can be obtained from central python repository:

```bash
pip3 install mariadb
```

or to upgrade to the most recent version

```bash
pip3 install --upgrade mariadb
```

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-1-1-7-changelog.md).

## Links:

* [Documentation](https://mariadb-corporation.github.io/mariadb-connector-python/index.htmli)
* [Bug tracker](https://jira.mariadb.org)
* Sources are hosted on [Github](https://github.com/mariadb-corporation/mariadb-connector-python)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
