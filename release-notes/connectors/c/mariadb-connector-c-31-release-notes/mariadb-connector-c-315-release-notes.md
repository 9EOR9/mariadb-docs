# MariaDB Connector/C 3.1.5 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](mariadb-connector-c-315-release-notes.md)[Changelog](../changelogs/mariadb-connector-c-31-changelogs/mariadb-connector-c-315-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-c/README.md)

**Release date:** 11 Nov 2019

This is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release of the MariaDB\
Connector/C, formerly known as MariaDB Client Library for C.

**For a description of this library see the**[**MariaDB Connector/C**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c) **page.**

## Notable Changes

* [MDEV-20469](https://jira.mariadb.org/browse/MDEV-20469): Plugin dialog could not be loaded (wrong path)
* [ODBC-440](https://jira.mariadb.org/browse/ODBC-440): Fixed typo in sha256\_password cmake configuration
* [CONC-418](https://jira.mariadb.org/browse/CONC-418): For unknown/not handled schannel error codes FormatMessage function will be used instead of returning "Unknown error" message.
* [CONC-417](https://jira.mariadb.org/browse/CONC-417), [MDEV-13492](https://jira.mariadb.org/browse/MDEV-13492): At irregular intervals older windows versions (prior Windows 10) fail to establish a secure (TLS) connection and return errors SEC\_E\_INVALID\_TOKEN, SEC\_E\_BUFFER\_TOO\_SMALL or SEC\_E\_MESSAGE\_ALTERED. This is a bug in windows schannel library and was only fixed in recent versions, also OpenSSL provided a workaround (see [1350](https://github.com/openssl/openssl/pull/1350)). Since we are unable to fix this, in case of an error during TLS handshake the errorcode Connector/C will try to reconnect up to three times if the error code was SEC\_E\_INVALID\_TOKEN, SEC\_E\_BUFFER\_TOO\_SMALL or SEC\_E\_MESSAGE\_ALTERED.
* Included in [MariaDB 10.4.10](../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-10410-release-notes.md), [MariaDB 10.3.20](../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10320-release-notes.md), and [MariaDB 10.2.29](../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10229-release-notes.md)

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-c-31-changelogs/mariadb-connector-c-315-changelog.md).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
