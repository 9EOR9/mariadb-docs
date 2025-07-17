# Connector/C 3.0.5 Release Notes

The most recent [_**Stable**_](../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.5)[Release Notes](mariadb-connector-c-305-release-notes.md)[Changelog](../changelogs/mariadb-connector-c-30-changelogs/mariadb-connector-c-305-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 7 Jun 2018

This is a [_**Stable**_](../../../community-server/about/release-criteria.md) _**(GA)**_ release of the MariaDB\
Connector/C, formerly known as MariaDB Client Library for C.

**For a description of this library see the**[**MariaDB Connector/C**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c) **page.**

## Notable Bug fixes

* [CONC-336](https://jira.mariadb.org/browse/CONC-336): Allow multiple initialization of client library
* Fixed string to MYSQL\_TIME conversion (prepared statements)
* [CONC-334](https://jira.mariadb.org/browse/CONC-334): Copy all members of MYSQL\_FIELD to internal statement structure
* [CONC-315](https://jira.mariadb.org/browse/CONC-315): Change default character set to latin1
* Fixed double free in dynamic column library
* Fixed plugin library on MacOS
* Added checks for corrupted packets in protocol
* [MDEV-15450](https://jira.mariadb.org/browse/MDEV-15450): Added default connection attribute \_server\_host
* [CONC-326](https://jira.mariadb.org/browse/CONC-326): fixed wrong openssl thread id callback
* [CONC-330](https://jira.mariadb.org/browse/CONC-330): Allow to build without TLS support
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-3081](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3081)
  * [CVE-2020-14550](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14550)
  * [CVE-2021-2011](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2011)

## Changelog

For a list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-c-30-changelogs/mariadb-connector-c-305-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
