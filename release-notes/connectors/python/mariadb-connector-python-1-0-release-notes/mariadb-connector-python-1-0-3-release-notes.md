# Connector/Python 1.0.3 Release Notes

{% include "../../../.gitbook/includes/latest-python.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="mariadb-connector-python-1-0-3-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/mariadb-connector-python-10-changelogs/mariadb-connector-python-103-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 7 Oct 2020

This is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release of MariaDB Connector/Python.

MariaDB Connector/Python enables python programs to access MariaDB and MySQL databases, using an API which is compliant with the Python DB API 2.0 (PEP-249). It is written in C and uses MariaDB Connector/C client library for client server communication.

## Notable Changes

* [CONPY-117](https://jira.mariadb.org/browse/CONPY-117): Add converter support: The connect() method now accepts an addtional parameter converter which points to a dictionary, containing one or more conversions. A conversion must be specified in the form {FIELD\_TYPE : conversion\_function}

## Bugs Fixed

* [CONPY-119](https://jira.mariadb.org/browse/CONPY-119): Fixed Memory leak with cursor type dictionary
* Check parameters (execute/executemany) for valid subtypes
* [CONPY-118](https://jira.mariadb.org/browse/CONPY-118): Removed statement allocation from cursor initialization function for text protocol
* Don't set unsigned flag if value will fit into unsigned integer (Workaround for [MDEV-23481](https://jira.mariadb.org/browse/MDEV-23481))
* [CONPY-116](https://jira.mariadb.org/browse/CONPY-116): Wrong type reported for MYSQL\_TYPE\_JSON

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-python-10-changelogs/mariadb-connector-python-103-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
