# MariaDB 10.2.33 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.33/)[Release Notes](mariadb-10233-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10233-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 10 Aug 2020

[MariaDB 10.2](what-is-mariadb-102.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.33](mariadb-10233-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

### Variables

* Limit [innodb\_encryption\_threads](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_encryption_threads) to 255 ([MDEV-22258](https://jira.mariadb.org/browse/MDEV-22258)).
* Minimum value of [max\_sort\_length](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#max_sort_length) raised to 8 (previously 4)\
  so fixed size [data types](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types) like [DOUBLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/numeric-data-types/double) and [BIGINT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/numeric-data-types/bigint) are not truncated for lower values of max\_sort\_length ([MDEV-22715](https://jira.mariadb.org/browse/MDEV-22715)).

### InnoDB

* [InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) updated to 5.7.29
* Fixed corruption in delete buffering ([MDEV-22497](https://jira.mariadb.org/browse/MDEV-22497))
* Fixed a deadlock in FLUSH TABLES…FOR EXPORT ([MDEV-22890](https://jira.mariadb.org/browse/MDEV-22890))
* InnoDB data file extension is not crash-safe ([MDEV-23190](https://jira.mariadb.org/browse/MDEV-23190))
* Minor fixes related to encryption and FULLTEXT INDEX
* Dropping the adaptive hash index may cause DDL to lock up InnoDB ([MDEV-22456](https://jira.mariadb.org/browse/MDEV-22456))
* `innodb_log_optimize_ddl=OFF` is not crash safe ([MDEV-21347](https://jira.mariadb.org/browse/MDEV-21347))
* Mariadb service won't shutdown when it's running and the OS datetime updated backwards ([MDEV-17481](https://jira.mariadb.org/browse/MDEV-17481))
* Doublewrite recovery can corrupt data pages ([MDEV-11799](https://jira.mariadb.org/browse/MDEV-11799))
* Fixed race conditions related to buffer pool resizing
* Crash recovery fixes ([MDEV-21347](https://jira.mariadb.org/browse/MDEV-21347), [MDEV-23190](https://jira.mariadb.org/browse/MDEV-23190), [MDEV-11799](https://jira.mariadb.org/browse/MDEV-11799))

### Replication

* Make the binlog dump thread to log into errorlog a requested GTID position ([MDEV-20428](https://jira.mariadb.org/browse/MDEV-20428))
* Fix stop of the optimistic parallel slave at requested START-SLAVE-UNTIL position ([MDEV-15152](https://jira.mariadb.org/browse/MDEV-15152))
* Properly handle `RESET MASTER TO` value, when the value exceeds the max allowed `2147483647` ([MDEV-22451](https://jira.mariadb.org/browse/MDEV-22451))
* Correct 'relay-log.info' updating by concurrent parallel workers ([MDEV-22806](https://jira.mariadb.org/browse/MDEV-22806))
* Eliminate deadlock involving parallel workers, `STOP SLAVE` and `FLUSH TABLES WITH READ LOCK` ([MDEV-23089](https://jira.mariadb.org/browse/MDEV-23089))
* Correct master-slave automatic reconnection by slave to always pass through all steps of the initial connect. Specifically, do not skip master notification about slave binlog checksum awareness ([MDEV-14203](https://jira.mariadb.org/browse/MDEV-14203))

### Optimizer

* ALTER TABLE ... ANALYZE PARTITION ... with EITS reads and locks all rows ... ([MDEV-21472](https://jira.mariadb.org/browse/MDEV-21472))
* Print ranges in the optimizer trace created for non-indexed columns when `optimizer_use_condition_selectivity >2` Now the optimizer trace shows the ranges constructed while getting estimates from EITS ([MDEV-22665](https://jira.mariadb.org/browse/MDEV-22665))
* `LATERAL DERIVED` is not clearly visible in `EXPLAIN FORMAT=JSON`, make `LATERAL DERIVED` tables visible in `EXPLAIN FORMAT=JSON` output ([MDEV-17568](https://jira.mariadb.org/browse/MDEV-17568))
* Crash on `WITH RECURSIVE` large query ([MDEV-22748](https://jira.mariadb.org/browse/MDEV-22748))
* Crash with Prepared Statement with a '?' parameter inside a re-used CTE ([MDEV-22779](https://jira.mariadb.org/browse/MDEV-22779))

### Other

* [div\_precision\_increment](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#div_precision_increment) is now taken into account for all intermediate calculations. Previously results could be unpredictable. Note that this means results will have a lower precision in some cases - see [div\_precision\_increment](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#div_precision_increment) ([MDEV-19232](https://jira.mariadb.org/browse/MDEV-19232))
* MariaDB could crash after changing the query\_cache size ([MDEV-5924](https://jira.mariadb.org/browse/MDEV-5924))
* Errors and SIGSEGV on CREATE TABLE w/ various charsets ([MDEV-22111](https://jira.mariadb.org/browse/MDEV-22111))
* Crash in `CREATE TABLE AS SELECT` when the precision of returning type = 0 ([MDEV-22502](https://jira.mariadb.org/browse/MDEV-22502))
* XA: Reject DDL operations between PREPARE and COMMIT ([MDEV-22420](https://jira.mariadb.org/browse/MDEV-22420))
* Stop `mariabackup --prepare` on errors during innodb redo log applying ([MDEV-22354](https://jira.mariadb.org/browse/MDEV-22354))
* Server crashes in `mysql_alter_table` upon adding a non-null date column under `NO_ZERO_DATE` with `ALGORITHM=INPLACE` ([MDEV-18042](https://jira.mariadb.org/browse/MDEV-18042))
* Can't uninstall plugin if the library file doesn't exist ([MDEV-21258](https://jira.mariadb.org/browse/MDEV-21258))
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-2022](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2022)

Upgrading from 10.2 versions earlier than 10.2.17 is **highly recommended**\
for all [**Galera**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability\
issues with earlier versions. See the bug issue page for more information.\
When upgrading from [MariaDB 10.2.16](mariadb-10216-release-notes.md) or earlier to [MariaDB 10.2.17](mariadb-10217-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in [MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.2.33](mariadb-10233-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10231-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.33](mariadb-10233-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-5-10-4-14-10-3-24-10-2-33-and-10-1-46-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
