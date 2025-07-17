# Connector/C 3.0.2 Release notes

The most recent [_**Stable**_](../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.2)[Release Notes](mariadb-connector-c-302-release-notes.md)[Changelog](../changelogs/mariadb-connector-c-30-changelogs/mariadb-connector-c-302-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 20 July 2017

This is a [_**Stable**_](../../../community-server/about/release-criteria.md) _**(GA)**_ release of the MariaDB\
Connector/C, formerly known as MariaDB Client Library for C.

**For a description of this library see the**[**MariaDB Connector/C**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c) **page.**

## Features

* Array support for prepared statements (bulk operations)
* TLS/SSL support for GnuTLS, Windows SChannel and LibreSSL
* Support for passphrase protected keys
* SHA256 authentication plugin

## New API functions

* mariadb\_get\_info and mariadb\_get\_infov (variable argument list): for obtaining general and connection specific values.
* mariadb\_get\_charset\_by\_name and mariadb\_get\_charset\_by\_nr: returns character set information for a given internal number or name of character set. These functions have been previously used internally by MariaDB Connector/ODBC and are now exported, so they can be used also within plugins.
* mysql\_reconnect which was used internally before (if the option MYSQL\_OPT\_RECONNECT was set) is now part of the API and can be used by applications and plugins to reestablish a failing connection
* mariadb\_cancel: aborts a connection immediately by making all subsequent read/write operations fail
* mariadb\_stmt\_execute\_direct: prepares and executes a prepared statement for one time execution
* mysql\_stmt\_warning\_count returns: the number of warnings from the last executed statement
* mysql\_reset\_connection: resets the current connection and clears session state
* Functions for obtaining session state changes:
  * mysql\_session\_track\_get\_first()
  * mysql\_session\_track\_get\_next()

## Notable Bug fixes

* [MDEV-13317](https://jira.mariadb.org/browse/MDEV-13317): Crash in PHP5 when using libmariadb and curl mpdules
* [MDEV-13320](https://jira.mariadb.org/browse/MDEV-13320): Wrong output for mariadb\_config on OSX
* [MDEV-12889](https://jira.mariadb.org/browse/MDEV-12889): Missing version info for shared object
* [MDEV-12965](https://jira.mariadb.org/browse/MDEV-12965): Connector/C reads only the first configuration file
* [MDEV-13100](https://jira.mariadb.org/browse/MDEV-13100): Can't read custom config file
* [MDEV-12423](https://jira.mariadb.org/browse/MDEV-12423): Install fails to create symlinks
* [MDEV-13040](https://jira.mariadb.org/browse/MDEV-13040): mariadb\_stmt.h contains c++ comments
* [MDEV-12763](https://jira.mariadb.org/browse/MDEV-12763): Don't use deprecated API calls with OpenSSL 1.1
* [MDEV-12247](https://jira.mariadb.org/browse/MDEV-12247): Server does not respond for single query execution
* [MDEV-12446](https://jira.mariadb.org/browse/MDEV-12446): double free if no default configuration is present
* [MDEV-11708](https://jira.mariadb.org/browse/MDEV-11708): cmake with option -DWITH\_ASAN no longer works
* [MDEV-11008](https://jira.mariadb.org/browse/MDEV-11008): Connector/C integration does not respect INSTALL\_LIBDIR or INSTALL\_DOCDIR
* [MDEV-10894](https://jira.mariadb.org/browse/MDEV-10894): Fixed conversion for big-endian platforms
* [CONC-252](https://jira.mariadb.org/browse/CONC-252): Use unsigned long instead of size\_t for api functions
* [CONC-265](https://jira.mariadb.org/browse/CONC-265): Big endian fixes
* [CONC-253](https://jira.mariadb.org/browse/CONC-253): Compiler warnings in gssapi\_client.c
* [CONC-250](https://jira.mariadb.org/browse/CONC-250): Added support for wildcards and SAN
* [CONC-231](https://jira.mariadb.org/browse/CONC-231): Incorrect FSF address
* [CONC-224](https://jira.mariadb.org/browse/CONC-224): Allow to build without TLS support
* [CONC-223](https://jira.mariadb.org/browse/CONC-223): Added missing collations
* [CONC-222](https://jira.mariadb.org/browse/CONC-222): Installation fixes for missing include files

For a list of changes made in this release, with links to detailed\
information on each push, see the[changelog](../changelogs/mariadb-connector-c-30-changelogs/mariadb-connector-c-302-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
