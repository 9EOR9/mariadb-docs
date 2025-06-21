# MariaDB 10.5.0 Release Notes

The most recent release of [MariaDB 10.5](what-is-mariadb-105.md) is:[**MariaDB 10.5.28**](mariadb-10-5-28-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.5.28/)

[Download](https://downloads.mariadb.org/mariadb/10.5.0/)[Release Notes](mariadb-1050-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-1050-changelog.md)[Overview of 10.5](what-is-mariadb-105.md)

**Release date:** 3 Dec 2019

[MariaDB 10.5](what-is-mariadb-105.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/mariadb-10-5-series/broken-reference/README.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.5.0](mariadb-1050-release-notes.md) is an [_**Alpha**_](../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

**For an overview of** [**MariaDB 10.5**](what-is-mariadb-105.md) **see the**[**What is MariaDB 10.5?**](what-is-mariadb-105.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the first alpha release in the [MariaDB 10.5](what-is-mariadb-105.md) series.

Notable changes of this release include:

### INET 6 Data Type

* New [INET6](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/inet6) data type for storing IPv6 addresses ([MDEV-274](https://jira.mariadb.org/browse/MDEV-274)).

### Syntax

* [INSERT ... RETURNING](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/inserting-loading-data/insertreturning) ([MDEV-10014](https://jira.mariadb.org/browse/MDEV-10014))
* [REPLACE ... RETURNING](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/replacereturning) ([MDEV-10014](https://jira.mariadb.org/browse/MDEV-10014))
* [EXCEPT ALL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/joins-subqueries/except#alldistinct) and [INTERSECT ALL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/joins-subqueries/intersect#alldistinct) ([MDEV-18844](https://jira.mariadb.org/browse/MDEV-18844))
* Database comments in [CREATE DATABASE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-database) and [ALTER DATABASE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-database) statements ([MDEV-307](https://jira.mariadb.org/browse/MDEV-307))
* Setup [default partitions for system versioning](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/system-versioned-tables) ([MDEV-19903](https://jira.mariadb.org/browse/MDEV-19903))
* Fix [REFERENCES constraint](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-indexes/foreign-keys) in column definition ([MDEV-20729](https://jira.mariadb.org/browse/MDEV-20729))

### JSON

* [JSON\_ARRAYAGG](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_arrayagg)
* [JSON\_OBJECTAGG](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_objectagg)
* Add information about packed addon fields in [ANALYZE FORMAT=JSON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/analyze-and-explain-statements/analyze-format-json) ([MDEV-21838](https://jira.mariadb.org/browse/MDEV-21838))

### S3 Storage Engine

* [S3 Storage Engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/s3-storage-engine), a read-only storage engine that stores its data in Amazon S3 ([MDEV-17841](https://jira.mariadb.org/browse/MDEV-17841))

### Thread Pool

* Information Schema tables ([THREADPOOL\_GROUPS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-thread_pool_groups-table), [THREADPOOL\_QUEUES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-thread_pool_queues-table) and [THREADPOOL\_STATS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-thread_pool_stats-table)) for internals of generic threadpool ([MDEV-19313](https://jira.mariadb.org/browse/MDEV-19313))

### InnoDB

* [innodb\_adaptive\_hash\_index](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_adaptive_hash_index) now defaults to `OFF` ([MDEV-20487](https://jira.mariadb.org/browse/MDEV-20487))
* [innodb\_checksum\_algorithm](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_checksum_algorithm) now defaults to `full_crc32` ([MDEV-19534](https://jira.mariadb.org/browse/MDEV-19534))
* [innodb\_checksums](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_checksums) has been removed ([MDEV-19534](https://jira.mariadb.org/browse/MDEV-19534))
* [innodb\_log\_checksums](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_log_checksums) has been deprecated ([MDEV-19543](https://jira.mariadb.org/browse/MDEV-19543))
* [innodb\_locks\_unsafe\_for\_binlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_locks_unsafe_for_binlog) has been removed ([MDEV-19544](https://jira.mariadb.org/browse/MDEV-19544))
* [innodb\_stats\_sample\_pages](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_stats_sample_pages) has been removed ([MDEV-19551](https://jira.mariadb.org/browse/MDEV-19551))
* [innodb\_undo\_logs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_undo_logs) has been deprecated ([MDEV-19570](https://jira.mariadb.org/browse/MDEV-19570))
* [innodb\_rollback\_segments](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_rollback_segments) has been removed ([MDEV-19570](https://jira.mariadb.org/browse/MDEV-19570))
* Set [innodb\_log\_files\_in\_group=1](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_log_files_in_group) by default ([MDEV-20907](https://jira.mariadb.org/browse/MDEV-20907))
* Extend [SHOW STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-status) LIKE 'Innodb\_%' ([MDEV-18582](https://jira.mariadb.org/browse/MDEV-18582))
* Clean up [INFORMATION\_SCHEMA.INNODB\_](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-innodb-tables) tables ([MDEV-19940](https://jira.mariadb.org/browse/MDEV-19940))
* Doublewrite buffer is unnecessarily used for newly (re)initialized pages ([MDEV-19738](https://jira.mariadb.org/browse/MDEV-19738))
* Defer change buffer merge until pages are requested ([MDEV-19514](https://jira.mariadb.org/browse/MDEV-19514))

#### InnoDB Refactoring

* Remove buf\_page\_t::newest\_modification ([MDEV-21132](https://jira.mariadb.org/browse/MDEV-21132))
* Replace recv\_sys\_t::addr\_hash with a std::map ([MDEV-19586](https://jira.mariadb.org/browse/MDEV-19586))
* Obsolete internal parser for FK in InnoDB ([MDEV-20480](https://jira.mariadb.org/browse/MDEV-20480))
* InnoDB thread pool for background tasks ([MDEV-16264](https://jira.mariadb.org/browse/MDEV-16264))

### Binary Log

* Extended [binlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log) metadata ([MDEV-20477](https://jira.mariadb.org/browse/MDEV-20477))

### Query Optimizer

* [ANALYZE for statements](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/analyze-and-explain-statements/analyze-statement) is improved, now it also shows the time spent checking the WHERE clause and doing other auxiliary operations ([MDEV-20854](https://jira.mariadb.org/browse/MDEV-20854))
* [Inferred IS NOT NULL predicates can be used by the range optimizer](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/not_null_range_scan-optimization) ([MDEV-15777](https://jira.mariadb.org/browse/MDEV-15777))

### Galera

* Galera 4 Inconsistency voting ([MDEV-17048](https://jira.mariadb.org/browse/MDEV-17048))

### General

* The [Information Schema SYSTEM\_VARIABLES Table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-system_variables-table) has a new column showing from which config file a variable derives its value ([MDEV-12684](https://jira.mariadb.org/browse/MDEV-12684))
* Switch Perl DBI scripts from DBD::mysql to DBD::MariaDB driver ([MDEV-19755](https://jira.mariadb.org/browse/MDEV-19755))
* The [Aria](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/aria) max key length is now 2000 bytes, compared to 1000 bytes in [MyISAM](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/myisam-storage-engine).

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

## Changelog

For a complete list of changes made in [MariaDB 10.5.0](mariadb-1050-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-1050-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.5.0](mariadb-1050-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-0-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
