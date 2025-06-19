# MariaDB 10.8.0 Release Notes

The most recent release of [MariaDB 10.8](what-is-mariadb-108.md) is:[**MariaDB 10.8.8**](mariadb-10-8-8-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.8.8/)

[Download 10.8.0](https://downloads.mariadb.org/mariadb/10.8.0/)[Release Notes](mariadb-10-8-0-release-notes.md)[Changelog](https://app.gitbook.com/o/diTpXxF5WsbHqTReoBsS/s/aEnK0ZXmUbJzqQrTjFyb/changelogs/changelogs-mariadb-100-series/mariadb-1008-changelog)[Overview of 10.8](what-is-mariadb-108.md)

**Release date:** 21 Dec 2021

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

[MariaDB 10.8](what-is-mariadb-108.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.7](../release-notes-mariadb-10-7-series/what-is-mariadb-107.md) with several entirely new features.

[MariaDB 10.8.0](mariadb-10-8-0-release-notes.md) is not a single release, but is instead a number of feature preview releases based on feature branches. Each should be considered as having a maturity of an [_**Alpha**_](../../../mariadb-release-criteria.md) release.\
Read more about feature preview releases [here](https://mariadb.org/preview-releases/).

Thanks, and enjoy MariaDB!

Remember, these features are in separate _preview packages_. The subsection header text corresponds to the preview package name.

## Stored Procedures INOUT Parameters

* Stored procedures already have support for the [IN, OUT and INOUT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/stored-routines/stored-procedures/create-procedure#inoutinout) parameter qualifiers. Added as well for [stored functions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-function#in-out-inout-in-out) and (IN only) [cursors](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/programmatic-compound-statements/programmatic-compound-statements-cursors/declare-cursor#in) ([MDEV-10654](https://jira.mariadb.org/browse/MDEV-10654)). This was a [contribution](https://github.com/MariaDB/server/pull/1931) by [ManoharKB](https://github.com/ManoharKB).

## Lag free ALTER TABLE in replication

* Normally, [ALTER TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table) gets fully executed on the primary first and only then it is [replicated](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication) and starts executing on replicas. With this feature `ALTER TABLE` gets replicated and starts executing on replicas when it starts executing on the primary, not when it finishes. This way the replication lag caused by a heavy `ALTER TABLE` can be completely eliminated ([MDEV-11675](https://jira.mariadb.org/browse/MDEV-11675)).

## Descending indexes

* Individual columns in the [index](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimization-and-indexes) can now be explicitly sorted in the ascending or descending order. This can be useful for optimizing certain [ORDER BY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/order-by) cases ([MDEV-13756](https://jira.mariadb.org/browse/MDEV-13756), [MDEV-26938](https://jira.mariadb.org/browse/MDEV-26938), [MDEV-26939](https://jira.mariadb.org/browse/MDEV-26939), [MDEV-26996](https://jira.mariadb.org/browse/MDEV-26996)).

## InnoDB redo log improvements

* autosize [innodb\_buffer\_pool\_chunk\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_buffer_pool_chunk_size) ([MDEV-25342](https://jira.mariadb.org/browse/MDEV-25342)).
* Improve the [redo log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-redo-log) for concurrency ([MDEV-14425](https://jira.mariadb.org/browse/MDEV-14425)).

## Auto create partition

* For [system versioned tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/system-versioned-tables) that are partitioned `BY SYSTEM_TIME` with the `LIMIT` or `INTERVAL` clause, that is, when the server automatically switches to the new history partition when the previous one becomes full, one can now use an `AUTO` keyword to tell the server to create more history partitions automatically as needed ([MDEV-17554](https://jira.mariadb.org/browse/MDEV-17554)).
* Note that this feature was not included in [MariaDB 10.8.1](mariadb-1081-release-notes.md).

## JSON Histograms

* Histograms in the statistics tables are more precise and stored as JSON, not binary ([MDEV-21130](https://jira.mariadb.org/browse/MDEV-21130), [MDEV-26519](https://jira.mariadb.org/browse/MDEV-26519), [blog post](https://mariadb.org/10-7-preview-feature-json-histograms/)).

## Spider Storage Engine Improvements

* This was mostly internal refactoring work. As a result one can now declare [Spider](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider) connections using the `REMOTE_SERVER`, `REMOTE_DATABASE`, and `REMOTE_TABLE` attributes and not abuse the `COMMENT` field for that. This works both for the whole table and per partition ([MDEV-5271](https://jira.mariadb.org/browse/MDEV-5271), [MDEV-27106](https://jira.mariadb.org/browse/MDEV-27106)).

## Misc. features

* Add an optional argument to the [CRC32()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/numeric-functions/crc32) function, as well as the [CRC32C()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/numeric-functions/crc32c) function, which uses the Castagnoli polynomial. ([MDEV-27208](https://jira.mariadb.org/browse/MDEV-27208)). Note: The order of the 2-ary arguments was swapped after the preview release: `crc32('MariaDB')=crc32(crc32('Maria'),'DB')`
* Deprecate the [keep\_files\_on\_create](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#keep_files_on_create) variable ([MDEV-23570](https://jira.mariadb.org/browse/MDEV-23570)).
* [my\_print\_defaults](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/administrative-tools/my_print_defaults) now handles `--default-*` options in exactly the same way as other MariaDB tools ([MDEV-26238](https://jira.mariadb.org/browse/MDEV-26238)).
* UCA [collations](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets) are now notably faster ([MDEV-27266](https://jira.mariadb.org/browse/MDEV-27266), [MDEV-27265](https://jira.mariadb.org/browse/MDEV-27265)).

## mysqlbinlog GTID support

* [mariadb-binlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog) (or `mysqlbinlog` as it was called back when the task was created) now supports both filtering events by GTID ranges through `--start-position` and `--stop-position,` and validating a binary log's ordering of GTIDs through `--gtid-strict-mode` ([MDEV-4989](https://jira.mariadb.org/browse/MDEV-4989)).

## Windows - Improved i18n support

* On newer versions of Windows (Windows 10 1903 or later), the `mariadb` client defaults to the utf8mb4 character set. Several problems with Unicode input and output in client were fixed. Command line utilities now accept all Unicode characters in user names, database names, file names etc (in the past, characters were restricted to the current ANSI codepage).

**Do not use&#x20;**_**alpha**_**&#x20;releases on production systems!**\
For a complete list of changes made in [MariaDB 10.8.0](mariadb-10-8-0-release-notes.md), with links to detailed\
information on each push, see the [changelog](https://github.com/mariadb-corporation/docs-release-notes/blob/test/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-8-series/mariadb-1080-changelog/README.md).

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
