# MariaDB 5.5.24 Release Notes

The most recent release in the [MariaDB 5.5](changes-improvements-in-mariadb-5-5.md) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.askmonty.org/mariadb/5.5.24) |**Release Notes** |[Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5524-changelog.md) |[Overview of 5.5](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md)

**Release date:** 31 May 2012

[MariaDB 5.5.24](mariadb-5524-release-notes.md) is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_\
release. In general this means that there are no known serious bugs, except for\
those marked as feature requests, that no bugs were fixed since last release\
that caused a notable code changes, and that we believe the code is ready for\
general usage (based on bug inflow).

**For a description of** [**MariaDB 5.5**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **see the**[**What is MariaDB 5.5**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) **page.**

For a list of changes made in [MariaDB 5.5.24](mariadb-5524-release-notes.md), with links to detailed\
information on each push, see the[MariaDB 5.5.24 Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5524-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Includes [MariaDB 5.3.7](../release-notes-mariadb-5-3-series/mariadb-537-release-notes.md) and MySQL 5.5.24

[MariaDB 5.5.24](mariadb-5524-release-notes.md) includes [MariaDB 5.3.7](../release-notes-mariadb-5-3-series/mariadb-537-release-notes.md) and MySQL 5.5.24. See the [MariaDB 5.3.7](../release-notes-mariadb-5-3-series/mariadb-537-release-notes.md)[Release Notes](../release-notes-mariadb-5-3-series/mariadb-537-release-notes.md) and[Changelog](../../../changelogs/changelogs-mariadb-53-series/mariadb-537-changelog.md) for more information on the changes in[MariaDB 5.3.7](../release-notes-mariadb-5-3-series/mariadb-537-release-notes.md). See[Changes in MySQL 5.5.24](https://dev.mysql.com/doc/refman/5.5/en/news-5-5-24.html)\
for what changed between this and previous MySQL versions.

## Security Fixes

This release includes fixes for the following security vulnerabilities:

* [CVE-2012-1735](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1735)
* [CVE-2012-0540](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0540)
* [CVE-2012-1757](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1757)
* [CVE-2012-1756](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1756)
* [CVE-2012-1734](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1734)

## RPM packages and YUM repositories

[MariaDB 5.5.24](mariadb-5524-release-notes.md) introduces new RPM packages and YUM repositories for RedHat,\
Fedora, and CentOS.

To get started with the repositories, head over to the[Installing MariaDB with yum](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/rpm/yum) page. We've also\
updated our[repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/)\
so that you can easily generate a custom MariaDB.repo for your distribution.

If you don't want to use yum you can, of course, still[download and install the MariaDB rpm files manually](https://kb.askmonty.org/en/installing-mariadb-with-the-rpm-tool/).

Lastly, we've created a page describing[what is included in each RPM file](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/rpm/about-the-mariadb-rpm-files), so you can\
easily determine which of the rpm packages you need or want.

This is our first attempt at providing YUM repositories for MariaDB, so please[let us know](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) if you run into\
any issues.

## Ubuntu 12.04 "Precise"

The MariaDB APT repositories have been updated to include packages for Ubuntu 12.04 Precise Pangolin. The [Installing MariaDB .deb Files](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/installing-mariadb-deb-files) page has instructions on how to set up the repository.

If you've previously added MariaDB to your sources.list, use our [repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/) to generate an updated entry for Ubuntu "Precise".

## BSD 9 and MacOS X Binaries

[MariaDB 5.5.24](mariadb-5524-release-notes.md) also includes binaries for BSD 9 and MacOS X 10.5. As with the new\
RPM packages, this is our first attempt at providing packages for these operating\
systems. So please[let us know](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/broken-reference/README.md) if you run into\
any issues.

Thanks, and enjoy MariaDB!

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
