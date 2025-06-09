# MariaDB 5.5.29 Release Notes

The most recent release in the [MariaDB 5.5](broken-reference) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.29) | **Release Notes** | [Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5529-changelog.md) |[Overview of 5.5](broken-reference)

**Release date:** 30 Jan 2013

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release. In general this\
means that there are no known serious bugs, except for those marked as feature\
requests, that no bugs were fixed since last release that caused a notable code\
changes, and that we believe the code is ready for general usage (based on bug\
inflow).

**For a description of** [**MariaDB 5.5**](broken-reference) **see the**[**What is MariaDB 5.5**](broken-reference) **page.**

For a list of changes made in this release, with links to detailed\
information on each push, see the[MariaDB 5.5.29 Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5529-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

This release is primarily a bug-fix release.

## Important Security Fixes

This release includes fixes for the following security vulnerabilities:

* A buffer overflow that can cause a server crash or arbitrary code execution (a variant of [CVE-2012-5611](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5611))
* [CVE-2012-5627](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5627)/[MDEV-3915](https://jira.mariadb.org/browse/MDEV-3915) fast password brute-forcing using the "change user" command
* [CVE-2012-5615](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5615)/[MDEV-3909](https://jira.mariadb.org/browse/MDEV-3909) information leakage about existing user accounts via the protocol handshake
* fixes for DoS attacks - crashes and server lockups (see the [Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5529-changelog.md))

Additionally, it includes all security fixes from MySQL 5.5.29, such as fix for [CVE-2012-5612](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5612)/[MDEV-3908](https://jira.mariadb.org/browse/MDEV-3908) and others such as:

* [CVE-2013-1531](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1531)
* [CVE-2013-0384](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0384)
* [CVE-2013-0389](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0389)
* [CVE-2013-0386](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0386)
* [CVE-2013-0385](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0385)
* [CVE-2012-1702](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1702)
* [CVE-2013-0383](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0383)
* [CVE-2013-0368](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0368)
* [CVE-2012-0572](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0572)
* [CVE-2013-0371](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0371)
* [CVE-2012-0574](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0574)
* [CVE-2012-1705](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-1705)
* [CVE-2012-0578](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-0578)
* [CVE-2013-0367](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-0367)
* [CVE-2012-5096](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-5096)

## Includes [MariaDB 5.3.12](../release-notes-mariadb-5-3-series/mariadb-5312-release-notes.md) and MySQL 5.5.29

This release includes [MariaDB 5.3.12](../release-notes-mariadb-5-3-series/mariadb-5312-release-notes.md) and MySQL 5.5.29. See[Changes in MySQL 5.5.29](https://dev.mysql.com/doc/relnotes/mysql/5.5/en/news-5-5-29.html)\
for what changed in MySQL.

## Fedora 18 and Ubuntu 12.10 Packages

This version of MariaDB includes packages for Fedora 18 "Spherical Cow" and Ubuntu 12.10 "Quantal". Visit the [Repository Configurator](https://downloads.mariadb.org/mariadb/repositories/) to generate the necessary commands to install MariaDB on these distributions.

## Discontinued builds

The MariaDB project tries to support as many different Operating Systems and\
Linux Distributions as we can. However, when a distribution or OS stops\
receiving security and other updates it becomes difficult to freely provide\
packages for that platform. In such cases, our policy is to deprecate that\
platform and stop providing binary packages for it.

As of 1 Feb 2013, we will stop building packages for the following:

* Fedora 16 "Verne"
* Debian 5 "Lenny"
* Ubuntu 10.10 "Maverick"
* Ubuntu 11.04 "Natty"

If your chosen Linux Distribution or Operating System is deprecated, packages\
or support are not completely unavailable. Companies such as[SkySQL](https://skysql.com) and [Monty Program](https://montyprogram.com)\
(and others) provide support for all versions of MariaDB back to even very old\
MySQL versions. This includes packaged binaries. Contact them for more details.

More information on our deprecation policy can be found at:

## Archived Releases

From the beginning of the MariaDB project in 2009 we've kept all of our old\
releases online via our network of mirrors. Doing this is great for those few\
who are interested in old releases, but the disk space required to host all of\
our old releases is over 130 Gigabytes at present and grows by several\
gigabytes with each new release. This is too much for some of our mirrors to\
handle. So, starting with this release our primary mirror will only host the\
most recent three or four releases in each series (5.5, 10.0, and so on).\
Mirrors are, of course, free to keep archiving every release, but the primary\
mirror that they pull from will not.

Old releases do have value, so for those that are interested in old releases,\
we are setting up a simple, no frills, archive server which will host them.\
Once the server is up and running, links to archived releases on[downloads.mariadb.org](https://downloads.mariadb.org) will point at the archive server. During the\
transition period, links to some old releases may disappear for a short time,\
but don't worry, they haven't been deleted, they're just being moved!

Thanks, and enjoy MariaDB!

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
