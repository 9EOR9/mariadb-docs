# MariaDB 5.5.41 Release Notes

The most recent release in the [MariaDB 5.5](broken-reference) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.mariadb.org/mariadb/5.5.41)[Release Notes](mariadb-5541-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5541-changelog.md)[Overview of 5.5](broken-reference)

**Release date:** 21 Dec 2014

This is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release. In general this\
means that there are no known serious bugs, except for those marked as feature\
requests, that no bugs were fixed since last release that caused notable code\
changes, and that we believe the code is ready for general usage (based on bug\
inflow).

**For a description of** [**MariaDB 5.5**](broken-reference) **see the**[**What is MariaDB 5.5?**](broken-reference) **page.**

For a list of changes made in this release, with links to detailed\
information on each push, see the[MariaDB 5.5.41 Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5541-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

### Updates & Bug Fixes

[MariaDB 5.5.41](mariadb-5541-release-notes.md) is a maintenance release. It includes several bugfixes and updates, including\
from MySQL 5.5.41. Notable updates include:

* This release includes two important bug fixes:
  * A fix to a serious bug in InnoDB and XtraDB that sometimes could cause a hard lock up of the server ([MDEV-7026](https://jira.mariadb.org/browse/MDEV-7026))
  * A fix to unnecessary waits in InnoDB and XtraDB ([MDEV-7100](https://jira.mariadb.org/browse/MDEV-7100))
* When compiled with OpenSSL, MariaDB now supports TLSv1.2 protocol. Limit it to TLSv1.2 ciphers only with `--ssl_cipher=TLSv1.2`. Limit it to SSLv3 ciphers with `--ssl-cipher=SSLv3`. RPM and DEB packages from [MariaDB.org](https://downloads.mariadb.org) are built with OpenSSL, others (for Windows and generic Linux) are built with yaSSL.
* [TokuDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/tokudb) updated to [version 7.5.3](https://docs.tokutek.com/tokudb/tokudb-release-notes.html#tokudb-7-5-3)
* We now offer openSUSE repos, see the [repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/)\
  for details on how to use it.
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2015-0411](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-0411)
  * [CVE-2015-0382](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-0382)
  * [CVE-2015-0381](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-0381)
  * [CVE-2015-0432](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-0432)
  * [CVE-2014-6568](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2014-6568)
  * [CVE-2015-0374](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-0374)

A full list of all changes is in the [changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5541-changelog.md).

Thanks, and enjoy MariaDB!

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.
