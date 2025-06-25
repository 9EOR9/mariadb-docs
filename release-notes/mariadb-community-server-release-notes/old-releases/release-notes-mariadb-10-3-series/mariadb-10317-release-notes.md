# MariaDB 10.3.17 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.17/)[Release Notes](mariadb-10317-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10317-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 31 Jul 2019

[MariaDB 10.3](what-is-mariadb-103.md) is the previous stable series of MariaDB, and an evolution of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features\
not found anywhere else and with backported and reimplemented features from\
MySQL.

[MariaDB 10.3.17](mariadb-10317-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-19922](https://jira.mariadb.org/browse/MDEV-19922): [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 10.2
* [MDEV-19795](https://jira.mariadb.org/browse/MDEV-19795): Merge upstream [MyRocks](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/myrocks).
* [MDEV-17228](https://jira.mariadb.org/browse/MDEV-17228): Encrypted temporary tables are not encrypted.
* [MDEV-18328](https://jira.mariadb.org/browse/MDEV-18328): [Disks Plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/disks-plugin) is now stable and requires the [FILE privilege](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant).
* Merge relevant InnoDB changes from MySQL 5.7.27
* Adjust spin loops to the x86 PAUSE instruction latency ([MDEV-19845](https://jira.mariadb.org/browse/MDEV-19845))
* [MDEV-20102](https://jira.mariadb.org/browse/MDEV-20102): When the ctas from a big table is interrupted ,then you can't drop or recreate the table
* [MDEV-19292](https://jira.mariadb.org/browse/MDEV-19292): InnoDB's row size calculations were fixed, which might result in "Row size too large" errors when creating or altering tables with lots columns. This can occur even if previous MariaDB releases did not throw errors for the same tables. Some workarounds are listed at [InnoDB Row Formats Overview: Upgrading Causes Row Size Too Large Errors](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-row-formats/innodb-row-formats-overview#upgrading-causes-row-size-too-large-errors).
* ALTER TABLE: [MDEV-15641](https://jira.mariadb.org/browse/MDEV-15641), [MDEV-19630](https://jira.mariadb.org/browse/MDEV-19630), [MDEV-19916](https://jira.mariadb.org/browse/MDEV-19916), [MDEV-19974](https://jira.mariadb.org/browse/MDEV-19974)
* Indexed virtual columns: [MDEV-16222](https://jira.mariadb.org/browse/MDEV-16222), [MDEV-17005](https://jira.mariadb.org/browse/MDEV-17005), [MDEV-19870](https://jira.mariadb.org/browse/MDEV-19870)
* FULLTEXT INDEX: [MDEV-14154](https://jira.mariadb.org/browse/MDEV-14154)
* Encryption: [MDEV-17228](https://jira.mariadb.org/browse/MDEV-17228), [MDEV-19914](https://jira.mariadb.org/browse/MDEV-19914)
* Galera + FOREIGN KEY: [MDEV-19660](https://jira.mariadb.org/browse/MDEV-19660)
* Recovery & mariadb-backup: [MDEV-19978](https://jira.mariadb.org/browse/MDEV-19978)
* [MDEV-19871](https://jira.mariadb.org/browse/MDEV-19871): Add page id matching check in innochecksum tool
* [MDEV-20091](https://jira.mariadb.org/browse/MDEV-20091): DROP TEMPORARY table is logged despite no CREATE was logged
* [MDEV-19427](https://jira.mariadb.org/browse/MDEV-19427): mysql\_upgrade\_service throws exception upgrading from 10.0 to 10.3
* [MDEV-19814](https://jira.mariadb.org/browse/MDEV-19814): Server crash in row\_upd\_del\_mark\_clust\_rec or Assertion
* [MDEV-17363](https://jira.mariadb.org/browse/MDEV-17363): Compressed columns cannot be restored from dump
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.3](what-is-mariadb-103.md) for Ubuntu 18.10 "Cosmic"
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2019-2805](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2805)
  * [CVE-2019-2740](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2740)
  * [CVE-2019-2739](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2739)
  * [CVE-2019-2737](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2737)
  * [CVE-2019-2758](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2758)
  * [CVE-2020-2922](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2922)
  * [CVE-2021-2007](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2007)

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.17](mariadb-10317-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10317-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.17](mariadb-10317-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-7-10-3-17-10-2-26-10-1-41-and-5-5-65-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
