# Changes and Improvements in MariaDB Connector/C 3.2

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

MariaDB Connector/C 3.2 is the current major development version. MariaDB Connector/C 3.1 is stable and feature-complete, so major new features to be developed are going into 3.2.

* [View the source tree](https://github.com/mariadb-corporation/mariadb-connector-c/tree/3.2)

## New Features

* [MDEV-19237](https://jira.mariadb.org/browse/MDEV-19237): Do not resend prepared statement metadata unnecessarily
* [CONC-508](https://jira.mariadb.org/browse/CONC-508): Added support for passwords > 255 characters
* LOAD DATA LOCAL is now supported in binary protocol
* Updated/extended cipher suite list for Schannel TLS module
* [CONC-433](https://jira.mariadb.org/browse/CONC-433): Added support for certificate revocation list in GnuTLS module
* [CONC-547](https://jira.mariadb.org/browse/CONC-547): Changed default character set from latin1 to utf8mb4
* [CONC-533](https://jira.mariadb.org/browse/CONC-533): Added support for non blocking calls using binary protocol
* [CONC-509](https://jira.mariadb.org/browse/CONC-509): mysql\_get\_client\_\* api functions now return Connector version

## Notable changes:

* The connection plugin "aurora" was removed
* Default character set is now utf8mb4
* Character set utf8 will be mapped to utf8mb3
* Added support for MSVC asan

{% @marketo/form formid="4316" formId="4316" %}
