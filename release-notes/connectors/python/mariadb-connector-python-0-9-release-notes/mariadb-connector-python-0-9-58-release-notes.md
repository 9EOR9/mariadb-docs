# Connector/Python 0.9.58-beta Release Notes

{% include "../../../.gitbook/includes/latest-python.md" %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/python-connector/" class="button primary">Download</a> <a href="mariadb-connector-python-0-9-58-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/mariadb-connector-python-09-changelogs/mariadb-connector-python-0958-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/connectors-quickstart-guides/connector-python-guide" class="button secondary">Connector/Python Overview</a>

**Release date:** 6 May 2020

This is a [_**beta**_](../../../community-server/about/release-criteria.md) release of MariaDB Connector/Python and not intended for production use.

{% hint style="danger" %}
**Do not use&#x20;**_**beta**_**&#x20;releases in production!**
{% endhint %}

MariaDB Connector/Python enables python programs to access MariaDB and MySQL databases, using an API which is compliant with the Python DB API 2.0 (PEP-249). It is written in C and uses MariaDB Connector/C client library for client server communication.

## Notable Updates

* [CONPY-62](https://jira.mariadb.org/browse/CONPY-62): When using binary protocol (which is forced when using a placeholder), the type NEW\_DECIMAL was ignored and internally converted as string instead of Decimal
* [CONPY-61](https://jira.mariadb.org/browse/CONPY-61): Fixed bug in execute\_many when using NULL values or indicator variables
* [CONPY-59](https://jira.mariadb.org/browse/CONPY-59): Fixed bug when converting invalid date "0000-00-00". Instead of raising an exception it will be converted to None value.
* [CONPY-58](https://jira.mariadb.org/browse/CONPY-58): Fixed parameter error when using paramstype PyFormat.

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-python-09-changelogs/mariadb-connector-python-0958-changelog.md).

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
