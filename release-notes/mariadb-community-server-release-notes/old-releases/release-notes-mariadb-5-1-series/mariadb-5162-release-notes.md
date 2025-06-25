# MariaDB 5.1.62 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://downloads.askmonty.org/mariadb/5.1.62) |**Release Notes** |[Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5162-changelog.md) |[Overview of 5.1](changes-improvements-in-mariadb-5-1.md)

**Release date:** 6 Apr 2012

[MariaDB 5.1.62](mariadb-5162-release-notes.md) is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release. In\
general this means that there are no known serious bugs, except for those\
marked as feature requests, that no bugs were fixed since last release that\
caused a notable code changes, and that we believe the code is ready for\
general usage (based on bug inflow).

**For a description of** [**MariaDB 5.1**](changes-improvements-in-mariadb-5-1.md) **see the**[**What is MariaDB 5.1**](changes-improvements-in-mariadb-5-1.md) **page.**

For a list of changes made in [MariaDB 5.1.62](mariadb-5162-release-notes.md), with links to detailed\
information on each push, see the[MariaDB 5.1.62 Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5162-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Important Security Fix for Rare Password Bug

[MariaDB 5.1.62](mariadb-5162-release-notes.md) fixes a bug that under certain rare circumstances allowed a user to\
connect with an invalid password. **This is a serious security issue.** We\
recommend upgrading from older versions as soon as possible.

## Other Security Fixes

This release includes fixes for the following security vulnerabilities:

* [CVE-2012-1703](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1703)
* [CVE-2012-1688](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1688)
* [CVE-2012-1690](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1690)

## Includes MySQL 5.1.62

This version of MariaDB includes MySQL 5.1.62. See[Changes in MySQL 5.1.62](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-62.html)\
for what changed between this and previous MySQL versions.

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
