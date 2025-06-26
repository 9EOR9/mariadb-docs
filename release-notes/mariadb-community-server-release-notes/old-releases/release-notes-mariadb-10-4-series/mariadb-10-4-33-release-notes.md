# MariaDB 10.4.33 Release Notes

The most recent release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download 10.4.33](https://downloads.mariadb.org/mariadb/10.4.33/)[Release Notes](mariadb-10-4-33-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10-4-33-changelog.md)[Overview of 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104)

**Release date:** 7 Feb 2024

[MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is a previous _stable_ series of MariaDB, [maintained until](https://mariadb.org/about/#maintenance-policy) June 2024. It is an evolution of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else and with backported and reimplemented features from MySQL.

[MariaDB 10.4.33](mariadb-10-4-33-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) **see the**[**What is MariaDB 10.4?**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

* Windows packages were delayed but have now been added to the downloads site

### InnoDB

* Unique hash key on column prefix is computed incorrectly ([MDEV-29954](https://jira.mariadb.org/browse/MDEV-29954))
* Query from `I_S.INNODB_SYS_INDEXES` exceeding `LIMIT ROWS EXAMINED` causes `ER_UNKNOWN_ERROR` and LeakSanitizer errors in `rec_copy_prefix_to_buf_old` ([MDEV-28613](https://jira.mariadb.org/browse/MDEV-28613))
* Assertion \`\`0'`failed in`row\_sel\_convert\_mysql\_key\_to\_innobase upon UPDATE\` using a partial-field key prefix in search ([MDEV-21245](https://jira.mariadb.org/browse/MDEV-21245))
* Assertion failure on `REPLACE` on `ROW_FORMAT=COMPRESSED` table ([MDEV-31574](https://jira.mariadb.org/browse/MDEV-31574))
* Crash emitting "Unsupported meta-data version number" error message ([MDEV-29972](https://jira.mariadb.org/browse/MDEV-29972))
* LeakSanitizer errors in `mem_heap_create_block_func` upon query from `I_S.INNODB_SYS_TABLES` with `LIMIT ROWS EXAMINED` ([MDEV-32890](https://jira.mariadb.org/browse/MDEV-32890))
* Inplace alter rebuild increases file size ([MDEV-26740](https://jira.mariadb.org/browse/MDEV-26740))
* `BLOB` corruption on `UPDATE` of `PRIMARY KEY` with `FOREIGN KEY` ([MDEV-31441](https://jira.mariadb.org/browse/MDEV-31441))
* GNU libc `posix_fallocate()` may be extremely slow ([MDEV-32268](https://jira.mariadb.org/browse/MDEV-32268))
* InnoDB wrong error message ([MDEV-32833](https://jira.mariadb.org/browse/MDEV-32833))
* Assertion failure on `ALTER TABLE…PAGE_COMPRESSED=1` ([MDEV-31000](https://jira.mariadb.org/browse/MDEV-31000))

### Backup

* mariadb-backup has wrong or missing plugin-dir default? ([MDEV-29110](https://jira.mariadb.org/browse/MDEV-29110))
* mariadb-backup fails when `innodb_max_dirty_pages_pct` contains a fraction (is not an integer) ([MDEV-20286](https://jira.mariadb.org/browse/MDEV-20286))
* [BACKUP LOCKS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/backup-commands/backup-lock) on table to be accessible to those with [database LOCK TABLES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#database-privileges) privileges ([MDEV-28367](https://jira.mariadb.org/browse/MDEV-28367))

### JSON

* Wrong function name in `ER_JSON_PATH_NO_WILDCARD` error message for `JSON_REPLACE` ([MDEV-24541](https://jira.mariadb.org/browse/MDEV-24541))
* `JSON_VALID` fail to validate integer zero in scientific notation ([MDEV-32587](https://jira.mariadb.org/browse/MDEV-32587))
* `ASAN` errors in `Item_func_json_contains_path::val_int` upon PS execution ([MDEV-32867](https://jira.mariadb.org/browse/MDEV-32867))

### Spider

* Thread (10.6+) and server hangs (10.4/10.5) in 'Opening tables' (on optimized builds) and SIGABRT in `safe_mutex_lock` (on debug) on `I_S` read when using Spider ([MDEV-29421](https://jira.mariadb.org/browse/MDEV-29421))
* SIGSEGV in `spider_db_mbase::append_lock_tables` on `LOCK TABLES` ([MDEV-29963](https://jira.mariadb.org/browse/MDEV-29963))
* `ASAN` `heap-use-after-free` in `spider_link_get_key` on `LOCK TABLES` ([MDEV-31357](https://jira.mariadb.org/browse/MDEV-31357))
* Crash when lateral derived is guaranteed to return no rows ([MDEV-31279](https://jira.mariadb.org/browse/MDEV-31279))
* Bogus error executing PS for query using CTE with renaming of columns ([MDEV-31995](https://jira.mariadb.org/browse/MDEV-31995))
* Spider: Valid `LEFT JOIN` results in ERROR 1064 ([MDEV-26247](https://jira.mariadb.org/browse/MDEV-26247))
* Trying to lock uninitialized mutex or hang upon shutdown after using Spider with `query_cache` ([MDEV-28739](https://jira.mariadb.org/browse/MDEV-28739))
* Spider tests failing in asan/valgrind builds ([MDEV-32849](https://jira.mariadb.org/browse/MDEV-32849))
* Backport fixes to spider init bugs to 10.4-10.6 once they have SQL service ([MDEV-29870](https://jira.mariadb.org/browse/MDEV-29870))
* Server crash with `SIGSEGV` or `dynamic-stack-buffer-overflow` in `spider_db_mbase_util::append_table` ([MDEV-29163](https://jira.mariadb.org/browse/MDEV-29163))
* `heap-use-after-free` in `ha_spider::lock_tables()`, highly sporadic `SIGSEGV` in `intern_close_table` ([MDEV-30014](https://jira.mariadb.org/browse/MDEV-30014))
* Syntax error upon query with subquery from Spider table ([MDEV-30392](https://jira.mariadb.org/browse/MDEV-30392))
* Spider doesn't recognize semi `JOIN` ([MDEV-31645](https://jira.mariadb.org/browse/MDEV-31645))
* MariaDB, SPIDER engine, usage of `REGEXP` ([MDEV-32986](https://jira.mariadb.org/browse/MDEV-32986))
* Spider: variable `spider_same_server_link` not functioning correctly ([MDEV-29718](https://jira.mariadb.org/browse/MDEV-29718))
* Spider fails to autodiscover structure (did in <=10.5) and reports `ERROR 12500` (HY000): unknown ([MDEV-33008](https://jira.mariadb.org/browse/MDEV-33008))
* Spider spawns unnecessarily many system threads for stats synchronization ([MDEV-29020](https://jira.mariadb.org/browse/MDEV-29020))
  * Defaults for [spider\_table\_crd\_thread\_count](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider/spider-system-variables#spider_table_crd_thread_count) and [spider\_table\_sts\_thread\_count](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider/spider-system-variables#spider_table_sts_thread_count) changed from `10` to `1`
* `SIGSEGV` in `spider_db_delete_all_rows` on `TRUNCATE`, `UBSAN`: member call on null pointer of type `'struct spider_db_handler'` in `spider_db_delete_all_rows` ([MDEV-33191](https://jira.mariadb.org/browse/MDEV-33191))
* mariadb-upgrade fails with `'System table spider_tables is different version' => Can't create database 'performance_schema'` ([MDEV-27103](https://jira.mariadb.org/browse/MDEV-27103))
* Spider: SIGSEGV in spider\_db\_direct\_delete, SIGSEGV in spider\_db\_connect, ASAN: heap-use-after-free in spider\_db\_direct\_delete ([MDEV-28683](https://jira.mariadb.org/browse/MDEV-28683))

### Optimizer

* Crash caused by multi-table UPDATE over derived with hanging CTE ([MDEV-28615](https://jira.mariadb.org/browse/MDEV-28615))
* Crash on query using CTE with the same name as a base table ([MDEV-31657](https://jira.mariadb.org/browse/MDEV-31657))
* Crash with query using constant subquery as left part of IN subquery ([MDEV-29362](https://jira.mariadb.org/browse/MDEV-29362))

### Data Definition, Data Manipulation

* `ALTER SEQUENCE IF NOT EXISTS` non\_existing\_seq Errors rather than note ([MDEV-32795](https://jira.mariadb.org/browse/MDEV-32795))
* Unexpected `ER_ERROR_ON_RENAME` upon `DROP` non-existing `FOREIGN KEY` with `ALGORITHM=COPY` ([MDEV-22230](https://jira.mariadb.org/browse/MDEV-22230))
* `FOREIGN_KEY_CHECKS` does not prevent non-copy alter from creating invalid FK structure ([MDEV-29092](https://jira.mariadb.org/browse/MDEV-29092))
* Assertion ``!"wrong page type"'` or Assertion`` "wrong page type" == 0'`failed in`innobase\_instant\_try`on`ALTER\` ([MDEV-18322](https://jira.mariadb.org/browse/MDEV-18322))
* Assertion `(col.vers_sys_end())` upon inplace `ALTER` with virtual columns ([MDEV-20545](https://jira.mariadb.org/browse/MDEV-20545))
* `DELETE with ORDER BY` and semijoin optimization causing crash ([MDEV-32212](https://jira.mariadb.org/browse/MDEV-32212))
* Invalid expr in `cleanup_session_expr()` upon INSERT DELAYED ([MDEV-29932](https://jira.mariadb.org/browse/MDEV-29932))
* SIGSEGV in `my_decimal::operator= and Assertion` 0'`failed in`Item\_type\_holder::val\_decimal\` on SELECT ([MDEV-29070](https://jira.mariadb.org/browse/MDEV-29070))

### Character Sets, Data Types

* InnoDB: CHAR+nopad does not work well ([MDEV-26743](https://jira.mariadb.org/browse/MDEV-26743))
* `CAST(AS UNSIGNED)` fails with `--view-protocol` ([MDEV-32645](https://jira.mariadb.org/browse/MDEV-32645))

### Plugins

* Backport SQL service, introduced by [MDEV-19275](https://jira.mariadb.org/browse/MDEV-19275) ([MDEV-27595](https://jira.mariadb.org/browse/MDEV-27595))
* `"plugin already loaded"` should be a Warning, not an Error ([MDEV-32041](https://jira.mariadb.org/browse/MDEV-32041))
* `mariadb-upgrade` should remove `mysql.plugin` entries for plugins that became bundled ([MDEV-32043](https://jira.mariadb.org/browse/MDEV-32043))

### Galera

* Node has been dropped from the cluster on Startup / Shutdown with async replica ([MDEV-31413](https://jira.mariadb.org/browse/MDEV-31413))
* Inconsistency in Galera caused by `ALTER` being aborted before entering TOI mode ([MDEV-32938](https://jira.mariadb.org/browse/MDEV-32938))
* Assertion \`\`total\_length + thd->wsrep\_sr().log\_position() == saved\_pos'`failed in int`wsrep\_write\_cache\_inc(THD\*, IO\_CACHE\*, size\_t\*)\` ([MDEV-28971](https://jira.mariadb.org/browse/MDEV-28971))
* `wsrep_provider_options` can be truncated on deep and long directory paths ([MDEV-32634](https://jira.mariadb.org/browse/MDEV-32634))
* Server crashes in `rpl_sql_thread_info::cached_charset_compare` / `wsrep_apply_events` ([MDEV-22232](https://jira.mariadb.org/browse/MDEV-22232))
* Galera crash when `"create a table as select"` ([MDEV-27806](https://jira.mariadb.org/browse/MDEV-27806))

### Replication

* Server crashes in `Item_func_binlog_gtid_pos::val_str / Binary_string::c_ptr_safe` ([MDEV-33045](https://jira.mariadb.org/browse/MDEV-33045))
* binlog corruption (/tmp no space left on device at the same moment) ([MDEV-27436](https://jira.mariadb.org/browse/MDEV-27436))
* multi source replication filters breaking GTID semantic ([MDEV-26632](https://jira.mariadb.org/browse/MDEV-26632))
* `SHOW SLAVE STATUS` Can Deadlock an Errored Slave ([MDEV-10653](https://jira.mariadb.org/browse/MDEV-10653))
* `main.rpl_mysqldump_slave` Fails with "Master binlog wasn't deleted" Assertion ([MDEV-32953](https://jira.mariadb.org/browse/MDEV-32953))
* `rpl_seconds_behind_master_spike` Sensitive to IO Thread Stop Position ([MDEV-33327](https://jira.mariadb.org/browse/MDEV-33327))

### General

* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) for Windows Server 2019
* Upgrade [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) to 12.6.
* Using two temporary tables in `OPTIMIZE TABLE` lead to crash ([MDEV-31523](https://jira.mariadb.org/browse/MDEV-31523))
* `REGEXP_REPLACE` treats empty strings different than `REPLACE` in ORACLE mode ([MDEV-29095](https://jira.mariadb.org/browse/MDEV-29095))
* `CREATE UNIQUE INDEX` fails with "ERROR 1286 (42000): Unknown storage engine 'partition'" ([MDEV-21618](https://jira.mariadb.org/browse/MDEV-21618))
* Failure when executing `PS` for query using `IN` subquery ([MDEV-32569](https://jira.mariadb.org/browse/MDEV-32569))
* Potential memory leak on execuing of create view statement ([MDEV-32466](https://jira.mariadb.org/browse/MDEV-32466))
* Assertion failures ([MDEV-32965](https://jira.mariadb.org/browse/MDEV-32965))
* Two JSON related tests running in PS mode fail on server built with `-DWITH_PROTECT_STATEMENT_MEMROOT=YES` ([MDEV-32733](https://jira.mariadb.org/browse/MDEV-32733))
* Alter sequence 2nd ps fails while alter sequence 2nd time (no ps) succeeds ([MDEV-33169](https://jira.mariadb.org/browse/MDEV-33169))
* Set `TaskMax=inifinity` in the MariaDB systemd unit ([MDEV-30236](https://jira.mariadb.org/browse/MDEV-30236))
* Unreliable autocommit flag on connection creation ([MDEV-32875](https://jira.mariadb.org/browse/MDEV-32875))
* A connection can control `RAND()` in following connection ([MDEV-33148](https://jira.mariadb.org/browse/MDEV-33148))
* `THD::rli_fake/rgi_fake` not cleared on new connection ([MDEV-32844](https://jira.mariadb.org/browse/MDEV-32844))
* Assertion failures in `tdc_remove_table` upon interrupted `CREATE TABLE LIKE <sequence>` ([MDEV-20471](https://jira.mariadb.org/browse/MDEV-20471))
* Server crash in `find_field_in_table` ([MDEV-32082](https://jira.mariadb.org/browse/MDEV-32082))
* `LPAD` in vcol created in `ORACLE` mode makes table corrupted in non-ORACLE ([MDEV-27744](https://jira.mariadb.org/browse/MDEV-27744))
* Failure to call SP invoking another SP with parameter requiring type conversion ([MDEV-33270](https://jira.mariadb.org/browse/MDEV-33270))
* The database part is not case sensitive in SP names ([MDEV-33019](https://jira.mariadb.org/browse/MDEV-33019))
* `EXCHANGE PARTITION` with non-matching vcol expression segfault ([MDEV-28127](https://jira.mariadb.org/browse/MDEV-28127))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-`-``#`

## Changelog

For a complete list of changes made in [MariaDB 10.4.33](mariadb-10-4-33-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10-4-33-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.33](mariadb-10-4-33-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-11-2-3-11-1-4-11-0-5-10-11-7-10-6-17-10-5-24-10-4-33-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
