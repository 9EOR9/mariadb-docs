# MariaDB Connector/C 3.0.4 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.4)[Release Notes](mariadb-connector-c-304-release-notes.md)[Changelog](../changelogs/mariadb-connector-c-30-changelogs/mariadb-connector-c-304-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 25 Apr 2018

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of the MariaDB\
Connector/C, formerly known as MariaDB Client Library for C.

**For a description of this library see the**[**MariaDB Connector/C**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c) **page.**

## Features

* Added option MYSQL\_OPT\_CAN\_HANDLE\_EXPIRED\_PASSWORDS for\
  mysql\_options()/mysql\_optionsv():If this option is set, client indicates that it will be able to handle expired passwords by setting the CLIENT\_CAN\_HANDLE\_EXPIRED\_PASSWORDS capability flag. If password is expired and CLIENT\_CAN\_HANDLE\_EXPIRED\_PASSWORDS is set, the server will not return an error when connecting, but will put the connection in sandbox mode, where all commands will return error 1820/1828 (ER\_MUST\_CHANGE\_PASSWORD/ER\_MUST\_CHANGE\_PASSWORD\_LOGIN) unless a new password was set.
* New plugin configuration interface: The default configuration for a specific plugin can be specified via cmake parameter -DCLIENT\_PLUGIN\_${PLUGIN}=\[DYNAMIC|STATIC|OFF].
* Added support for linux abstract socket ([MDEV-15655](https://jira.mariadb.org/browse/MDEV-15655)). Thanks to Daniel Black for his contribution.
* Added Travis and Appveyor build support
* [CONC-320](https://jira.mariadb.org/browse/CONC-320): Added asynchronous/non-blocking support for OpenSSL and GnuTLS

## Notable Bug fixes

* Fixed various clang compiler warnings
* [CONC-294](https://jira.mariadb.org/browse/CONC-294): Access violation in mysql\_close when using a connection plugin.
* [MDEV-14977](https://jira.mariadb.org/browse/MDEV-14977): If built dynamically the old\_password plugin could not be located due to wrong filename (must be mysql\_old\_password.so instead of old\_password.so).
* [CONC-315](https://jira.mariadb.org/browse/CONC-315): If no default client character set was specified, the utf8 character set will be used by default (instead of setting the client character set to server character set)
* [CONC-317](https://jira.mariadb.org/browse/CONC-317): Parsing of configuration file fails if key/value pairs contain white spaces.
* [CONC-322](https://jira.mariadb.org/browse/CONC-322): Correct handling of EAGAIN and EINPROGRESS in internal\_connect (socket) for non windows platforms.
* [CONC-323](https://jira.mariadb.org/browse/CONC-323): mariadb\_stmt\_execute\_direct hangs forever if compression used.
* [CONC-324](https://jira.mariadb.org/browse/CONC-324): Wrong codepage numbers for some collations.
* [CONC-326](https://jira.mariadb.org/browse/CONC-326): ssl\_thread\_init() uses wrong openssl threadid callback

For a list of changes made in this release, with links to detailed\
information on each push, see the[changelog](../changelogs/mariadb-connector-c-30-changelogs/mariadb-connector-c-304-changelog.md).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
