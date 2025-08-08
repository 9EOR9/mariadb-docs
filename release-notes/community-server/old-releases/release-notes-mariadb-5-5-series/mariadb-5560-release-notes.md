# MariaDB 5.5.60 Release Notes

The most recent release in the [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.60) | [Release Notes](mariadb-5560-release-notes.md) | [Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5560-changelog.md) | [Overview of 5.5](changes-improvements-in-mariadb-5-5.md)

**Release date:** 23 Apr 2018

This is a [_**Stable**_](../../about/release-criteria.md) _**(GA)**_ release.

**For a description of** [**MariaDB 5.5**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **see the**[**What is MariaDB 5.5?**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **page.**

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Updates & Bug Fixes

[MariaDB 5.5.60](mariadb-5560-release-notes.md) is a maintenance release. It includes bugfixes and\
updates, including from MySQL 5.5.60.

* [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) updated to 5.5.59-38.11
* The embedded server library now supports SSL when connecting to remote servers.
* [MDEV-7049](https://jira.mariadb.org/browse/MDEV-7049) MySQL#74585 - InnoDB: Failing assertion: \*mbmaxlen < 5
* As per the [MariaDB Deprecation Policy](../../about/platform-deprecation-policy.md), this will be\
  the last release of [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) for Debian 7 Wheezy
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-2755](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2755)
  * [CVE-2018-2761](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2761)
  * [CVE-2018-2767](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2767)
  * [CVE-2018-2771](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2771)
  * [CVE-2018-2781](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2781)
  * [CVE-2018-2813](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2813)
  * [CVE-2018-2817](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2817)
  * [CVE-2018-2819](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2819)
  * [CVE-2019-2455](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2455)

## Changelog

A full list of all changes is in the [changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5560-changelog.md).

Thanks, and enjoy MariaDB!

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
