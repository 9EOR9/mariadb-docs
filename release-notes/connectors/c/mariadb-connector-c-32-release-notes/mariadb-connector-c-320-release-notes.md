# Connector/C 3.2.0 Release notes

The most recent [_**Stable**_](../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](mariadb-connector-c-320-release-notes.md)[Changelog](../changelogs/mariadb-connector-c-32-changelogs/mariadb-connector-c-320-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-c/README.md)

**Release date:** 10 Jun 2021

This is a [_**Beta**_](../../../community-server/about/release-criteria.md) release of the MariaDB\
Connector/C, formerly known as MariaDB Client Library for C.

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

**For a description of this library see the**[**MariaDB Connector/C**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c) **page.**

## New Features

* [MDEV-19237](https://jira.mariadb.org/browse/MDEV-19237): Do not resend prepared statement metadata unnecessarily
* [CONC-508](https://jira.mariadb.org/browse/CONC-508): Added support for passwords > 255 characters
* LOAD DATA LOCAL is now supported in binary protocol
* Updated/extended cipher suite list for Schannel TLS module
* [CONC-433](https://jira.mariadb.org/browse/CONC-433): Added support for certificate revocation list in GnuTLS module
* [CONC-547](https://jira.mariadb.org/browse/CONC-547): Changed default character set from latin1 to utf8mb4
* [CONC-533](https://jira.mariadb.org/browse/CONC-533): Added support for non blocking calls using binary protocol
* [CONC-509](https://jira.mariadb.org/browse/CONC-509): mysql\_get\_client\_\* api functions now return Connector version

## Bug fixes

* various address sanitizer (asan) fixes
* Build fxes for latest CMake version
* [CONC-548](https://jira.mariadb.org/browse/CONC-548): Fixed symbol conflict when linking against libsodium
* [CONC-490](https://jira.mariadb.org/browse/CONC-490): unset CLIENT\_CONNECT\_WITH\_DB flag if no database was specified
* [CONC-543](https://jira.mariadb.org/browse/CONC-543): renamed internal hash functions (to avoid conflicts with statically linked GnuTLS library)
* [CONC-537](https://jira.mariadb.org/browse/CONC-537): Only use MYSQL\_HOME environment variable if MARIADB\_HOME was not specified.
* [CONC-535](https://jira.mariadb.org/browse/CONC-535): disabled checksum ignored in event processing (Replication/Binlog API)
* [CONC-475](https://jira.mariadb.org/browse/CONC-475): export function mariadb\_rpl\_init\_ex (Replication/Binlog API)
* [CONC-521](https://jira.mariadb.org/browse/CONC-521): define \_XOPEN\_SOURCE before including ucontext.h (MacOS)
* [CONC-518](https://jira.mariadb.org/browse/CONC-518): Added macro IS\_MYSQL\_ASYNC() which now checks if memory for extension was allocated.
* [CONC-517](https://jira.mariadb.org/browse/CONC-517): if plugin dir was not specified, plugin needs to be loaded from current path, DLPATH or PATH (Windows)

## Notable changes:

* The connection plugin "aurora" was removed
* Default character set is now utf8mb4
* Character set utf8 will be mapped to utf8mb3
* Added support for MSVC asan

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-c-32-changelogs/mariadb-connector-c-320-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
