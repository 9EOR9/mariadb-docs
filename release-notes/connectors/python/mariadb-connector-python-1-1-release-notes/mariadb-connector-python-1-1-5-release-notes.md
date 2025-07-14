# Connector/Python 1.1.5 Release Notes

{% include "../../../.gitbook/includes/latest-python.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="mariadb-connector-python-1-1-5-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-1-1-5-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 7 Nov 2022

This is a [_**stable**_](../../../mariadb-release-criteria.md) release of MariaDB Connector/Python.

**For a description of this library see the**[**MariaDB Connector/Python documentation**](https://mariadb-corporation.github.io/mariadb-connector-python/index.html) **.**

MariaDB Connector/Python enables python programs to access MariaDB and MySQL databases, using an API which is compliant with the Python DB API 2.0 (PEP-249). It is written in C and uses MariaDB Connector/C client library for client server communication.

## Notable changes

* [CONPY-220](https://jira.mariadb.org/browse/CONPY-220): Added \_get\_socket() method
* Performance improvement: Instead of iterating via fetchone(), fetchall() and fetchmany() methods now load the data directly at once.

## Bug fixes

* [CONPY-222](https://jira.mariadb.org/browse/CONPY-222): Removed del() method from cursor
* [CONPY-224](https://jira.mariadb.org/browse/CONPY-224): Fixed bulk\_operation when reexecuted using same cursor
* [CONPY-225](https://jira.mariadb.org/browse/CONPY-225): Fixed cursor.affected\_rows property
* [CONPY-226](https://jira.mariadb.org/browse/CONPY-226): Replaced deprecated distutils (PEP-632)
* [CONPY-227](https://jira.mariadb.org/browse/CONPY-227): Replaced collections.named\_tuple by PyStruct\_Sequence (C-Python)
* [CONPY-228](https://jira.mariadb.org/browse/CONPY-228): Fixed Installation error (if C/C version < 3.2.4 was found)
* [CONPY-229](https://jira.mariadb.org/browse/CONPY-229): Converter: added missing support for None conversions
* [CONPY-231](https://jira.mariadb.org/browse/CONPY-231): Fixed memory leak

## Installation

MariaDB Connector/Python 1.1.5 can be obtained from central python repository:

```bash
pip3 install mariadb
```

or to upgrade to the most recent version

```bash
pip3 install --upgrade mariadb
```

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-python-11-changelogs/mariadb-connector-python-1-1-5-changelog.md).

## Links:

* [Documentation](https://mariadb-corporation.github.io/mariadb-connector-python/index.htmli)
* [Bug tracker](https://jira.mariadb.org)
* Sources are hosted on [Github](https://github.com/mariadb-corporation/mariadb-connector-python)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
