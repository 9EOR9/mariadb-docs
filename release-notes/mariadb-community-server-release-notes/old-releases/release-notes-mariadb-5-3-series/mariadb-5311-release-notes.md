# MariaDB 5.3.11 Release Notes

The most recent release in the [MariaDB 5.3 series](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) is:[**MariaDB 5.3.12**](mariadb-5312-release-notes.md)

[Download](https://downloads.mariadb.org/mariadb/5.3.11) | **Release Notes** | [Changelog](../../changelogs/changelogs-mariadb-53-series/mariadb-5311-changelog.md) |[Overview of 5.3](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md)

**Release date:** 29 Nov 2012

[MariaDB 5.3.11](mariadb-5311-release-notes.md) is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release. In general this means that there are no known serious bugs, except for those marked as feature requests, that no bugs were fixed since last release that caused notable code changes, and that we believe the code is ready for general usage (based on bug inflow).

**For a description of** [**MariaDB 5.3**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) **see the** [**What is MariaDB 5.3**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) **page.**

For a list of changes made in [MariaDB 5.3.11](mariadb-5311-release-notes.md), with links to detailed information on each push, see the [MariaDB 5.3.11 Changelog](../../changelogs/changelogs-mariadb-53-series/mariadb-5311-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands, interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Important Security Fix for a Buffer Overflow Bug

[MariaDB 5.3.11](mariadb-5311-release-notes.md) includes a fix for [CVE-2012-5611](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5611), a vulnerability that allowed an authenticated user to crash MariaDB server or to execute arbitrary code with the privileges of the `mysqld` process. **This is a serious security issue.** We recommend upgrading from older versions as soon as possible.

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
