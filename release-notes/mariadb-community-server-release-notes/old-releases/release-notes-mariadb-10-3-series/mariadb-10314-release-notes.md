# MariaDB 10.3.14 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.14)[Release Notes](mariadb-10314-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-10314-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 2 Apr 2019

[MariaDB 10.3](what-is-mariadb-103.md) is an evolution of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features\
not found anywhere else and with backported and reimplemented features from\
MySQL.

[MariaDB 10.3.14](mariadb-10314-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* Repositories for CentOS 7, RHEL 7 & 8, Fedora 28 & 29, and SLES 12 & 15 now\
  include a src.rpm file that you can use to build MariaDB. Instructions for\
  doing so are found on the[Building MariaDB from a Source RPM](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/compiling-mariadb-from-source/building-mariadb-from-a-source-rpm)\
  page
* InnoDB corruption fixes: [MDEV-14126](https://jira.mariadb.org/browse/MDEV-14126), [MDEV-18272](https://jira.mariadb.org/browse/MDEV-18272), [MDEV-18879](https://jira.mariadb.org/browse/MDEV-18879), [MDEV-18972](https://jira.mariadb.org/browse/MDEV-18972), [MDEV-18981](https://jira.mariadb.org/browse/MDEV-18981)
* InnoDB purge performance fixes: [MDEV-18878](https://jira.mariadb.org/browse/MDEV-18878), [MDEV-18936](https://jira.mariadb.org/browse/MDEV-18936)
* InnoDB ALTER TABLE fixes: [MDEV-13818](https://jira.mariadb.org/browse/MDEV-13818), [MDEV-18775](https://jira.mariadb.org/browse/MDEV-18775), [MDEV-18732](https://jira.mariadb.org/browse/MDEV-18732), [MDEV-18749](https://jira.mariadb.org/browse/MDEV-18749), [MDEV-18637](https://jira.mariadb.org/browse/MDEV-18637), [MDEV-18869](https://jira.mariadb.org/browse/MDEV-18869)
* Galera fixes: [MDEV-9519](https://jira.mariadb.org/browse/MDEV-9519), [MDEV-18577](https://jira.mariadb.org/browse/MDEV-18577), [MDEV-17262](https://jira.mariadb.org/browse/MDEV-17262)
* Debug symbols on CentOS 7, RHEL 7, and SLES 12 distributions have been moved\
  into `debuginfo` packages ([MDEV-18893](https://jira.mariadb.org/browse/MDEV-18893))
* The [Galera library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) in the repositories has\
  been updated to version 25.3.26
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be\
  the last release of [MariaDB 10.3](what-is-mariadb-103.md) for Ubuntu 14.04 Trusty,\
  Debian has also stopped supporting the ppc64el architecture for Debian 8\
  Jessie and so this is the last release of [MariaDB 10.3](what-is-mariadb-103.md) on Jessie for that\
  architecture
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running `[mysql_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade)` is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.14](mariadb-10314-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-10314-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.14](mariadb-10314-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-3-14).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
