# MariaDB 11.4.0 Release Notes

{% include "../../.gitbook/includes/latest-11-4.md" %}

<a href="https://mariadb.com/downloads" class="button primary">Download</a> <a href="mariadb-11-4-0-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-11-4-series/mariadb-11-4-5-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-114.md" class="button secondary">Overview of 11.4</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/11.4.5/)

**Release date:** 24 December 2023

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

[MariaDB 11.4](what-is-mariadb-114.md) is a long-term development series of MariaDB. It is an evolution of [MariaDB 11.3](../old-releases/release-notes-mariadb-11-3-rolling-releases/what-is-mariadb-113.md) with several entirely new features.

[MariaDB 11.4.0](mariadb-11-4-0-release-notes.md) is a single preview release. Features are to be considered preview, and none are guaranteed to make it into [MariaDB 11.4](what-is-mariadb-114.md).

The preview is available as a container **quay.io/mariadb-foundation/mariadb-devel:11.4**.

**For an overview of** [**MariaDB 11.4**](what-is-mariadb-114.md) **see the** [**What is MariaDB 11.4?**](what-is-mariadb-114.md) **page.**

Thanks, and enjoy MariaDB!

## Partitioning

* [ALTER TABLE … EXCHANGE PARTITION](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/mariadb-11-4-series/broken-reference/README.md) and [ALTER TABLE … CONVERT TABLE … TO](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/mariadb-11-4-series/broken-reference/README.md) now support the `WITH VALIDATION` and `WITHOUT VALIDATION` clauses. If neither is specified, the default behavior is `WITH VALIDATION` ([MDEV-22164](https://jira.mariadb.org/browse/MDEV-22164))

## Sys Schema

* New view [sys.privileges\_by\_table\_by\_level](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/sys-schema/sys-schema-views/privileges_by_table_by_level-sys-schema-view) shows granted privileges broken down by table on which they allow access and level on which they were granted. For example, if a user `x` has `SELECT` privilege granted `ON db.*`, this view will list all tables in the `db` schema with the user `x` having `SELECT` privilege on them. This is different from [INFORMATION\_SCHEMA.TABLE\_PRIVILEGES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-table_privileges-table), which only lists privileges granted on the table level ([MDEV-24486](https://jira.mariadb.org/browse/MDEV-24486))

## Optimizer

* Not only ascending, but also [descending indexes](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-table#index-types) can now be used to optimize [MIN()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/aggregate-functions/min) and [MAX()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/aggregate-functions/max) ([MDEV-27576](https://jira.mariadb.org/browse/MDEV-27576))

## Spider

* The preferred way to specify [Spider parameters](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider/spider-table-parameters) is to use the dedicated Spider table options (implemented in [MariaDB 11.3](../old-releases/release-notes-mariadb-11-3-rolling-releases/what-is-mariadb-113.md)). Abusing the table `COMMENT` clause is now deprecated ([MDEV-28861](https://jira.mariadb.org/browse/MDEV-28861))

## Miscellaneous

* [CONV()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/numeric-functions/conv) function now supports conversion up to base 62 ([MDEV-30879](https://jira.mariadb.org/browse/MDEV-30879))
* Added support for packages ([CREATE PACKAGE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-package)) outside of [ORACLE sql\_mode](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/mariadb-11-4-series/broken-reference/README.md) ([MDEV-32101](https://jira.mariadb.org/browse/MDEV-32101))
* Remove thr\_alarm from server codebase
  * Includes removal of the [debug\_no\_thread\_alarm](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#debug_no_thread_alarm) system variable ([MDEV-32567](https://jira.mariadb.org/browse/MDEV-32567))

## Replication

* [Binary log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log) writing speed was improved by moving checksum calculations out of the global binlog mutex ([MDEV-31273](https://jira.mariadb.org/browse/MDEV-31273)). This is a contribution by Kristian Nielsen
* New system variable [max\_binlog\_total\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#max_binlog_total_size) enables binary log purging when the total size of all binary logs exceeds the specified threshold. The implementation is based on the patch from Percona ([MDEV-31404](https://jira.mariadb.org/browse/MDEV-31404))
* New system variable [slave\_connections\_needed\_for\_purge](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#slave_connections_needed_for_purge) disables binary log purging until the number of connected slaves reaches the specified threshold ([MDEV-31404](https://jira.mariadb.org/browse/MDEV-31404)).
* `FULL_NODUP` is a new value for the [binlog\_row\_image](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#binlog_row_image) system variable. It essentially works like `FULL`, that is all columns are included in the event, but it takes less space, because the after image omits columns that were not changed by the `UPDATE` statement, and have same values as in the before image. This is a contribution from Alibaba ([MDEV-32589](https://jira.mariadb.org/browse/MDEV-32589))
* [mariadb-binlog --flashback](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log/flashback) support for the [FULL\_NODUP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#binlog_row_image) mode. This is a contribution from Alibaba ([MDEV-32894](https://jira.mariadb.org/browse/MDEV-32894)).
* MariaDB can optionally maintain a [special index of GTIDs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/gtid#binlog-indexing) and their location in the binary log. If enabled (the default), it allows finding very quickly where a new connecting replica should start replicating from. Without an index, this required scanning the binlog. This is a contribution by Kristian Nielsen ([MDEV-4991](https://jira.mariadb.org/browse/MDEV-4991)).
* Note that this feature was not included in [MariaDB 11.4](what-is-mariadb-114.md). [GTID](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/gtid) events in the [binary log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log) now include connection id of the client connection that generated the event. This allows [mariadb-binlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog) to tag all row events with a corresponding connection id ([MDEV-7850](https://jira.mariadb.org/browse/MDEV-7850)).

## Data Types

* The [TIMESTAMP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/timestamp) range of values was extended. The maximal allowed value for timestamps was '2038-01-19 03:14:07 UTC', and is now '2106-02-07 06:28:15 UTC'. This does not change the storage format, and new tables can be read by old MariaDB servers as long as timestamp values are within the old timestamp range. At the moment this is only supported on 64-bit platforms ([MDEV-32188](https://jira.mariadb.org/browse/MDEV-32188)). This was not included in [MariaDB 11.4](what-is-mariadb-114.md).

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
