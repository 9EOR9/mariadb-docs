# MariaDB 10.2.21 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.21/)[Release Notes](mariadb-10221-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10221-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 2 Jan 2019

[MariaDB 10.2](what-is-mariadb-102.md) is the previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.21](mariadb-10221-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Upgrading from earlier 10.2.x versions is **highly recommended** for all **Galera** users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability issues with earlier versions. See the bug issue page for more information.

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-17589](https://jira.mariadb.org/browse/MDEV-17589) - Stack-buffer-overflow with indexed varchar (utf8) field
* [MDEV-16987](https://jira.mariadb.org/browse/MDEV-16987) - [ALTER DATABASE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-database) possible in read-only mode (forbid ALTER DATABASE in read\_only)
* [MDEV-17720](https://jira.mariadb.org/browse/MDEV-17720) - [slave\_ddl\_exec\_mode=IDEMPOTENT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#slave_ddl_exec_mode) does not handle [DROP DATABASE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/drop/drop-database)
* [MDEV-6453](https://jira.mariadb.org/browse/MDEV-6453) - Assertion \`inited==NONE || (inited==RND && scan)' failed in handler::ha\_rnd\_init(bool) with InnoDB, joins, AND/OR conditions
* [MDEV-18105](https://jira.mariadb.org/browse/MDEV-18105) - [mariadb-backup](broken-reference) fails to copy encrypted InnoDB system tablespace if LSN>4G
* [MDEV-18041](https://jira.mariadb.org/browse/MDEV-18041) - Database corruption after renaming a prefix-indexed column
* [MDEV-17470](https://jira.mariadb.org/browse/MDEV-17470) - Orphan temporary files after interrupted [ALTER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table) cause InnoDB: Operating system error number 17 and eventual fatal error 71
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

When upgrading from [MariaDB 10.2.16](mariadb-10216-release-notes.md) or earlier to [MariaDB 10.2.17](mariadb-10217-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.2.21](mariadb-10221-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10221-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.21](mariadb-10221-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-2-21-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
