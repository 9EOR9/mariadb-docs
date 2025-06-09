# MariaDB 10.2.15 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.15)[Release Notes](mariadb-10215-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10215-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 17 May 2018

[MariaDB 10.2](what-is-mariadb-102.md) is the current stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.15](mariadb-10215-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) updated to 5.7.22
* [PCRE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/regular-expressions-functions/pcre) updated to 8.42
* The embedded server library now supports SSL when connecting to remote servers
* [MDEV-15325](https://jira.mariadb.org/browse/MDEV-15325) - Incomplete validation of missing tablespace during recovery
* [MDEV-15720](https://jira.mariadb.org/browse/MDEV-15720) - ib\_buffer\_pool unnecessarily includes the temporary tablespace
* [MDEV-15764](https://jira.mariadb.org/browse/MDEV-15764) - InnoDB may write uninitialized garbage to redo log
* [MDEV-15553](https://jira.mariadb.org/browse/MDEV-15553) - Virtual Columns: Assertion failed in dict\_table\_get\_col\_name
* [MDEV-14705](https://jira.mariadb.org/browse/MDEV-14705) - slow innodb startup/shutdown can exceed systemd timeout
* [MDEV-15707](https://jira.mariadb.org/browse/MDEV-15707) - deadlock in Innodb IO code, caused by change buffering (Windows)
* [MDEV-15507](https://jira.mariadb.org/browse/MDEV-15507) - Assertion failed in dict\_check\_sys\_tables on upgrade from 5.5
* [MDEV-15916](https://jira.mariadb.org/browse/MDEV-15916) - Change buffer crash during TRUNCATE or DROP TABLE
* encryption fixes - [MDEV-12632](https://jira.mariadb.org/browse/MDEV-12632), [MDEV-13516](https://jira.mariadb.org/browse/MDEV-13516), [MDEV-15752](https://jira.mariadb.org/browse/MDEV-15752), [MDEV-15566](https://jira.mariadb.org/browse/MDEV-15566), [MDEV-16092](https://jira.mariadb.org/browse/MDEV-16092)
* temporary table ROLLBACK fixes - [MDEV-15826](https://jira.mariadb.org/browse/MDEV-15826), [MDEV-15374](https://jira.mariadb.org/browse/MDEV-15374)
* applicable changes from 5.7.22 - [MDEV-16142](https://jira.mariadb.org/browse/MDEV-16142)
* Ubuntu 18.04 "bionic" and Fedora 28 packages and repositories are being introduced in this release. See the [MariaDB Repository Configuration Tool](https://downloads.mariadb.org/mariadb/repositories/) for instructions on setting up these repositories.
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.2](what-is-mariadb-102.md) for Debian 7 Wheezy and Fedora 26
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-2755](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2755)
  * [CVE-2018-2759](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2759)
  * [CVE-2018-2761](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2761)
  * [CVE-2018-2766](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2766)
  * [CVE-2018-2767](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2767)
  * [CVE-2018-2771](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2771)
  * [CVE-2018-2777](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2777)
  * [CVE-2018-2781](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2781)
  * [CVE-2018-2782](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2782)
  * [CVE-2018-2784](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2784)
  * [CVE-2018-2786](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2786)
  * [CVE-2018-2787](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2787)
  * [CVE-2018-2810](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2810)
  * [CVE-2018-2813](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2813)
  * [CVE-2018-2817](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2817)
  * [CVE-2018-2819](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2819)
  * [CVE-2018-3081](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3081)
  * [CVE-2019-2455](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2455)
  * [CVE-2020-14550](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14550)
  * [CVE-2021-2011](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2011)

## Notes

For a complete list of changes made in [MariaDB 10.2.15](mariadb-10215-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10215-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.15](mariadb-10215-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-2-15-and-mariadb-connector-j-2-2-4-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
