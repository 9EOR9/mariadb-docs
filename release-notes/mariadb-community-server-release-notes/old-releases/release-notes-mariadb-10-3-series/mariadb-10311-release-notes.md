# MariaDB 10.3.11 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.11/)[Release Notes](mariadb-10311-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10311-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 20 Nov 2018

[MariaDB 10.3](what-is-mariadb-103.md) is an evolution\
of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.3.11](mariadb-10311-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

Notable changes of this release include:

* [mysqldump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysqldump) now uses `utf8mb4` as a default [character set](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets), instead of `utf8`.
* [sql\_safe\_updates](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#sql_safe_updates) can now be set as a command-line and `my.cnf` option.
* Fixed crash on upgrade from [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) or earlier: [MDEV-12023](https://jira.mariadb.org/browse/MDEV-12023)
* [MDEV-17073](https://jira.mariadb.org/browse/MDEV-17073) - [INSERT…ON DUPLICATE KEY UPDATE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/inserting-loading-data/insert-on-duplicate-key-update) is now less deadlock-prone
* [MDEV-17289](https://jira.mariadb.org/browse/MDEV-17289) - Multi-pass recovery fails to apply some redo log records
* [MDEV-17541](https://jira.mariadb.org/browse/MDEV-17541) - [KILL QUERY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/kill) during lock wait in [FOREIGN KEY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-indexes/foreign-keys) check no longer causes hang
* [MDEV-17531](https://jira.mariadb.org/browse/MDEV-17531) - Fix crash in [RENAME TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/rename-table) with [FOREIGN KEY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-indexes/foreign-keys) and [FULLTEXT INDEX](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-indexes/full-text-indexes)
* [Spatial index](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/geometry/spatial-index) fixes: [MDEV-17545](https://jira.mariadb.org/browse/MDEV-17545), [MDEV-17546](https://jira.mariadb.org/browse/MDEV-17546)
* [Virtual column](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/generated-columns) fixes: [MDEV-17215](https://jira.mariadb.org/browse/MDEV-17215), [MDEV-17548](https://jira.mariadb.org/browse/MDEV-17548)
* [mariadb-backup](broken-reference) fixes:
  * [MDEV-13564](https://jira.mariadb.org/browse/MDEV-13564) - [TRUNCATE TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/truncate-table) now works with [mariadb-backup](broken-reference)
  * [MDEV-17433](https://jira.mariadb.org/browse/MDEV-17433) - Allow InnoDB start up with empty ib\_logfile0 from mariabackup --prepare
* Packages for Fedora 29 and Ubuntu 18.10 Cosmic have been added in this release
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be\
  the last release of [MariaDB 10.3](what-is-mariadb-103.md) for Fedora 27
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-3282](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3282)
  * [CVE-2016-9843](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-9843)
  * [CVE-2018-3174](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3174)
  * [CVE-2018-3143](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3143)
  * [CVE-2018-3156](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3156)
  * [CVE-2018-3251](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3251)
  * [CVE-2018-3185](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3185)
  * [CVE-2018-3277](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3277)
  * [CVE-2018-3162](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3162)
  * [CVE-2018-3173](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3173)
  * [CVE-2018-3200](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3200)
  * [CVE-2018-3284](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3284)

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.11](mariadb-10311-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10311-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.11](mariadb-10311-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-3-11-and-mariadb-connector-c-3-0-7-connector-odbc-3-0-7-and-connector-node-js-2-0-1-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
