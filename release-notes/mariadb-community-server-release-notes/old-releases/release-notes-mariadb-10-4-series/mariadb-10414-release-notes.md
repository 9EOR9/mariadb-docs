# MariaDB 10.4.14 Release Notes

The most recent release of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download](https://downloads.mariadb.org/mariadb/10.4.14/)[Release Notes](mariadb-10414-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10414-changelog.md)[Overview of 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md)

**Release date:** 10 Aug 2020

[MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) is the current _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.14](mariadb-10414-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) **see the**[**What is MariaDB 10.4?**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

### Variables

* Limit [innodb\_encryption\_threads](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_encryption_threads) to 255 ([MDEV-22258](https://jira.mariadb.org/browse/MDEV-22258)).
* Minimum value of [max\_sort\_length](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#max_sort_length) raised to 8 (previously 4)\
  so fixed size [data types](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types) like [DOUBLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/numeric-data-types/double) and [BIGINT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/numeric-data-types/bigint) are not truncated for lower values of max\_sort\_length ([MDEV-22715](https://jira.mariadb.org/browse/MDEV-22715)).

### InnoDB

* Fixed corruption in delete buffering ([MDEV-22497](https://jira.mariadb.org/browse/MDEV-22497))
* Fixed a deadlock in FLUSH TABLES…FOR EXPORT ([MDEV-22890](https://jira.mariadb.org/browse/MDEV-22890))
* InnoDB data file extension is not crash-safe ([MDEV-23190](https://jira.mariadb.org/browse/MDEV-23190))
* Minor fixes related to encryption and FULLTEXT INDEX
* Dropping the adaptive hash index may cause DDL to lock up InnoDB ([MDEV-22456](https://jira.mariadb.org/browse/MDEV-22456))
* `innodb_log_optimize_ddl=OFF` is not crash safe ([MDEV-21347](https://jira.mariadb.org/browse/MDEV-21347))
* Mariadb service won't shutdown when it's running and the OS datetime updated backwards ([MDEV-17481](https://jira.mariadb.org/browse/MDEV-17481))
* Doublewrite recovery can corrupt data pages ([MDEV-11799](https://jira.mariadb.org/browse/MDEV-11799))
* Fixed race conditions related to buffer pool resizing
* ALTER TABLE fixes ([MDEV-22637](https://jira.mariadb.org/browse/MDEV-22637), [MDEV-23244](https://jira.mariadb.org/browse/MDEV-23244), [MDEV-22988](https://jira.mariadb.org/browse/MDEV-22988), [MDEV-23295](https://jira.mariadb.org/browse/MDEV-23295), [MDEV-22771](https://jira.mariadb.org/browse/MDEV-22771))
* Slow InnoDB shutdown on large instance ([MDEV-22778](https://jira.mariadb.org/browse/MDEV-22778))
* Performance improvements ([MDEV-22778](https://jira.mariadb.org/browse/MDEV-22778))
* Crash recovery fixes ([MDEV-21347](https://jira.mariadb.org/browse/MDEV-21347), [MDEV-23190](https://jira.mariadb.org/browse/MDEV-23190), [MDEV-11799](https://jira.mariadb.org/browse/MDEV-11799))

### Replication

* Make the binlog dump thread to log into errorlog a requested GTID position ([MDEV-20428](https://jira.mariadb.org/browse/MDEV-20428))
* Fix stop of the optimistic parallel slave at requested START-SLAVE-UNTIL position ([MDEV-15152](https://jira.mariadb.org/browse/MDEV-15152))
* Properly handle `RESET MASTER TO` value, when the value exceeds the max allowed `2147483647` ([MDEV-22451](https://jira.mariadb.org/browse/MDEV-22451))
* Correct 'relay-log.info' updating by concurrent parallel workers ([MDEV-22806](https://jira.mariadb.org/browse/MDEV-22806))
* Eliminate deadlock involving parallel workers, `STOP SLAVE` and `FLUSH TABLES WITH READ LOCK` ([MDEV-23089](https://jira.mariadb.org/browse/MDEV-23089))
* Correct master-slave automatic reconnection by slave to always pass through all steps of the initial connect. Specifically, do not skip master notification about slave binlog checksum awareness ([MDEV-14203](https://jira.mariadb.org/browse/MDEV-14203))
* Refine mysqlbinlog output to print out `START TRANSACTION` at `Gtid_log_event` processing which satisfies clients that submit the output with `sql_mode=oracle` ([MDEV-23108](https://jira.mariadb.org/browse/MDEV-23108))
* Replication aborts with `ER_SLAVE_CONVERSION_FAILED` upon `CREATE ... SELECT` in ORACLE mode ([MDEV-19632](https://jira.mariadb.org/browse/MDEV-19632))

### Optimizer

* ALTER TABLE ... ANALYZE PARTITION ... with EITS reads and locks all rows ... ([MDEV-21472](https://jira.mariadb.org/browse/MDEV-21472))
* Print ranges in the optimizer trace created for non-indexed columns when `optimizer_use_condition_selectivity >2` Now the optimizer trace shows the ranges constructed while getting estimates from EITS ([MDEV-22665](https://jira.mariadb.org/browse/MDEV-22665))
* `LATERAL DERIVED` is not clearly visible in `EXPLAIN FORMAT=JSON`, make `LATERAL DERIVED` tables visible in `EXPLAIN FORMAT=JSON` output ([MDEV-17568](https://jira.mariadb.org/browse/MDEV-17568))
* Crash on `WITH RECURSIVE` large query ([MDEV-22748](https://jira.mariadb.org/browse/MDEV-22748))
* Crash with Prepared Statement with a '?' parameter inside a re-used CTE ([MDEV-22779](https://jira.mariadb.org/browse/MDEV-22779))

### Other

* [div\_precision\_increment](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#div_precision_increment) is now taken into account for all intermediate calculations. Previously results could be unpredictable. Note that this means results will have a lower precision in some cases - see [div\_precision\_increment](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#div_precision_increment) ([MDEV-19232](https://jira.mariadb.org/browse/MDEV-19232))
* [mariadb\_schema](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/mariadb_schema) data type qualifier allowing MariaDB native date types in an SQL\_MODE that has conflicting data type translations.
* MariaDB could crash after changing the query\_cache size ([MDEV-5924](https://jira.mariadb.org/browse/MDEV-5924))
* Errors and SIGSEGV on CREATE TABLE w/ various charsets ([MDEV-22111](https://jira.mariadb.org/browse/MDEV-22111))
* Crash in `CREATE TABLE AS SELECT` when the precision of returning type = 0 ([MDEV-22502](https://jira.mariadb.org/browse/MDEV-22502))
* XA: Reject DDL operations between PREPARE and COMMIT ([MDEV-22420](https://jira.mariadb.org/browse/MDEV-22420))
* Stop `mariadb-backup --prepare` on errors during innodb redo log applying ([MDEV-22354](https://jira.mariadb.org/browse/MDEV-22354))
* Server crashes in `mysql_alter_table` upon adding a non-null date column under `NO_ZERO_DATE` with `ALGORITHM=INPLACE` ([MDEV-18042](https://jira.mariadb.org/browse/MDEV-18042))
* Can't uninstall plugin if the library file doesn't exist ([MDEV-21258](https://jira.mariadb.org/browse/MDEV-21258))
* mariadb-backup parameter cleanup ([MDEV-18215](https://jira.mariadb.org/browse/MDEV-18215), [MDEV-21298](https://jira.mariadb.org/browse/MDEV-21298), [MDEV-21301](https://jira.mariadb.org/browse/MDEV-21301), [MDEV-22894](https://jira.mariadb.org/browse/MDEV-22894))
* Rounding functions return wrong datatype ([MDEV-23366](https://jira.mariadb.org/browse/MDEV-23366), [MDEV-23367](https://jira.mariadb.org/browse/MDEV-23367), [MDEV-23368](https://jira.mariadb.org/browse/MDEV-23368), [MDEV-23350](https://jira.mariadb.org/browse/MDEV-23350), [MDEV-23351](https://jira.mariadb.org/browse/MDEV-23351), [MDEV-23337](https://jira.mariadb.org/browse/MDEV-23337), [MDEV-23323](https://jira.mariadb.org/browse/MDEV-23323))
* Create `mariadb.sys` user on each update even is the user is not needed ([MDEV-23102](https://jira.mariadb.org/browse/MDEV-23102))
* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) updated to 26.4.5
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) for Ubuntu 19.10 Eoan and Fedora 30
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-2022](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2022)

## Changelog

For a complete list of changes made in [MariaDB 10.4.14](mariadb-10414-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10414-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.5.5](../../mariadb-10-5-series/mariadb-1055-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-5-10-4-14-10-3-24-10-2-33-and-10-1-46-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
