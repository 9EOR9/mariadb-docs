# MariaDB Connector/ODBC 3.2.1 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/odbc-connector/)[Release Notes](mariadb-connector-odbc-3-2-1-release-notes.md)[Changelog](../changelogs/mariadb-connector-odbc-3-2-changelogs/mariadb-connector-odbc-3-2-1-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 1 Dec 2023

This is a [Release Candidate (RC)](../../../mariadb-release-criteria.md) release of MariaDB Connector/ODBC 3.2.

**Do not use non-stable (non-GA) releases in production!**

MariaDB Connector/ODBC 3.2.1 is built on top of[MariaDB Connector/C v.3.3.8](https://app.gitbook.com/o/diTpXxF5WsbHqTReoBsS/s/aEnK0ZXmUbJzqQrTjFyb/connectors/c/mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-8-release-notes).

## Notable Changes

* [ODBC-66](https://jira.mariadb.org/browse/ODBC-66) - Support ODBC 3.8 standard\
  The driver is now compliant with ODBC standard version 3.8. Mainly that means implementation of SQLCancelHandle API function and SQL\_ATTR\_RESET\_CONNECTION connection attribute support.
* [ODBC-397](https://jira.mariadb.org/browse/ODBC-397) - Add Prepared Statement Cache to the Connector.\
  The driver now uses cache for server side prepared statements, that allows not to re-prepare statements, but use them from the cache. Application can configure the cache with PSCACHESIZE and MAXCACHEKEY connection string options. The former sets the size of the cache, i.e. the number of statements that will be cached, the latter is the maximal size of the cache key, that effectively limits the maximum query length, that will be the value of `MAXCACHEKEY - length of the current schema name - 1`.
* Connector/ODBC is now available as RPM and DEB packages for selected platforms(RHEL, Ubuntu, Debian)
* Improved protocol resilience in case of resultset streaming. In the version 3.1 if the resultset streaming is used, it will block the connection, and the driver will return error on any new query. The 3.2.1 driver in this case will cache the rest of currently streamed resultset, and execute the new query without error

## Bug Fixes

* [ODBC-389](https://jira.mariadb.org/browse/ODBC-389) - alloc-dealloc-mismatch in MADB\_DbcFree
* [ODBC-394](https://jira.mariadb.org/browse/ODBC-394) - Transaction Isolation with 11.1.1 server
* [ODBC-395](https://jira.mariadb.org/browse/ODBC-395) - Transaction Isolation Level is not applied if set before connect
* [ODBC-401](https://jira.mariadb.org/browse/ODBC-401) - SQLCancel won't work in case of encrypted connection, and in some other cases

## Changelog

For a complete list of every change made in this release, with links to\
detailed information on each push, see the[changelog](../changelogs/mariadb-connector-odbc-3-2-changelogs/mariadb-connector-odbc-3-2-1-changelog.md).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
