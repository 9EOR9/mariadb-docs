# MariaDB 5.5.47 Release Notes

The most recent release in the [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.47)[Release Notes](mariadb-5547-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5547-changelog.md)[Overview of 5.5](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md)

**Release date:** 10 Dec 2015

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

**For a description of** [**MariaDB 5.5**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **see the**[**What is MariaDB 5.5?**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **page.**

For a list of changes made in this release, with links to detailed\
information on each push, see the[MariaDB 5.5.47 Changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5547-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Updates & Bug Fixes

[MariaDB 5.5.47](mariadb-5547-release-notes.md) is a maintenance release. It includes several bugfixes and\
updates, including from MySQL 5.5.47. Notable updates include:

* [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) updated to 5.5.46-37.6
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2016-0546](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0546)
  * [CVE-2016-0505](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0505)
  * [CVE-2016-0596](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0596)
  * [CVE-2016-0597](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0597)
  * [CVE-2016-0616](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0616)
  * [CVE-2016-0598](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0598)
  * [CVE-2016-0600](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0600)
  * [CVE-2016-0606](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0606)
  * [CVE-2016-0608](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0608)
  * [CVE-2016-0609](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0609)
  * [CVE-2016-0642](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0642)
  * [CVE-2016-0651](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-0651)
  * [CVE-2016-2047](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-2047): [MDEV-9212](https://jira.mariadb.org/browse/MDEV-9212): Fixed incorrect implementation of the `--ssl-verify-server-cert`\
    option that allowed a malicious attacker (with a capability to perform a\
    man-in-the-middle attack) to replace the server SSL certificate, bypassing\
    the client-side hostname verification. This vulnerability was discovered by\
    Paul Kehrer and Alex Gaynor.

### SLES 11 Support

Previous builds of [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) for Suse Linux Enterprise Server (SLES) 11 only\
supported SLES 11 SP3 and SP4. Starting with this release, SLES 11 builds for\
x86\_64 also support SLES 11 SP1 and SP2.

## Changelog

A full list of all changes is in the [changelog](../../changelogs/changelogs-mariadb-55-series/mariadb-5547-changelog.md).

Thanks, and enjoy MariaDB!

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
