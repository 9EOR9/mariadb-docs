# MariaDB 10.3.16 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.16/)[Release Notes](mariadb-10316-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-10316-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 17 Jun 2019

[MariaDB 10.3](what-is-mariadb-103.md) is an evolution of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features\
not found anywhere else and with backported and reimplemented features from\
MySQL.

[MariaDB 10.3.16](mariadb-10316-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-13992](https://jira.mariadb.org/browse/MDEV-13992): [JSON\_MERGE\_PATCH](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_merge_patch) and [JSON\_MERGE\_PRESERVE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_merge_preserve)
* [MDEV-19490](https://jira.mariadb.org/browse/MDEV-19490): show tables fails when selecting the information\_schema database
* [MDEV-19491](https://jira.mariadb.org/browse/MDEV-19491): multi-update with triggers and stored routines
* [MDEV-19541](https://jira.mariadb.org/browse/MDEV-19541): InnoDB crashes when trying to recover a corrupted page
* [MDEV-19725](https://jira.mariadb.org/browse/MDEV-19725): Incorrect error handling in ALTER TABLE
* [MDEV-19445](https://jira.mariadb.org/browse/MDEV-19445): FULLTEXT INDEX fix
* [MDEV-19486](https://jira.mariadb.org/browse/MDEV-19486): System Versioning fix
* [MDEV-19509](https://jira.mariadb.org/browse/MDEV-19509): InnoDB skips the tablespace in rotation list
* [MDEV-19614](https://jira.mariadb.org/browse/MDEV-19614): SET GLOBAL innodb\_ deadlock due to LOCK\_global\_system\_variables
* [MDEV-17458](https://jira.mariadb.org/browse/MDEV-17458): Unable to start galera node
* [MDEV-17456](https://jira.mariadb.org/browse/MDEV-17456): Malicious SUPER user can possibly change audit log configuration without leaving traces
* [MDEV-19588](https://jira.mariadb.org/browse/MDEV-19588): Wrong results from query, using left join
* [MDEV-19258](https://jira.mariadb.org/browse/MDEV-19258): RIGHT JOIN hangs in MariaDB
* Virtual columns fixes: [MDEV-19027](https://jira.mariadb.org/browse/MDEV-19027), [MDEV-19602](https://jira.mariadb.org/browse/MDEV-19602)
* Crash recovery fixes: [MDEV-13080](https://jira.mariadb.org/browse/MDEV-13080), [MDEV-19587](https://jira.mariadb.org/browse/MDEV-19587), [MDEV-19435](https://jira.mariadb.org/browse/MDEV-19435)
* [MDEV-11094](https://jira.mariadb.org/browse/MDEV-11094): Fixed row-based event applying with an error anymore when the events aim at the blackhole engine and row annotation is enabled
* [MDEV-19076](https://jira.mariadb.org/browse/MDEV-19076): Fixed slave\_parallel\_mode=optimistic did not always properly order replication events on temporary tables in some case to attempt execution before a parent event has been already processed
* [MDEV-19158](https://jira.mariadb.org/browse/MDEV-19158): Fixed duplicated entries in binlog occurred in combination of LOCK TABLES and binlog\_format=MIXED when a being locked table was under replication unsafe operation
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.3](what-is-mariadb-103.md) for OpenSUSE 42.3
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.16](mariadb-10316-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-10316-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.16](mariadb-10316-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-3-16-and-mariadb-10-2-25-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
