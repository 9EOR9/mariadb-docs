# MariaDB 5.5.31 Release Notes

The most recent release in the [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.31) | **Release Notes** | [Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5531-changelog.md) | [Overview of 5.5](broken-reference/)

**Release date:** 23 May 2013

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release. In general this\
means that there are no known serious bugs, except for those marked as feature\
requests, that no bugs were fixed since last release that caused a notable code\
changes, and that we believe the code is ready for general usage (based on bug\
inflow).

**For a description of** [**MariaDB 5.5**](broken-reference/) **see the**[**What is MariaDB 5.5?**](broken-reference/) **page.**

For a list of changes made in this release, with links to detailed\
information on each push, see the[MariaDB 5.5.31 Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5531-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

This is primarily a bug-fix release.

## Includes [MariaDB 5.3.12](../release-notes-mariadb-5-3-series/mariadb-5312-release-notes.md) and MySQL 5.5.31

This release includes [MariaDB 5.3.12](../release-notes-mariadb-5-3-series/mariadb-5312-release-notes.md) and MySQL 5.5.31. See[Changes in MySQL 5.5.31](https://dev.mysql.com/doc/relnotes/mysql/5.5/en/news-5-5-31.html)\
for what changed in MySQL.

## Security fixes

This release includes fixes for the following security vulnerabilities:

* [CVE-2013-3805](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-3805)
* [CVE-2013-3808](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-3808)
* [CVE-2013-3801](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-3801)
* [CVE-2013-3794](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-3794)
* [CVE-2013-2375](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-2375)
* [CVE-2013-1544](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1544)
* [CVE-2013-1532](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1532)
* [CVE-2013-2389](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-2389)
* [CVE-2013-2392](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-2392)
* [CVE-2013-2376](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-2376)
* [CVE-2013-1511](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1511)
* [CVE-2013-2391](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-2391)
* [CVE-2013-1502](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1502)

## Other Notable Updates

* Includes [XtraDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) from Percona Server-5.5.30-rel30.2
* Includes an alpha version of the [QUERY\_CACHE\_INFO plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/query-cache-information-plugin), that allows to see the content of the query cache via the corresponding INFORMATION\_SCHEMA table.
* MariaDB MSI packages for Windows include the latest [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) 8.0.
* Support for FusionIO/directFS atomic writes added ([MDEV-4338](https://jira.mariadb.org/browse/MDEV-4338)). See the following\
  for more information:
  * [MariaDB Introduces Atomic Writes](https://blog.mariadb.org/mariadb-introduces-atomic-writes/)
  * [FusionIO DirectFS atomic write support](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/configuring-mariadb/mariadb-performance-advanced-configurations/atomic-write-support)
  * [Fusion-io Introduction](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/configuring-mariadb/mariadb-performance-advanced-configurations/fusion-io/fusion-io-introduction)

## Ubuntu 13.04 "Raring" Packages

Packages are now available for Ubuntu 13.04 "Raring". Use the [repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/) to get the appropriate commands.

## Ubuntu 8.04 LTS "Hardy" and 11.10 "Oneiric" Deprecated

In accordance with the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md) the following distributions have reached the end of their support periods (EOL):

* Ubuntu 8.04 LTS "Hardy"
* Ubuntu 11.10 "Oneiric"
* Mint 9 LTS "Isadora"
* Mint 12 "Lisa"

This release ([MariaDB 5.5.31](mariadb-5531-release-notes.md)) is therefore the last MariaDB release to feature packages for these distros. The [repositories](https://downloads.mariadb.org/mariadb/repositories/) for them will remain online until the 5.5.32 release. At that time they will go away.

Binary tar.gz files built on Ubuntu "Hardy" will also be going away. These are the ones that _do not_ require GLIBC\_2.14+. So for the next release, all binary tar.gz files for Linux will require GLIBC\_2.14+.

Thanks, and enjoy MariaDB!

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
