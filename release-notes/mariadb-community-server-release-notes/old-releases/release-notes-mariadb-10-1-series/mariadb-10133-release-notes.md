# MariaDB 10.1.33 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.33)[Release Notes](mariadb-10133-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10133-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 9 May 2018

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is the previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.33](mariadb-10133-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [PCRE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/regular-expressions-functions/pcre) updated to 8.42
* The embedded server library now supports SSL when connecting to remote servers.
* ALTER TABLE fixes: [MDEV-14693](https://jira.mariadb.org/browse/MDEV-14693), [MDEV-16080](https://jira.mariadb.org/browse/MDEV-16080), [MDEV-15937](https://jira.mariadb.org/browse/MDEV-15937)
* encryption fixes: [MDEV-15937](https://jira.mariadb.org/browse/MDEV-15937), [MDEV-16092](https://jira.mariadb.org/browse/MDEV-16092), [MDEV-15752](https://jira.mariadb.org/browse/MDEV-15752), [MDEV-15566](https://jira.mariadb.org/browse/MDEV-15566)
* systemd and shutdown fixes: [MDEV-14705](https://jira.mariadb.org/browse/MDEV-14705)
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be\
  the last release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) for Debian 7 Wheezy
* In this release experimental Ubuntu 18.04 "bionic" packages are present in the [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) repository. However, because Ubuntu includes [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) in its main repositories we recommend using the Ubuntu provided [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) packages for general use.

### Security Fixes

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-2755](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2755)
  * [CVE-2018-2761](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2761)
  * [CVE-2018-2766](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2766)
  * [CVE-2018-2767](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2767)
  * [CVE-2018-2771](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2771)
  * [CVE-2018-2781](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2781)
  * [CVE-2018-2782](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2782)
  * [CVE-2018-2784](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2784)
  * [CVE-2018-2787](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2787)
  * [CVE-2018-2813](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2813)
  * [CVE-2018-2817](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2817)
  * [CVE-2018-2819](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2819)
  * [CVE-2018-3081](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3081)
  * [CVE-2019-2455](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2455)
  * [CVE-2020-14550](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14550)
  * [CVE-2021-2011](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2011)

## Notes

For a complete list of changes made in [MariaDB 10.1.33](mariadb-10133-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10133-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.1.33](mariadb-10133-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-1-33-and-mariadb-galera-cluster-10-0-35-now-available/).

A file format compatibility bug that was introduced in [MariaDB 10.1.0](mariadb-10-1-0-release-notes.md) was fixed in [MariaDB 10.1.21](mariadb-10121-release-notes.md).\
Using [page\_compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression) or non-default [innodb\_page\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) created files that were incompatible with [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) or MySQL 5.6. [MariaDB 10.1.21](mariadb-10121-release-notes.md) and higher will convert affected files from earlier [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) releases to a compatible format.**This prevents a downgrade to earlier** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **versions.**[See the commit for details.](https://github.com/MariaDB/server/commit/ab1e6fefd869242d962cb91a006f37bb9ad534a7)

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
