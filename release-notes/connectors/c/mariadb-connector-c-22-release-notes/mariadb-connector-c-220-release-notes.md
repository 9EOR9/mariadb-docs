# MariaDB Connector/C 2.2.0 Release notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/2.2.0)[Release Notes](mariadb-connector-c-220-release-notes.md)[Changelog](../changelogs/mariadb-connector-c-22-changelogs/mariadb-connector-c-220-changelog.md)[About of MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-c/README.md)

**Release date:** 29 Sept 2015

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of the MariaDB\
Connector/C, formerly known as MariaDB Client Library for C. In general,\
marking this release as _stable_ means that there are no known serious bugs,\
except for those marked as feature requests, that no bugs were fixed since last\
release that caused a notable code changes, and that we believe the code is\
ready for general usage (based on bug inflow).

**For a description of this library see the**[**MariaDB Connector/C**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c) **page.**

## New features

SSL: For preventing man in the middle attacks MariaDB Connector/C now supports additional validation of a server certificate by checking the SHA1-fingerprint.\
(New options: MARIADB\_OPT\_SSL\_FP and MARIADB\_OPT\_SSL\_FP\_LIST)

## Bug fixes

* [CONC-129](https://jira.mariadb.org/browse/CONC-129): fix crash in mysql\_close\_start if connection is broken
* [CONC-130](https://jira.mariadb.org/browse/CONC-130): Initial wait on connect is wrong direction
* [CONC-131](https://jira.mariadb.org/browse/CONC-131): memory leak in mysql\_close (asynchronous)
* [CONC-132](https://jira.mariadb.org/browse/CONC-132): Prevent overriding of SUFFIX\_INSTALL\_DIR
* [CONC-133](https://jira.mariadb.org/browse/CONC-133): Centos 6 32 bits: Release build error: my\_context.c:454: Error: CFI instruction used without previous .cfi\_startproc
* [CONC-135](https://jira.mariadb.org/browse/CONC-135): mysql\_get\_socket now returns MARIADB\_INVALID\_SOCKET
* [CONC-136](https://jira.mariadb.org/browse/CONC-136): Asynchronous version of mysql\_select\_db was not exported
* [CONC-137](https://jira.mariadb.org/browse/CONC-137): Error code not set in mysql\_stmt\_send\_long\_data
* [CONC-138](https://jira.mariadb.org/browse/CONC-138): memory leak in mysql\_ssl\_set
* [CONC-139](https://jira.mariadb.org/browse/CONC-139): Xcode/OSX build doesn't work
* [CONC-140](https://jira.mariadb.org/browse/CONC-140): MinGW/Windows7 build doesn't work because ssize\_t is redefined
* [CONC-141](https://jira.mariadb.org/browse/CONC-141): Hang when working with prepared statements
* [CONC-143](https://jira.mariadb.org/browse/CONC-143): use #include "my\_stmt.h" instead of \<my\_stmt.h> in mysql.h
* Fixed possible memory overrun: When reallocating net->buffer we need to allocate extra space for header and compressed header
* removed dynamic column dependencies from my\_global.h
* fixed plugin path in mariadb\_config
* security fix: Don’t switch to untrusted connection if mysql\_ssl\_set was called and option for checking server certificate was enabled.
* Added a global variable mariadb\_deinitialize\_ssl which controls if SSL will be deinitialized in mysql\_server\_end (see [MDEV-6671](https://jira.mariadb.org/browse/MDEV-6671))
* Fixed string for hex\_symbols in mysql\_hex\_string function

## Changelog

For a list of changes made in this release, with links to detailed\
information on each push, see the[changelog](../changelogs/mariadb-connector-c-22-changelogs/mariadb-connector-c-220-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
