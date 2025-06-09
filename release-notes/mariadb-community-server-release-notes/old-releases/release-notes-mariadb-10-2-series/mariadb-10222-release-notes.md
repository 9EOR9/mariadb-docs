# MariaDB 10.2.22 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.22/)[Release Notes](mariadb-10222-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10222-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 11 Feb 2019

[MariaDB 10.2](what-is-mariadb-102.md) is the previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.22](mariadb-10222-release-notes.md) will be a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Upgrading from earlier 10.2.x versions is **highly recommended** for all **Galera** users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability issues with earlier versions. See the bug issue page for more information.

Thanks, and enjoy MariaDB!

## Notable Changes

* [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 9.5
* Backport [Information Schema CHECK\_CONSTRAINTS Table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-check_constraints-table).
* [MDEV-17475](https://jira.mariadb.org/browse/MDEV-17475): Maximum value of [table\_definition\_cache](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#table_definition_cache) is now `2097152`.
* InnoDB ALTER TABLE fixes:[MDEV-16499](https://jira.mariadb.org/browse/MDEV-16499), [MDEV-18186](https://jira.mariadb.org/browse/MDEV-18186), [MDEV-18237](https://jira.mariadb.org/browse/MDEV-18237), [MDEV-18222](https://jira.mariadb.org/browse/MDEV-18222), [MDEV-18256](https://jira.mariadb.org/browse/MDEV-18256), [MDEV-18016](https://jira.mariadb.org/browse/MDEV-18016), [MDEV-16849](https://jira.mariadb.org/browse/MDEV-16849)
* Mariabackup fixes: [MDEV-18185](https://jira.mariadb.org/browse/MDEV-18185), [MDEV-18201](https://jira.mariadb.org/browse/MDEV-18201), [MDEV-18194](https://jira.mariadb.org/browse/MDEV-18194)
* Galera crash recovery fix: [MDEV-15740](https://jira.mariadb.org/browse/MDEV-15740)
* Encryption fixes: [MDEV-18129](https://jira.mariadb.org/browse/MDEV-18129), [MDEV-18183](https://jira.mariadb.org/browse/MDEV-18183), [MDEV-18279](https://jira.mariadb.org/browse/MDEV-18279)
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2019-2510](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2510)
  * [CVE-2019-2537](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2537)

When upgrading from [MariaDB 10.2.16](mariadb-10216-release-notes.md) or earlier to [MariaDB 10.2.17](mariadb-10217-release-notes.md) or higher,\
running `[mysql_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade)` is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.2.22](mariadb-10222-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10222-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.22](mariadb-10222-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-2-22-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
