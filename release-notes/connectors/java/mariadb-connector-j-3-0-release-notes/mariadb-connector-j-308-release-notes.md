# MariaDB Connector/J 3.0.8 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of [MariaDB Connector/J](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-j/README.md) is:[**MariaDB Connector/J 3.5.3**](../mariadb-connector-j-3-5-release-notes/mariadb-connector-j-3-5-3-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](mariadb-connector-j-308-release-notes.md)[Changelog](../changelogs/mariadb-connectorj-30-changelogs/mariadb-connector-j-308-changelog.md)[Connector/J Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-j/README.md)

**Release date:** 20 Sep 2022

MariaDB Connector/J 3.0.8 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

**For an overview of MariaDB Connector/J see the**[**About MariaDB Connector/J**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-j/README.md) **page**

### Notable Changes

* [CONJ-1010](https://jira.mariadb.org/browse/CONJ-1010) improve client side prepared parameter parameter substitution

### Bugs Fixed

* [CONJ-997](https://jira.mariadb.org/browse/CONJ-997) regression in 3.x when using option galeraAllowedState resulting in an IndexOutOfBoundsException
* [CONJ-1002](https://jira.mariadb.org/browse/CONJ-1002) 2nd failover reconnection ignores default database/schema setting when not set by connection string
* [CONJ-1003](https://jira.mariadb.org/browse/CONJ-1003) replication configuration always use 1st replica on 3.0
* [CONJ-996](https://jira.mariadb.org/browse/CONJ-996) BatchUpdateException doesn't inherited the SQLState & vendorCode from the cause SQL exception
* [CONJ-1006](https://jira.mariadb.org/browse/CONJ-1006) disabling cachePrepStmts with useServerPrepStmts might result in Exception
* [CONJ-1007](https://jira.mariadb.org/browse/CONJ-1007) Socket file descriptors are leaked after connecting with unix socket if DB is not up running
* [CONJ-999](https://jira.mariadb.org/browse/CONJ-999) setting createDatabaseIfNotExist option use on read-only server will refuse connection on 3.0

## Changelog

For a complete list of changes made in MariaDB Connector/J 3.0.8, with links to detailed\
information on each push, see the [changelog](../changelogs/mariadb-connectorj-30-changelogs/mariadb-connector-j-308-changelog.md).

{% @marketo/form formid="4316" formId="4316" %}
