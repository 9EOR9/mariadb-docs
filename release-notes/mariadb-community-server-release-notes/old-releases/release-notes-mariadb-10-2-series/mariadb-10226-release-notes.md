# MariaDB 10.2.26 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.26/)[Release Notes](mariadb-10226-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10226-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 31 Jul 2019

[MariaDB 10.2](what-is-mariadb-102.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.26](mariadb-10226-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-19922](https://jira.mariadb.org/browse/MDEV-19922): [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 10.2
* [MDEV-19795](https://jira.mariadb.org/browse/MDEV-19795): Merge upstream [MyRocks](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/myrocks).
* [MDEV-17228](https://jira.mariadb.org/browse/MDEV-17228): Encrypted temporary tables are not encrypted.
* [MDEV-18328](https://jira.mariadb.org/browse/MDEV-18328): [Disks Plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/disks-plugin) is now stable and requires the [FILE privilege](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant).
* Merge relevant InnoDB changes from MySQL 5.7.27
* [MDEV-20102](https://jira.mariadb.org/browse/MDEV-20102): When the ctas from a big table is interrupted ,then you can't drop or recreate the table
* [MDEV-19292](https://jira.mariadb.org/browse/MDEV-19292): InnoDB's row size calculations were fixed, which might result in "Row size too large" errors when creating or altering tables with lots columns. This can occur even if previous MariaDB releases did not throw errors for the same tables. Some workarounds are listed at [InnoDB Row Formats Overview: Upgrading Causes Row Size Too Large Errors](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-row-formats/innodb-row-formats-overview#upgrading-causes-row-size-too-large-errors).
* ALTER TABLE: [MDEV-15641](https://jira.mariadb.org/browse/MDEV-15641)
* Indexed virtual columns: [MDEV-16222](https://jira.mariadb.org/browse/MDEV-16222), [MDEV-17005](https://jira.mariadb.org/browse/MDEV-17005)
* FULLTEXT INDEX: [MDEV-14154](https://jira.mariadb.org/browse/MDEV-14154)
* Encryption: [MDEV-17228](https://jira.mariadb.org/browse/MDEV-17228), [MDEV-19914](https://jira.mariadb.org/browse/MDEV-19914)
* Galera + FOREIGN KEY: [MDEV-19660](https://jira.mariadb.org/browse/MDEV-19660)
* Recovery & Mariabackup: [MDEV-19978](https://jira.mariadb.org/browse/MDEV-19978)
* [MDEV-19871](https://jira.mariadb.org/browse/MDEV-19871): Add page id matching check in innochecksum tool
* [MDEV-20091](https://jira.mariadb.org/browse/MDEV-20091): DROP TEMPORARY table is logged despite no CREATE was logged
* [MDEV-19421](https://jira.mariadb.org/browse/MDEV-19421): Basic 3-way join queries are not parsed - parsing problem of joins fixed
* [MDEV-19427](https://jira.mariadb.org/browse/MDEV-19427): mysql\_upgrade\_service throws exception upgrading from 10.0 to 10.3
* [MDEV-18661](https://jira.mariadb.org/browse/MDEV-18661): loading the audit plugin causes performance regression
* [MDEV-19771](https://jira.mariadb.org/browse/MDEV-19771): REPLACE on table with virtual\_field can cause crash
* [MDEV-19595](https://jira.mariadb.org/browse/MDEV-19595): fix Aria ER\_CRASHED\_ON\_USAGE and Assertion
* [MDEV-18328](https://jira.mariadb.org/browse/MDEV-18328): Make DISKS plugin check some privilege to access information\_schema.DISKS table
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.2](what-is-mariadb-102.md) for Ubuntu 18.10 "Cosmic"
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2019-2805](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2805)
  * [CVE-2019-2740](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2740)
  * [CVE-2019-2739](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2739)
  * [CVE-2019-2737](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2737)
  * [CVE-2019-2758](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2758)
  * [CVE-2020-2922](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2922)
  * [CVE-2021-2007](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2007)

Upgrading from 10.2 versions earlier than 10.2.17 is **highly recommended**\
for all [**Galera**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability\
issues with earlier versions. See the bug issue page for more information.\
When upgrading from [MariaDB 10.2.16](mariadb-10216-release-notes.md) or earlier to [MariaDB 10.2.17](mariadb-10217-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in [MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.2.26](mariadb-10226-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10226-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.26](mariadb-10226-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-7-10-3-17-10-2-26-10-1-41-and-5-5-65-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
