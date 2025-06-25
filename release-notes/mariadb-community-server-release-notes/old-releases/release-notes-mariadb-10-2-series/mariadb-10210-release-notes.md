# MariaDB 10.2.10 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.10)[Release Notes](mariadb-10210-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10210-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 31 Oct 2017

[MariaDB 10.2](what-is-mariadb-102.md) is the current stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.10](mariadb-10210-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-versions) updated to 5.7.20
* [CONNECT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) updated to 1.6.0005
* [MariaDB Backup](broken-reference) now Stable (GA)
* [MDEV-14051](https://jira.mariadb.org/browse/MDEV-14051): 'Undo log record is too big.' error occurring in very narrow range of string lengths
* [MDEV-13918](https://jira.mariadb.org/browse/MDEV-13918): Race condition between [INFORMATION\_SCHEMA.INNODB\_SYS\_TABLESTATS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-innodb-tables/information-schema-innodb_sys_tablestats-table) and [ALTER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table)/[DROP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/drop/drop-table)/[TRUNCATE TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/truncate-table)
* [MDEV-13838](https://jira.mariadb.org/browse/MDEV-13838): Wrong result after altering a partitioned table
* fixed bugs in InnoDB [FULLTEXT INDEX](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-indexes/full-text-indexes)
  * [MDEV-12676](https://jira.mariadb.org/browse/MDEV-12676): InnoDB FTS duplicate key error
  * [MDEV-13051](https://jira.mariadb.org/browse/MDEV-13051): InnoDB crash after failed ADD INDEX and table\_definition\_cache eviction
  * [MDEV-13446](https://jira.mariadb.org/browse/MDEV-13446): fts\_create\_doc\_id() unnecessarily allocates 8 bytes for every inserted row
* [MDEV-13941](https://jira.mariadb.org/browse/MDEV-13941) Fix high NTFS fragmentation
* [MDEV-13512](https://jira.mariadb.org/browse/MDEV-13512) Fix corruption of SPATIAL INDEX in [ROW\_FORMAT=COMPRESSED](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-row-formats/innodb-row-formats-overview) tables
* [MDEV-14023](https://jira.mariadb.org/browse/MDEV-14023) 10.1 InnoDB tables with virtual columns cannot be accessed in 10.2
* [MDEV-11336](https://jira.mariadb.org/browse/MDEV-11336) [innodb\_defragment](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimizing-tables/defragmenting-innodb-tablespaces) was enabled
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2017-10378](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-10378), [MDEV-13819](https://jira.mariadb.org/browse/MDEV-13819)
  * [CVE-2017-10268](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-10268)
  * [CVE-2017-15365](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-15365)

## Notes

For a complete list of changes made in [MariaDB 10.2.10](mariadb-10210-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10210-changelog.md).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
