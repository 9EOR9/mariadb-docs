# MariaDB 5.1.66 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://downloads.askmonty.org/mariadb/5.1.66) |**Release Notes** |[Changelog](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/changes-improvements-in-mariadb-5-1)
**Release date:** 29 Nov 2012

[MariaDB 5.1.66](mariadb-5166-release-notes.md) is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release. In general this means that there are no known serious bugs, except for those marked as feature requests, that no bugs were fixed since last release that caused a notable code changes, and that we believe the code is ready for general usage (based on bug inflow).

**For a description of** [**MariaDB 5.1**](changes-improvements-in-mariadb-5-1.md) **see the**[**What is MariaDB 5.1**](changes-improvements-in-mariadb-5-1.md) **page.**

For a list of changes made in [MariaDB 5.1.66](mariadb-5166-release-notes.md), with links to detailed information on each push, see the [MariaDB 5.1.66 Changelog](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/broken-reference/README.md).

In most respects [MariaDB](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series) will work exactly as MySQL: all commands, interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Important Security Fixes

* [MariaDB 5.1.66](mariadb-5166-release-notes.md) includes a fix for [CVE-2012-5611](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5611), a vulnerability that allowed an authenticated user to crash MariaDB server or to execute arbitrary code with the privileges of the `mysqld` process. This is a serious security issue. We recommend upgrading from older versions as soon as possible.
* A fix is also included for multiple SQL injection vulnerabilities in the replication code. See [MDEV-382](https://jira.mariadb.org/browse/MDEV-382) ([CVE-2012-4414](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-4414)) for details.

This release also includes fixes for the following security vulnerabilities:

* [CVE-2012-5060](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5060)
* [CVE-2012-3177](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3177)
* [CVE-2012-3180](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3180)
* [CVE-2012-3160](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3160)
* [CVE-2012-3163](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3163)
* [CVE-2012-3158](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3158)
* [CVE-2012-3177](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3177)
* [CVE-2012-3150](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3150)
* [CVE-2012-3197](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3197)
* [CVE-2013-1548](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1548)
* [CVE-2012-3166](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3166)
* [CVE-2012-3173](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3173)
* [CVE-2012-3167](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-3167)
* [CVE-2012-0540](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0540)
* [CVE-2012-1734](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1734)
* [CVE-2012-1689](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1689)

## Includes MySQL 5.1.66

This version of MariaDB includes MySQL 5.1.66. See [Changes in MySQL 5.1.66](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-66.html) for what changed between this and previous MySQL versions.

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
