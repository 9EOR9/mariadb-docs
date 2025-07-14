# MariaDB Connector/Python 1.0.0 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/Python is:[**MariaDB Connector/Python 1.1.12**](../mariadb-connector-python-1-1-release-notes/mariadb-connector-python-1-1-12-release-notes.md)

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a>  <a href="mariadb-connector-python-1-0-0-release-notes.md" class="button secondary">Release Notes</a>  <a href="../changelogs/mariadb-connector-python-10-changelogs/mariadb-connector-python-100-changelog.md" class="button secondary">Changelog</a>  <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 24 June 2020

This is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release of the MariaDB\
Connector/Python.

MariaDB Connector/Python enables python programs to access MariaDB and MySQL\
databases, using an API which is compliant with the Python DB API 2.0\
(PEP-249). It is written in C and uses MariaDB Connector/C client library for\
client server communication.

## Notable Updates

* [CONPY-81](https://jira.mariadb.org/browse/CONPY-81): Fixed crash when switching between text and binary protocol with same cursor
* [CONPY-80](https://jira.mariadb.org/browse/CONPY-80): Parameters in set\_config() method of ConnectionPool class have to be checked against the list of DSN keywords
* [CONPY-79](https://jira.mariadb.org/browse/CONPY-79): When inserting NULL values with executemany() method on a server which doesn't support BULK statements NULL values weren't inserted correctly.
* [CONPY-78](https://jira.mariadb.org/browse/CONPY-78): Since MaxScale doesn't support bulk operations yet, we have to check servers extended capability flag to determine if this feature is supported or not.
* [CONPY-76](https://jira.mariadb.org/browse/CONPY-76): Added aliases username, passwd and db to connection keywords.
* [CONPY-70](https://jira.mariadb.org/browse/CONPY-70): set\_config() method needs to check the passed parameter and raise an exception if the parameter type is not a dictionary.
* [CONPY-72](https://jira.mariadb.org/browse/CONPY-72): When deallocating the connection pool class, we need to check beside pool\_size if the array containing the connections is valid.
* Fixed bug when inserting negative integer values with cursor.execute() method
* [CONPY-69](https://jira.mariadb.org/browse/CONPY-69): Set default character set (utf8mb4) with authentication packet

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-python-10-changelogs/mariadb-connector-python-100-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
