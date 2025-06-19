# MariaDB 10.3.15 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.15/)[Release Notes](mariadb-10315-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-10315-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 14 May 2019

[MariaDB 10.3](what-is-mariadb-103.md) is an evolution of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features\
not found anywhere else and with backported and reimplemented features from\
MySQL.

[MariaDB 10.3.15](mariadb-10315-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

### General server

* [MDEV-17894](https://jira.mariadb.org/browse/MDEV-17894) - Assertion \`\`(thd->lex)->current\_select'`failed in`MYSQLparse()`, query with` VALUES()\`
* [MDEV-18968](https://jira.mariadb.org/browse/MDEV-18968) - Both `(WHERE 0.1)` and `(WHERE NOT 0.1)` return empty set
* [MDEV-18466](https://jira.mariadb.org/browse/MDEV-18466) - Unsafe to log updates on tables referenced by foreign keys with triggers in statement format
* [MDEV-18899](https://jira.mariadb.org/browse/MDEV-18899) - Server crashes in `Field::set_warning_truncated_wrong_value`
* [MDEV-18298](https://jira.mariadb.org/browse/MDEV-18298) - Crashes server with segfault during role grants
* [MDEV-17610](https://jira.mariadb.org/browse/MDEV-17610) - Unexpected connection abort after certain operations from within stored procedure
* [MDEV-19112](https://jira.mariadb.org/browse/MDEV-19112) - WITH clause does not work with information\_schema as default database
* [MDEV-17830](https://jira.mariadb.org/browse/MDEV-17830) - Server crashes in `Item_null_result::field_type` upon `SELECT with CHARSET(date)` and `ROLLUP`
* [MDEV-14041](https://jira.mariadb.org/browse/MDEV-14041) - Server crashes in `String::length` on queries with functions and `ROLLUP`
* [MDEV-18920](https://jira.mariadb.org/browse/MDEV-18920) - Prepared statements with `st_convexhull` hang and eat 100% cpu.
* [MDEV-15837](https://jira.mariadb.org/browse/MDEV-15837) - Assertion `item1->type() == Item::FIELD_ITEM && item2->type() == Item::FIELD_ITEM`
* [MDEV-9531](https://jira.mariadb.org/browse/MDEV-9531) - GROUP\_CONCAT with ORDER BY inside takes a lot of memory while it's executed
* [MDEV-17036](https://jira.mariadb.org/browse/MDEV-17036) - BULK with replace doesn't take the first parameter in account
* Bug#28986737 - RENAMING AND REPLACING MYSQL.USER TABLE CAN LEAD TO A SERVER CRASH
* [MDEV-19350](https://jira.mariadb.org/browse/MDEV-19350) - Server crashes in `delete_tree_element / ... / Item_func_group_concat::repack_tree`
* [MDEV-19188](https://jira.mariadb.org/browse/MDEV-19188) - Server Crash When Using a Trigger With A Number of Virtual Columns on INSERT/UPDATE
* [MDEV-19352](https://jira.mariadb.org/browse/MDEV-19352) - Server crash in `alloc_histograms_for_table_share` upon query from information schema

### InnoDB

* Merge InnoDB changes from MySQL 5.6.44 and 5.7.26
* Fixes of corruption or crashes: [MDEV-19241](https://jira.mariadb.org/browse/MDEV-19241), [MDEV-13942](https://jira.mariadb.org/browse/MDEV-13942), [MDEV-19385](https://jira.mariadb.org/browse/MDEV-19385), [MDEV-16060](https://jira.mariadb.org/browse/MDEV-16060), [MDEV-18220](https://jira.mariadb.org/browse/MDEV-18220), [MDEV-17540](https://jira.mariadb.org/browse/MDEV-17540)
* InnoDB recovery fixes and speedup: [MDEV-18733](https://jira.mariadb.org/browse/MDEV-18733), [MDEV-12699](https://jira.mariadb.org/browse/MDEV-12699), [MDEV-19356](https://jira.mariadb.org/browse/MDEV-19356)

### Encryption

* [MDEV-14398](https://jira.mariadb.org/browse/MDEV-14398) - `innodb_encrypt_tables` will work even with `innodb_encryption_rotate_key_age=0`

### Protocol

* [MDEV-17036](https://jira.mariadb.org/browse/MDEV-17036) - BULK with replace doesn't take the first parameter in account

### Replication

* [MDEV-14784](https://jira.mariadb.org/browse/MDEV-14784) - Slave crashes in show\_status\_array upon running a trigger with select from I\_S

### mariadb-backup

* [MDEV-19060](https://jira.mariadb.org/browse/MDEV-19060) - mariabackup continues, despite failing to open a tablespace

### Packaging & Misc

* [MDEV-19054](https://jira.mariadb.org/browse/MDEV-19054) - `mysql_upgrade_service` now allows MySQL 5.7 to [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) upgrade
* Starting with this release, we are now providing [src.rpm packages](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/compiling-mariadb-from-source/building-mariadb-from-a-source-rpm) for [some platforms](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/rpm/why-source-rpms-srpms-arent-packaged-for-some-platforms) ([MDEV-7066](https://jira.mariadb.org/browse/MDEV-7066))
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be\
  the last release of [MariaDB 10.3](what-is-mariadb-103.md) for Fedora 28

### Security

* [MDEV-18686](https://jira.mariadb.org/browse/MDEV-18686) - Add option to PAM authentication plugin to allow case insensitive username matching
* bugfix - multi-update checked privileges on views incorrectly (commit 5057d4637525eadad438d25ee6a4870a4e6b384c)
* [MDEV-19276](https://jira.mariadb.org/browse/MDEV-19276) - during connect, write error log warning for `ER_DBACCESS_DENIED_ERROR`, if `log_warnings > 1`
* [MDEV-17456](https://jira.mariadb.org/browse/MDEV-17456) - Malicious SUPER user can possibly change audit log configuration without leaving traces.
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2019-2614](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2614)
  * [CVE-2019-2627](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2627)
  * [CVE-2019-2628](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-2628)

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running `[mysql_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade)` is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.15](mariadb-10315-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-10315-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.15](mariadb-10315-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-3-15-mariadb-connector-c-3-0-10-mariadb-connector-node-js-2-0-5-and-mariadb-connector-odbc-3-1-1-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
