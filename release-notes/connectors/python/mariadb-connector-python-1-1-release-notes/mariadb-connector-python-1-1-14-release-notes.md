# Connector/Python 1.1.14 Release Notes

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="mariadb-connector-python-1-1-14-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/mariadb-connector-python-11-changelogs/connector-python-1.1.13-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 6 Oct 2025

This is a [_**stable**_](../../../community-server/about/release-criteria.md) release of MariaDB Connector/Python.

**For a description of this library see the** [**MariaDB Connector/Python documentation**](https://mariadb-corporation.github.io/mariadb-connector-python/index.html) **.**

MariaDB Connector/Python enables python programs to access MariaDB and MySQL databases, using an API which is compliant with the Python DB API 2.0 (PEP-249). It is written in C and uses MariaDB Connector/C client library for client server communication.

## Notable changes

* Python 3.14 Windows binary wheels
* CI moved from travis to github actions

## Bug fixes

* CONPY-318: Fixed segfault when clearing cursors after connection dropped
* CONPY-321: Fixed index error in pool initialization. Kudos to G.Mech for providing a fix

## Installation

MariaDB Connector/Python 1.1.14 can be obtained from central python repository:

```bash
pip3 install mariadb
```

or to upgrade to the most recent version

```bash
pip3 install --upgrade mariadb
```

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-python-11-changelogs/connector-python-1.1.14-changelog.md).

## Links

* [Documentation](https://mariadb-corporation.github.io/mariadb-connector-python/index.htmli)
* [Bug tracker](https://jira.mariadb.org)
* Sources are hosted on [Github](https://github.com/mariadb-corporation/mariadb-connector-python)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
