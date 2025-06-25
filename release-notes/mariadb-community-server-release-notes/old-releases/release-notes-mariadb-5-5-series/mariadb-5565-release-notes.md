# MariaDB 5.5.65 Release Notes

The most recent release in the [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.65/)[Release Notes](mariadb-5565-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5565-changelog.md)[Overview of 5.5](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md)

**Release date:** 31 Jul 2019

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

**For a description of** [**MariaDB 5.5**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **see the**[**What is MariaDB 5.5?**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **page.**

In most respects MariaDB will work exactly as MySQL: all commands,interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Updates & Bug Fixes

[MariaDB 5.5.65](mariadb-5565-release-notes.md) is a maintenance release.

* [MDEV-19922](https://jira.mariadb.org/browse/MDEV-19922): [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 10.2
* Revert a change related to `auto_increment_increment` (Oracle Bug#14049391, regression reported as Oracle Bug#15851528)
* Replace [MDEV-8827](https://jira.mariadb.org/browse/MDEV-8827) with a backport from MySQL 5.6
* [MDEV-19491](https://jira.mariadb.org/browse/MDEV-19491): update query stopped working after mariadb upgrade
* [MDEV-20110](https://jira.mariadb.org/browse/MDEV-20110): don't try to load client plugins with invalid names
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2019-2805](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2805)
  * [CVE-2019-2740](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2740)
  * [CVE-2019-2739](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2739)
  * [CVE-2019-2737](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2737)
  * [CVE-2020-2922](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2922)
  * [CVE-2021-2007](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2007)

## Changelog

A full list of all changes is in the [changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5565-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 5.5.65](mariadb-5565-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-7-10-3-17-10-2-26-10-1-41-and-5-5-65-now-available/).

Thanks, and enjoy MariaDB!

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
