# MariaDB 5.5.48 Release Notes

The most recent release in the [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.48)[Release Notes](mariadb-5548-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5548-changelog.md)[Overview of 5.5](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md)

**Release date:** 11 Feb 2016

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

**For a description of** [**MariaDB 5.5**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **see the**[**What is MariaDB 5.5?**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **page.**

For a list of changes made in this release, with links to detailed\
information on each push, see the[MariaDB 5.5.48 Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5548-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Updates & Bug Fixes

[MariaDB 5.5.48](mariadb-5548-release-notes.md) is a maintenance release. It includes several bugfixes and\
updates, including from MySQL 5.5.48. Notable updates include:

* [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) updated to 5.5.47-37.7
* Backport new proxy server option for the [Feedback Plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/feedback-plugin), [feedback\_http\_proxy](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/feedback-plugin#feedback_http_proxy), for use when http calls cannot be made, such as in a firewall environment.
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2016-0640](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0640)
  * [CVE-2016-0644](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0644)
  * [CVE-2016-0646](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0646)
  * [CVE-2016-0649](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0649)
  * [CVE-2016-0650](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0650)
  * [CVE-2016-0641](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0641)

### Deprecated Distributions

As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the\
last release of [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) for Debian 6 "Squeeze".

## Changelog

A full list of all changes is in the [changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5548-changelog.md).

Thanks, and enjoy MariaDB!

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
