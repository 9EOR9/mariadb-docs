# MariaDB 5.5.68 Release Notes

[Download](https://downloads.mariadb.org/mariadb/5.5.68/)[Release Notes](mariadb-5568-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5568-changelog.md)[Overview of 5.5](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md)

**Release date:** 12 May 2020

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release. Note that with this release, [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) is now end-of-life, and no longer supported.

**For a description of** [**MariaDB 5.5**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **see the**[**What is MariaDB 5.5?**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **page.**

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/mariadb/README.md) 5.5 will work exactly as MySQL 5.5: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Updates & Bug Fixes

[MariaDB 5.5.68](mariadb-5568-release-notes.md) is a maintenance release.

* [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 11.0 ([MDEV-22032](https://jira.mariadb.org/browse/MDEV-22032))
* Unregister of slave threads disconnected before COM\_BINLOG\_DUMP (Bug#29915479)
* Server can fail while replicating conditional comments (Bug#28388217)
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2020-2752](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2752)
  * [CVE-2020-2812](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2812)

## Changelog

A full list of all changes is in the [changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5568-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 5.5.68](mariadb-5568-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-13-10-3-23-10-2-32-10-1-45-and-5-5-68-now-available).\
Thanks, and enjoy MariaDB!

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
