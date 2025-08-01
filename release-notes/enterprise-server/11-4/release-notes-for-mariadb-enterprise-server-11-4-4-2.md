# Release Notes for MariaDB Enterprise Server 11.4.4-2

MariaDB Enterprise Server 11.4.4-2 is the first GA release of [MariaDB Enterprise Server](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/mariadb-enterprise-server/README.md) 11.4.

The changes listed here are relative to MariaDB Enterprise Server 10.6.19-15

MariaDB Enterprise Server 11.4.4-2 was released on 2025-01-16.

## Changes in Storage Engines

* With InnoDB storage engine, the process to import an InnoDB tablespace has been simplified. ([MDEV-26137](https://jira.mariadb.org/browse/MDEV-26137))
  * Prior to this release, the process was to create a table, discard the tablespace, then execute `ALTER TABLE IMPORT TABLESPACE`.
  * Starting with this release, `ALTER TABLE IMPORT TABLESPACE` is the only command needed.
  * For example:

```sql
FLUSH TABLES t1 FOR EXPORT;
--copy_file $MYSQLD_DATADIR/test/t1.cfg $MYSQLD_DATADIR/test/t2.cfg
--copy_file $MYSQLD_DATADIR/test/t1.frm $MYSQLD_DATADIR/test/t2.frm
--copy_file $MYSQLD_DATADIR/test/t1.ibd $MYSQLD_DATADIR/test/t2.ibd
UNLOCK TABLES;
ALTER TABLE t2 IMPORT TABLESPACE;
```

* With InnoDB storage engine, space occupied by freed pages within the InnoDB system tablespace can be reclaimed. ([MDEV-14795](https://jira.mariadb.org/browse/MDEV-14795))
  * Prior to this release, InnoDB data files would never shrink during normal operation. .ibd files could be shrunk by rebuilding tables with `OPTIMIZE TABLE` and undo tablespace files using `SET GLOBAL innodb_undo_log_truncate=ON`
  * Starting with this release, an `:autoshrink` attribute has been added for the `innodb_data_file_path` system variable.
  * With `:autoshrink`, the InnoDB system tablespace can be truncated after the last allocated page within it, down to the specified minimum size.
  * For example, with this configuration the InnoDB system tablespace can be shrunk down to 12MiB:

```
[mariadb]
...
innodb_data_file_path=ibdata1:12M;ibdata2:50M:autoextend:autoshrink
```

* With InnoDB storage engine, system variable changes provide improved control of log files and data files: ([MDEV-30136](https://jira.mariadb.org/browse/MDEV-30136))
  * The [innodb\_log\_file\_buffering](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_log_file_buffering) and [innodb\_log\_file\_write\_through](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_log_file_write_through) system variables have been added for log file control. These system variables are boolean and can be set dynamically while the server is running.
  * The [innodb\_data\_file\_buffering](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_data_file_buffering) and [innodb\_data\_file\_write\_through](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_data_file_write_through) system variables have been added for data file control. These system variables are boolean and can be set dynamically while the server is running.
  * The [innodb\_flush\_method system variable](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_flush_method) has been deprecated.
* With InnoDB storage engine, performance of bulk inserts is improved. ([MDEV-25036](https://jira.mariadb.org/browse/MDEV-25036))
* With InnoDB storage engine, changes to the InnoDB redo log format reduce write amplification, which can result in better performance. ([MDEV-14425](https://jira.mariadb.org/browse/MDEV-14425))
* With InnoDB storage engine, the InnoDB change buffer has been removed: ([MDEV-29694](https://jira.mariadb.org/browse/MDEV-29694))
  * With modern storage speeds, the InnoDB change buffer tends to add more overhead, rather than providing a performance gain.
  * The removal of the InnoDB change buffer also simplifies the internal recovery process.
  * The [innodb\_change\_buffering](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_change_buffering) and [innodb\_change\_buffer\_max\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_change_buffer_max_size) system variables have been removed.
  * The [Innodb\_ibuf\_discarded\_delete\_marks](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_ibuf_discarded_delete_marks), [Innodb\_ibuf\_discarded\_deletes](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_ibuf_discarded_deletes), [Innodb\_ibuf\_discarded\_inserts](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_ibuf_discarded_inserts), [Innodb\_ibuf\_free\_list](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_ibuf_free_list), [Innodb\_ibuf\_merged\_delete\_marks](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_ibuf_merged_delete_marks), [Innodb\_ibuf\_merged\_deletes](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_ibuf_merged_deletes), [Innodb\_ibuf\_merged\_inserts](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_ibuf_merged_inserts), [Innodb\_ibuf\_merges](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_ibuf_merges), [Innodb\_ibuf\_segment\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_ibuf_segment_size), and [Innodb\_ibuf\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_ibuf_size) status variables have been removed.
* With InnoDB storage engine, the Prefix Index Queries Optimization is always used: ([MDEV-28540](https://jira.mariadb.org/browse/MDEV-28540))
  * This feature was originally implemented as an optional optimization in MariaDB Server 10.1.
  * The [Innodb\_secondary\_index\_triggered\_cluster\_reads](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_secondary_index_triggered_cluster_reads) and [Innodb\_secondary\_index\_triggered\_cluster\_reads\_avoided](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables#Innodb_secondary_index_triggered_cluster_reads_avoided) status variables have been removed.
* With InnoDB storage engine, multiple undo tablespaces are now enabled by default, so that the default configuration enables undo logs to be truncated while the server is running: ([MDEV-29986](https://jira.mariadb.org/browse/MDEV-29986))
  * Truncation does not apply to undo logs in the system tablespace.
  * [innodb\_undo\_tablespaces](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_undo_tablespaces) default changed from `0` to `3`.
  * To reclaim space, [innodb\_undo\_log\_truncate](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_undo_log_truncate)=ON must be set
  * `innodb_undo_log_truncate=ON` can have a performance impact for some workloads. In those cases, undo truncation can be enabled by temporarily setting the following:

```sql
SET GLOBAL innodb_undo_log_truncate=ON;
```

* With InnoDB storage engine, the temporary InnoDB tablespaces can now be shrunk without restart
  * Before MariaDB Enterprise Server 11.4 the only way to reclaim disk space used by temporary InnoDB tablespaces was to restart the server, as temporary tablespaces are deleted when you stop the server and are recreated with their configured size
  * The disk space can now be reclaimed, tables in use will not be removed. The command to trigger the new feature is:

```sql
SET GLOBAL innodb_truncate_temporary_tablespace_now=1;
```

Example:

```sql
CREATE TEMPORARY TABLE t1(f1 INT NOT NULL, f2 INT NOT NULL)ENGINE=InnoDB;
INSERT INTO t1 SELECT seq, seq FROM seq_1_to_65536;
DROP TABLE t1;
SELECT NAME, FILE_SIZE FROM INFORMATION_SCHEMA.INNODB_SYS_TABLESPACES WHERE NAME="innodb_temp
orary";
```

```
+------------------+-----------+
| NAME             | FILE_SIZE |
+------------------+-----------+
| innodb_temporary |  79691776 |
+------------------+-----------+
```

```sql
SET GLOBAL INNODB_TRUNCATE_TEMPORARY_TABLESPACE_NOW= 1;
SELECT NAME, FILE_SIZE FROM INFORMATION_SCHEMA.INNODB_SYS_TABLESPACES WHERE NAME="innodb_temp
orary";
```

```
+------------------+-----------+
| NAME             | FILE_SIZE |
+------------------+-----------+
| innodb_temporary |  12582912 |
+------------------+-----------+
```

* With Spider storage engine, engine-defined attributes (table options) are accepted. Previously, Spider required parameters to be provided via `COMMENT` for a table: ([MDEV-27106](https://jira.mariadb.org/browse/MDEV-27106))

| New Table Option | Old COMMENT Option | Description                                                                    |
| ---------------- | ------------------ | ------------------------------------------------------------------------------ |
| REMOTE\_DATABASE | database           | The remote database that contains the remote table                             |
| REMOTE\_SERVER   | srv                | The IP address or hostname of the remote server that contains the remote table |
| REMOTE\_TABLE    | tbl                | The remote table                                                               |

* Spider storage engine system variable defaults have changed.
* With the Spider storage engine the preferred way to specify Spider parameters is now to use the dedicated Spider table options. Abusing the table COMMENT clause is now deprecated ([MDEV-28861](https://jira.mariadb.org/browse/MDEV-28861))
* With MyRocks storage engine, log files can be stored in a user-defined directory specified by the [rocksdb\_log\_dir system variable](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/myrocks/myrocks-system-variables#rocksdb_log_dir). ([MDEV-27791](https://jira.mariadb.org/browse/MDEV-27791))

## Compatibility Enhancements

* Stored function parameters can be qualified with `IN`, `OUT`, `INOUT`, and `IN OUT`: ([MDEV-10654](https://jira.mariadb.org/browse/MDEV-10654))
  * When a parameter is qualified with `IN`, a value is passed to the function.
  * When a parameter is qualified with `OUT`, the function returns a value to the caller.
  * When a parameter is qualified with `INOUT` or `IN OUT`, a value is passed to the function, and the function also returns a value to the caller.
  * `OUT`, `INOUT`, and `INOUT` can only be used when called from SET and not when called from SELECT
  * `OUT`, `INOUT`, and `INOUT` allow a function to return more than one value, which allows for more complex and nested functions.
  * In previous releases, the qualifiers were supported for stored procedures, but not for stored functions.
  * Starting with this release, the qualifiers are accepted in stored functions using the same syntax previously used for stored procedures.
  * When [sql\_mode=ORACLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/variables-and-modes/sql-mode) is set, the behavior is adjusted to match the behavior of Oracle.
* Changed default behavior for [TIMESTAMP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/timestamp) field properties: ([MDEV-28632](https://jira.mariadb.org/browse/MDEV-28632))
  * Previous to this release, implementation-specific behavior was present by default for the first `TIMESTAMP` column in a table. This behavior added `DEFAULT current_timestamp() ON UPDATE current_timestamp()` to the `TIMESTAMP` field properties.
  * Starting this release, the implementation-specific behavior for `TIMESTAMP` field properties is disabled by default. The default value of the [explicit\_defaults\_for\_timestamp system variable](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#explicit_defaults_for_timestamp) is changed to OFF
  * As a result of this change, new `TIMESTAMP` columns without explicit default values will be created with `DEFAULT NULL`

## Operational Enhancements

* [Online Schema Change (OSC)](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table/online-schema-change) is new server internal functionality which makes all schema changes ([ALTER TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements-and-structure/sql-statements/data-definition/alter/alter-table) commands) non-blocking. ([MDEV-16329](https://jira.mariadb.org/browse/MDEV-16329))
  * OSC targets a problem previously solvable using third-party solutions, in a way which reduces operational impact. Some aspects of the OSC implementation are operationally significant:
    * OSC performs internal Copy-Apply-Replace: First, the altered table gets copied, then the online changes get applied. A short table lock occurs when applying last changes and renaming the tables. The binary log is not used in this process. This is significant because some third-party approaches to this problem depend on client connections which can be subject to connection timeouts and similar factors.
    * OSC is asynchronous: Changes from applications are first stored in an online change buffer. This is significant because some third-party approaches to this problem are synchronous and as result impact the execution of other transactions.
    * OSC is trigger-less: Only server internal handlers for a DML-side check if `ALTER TABLE` is in progress are used. `INSERT`, `UPDATE`, or `DELETE` triggers based on stored routines are not used. This is significant because some third-party approaches to this problem depend on triggers.
  * By default, when an `ALTER` operation cannot be executed `INSTANT`, OSC will be used. If OSC cannot be used, another algorithm will be used.
  * If the `LOCK=NONE` option is explicitly specified in the `ALTER` statement, or if the equivalent statement `ALTER ONLINE TABLE` is used, the operation will be performed if it can be done as OSC and fails otherwise.
  * As an override to this new behavior, if the `old_mode` system variable is set with `LOCK_ALTER_TABLE_COPY`, the old behavior is preferred when `LOCK=NON`E is not explicitly set. ([MDEV-31812](https://jira.mariadb.org/browse/MDEV-31812))
* Stored routine calls reflect all changes to metadata for objects the stored routine depends on. ([MDEV-5816](https://jira.mariadb.org/browse/MDEV-5816))
* Prior to this release, a reconnect was needed before a stored routine was able to update its metadata from altered objects. For example, absent a reconnect:

```sql
CREATE TABLE t1 (id INT);
INSERT INTO t1 VALUES (100);
CREATE PROCEDURE p1() SELECT * FROM t1;
CALL p1;
```

```
+------+
| id   |
+------+
|  100 |
+------+
```

```sql
ALTER TABLE t1 ADD COLUMN b INT DEFAULT 0;
CALL p1;
```

```
+------+
| id   |
+------+
|  100 |
+------+
```

• Starting with this release, metadata changes are reflected without a reconnect:

```sql
CREATE TABLE t1 (id INT);
INSERT INTO t1 VALUES (100);
CREATE PROCEDURE p1() SELECT * FROM t1;
CALL p1;
```

```
+------+
| id   |
+------+
|  100 |
+------+
```

```sql
ALTER TABLE t1 ADD COLUMN b INT DEFAULT 0;
CALL p1;
```

```
+------+------+
| id   | b    |
+------+------+
|  100 |    0 |
+------+------+
```

* Temporary tables are now included in `information_schema.TABLES`, in `SHOW TABLES` output, and in `SHOW TABLE STATUS` output. ([MDEV-12459](https://jira.mariadb.org/browse/MDEV-12459))
  * For example:

```sql
CREATE DATABASE test;
USE test;
CREATE TABLE t1 (id INT);
CREATE TEMPORARY TABLE t2_temp (id INT);
SHOW FULL TABLE;
```

```
+----------------+-----------------+
| Tables_in_test | Table_type      |
+----------------+-----------------+
| t2_temp        | TEMPORARY TABLE |
| t1             | BASE TABLE      |
+----------------+-----------------+
```

```sql
SELECT table_schema, table_name, table_type FROM information_schema.TABLES WHERE table_schema='test';
```

```
+--------------+------------+------------+
| table_schema | table_name | table_type |
+--------------+------------+------------+
| test         | t2_temp    | TEMPORARY  |
| test         | t1         | BASE TABLE |
+--------------+------------+------------+
```

* For [INSERT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/inserting-loading-data/insert) operations that insert multiple rows, error reporting has been improved: ([MDEV-10075](https://jira.mariadb.org/browse/MDEV-10075))
  * In [GET DIAGNOSTICS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/programmatic-compound-statements/programmatic-compound-statements-diagnostics/get-diagnostics), the `ROW_NUMBER` property allows retrieval of the row number that caused the error or warning:

```sql
GET DIAGNOSTICS CONDITION 1 @failed_row=ROW_NUMBER;
```

* Information Schema system table optimizations: ([MDEV-20609](https://jira.mariadb.org/browse/MDEV-20609))
  * When [PARAMETERS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-parameters-table) is queried and the `WHERE` clause filters on `SPECIFIC_SCHEMA` and `SPECIFIC_NAME`, an index is used to avoid a full table scan.
  * When [ROUTINES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-routines-table) is queried and the `WHERE` clause filters on `ROUTINE_SCHEMA` and `ROUTINE_NAME`, an index is used to avoid a full table scan.
* [SHOW EXPLAIN FOR CONNECTION\_ID](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-explain) can show the query plan for a query running in another connection: ([MDEV-25956](https://jira.mariadb.org/browse/MDEV-25956))

```sql
SHOW EXPLAIN FOR 1;
```

* The statement returns the query itself as a warning, which can be obtained via [SHOW WARNINGS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-warnings).
* `SHOW ANALYZE [FORMAT=JSON] FOR CONNECTION_ID` can analyze a query running in another connection: ([MDEV-27021](https://jira.mariadb.org/browse/MDEV-27021))

```sql
SHOW ANALYZE FOR 1;
```

* `ANALYZE FORMAT=JSON` now shows the time spent in the query optimizer. ([MDEV-28926](https://jira.mariadb.org/browse/MDEV-28926))
* With [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump), the new [--order-by-size command-line option](https://github.com/mariadb-corporation/docs-release-notes/blob/test/mariadb-enterprise-server-release-notes/mariadb-enterprise-server-11-4/maria-dump/README.md#options) allows tables to be dumped in order of size (smallest tables first): ([MDEV-28074](https://jira.mariadb.org/browse/MDEV-28074))

```bash
$ mariadb-dump \
 --user=USER \
 --password='PASSWORD' \
 --all-databases \
 --single-transaction \
 --order-by-size
```

* This new option is useful when the [--single-transaction command-line option](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) is specified and the backup contains tables that are truncated frequently. Since tables that are truncated frequently tend to be smaller, those tables will be backed up earlier, which reduces the chance that the backup will fail with the [ER\_TABLE\_DEF\_CHANGED error code](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/mariadb-internals/using-mariadb-with-your-programs-api/error-codes/mariadb-error-codes-1400-to-1499/e1412).
* The [transaction\_isolation system variable](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#transaction_isolation) can now be used to set the transaction isolation: ([MDEV-21921](https://jira.mariadb.org/browse/MDEV-21921))
  * The `tx_isolation` system variable is still available as an alias, but it has been deprecated and will be removed in a later release.
* The [transaction\_read\_only system variable](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#transaction_read_only) can now be used to set a transaction to read-only. ([MDEV-21921](https://jira.mariadb.org/browse/MDEV-21921))
* Process list now includes the number of rows sent by the statement. The new value `SENT_ROWS` in the information schema table `PROCESSLIST` includes the number of rows sent by the current statement, shown in the processlist.
  * `SELECTS` with functions show the total number of rows sent by the main statement and all functions
  * Stored procedures show the total number of rows sent per stored procedure statement
  * `INSERT RETURNING` and `DELETE RETURNING` show the total number of rows sent for the returning data set
  * Example:

```sql
SELECT * FROM processlist\G
```

```
*************************** 1. row ***************************
...
*************************** 2. row ***************************
             ID: 6
           USER: root
           HOST: localhost
             DB: test
        COMMAND: Query
           TIME: 1
          STATE: Sending data
           INFO: select * from t1
        TIME_MS: 1340.406
          STAGE: 0
      MAX_STAGE: 0
       PROGRESS: 0.000
    MEMORY_USED: 89856
MAX_MEMORY_USED: 392544
  EXAMINED_ROWS: 0
      SENT_ROWS: 3895737
       QUERY_ID: 436
    INFO_BINARY: select * from t1
            TID: 100
```

* The `SQL Error Log Plugin`, used to log errors sent to clients for later analysis, has been enhanced. When option `sql_error_log_with_db_and_thread_info=ON` is set, the log file is now also showing thread id and the current default schema for the error.
* When mariadb-dump is used with the option `-T / --tab=` to produce tab-separated text-format data files per table, the new option `--parallel` (synonym `--use-threads`) can be used to use several threads in parallel to dump the table data to their .txt files.
  * Parallelism also works if the option `--single-transaction` is used.
* The option `--parallel` has been added to mariadb-import as a synonym to `--use-threads`, which has been available before.

## Optimizer

* MariaDB Query Optimizer performs cost-based optimizations with an understanding of storage engine-specific costs: ([MDEV-26974](https://jira.mariadb.org/browse/MDEV-26974))
  * The query optimizer now defaults to assume SSD storage is used. Costs for disk access can be overridden.
  * [Optimizer costs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/mariadb-internals/mariadb-internals-documentation-query-optimizer/the-optimizer-cost-model-from-mariadb-11-0#description-of-the-different-cost-variables) can be tuned by setting the following system variables via configuration file, command-line parameter, or the [SET SQL statement](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/set-commands/set):

| System Variable                     | Type    | Description                                                                                                                                                                    |
| ----------------------------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| optimizer\_disk\_read\_cost         | Engine  | Sets the time in microseconds required to read a 4K block from storage. The default value is tuned for an SSD reading at 400 MB/second.                                        |
| optimizer\_index\_block\_copy\_cost | Engine  | Sets the cost to lock a block in the global cache and copy it to the local cache. The cost applies to every block accessed, regardless of whether the block is already cached. |
| optimizer\_key\_compare\_cost       | Engine  | Sets the cost to compare two key values.                                                                                                                                       |
| optimizer\_key\_copy\_cost          | Engine  | Sets the cost to copy a key value from the index to the local buffer while searching for a key value.                                                                          |
| optimizer\_key\_lookup\_cost        | Engine  | Sets the cost to find a key entry in the index.                                                                                                                                |
| optimizer\_row\_copy\_cost          | Engine  | Sets the cost to find the next key entry in the index.                                                                                                                         |
| optimizer\_rowid\_compare\_cost     | Engine  | Sets the cost to compare two rowid values.                                                                                                                                     |
| optimizer\_rowid\_copy\_cost        | Engine  | Sets the cost to copy a rowid from the index.                                                                                                                                  |
| optimizer\_row\_lookup\_cost        | Engine  | Sets the cost to find a row based on the rowid. The rowid is stored in the index with the key.                                                                                 |
| optimizer\_row\_next\_find\_cost    | Engine  | Sets the cost to find the next row.                                                                                                                                            |
| optimizer\_scan\_setup\_cost        | Session | Sets the cost to start a table or index scan. The default low value configures the optimizer to use index lookups for tables with very few rows.                               |
| optimizer\_where\_cost              | Session | Sets the cost to execute the WHERE clause for every row found. As this value is increases, the optimizer is more likely to choose plans which read fewer rows.                 |

* Optimizer costs can be tuned per storage engine by prefixing the system variable with the storage engine name.
  * Current optimizer costs for each storage engine can be queried via [information\_schema.OPTIMIZER\_COSTS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/mariadb-internals/mariadb-internals-documentation-query-optimizer/the-optimizer-cost-model-from-mariadb-11-0#new-cost-model)
* For JOIN with many eq\_ref tables, query performance is improved: ([MDEV-28852](https://jira.mariadb.org/browse/MDEV-28852))
  * New system variable [optimizer\_extra\_pruning\_depth](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#optimizer_extra_pruning_depth)
  * Default changed for system variable [optimizer\_prune\_level](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#optimizer_prune_level) from 1 to 2 to enable prune join prefixes
  * New status variable `Optimizer_join_prefixes_check_calls`
* An index can now be used when comparing the return value of the [DATE() function](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/date) to a constant value. ([MDEV-8320](https://jira.mariadb.org/browse/MDEV-8320))
* Single-table [UPDATE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/update) and [DELETE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/delete) can now benefit from semi-join optimization. ([MDEV-7487](https://jira.mariadb.org/browse/MDEV-7487))
* JSON histograms with detailed histogram collection: ([MDEV-26519](https://jira.mariadb.org/browse/MDEV-26519))
  * Enabled when [histogram\_type=JSON\_HB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/histogram-based-statistics#histogram_type) is set, which is now the default.
  * JSON histograms result in more precise data statistics for string data types or when columns have highly-uneven data distribution.
  * With more precise data statistics the optimizer can create better query plans, resulting in faster queries.

## Partitioning

* A table can be converted into a partition with `ALTER TABLE .. CONVERT TABLE .. TO PARTITION`: ([MDEV-22165](https://jira.mariadb.org/browse/MDEV-22165))

```sql
ALTER TABLE partitioned_tab
 CONVERT TABLE tab1
 TO PARTITION part_name VALUES LESS THAN (1000000);
```

* The `ALTER TABLE .. CONVERT TABLE .. TO PARTITION` operation was previously backported to MariaDB Enterprise Server 10.6.11-6.
* A partition can be converted into a table with `ALTER TABLE .. CONVERT PARTITION .. TO TABLE:` ([MDEV-22166](https://jira.mariadb.org/browse/MDEV-22166))

```sql
ALTER TABLE partitioned_tab
 CONVERT PARTITION part_name
 TO TABLE tab1;
```

* The `ALTER TABLE .. CONVERT PARTITION .. TO TABLE` operation was previously backported to MariaDB Enterprise Server 10.6.11-6.
* [CREATE TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-table) syntax has been extended, so the PARTITION keyword is optional in each partition definition: ([MDEV-26471](https://jira.mariadb.org/browse/MDEV-26471))

```sql
CREATE TABLE partitioned_tab (
 col1 INT
)
PARTITION BY RANGE(col1) (
 part1 VALUES LESS THAN (1000000),
 part2 VALUES LESS THAN (2000000),
 part3 VALUES LESS THAN (3000000),
 part4 VALUES LESS THAN (4000000),
 part5 VALUES LESS THAN (5000000),
 part_end VALUES LESS THAN MAXVALUE
);
```

* Engine-defined attributes can be defined per-partition: ([MDEV-5271](https://jira.mariadb.org/browse/MDEV-5271))

```sql
CREATE TABLE remote_spider_tab (
 id INT,
 str VARCHAR(255),
 PRIMARY KEY(id)
) ENGINE=Spider
PARTITION BY RANGE(id) (
 PARTITION east_part VALUES LESS THAN (100) REMOTE_SERVER="mdb-east.example.org" REMOTE_TABLE="tab1",
 PARTITION west_part VALUES LESS THAN MAXVALUE REMOTE_SERVER="mdb-west.example.org", REMOTE_TABLE="tab1"
);
```

* Exchanging partition or converting a table is now possible without a validation of the partitioning expression
  * This new feature should be used with care, as it can lead to inconsistencies if the partitioning rules are not met.
  * The new addition to `ALTER TABLE` is:

```sql
EXCHANGE PARTITION partition_name WITH TABLE tbl_name [{WITH | WITHOUT} VALIDATION]

CONVERT TABLE normal_table TO partition_definition [{WITH | WITHOUT} VALIDATION]
```

## System Versioning

* History partition creation can be automated using the `AUTO` keyword when partitioned by `INTERVAL` or `LIMIT`: ([MDEV-17554](https://jira.mariadb.org/browse/MDEV-17554))

```sql
CREATE TABLE t1 (x INT) WITH SYSTEM VERSIONING
 PARTITION BY SYSTEM_TIME INTERVAL 1 months AUTO;
```

* In the above example, a new history partition to store historical row versions is created on a monthly basis.
* [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) can backup historical data from system-versioned tables if the [--dump-history command-line option](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump#options) is specified. ([MDEV-16029](https://jira.mariadb.org/browse/MDEV-16029))
* [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) can perform a dump of historical data as of a point in time if the [--as-of command-line option](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump#options) is specified. ([MDEV-16355](https://jira.mariadb.org/browse/MDEV-16355))
* More Information about Application-time Period Tables is now available in the information schema
  * New views `PERIOD` and `KEY_PERIOD_USAGE` are added to information\_schema.
    * View `PERIODS` includes the columns
      * `TABLE_CATALOG`
      * `TABLE_SCHEMA`
      * `TABLE_NAME`
      * `PERIOD_NAME`
      * `START_COLUMN_NAME`
      * `END_COLUMN_NAME`to list Application-time period tables, the name defined for a period and the columns used for start and end timestamps.
    * View `KEY_PERIOD_USAGE` includes the columns
      * `CONSTRAINT_CATALOG`
      * `CONSTRAINT_SCHEMA`
      * `CONSTRAINT_NAME`
      * `TABLE_CATALOG`
      * `TABLE_SCHEMA`
      * `TABLE_NAME`
      * `PERIOD_NAME`
* Two new columns are added to the `COLUMNS` view of `information_schema`
  * `IS_SYSTEM_TIME_PERIOD_START`
  * `IS_SYSTEM_TIME_PERIOD_END`

## SQL Level Enhancements

* General Support of Packages for Stored Routines has been added
  * Before MariaDB Enterprise Server 11.4, the `CREATE PACKAGE` feature, as well as `CREATE PACKAGE BODY`, were only supported with `sql_mode = ORACLE`. They can now be used with any SQL mode.
  * Example:

```sql
DELIMITER $$

CREATE OR REPLACE PACKAGE myPkg
  PROCEDURE p1();
  FUNCTION f1() RETURNS INT;
END;

$$

CREATE OR REPLACE PACKAGE BODY myPkg

  -- variable declarations
  DECLARE v1 INT DEFAULT 1;
  DECLARE v2 INT DEFAULT 10;

  -- routine declarations
  PROCEDURE p1()
  BEGIN
    SELECT v1, v2;
  END;

  FUNCTION f1() RETURNS INT
  BEGIN
    RETURN v1;
  END;

  -- package initialization
  SET v1=v1 + 2;
END;
$$

DELIMITER ;

SELECT myPkg.f1();
```

```
+------------+
| myPkg.f1() |
+------------+
|          3 |
+------------+
```

```sql
CALL myPkg.p1();
```

```
+------+------+
| v1   | v2   |
+------+------+
|    3 |   10 |
+------+------+
```

#### Indexes

* Descending indexes are supported: ([MDEV-13756](https://jira.mariadb.org/browse/MDEV-13756))
  * When used with a composite index, can be used to get a significant performance boost for queries that perform `ORDER BY` operations on columns in different orders than the defined order.
  * In previous releases, MariaDB Enterprise Server already supported the `DESC` option for `ORDER BY`, but the optimizer would use the ascending index. For a composite index, the optimizer would have to use an index and perform a file sort.
  * For example, using the following example table:

```sql
CREATE TABLE sections (
   top_level INT,
   sub_level INT,
   INDEX top_asc_sub_asc (top_level ASC, sub_level ASC),
   INDEX top_asc_sub_desc (top_level ASC, sub_level DESC),
   INDEX top_desc_sub_asc (top_level DESC, sub_level ASC),
   INDEX top_desc_sub_desc (top_level DESC, sub_level DESC)
);
INSERT INTO sections VALUES
   (1, 1), (1, 2), (2, 1), (2, 2),
   (3, 1), (3, 2), (3, 3);
```

• Performing an `ORDER BY .. ASC` on multiple columns still shows `"Using index"` in the `EXPLAIN` output:

```sql
EXPLAIN SELECT * FROM sections
   ORDER BY top_level ASC, sub_level ASC;
```

```
+------+-------------+----------+-------+---------------+-----------------+---------+------+------+-------------+
| id   | select_type | table    | type  | possible_keys | key             | key_len | ref  | rows | Extra       |
+------+-------------+----------+-------+---------------+-----------------+---------+------+------+-------------+
|    1 | SIMPLE      | sections | index | NULL          | top_asc_sub_asc | 10      | NULL | 7    | Using index |
+------+-------------+----------+-------+---------------+-----------------+---------+------+------+-------------+
```

• With this change, performing a mix of `ORDER BY .. ASC, .. DESC` on multiple columns also shows `"Using index"` in the `EXPLAIN` output:

```sql
EXPLAIN SELECT * FROM sections
   ORDER BY top_level ASC, sub_level DESC;
```

```
+------+-------------+----------+-------+---------------+------------------+---------+------+------+-------------+
| id   | select_type | table    | type  | possible_keys | key              | key_len | ref  | rows | Extra       |
+------+-------------+----------+-------+---------------+------------------+---------+------+------+-------------+
|    1 | SIMPLE      | sections | index | NULL          | top_asc_sub_desc | 10      | NULL | 7    | Using index |
+------+-------------+----------+-------+---------------+------------------+---------+------+------+-------------+
```

#### JSON

* `JSON_KEY_VALUE()` extracts key/value pairs from a JSON object. ([MDEV-30145](https://jira.mariadb.org/browse/MDEV-30145))
  * Syntax: JSON\_KEY\_VALUE(`<json_doc>, <json_path>`)
  * The `<json_path>` specifies the JSON objects whose key/value pairs should be returned. For example:

```sql
SELECT JSON_KEY_VALUE('[[1, {"key1":"val1", "key2":"val2"}, 3], 2, 3]', '$[0][1]');
```

```
+-----------------------------------------------------------------------------+
| JSON_KEY_VALUE('[[1, {"key1":"val1", "key2":"val2"}, 3], 2, 3]', '$[0][1]') |
+-----------------------------------------------------------------------------+
| [{"key": "key1", "value": "val1"}, {"key": "key2", "value": "val2"}]        |
+-----------------------------------------------------------------------------+
```

• `JSON_KEY_VALUE()` can be used as an argument to `JSON_TABLE(`), adding the key to a result set. For example:

```sql
SELECT jt.* FROM JSON_TABLE(
  JSON_KEY_VALUE('[[1, {"key1":"val1", "key2":"val2"}, 3], 2, 3]', '$[0][1]'),'$[*]'
      COLUMNS (
         k VARCHAR(20) PATH '$.KEY',
         v VARCHAR(20) PATH '$.value',
        id FOR ORDINALITY )) AS jt;
```

```
+------+------+------+
| k    | v    | id   |
+------+------+------+
| key1 | val1 |    1 |
| key2 | val2 |    2 |
+------+------+------+

* ##JSON_ARRAY_INTERSECT()## finds the intersection between two JSON arrays. (MDEV-26182)
** Syntax: ##JSON_ARRAY_INTERSECT(<array1>, <array2>)##
** For example:<<sql inline=false>>SET @array1= '[1,2,3]';
SET @array2= '[1,2,4]';
SELECT json_array_intersect(@array1, @array2) as result;
```

```
+--------+
| result |
+--------+
| [1, 2] |
+--------+
```

```sql
SET @json1= '[[1,2,3],[4,5,6],[1,1,1]]';
SET @json2= '[[1,2,3],[4,5,6],[1,3,2]]';
SELECT json_array_intersect(@json1, @json2) AS result;
```

```
+------------------------+
| result                 |
+------------------------+
| [[1, 2, 3], [4, 5, 6]] |
+------------------------+
```

* `JSON_OBJECT_TO_ARRAY()` converts all JSON objects found in a JSON document to JSON arrays. ([MDEV-26182](https://jira.mariadb.org/browse/MDEV-26182))
  * Syntax: `JSON_OBJECT_TO_ARRAY(<json_doc>)`
  * For example:

```sql
SET @json1= '{ "a" : [1,2,3] , "b": {"key1": "val1", "key2": {"key3": "val3"}} }';
SELECT JSON_OBJECT_TO_ARRAY(@json1) AS result;
```

```
+-----------------------------------------------------------------------+
| result                                                                |
+-----------------------------------------------------------------------+
| [["a", [1, 2, 3]], ["b", {"key1": "val1", "key2": {"key3": "val3"}}]] |
+-----------------------------------------------------------------------+
```

* Resulting arrays can be compared using `JSON_ARRAY_INTERSECT()`. For example:

```sql
SET @json1='{"a":[1,2,3],"b":{"key1":"val1","key2":{"key3":"val3"}}}';
SET @json2='{"a":[1,2,3]}';
SELECT JSON_OBJECT_TO_ARRAY(@json1) INTO @array1;
SELECT JSON_OBJECT_TO_ARRAY(@json2) INTO @array2;
SELECT JSON_ARRAY_INTERSECT(@array1,@array2) AS result;
```

```
+--------------------+
| result             |
+--------------------+
| [["a", [1, 2, 3]]] |
+--------------------+
```

* `JSON_OBJECT_FILTER_KEYS()` returns key/value pairs from a JSON string for keys in an array. ([MDEV-26182](https://jira.mariadb.org/browse/MDEV-26182))
* Syntax: JSON\_OBJECT\_FILTER\_KEYS`(<json_doc>,<array_keys>)\`
* For example:

```sql
SET @json1= '{ "a": 1, "b": 2, "c": 3}';
SELECT JSON_OBJECT_FILTER_KEYS (@json1, ' ["b", "c"] ') AS result;
```

```
+------------------+
| result           |
+------------------+
| {"b": 2, "c": 3} |
+------------------+
```

* Using `JSON_ARRAY_INTERSECT()` and `JSON_KEY()` as arguments for `JSON_OBJECT_FILTER_KEYS()`, a comparison of two JSON strings is possible where only the same keys are compared, not the key/value pairs. For example:

```sql
SET @json1= '{ "a": 1, "b": 2, "c": 3}';
SET @json2= '{"b" : 10, "c": 20, "d": 30}';
SELECT JSON_OBJECT_FILTER_KEYS (@json1, json_array_intersect(json_keys(@json1), json_keys(@json2))) AS result;
```

```
+------------------+
| result           |
+------------------+
| {"b": 2, "c": 3} |
+------------------+
```

* [JSON\_EQUALS()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_equals) can be used to compare two documents and determine if they are equal. ([MDEV-16375](https://jira.mariadb.org/browse/MDEV-16375))
  * The `JSON_EQUALS()` function was previously backported to MariaDB Enterprise Server 10.4.25-16, 10.5.16-11, and 10.6.8-4.
* \#[#JSON\_NORMALIZE()##](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_normalize) can be used to normalize two JSON documents to make them more comparable. ([MDEV-23143](https://jira.mariadb.org/browse/MDEV-23143))
  * For example, this function can be used when defining a unique key on JSON data.
  * The `JSON_NORMALIZE()` function was previously backported to MariaDB Enterprise Server 10.4.25-16, 10.5.16-11, and 10.6.8-4.
* [JSON\_OVERLAPS()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_overlaps) can be used to compare two JSON documents to determine if they have any key-value pairs or array elements in common. ([MDEV-27677](https://jira.mariadb.org/browse/MDEV-27677))

```sql
SELECT JSON_OVERLAPS('{"A": 1, "B": {"C":2}}', '{"A": 2, "B": {"C":2}}') AS is_overlap;
```

```
+---------------------+
| is_overlap          |
+---------------------+
| 1                   |
+---------------------+
```

* [JSON\_SCHEMA\_VALID()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_schema_valid) can be used to validate a JSON document against a JSON schema, as documented by the [JSON Schema Draft 2020](https://json-schema.org/draft/2020-12/release-notes.html). ([MDEV-27128](https://jira.mariadb.org/browse/MDEV-27128))
  * This function can also be used in a `CHECK` constraint to verify that JSON documents are only stored in the database if they include required items and that the values are within a given range and length.
* Negative indexes can be used to access values in JSON arrays relative to the end of the array when a JSON Path expression is used as a parameter to a JSON function. ([MDEV-22224](https://jira.mariadb.org/browse/MDEV-22224))

```sql
SELECT JSON_REMOVE(@json, '$.A[-10]')
```

* The `last` index can be used to access the last value in a JSON array when a JSON Path expression is used as a parameter to a JSON function. ([MDEV-22224](https://jira.mariadb.org/browse/MDEV-22224))

```sql
SELECT JSON_REMOVE(@json, '$.A[last]');
```

* A range of indexes can be used to access the values in that range in a JSON array when a JSON Path expression is used as a parameter to a JSON function. ([MDEV-27911](https://jira.mariadb.org/browse/MDEV-27911))

```sql
SELECT JSON_REMOVE(@json, '$.A[1 TO 3]');
```

#### Data Types

The `TIMESTAMP` range of values was extended from '`2038-01-19 03:14:07 UTC`', to '`2106-02-07 06:28:15 UTC`'.\
The storage format is not changed, and new tables can be read by old MariaDB servers as long as timestamp values are within the old timestamp range.

INET4 values can now be compared with INET6 values and can be inserted into INET6 columns; the server does automatically convert INET4 value into INET6 as needed.

UUID data type is added to store UUIDs more efficiently. ([MDEV-4958](https://jira.mariadb.org/browse/MDEV-4958))\
The UUID data type was previously backported to MariaDB Enterprise Server 10.6.9-5.

INET4 data type is added to store IPv4 addresses as BINARY(4), where each byte stores one octet. ([MDEV-23287](https://jira.mariadb.org/browse/MDEV-23287))\
The data type provides the following functionality:\
Validation of incorrect values\
Comparisons\
Sorting\
Functions like `CAST()`

#### Functions

* New time zone options for function `DATE_FORMAT()`
  * The new options %Z and %z can be used for the format string of the function

```sql
DATE_FORMAT(DATE, format)
```

for adding time zone information to the date string.

* %Z Time zone abbreviation
* %z Numeric time zone +hhmm or -hhmm presenting the hour and minute offset from UTC
* Example:

```sql
SELECT DATE_FORMAT(NOW(), '%W %d %M %Y %H:%i:%s %Z %z');
```

```
+--------------------------------------------------+
| DATE_FORMAT(NOW(), '%W %d %M %Y %H:%i:%s %Z %z') |
+--------------------------------------------------+
| Tuesday 21 November 2023 13:28:34 EST -0500      |
+--------------------------------------------------+
```

* SQL function KDF() for key derivation
  * A possible use case is to generate encryption keys from a user provided password or a passphrase. It can be used to generate encryption keys for encryption functions such as `AES_ENCRYPT`.

```sql
KDF(key_str, salt [, {info | iterations} [, kdf_name [, width ]]])
```

```
* `kdf_name` is "hkdf" or "pbkdf2_hmac"
* `width` (in bits) can be any number divisible by 8
* `info` is a non-secret parameter of the hkdf method, it allows to generate different encryption keys for different purposes from the same secret password
* `iterations` is a positive numeric parameter of the pbkdf2_hmac method. Larger values make the password more difficult to brute-force.
```

* Example:

```sql
SELECT hex(kdf('foo', 'bar', 'info', 'hkdf'));
```

```
+----------------------------------------+
| hex(kdf('foo', 'bar', 'info', 'hkdf')) |
+----------------------------------------+
| 710583081D40A55F0B573A76E02D8975       |
+----------------------------------------+
```

```sql
INSERT INTO tbl VALUES (aes_encrypt(@secret_data, kdf("Passw0rd", "NaCl", "info", 'hkdf'), "iv"));
```

* Function `CONV()` now supports conversions up to base 62
  * The function `CONV()`, which converts a number between numeric base systems, now supports conversions up to base 62.
  * This allows conversions to encodings to capital letters A-Z, lower case letters a-z, and numbers 0-9.
  * The old limit was 36, not including lower case letters.
  * Example:

```sql
SELECT CONV(61,10,36);
```

```
+----------------+
| CONV(61,10,36) |
+----------------+
| 1P             |
+----------------+
```

```sql
SELECT CONV(61,10,62);
```

```
+----------------+
| CONV(61,10,62) |
+----------------+
| z              |
+----------------+
```

* [AES\_ENCRYPT()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/encryption-hashing-and-compression-functions/aes_encrypt) and [AES\_DECRYPT()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/encryption-hashing-and-compression-functions/aes_decrypt) allow specifying the initialization vector (iv) and block encryption mode (mode). ([MDEV-9069](https://jira.mariadb.org/browse/MDEV-9069))
  * `AES_ENCRYPT` syntax prior to this release: A`ES_ENCRYPT(<str>, <key_str>)`
  * `AES_ENCRYPT` syntax starting with this release: `AES_ENCRYPT(<str>, <key>, [, iv [, mode]])`
  * `AES_DECRYPT` syntax prior to this release: `AES_DECRYPT(<str>, <key_str>)`
  * `AES_DECRYPT` syntax starting with to this release: `AES_DECRYPT(<str>, <key>, [, iv [, mode]])`
  * The `block_encryption_mode` system variable specifies which mode will be used if the mode is not specified as a function argument.
  * For example, using the default mode from the `block_encryption_mode`:

```sql
SELECT @@block_encryption_mode;
```

```
+-------------------------+
| @@block_encryption_mode |
+-------------------------+
| aes-128-ecb             |
+-------------------------+
```

```sql
SELECT HEX(AES_ENCRYPT('MariaDB','mykey','VECTOR')) AS result;
```

```
+----------------------------------+
| result                           |
+----------------------------------+
| CD0352A4B2FB18A592C04FF8CDA6C2F2 |
+----------------------------------+
```

```sql
SELECT AES_DECRYPT(x'CD0352A4B2FB18A592C04FF8CDA6C2F2','mykey','VECTOR') AS result;
```

```
+---------+
| result  |
+---------+
| MariaDB |
+---------+
```

* For example, specifying the mode as an argument: `<<sql inline=false>>` SELECT HEX(AES\_ENCRYPT('MariaDB','mykey','thisismy256vector','aes-256-cbc')) as result;

```
+----------------------------------+
| result                           |
+----------------------------------+
| CD6C47183B89A813557BFD639A893CE3 |
+----------------------------------+
```

```sql
SELECT AES_DECRYPT(x'CD6C47183B89A813557BFD639A893CE3','mykey','thisismy256vector','aes-256-cbc') AS result;
```

```
+---------+
| result  |
+---------+
| MariaDB |
+---------+
```

* [RANDOM\_BYTES()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/encryption-hashing-and-compression-functions/random_bytes) returns a binary string of a length between 1 and 1024 bytes. ([MDEV-25704](https://jira.mariadb.org/browse/MDEV-25704))
  * This nondeterministic value is generated by the cryptographically secure pseudo random generator (CSPRNG) of the SSL library, so it generates an arbitrary length string of cryptographic random bytes that are suitable for cryptographic use.
* [NATURAL\_SORT\_KEY()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/natural_sort_key) can be used to perform a natural sort of strings. ([MDEV-4742](https://jira.mariadb.org/browse/MDEV-4742))
  * Characters are sorted in alphabetical order, whereas numbers are sorted, such that "10" is greater than "9".
  * For example, "v10" would appear after the string "v9".
* [SFORMAT()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/sformat) formats strings based on the specified options and values to generate a custom formatted string. ([MDEV-25015](https://jira.mariadb.org/browse/MDEV-25015))

```
SELECT SFORMAT("MariaDB version {}", VERSION());
```

* This function uses the fmtlib library for string formatting similar to Python, Rust, C++20.
* `CRC32()` computes a cyclic redundancy check (CRC) as a 32-bit unsigned value using the ISO 3309 polynomial. ([MDEV-27208](https://jira.mariadb.org/browse/MDEV-27208))
  * The CRC can now be computed in pieces, using an optional second parameter: `CRC32('String')` is equal to `CRC32(CRC32('Str','ing'))`.
  * `CRC32C()` can be used to compute checksums using the alternate Castagnoli polynomial.

#### Character Sets and Collations

* The `character_set_collations` system variable allows the default collation for a character set to be changed globally or for a session. ([MDEV-30164](https://jira.mariadb.org/browse/MDEV-30164))
  * Starting with this release, the default collation is used whenever a character set is defined for a database object but the collation is not defined.
  * Starting with this release, when the character set is not defined, the default collation is as specified by the `collation_server` system variable.

```sql
SET @@character_set_collations='utf8mb4=uca1400_ai_ci';
CREATE DATABASE test_with_charset CHARACTER SET utf8mb4;
CREATE DATABASE test;
SELECT SCHEMA_NAME,DEFAULT_COLLATION_NAME FROM SCHEMATA WHERE SCHEMA_NAME LIKE "test%";
```

```
+-------------------+------------------------+
| SCHEMA_NAME       | DEFAULT_COLLATION_NAME |
+-------------------+------------------------+
| test_with_charset | utf8mb4_uca1400_ai_ci  |
| test              | utf8mb4_general_ci     |
+-------------------+------------------------+
```

* Collations based on the Unicode Collation Algorithm (UCA) 14.0.0 have been added for the character sets [utf8mb3, utf8mb4, ucs2, utf16, and utf32](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets): ([MDEV-27009](https://jira.mariadb.org/browse/MDEV-27009))
  * One neutral and 22 language specific collations have been added.
  * Accent sensitive, accent insensitive, case sensitive, case insensitive, no-pad variants have been added.
  * Collation names for new UCA 14.0.0 collations can be specified without the character set prefix, because the character set prefix can be automatically detected from the context. For example, `uca1400_german_as_ci` can be specified instead of `utf8mb4_uca1400_german_as_ci`. Collation names with character set prefixes are accepted for the new UCA 14.0.0 collations, but they are optional.
  * When the [information\_schema.COLLATIONS table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-collations-table) is queried for metadata about the new UCA 14.0.0 collations, the `COLLATION_NAME` column contains the collation name without a character set prefix, and the `CHARACTER_SET_NAME` column contains NULL, which indicates that these collations can apply to multiple character sets.
  * When the [information\_schema.COLLATION\_CHARACTER\_SET\_APPLICABILITY table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-collation_character_set_applicability-table) is queried for character set applicability of the new UCA 14.0.0 collations, the `COLLATION_NAME column also contains the collation name without a character set prefix. A new`FULL\_COLLATION\_NAME`column has been added, which contains the full collation name (with a character set prefix) for all collations, including new UCA 14.0.0 collations.`
  * Improved contraction performance in UCA collations.
  * Improved UCA collation performance for the `utf8mb3` and `utf8mb4` character sets.
* On Microsoft Windows, MariaDB command-line tools now include full Unicode support. ([MDEV-26713](https://jira.mariadb.org/browse/MDEV-26713))
  * Unicode support is available on Microsoft Windows 10 1909 or later, Microsoft Windows 11, and Microsoft Windows Server 2020.
  * The `my.ini` configuration file is now UTF-8 encoded.
  * The `mariadb.exe` command-line client uses [utf8mb4](../11.8/whats-new-in-mariadb-enterprise-server-11.8.md#data-types-and-compatibility) as the default character set.

## Security Features

* Client to server connection now requires SSL encryption by default
  * Using SSL (a more correct term would be TLS, but in reality SSL is more commonly used) has been simplified with MariaDB Enterprise Server 11.4.
  * Before version 11.4, proper SSL configuration required multiple manual steps for the server and all the clients connecting to it.
  * Now the client can verify the server self-signed certificate without any configuration whatsoever. The server completely automatically generates the SSL certificate and the client automatically verifies it as needed.
  * A default configuration now refuses unencrypted connections.
* New Privilege `SHOW CREATE ROUTINE` to enable any user with this privilege to view the definition of a stored routine.
  * Before MariaDB Enterprise Server 11.4 a user only could see the definition of a routine, a stored feature, or function, when:
    * `SELECT` privilege exists for the mysql.procs table
    * The user is the definer of the Stored Procedure
  * `SHOW CREATE ROUTINE` privilege can be granted globally, per schema, or on individual routines.
  * Example without privilege `SHOW CREATE ROUTINE`:

```sql
SHOW grants;
```

```
+--------------------------------------------------+
| Grants for user1@%                               |
+--------------------------------------------------+
| GRANT USAGE ON *.* TO `user1`@`%`                |
| GRANT SELECT, EXECUTE ON `test`.* TO `user1`@`%` |
+--------------------------------------------------+
```

```sql
SHOW CREATE PROCEDURE myProc \G
```

```
*************************** 1. row ***************************
           Procedure: myProc
            sql_mode: STRICT_TRANS_TABLES,ERROR_FOR_DIVISION_BY_ZERO,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION
    Create Procedure: NULL
character_set_client: utf8mb3
collation_connection: utf8mb3_general_ci
  Database Collation: utf8mb4_general_ci
```

* Example with the new privilege SHOW CREATE ROUTINE:

```sql
SHOW grants;
```

```
+-----------------------------------------------------------------------+
| Grants for user1@%                                                    |
+-----------------------------------------------------------------------+
| GRANT USAGE ON *.* TO `user1`@`%`                                     |
| GRANT SELECT, EXECUTE, SHOW CREATE ROUTINE ON `test`.* TO `user1`@`%` |
+-----------------------------------------------------------------------+
```

```sql
SHOW CREATE PROCEDURE myProc \G
```

```
*************************** 1. row ***************************
           Procedure: myProc
            sql_mode: STRICT_TRANS_TABLES,ERROR_FOR_DIVISION_BY_ZERO,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION
    Create Procedure: CREATE DEFINER=`root`@`localhost` PROCEDURE `myProc`()
BEGIN
    SELECT "My Definiton of a Stored Procedure";
END
character_set_client: utf8mb3
collation_connection: utf8mb3_general_ci
  Database Collation: utf8mb4_general_ci
```

* New view in the SYS schema to retrieve user privileges per specific table
  * View privileges\_by\_table\_by\_level in the SYS schema lists the privilege and privilege level per user, schema, and table.
  * Example:

```sql
CREATE DATABASE test;
USE test;
CREATE TABLE t1 (id INT);
CREATE USER user1;
GRANT SELECT, UPDATE ON *.* TO user1;
CREATE USER user2;
GRANT SELECT ON test.* TO user2;
CREATE USER user3;
GRANT SELECT ON test.t1 TO user3;

SELECT * FROM sys.privileges_by_table_by_level WHERE GRANTEE NOT LIKE "'root'@'%'";
```

```
+--------------+------------+-------------+-----------+--------+
| TABLE_SCHEMA | TABLE_NAME | GRANTEE     | PRIVILEGE | LEVEL  |
+--------------+------------+-------------+-----------+--------+
| test         | t1         | 'user1'@'%' | SELECT    | GLOBAL |
| test         | t1         | 'user1'@'%' | UPDATE    | GLOBAL |
| test         | t1         | 'user2'@'%' | SELECT    | SCHEMA |
| test         | t1         | 'user3'@'%' | SELECT    | TABLE  |
+--------------+------------+-------------+-----------+--------+
```

* New Information Schema Table For Password Related Data (MENT-2145)
  * A new information Schema view, USERS, has been added, which DBAs can use to get insights about password related information for a user. This information can be used:
    * by an application to inform a user about a password about to expire or an account which is at risk of being blocked due to the number of wrong passwords entered
    * by DBAs to query users which have been blocked because of too many invalid passwords entered
  * The new view includes the fields:
    * USER – A string including user name and host\
      PASSWORD\_ERRORS – A counter with the current number of wrong passwords entered
      * Reset to 0 when a correct password has been entered
      * An account is blocked, if max\_password\_errors is reached
      * NULL for accounts with privilege CONNECTION ADMIN
    * PASSWORD\_EXPIRATION\_TIME – The date and time when the password expires or NULL, if the password never expires
* New Authentication Plugin — PARSEC (Password Authentication using Response Signed with Elliptic Curves) (MENT-2142)
  * PARSEC improves security over old authentication plugins by introducing salted passwords, time consuming key derivation function, and a client-side scramble to ensure that man-in-the-middle attackers cannot control the client response.
  * Example on how to create a user using the new authentication plugin:

```sql
CREATE USER 'MariaDBUser'@'%' IDENTIFIED VIA PARSEC USING PASSWORD('MyPassword123!');
```

* This will result in:

```sql
SHOW GRANTS FOR MariaDBUser@'%';
Grants FOR MariaDBUser@%
GRANT USAGE ON *.* TO `MariaDBUser`@`%` IDENTIFIED VIA parsec USING 'P0:lhXyNv1cIxpB8EnTxR7ON7S7:1l3rWRW1/jw45yrvYXB8eh02wzk7lcJcz4CMcWw2b+8'
```

* The [password\_reuse\_check plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/password-validation-plugins/password-reuse-check-plugin) implements a way to prevent a user from setting a password that had been set for that user previously. ([MDEV-5245](https://jira.mariadb.org/browse/MDEV-5245))
  * The [password\_reuse\_check\_interval system variable](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/password-validation-plugins/password_reuse_check_interval) specifies the number of days before a password can be reused.
  * The plugin only affects a SQL statement that sets a user password using a literal password string. It cannot check the password of a SQL statement that makes use of a hashed password value.
  * The plugin makes use of password history records stored in the [mysql.password\_reuse\_check\_history system table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysqlpassword_reuse_check_history-table). Each row in the table stores a cryptographic hash and a date. The hashed data includes information about the affected user and the password that is being set. Because it is a one-way cryptographic hash, the stored data cannot be used to extract the prior password values nor which user the historical record is associated with.
  * The `password_reuse_check` plugin was previously backported to MariaDB Enterprise Server 10.4.25-16, 10.5.16-11, and 10.6.8-4.
* [GRANT .. TO PUBLIC](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant) can be used to grant privileges to all currently authenticated users and newly authenticated users on the system. ([MDEV-5215](https://jira.mariadb.org/browse/MDEV-5215))
* [SHOW GRANTS FOR PUBLIC](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-grants) retrieves all privileges granted to public. ([MDEV-5215](https://jira.mariadb.org/browse/MDEV-5215))
* Fine-grained privileges have been removed from the [SUPER privilege](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#super): ([MDEV-29668](https://jira.mariadb.org/browse/MDEV-29668), [MDEV-29596](https://jira.mariadb.org/browse/MDEV-29596))|=Fine-grained privilege removed from [SUPER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#super) as of ES 11.4.4-2|

|                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [READ ONLY ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#read-only-admin)                   |
| [BINLOG ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#binlog-admin)                         |
| [BINLOG MONITOR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#binlog-monitor)                     |
| [FEDERATED ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#federated-admin)                   |
| [REPLICATION MASTER ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replication-master-admin) |
| [REPLICATION SLAVE ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#eplication-slave-admin)    |
| [SET USER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#set-user)                                 |
| [SLAVE MONITOR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#slave-monitor)                       |

**Upon upgrade, each user that has the SUPER privilege will be granted the privileges removed from `SUPER`, so that the user's capabilities will not change.** The `SUPER` privilege is still used for some special cases, including:\
\*\*\* Calling [DES\_ENCRYPT()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/encryption-hashing-and-compression-functions/des_encrypt) and [DES\_DECRYPT()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/encryption-hashing-and-compression-functions/des_decrypt) without an explicit key\*\*\* Dynamically changing certain system variables with [SET GLOBAL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/set-commands/set)\
\*\*\* Changing certain debug settings\*\* Due to this change, the consistency of read-only replicas are now protected when users with the `SUPER` privilege attempt to write to a read-only replica if they do not also have the [READ ONLY ADMIN privilege](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#read-only-admin).\
\*\*\* Read-only replicas are replica servers that have [read\_only=1](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#read_only) set to ensure that they stay consistent with the primary.\*\*\* If a user with the `SUPER` privilege requires write access to a read-only replica server, the user must be explicitly granted the `READ ONLY ADMIN` privilege.

## MariaDB Replication

* New option to limit the space used by binary bogs per server instance
  * The new system variable `max_binlog_total_size` (alias `binlog_space_limit`) enables binary log purging when the total size of all binary logs exceeds the specified threshold.
  * The default for `max_binlog_total_size` is 0, meaning that there is no limit.
  * The system variable can be changed without restarting the server.
* New system variable `--slave-connections-needed-for-purge` set to 1 by default.
  * Assures that binary log purging will not happen until at least that many replicas are connected and do not need purged binary logs anymore.
* New status variable `binlog_disk_use` provides the disk space currently used by the binary logs.
* New options `SQL_BEFORE_GTIDS` and `SQL_AFTER_GTIDS` for `START REPLICA UNTIL`
  * The new options `SQL_BEFORE_GTIDS` and `SQL_AFTER_GTIDS` for `START REPLICA UNTIL` allow the user to control of whether the replica stops before or after a provided GTID state.
    * Its syntax is:

```sql
START SLAVE UNTIL (SQL_BEFORE_GTIDS|SQL_AFTER_GTIDS)="<gtid_list>"
```

* When providing `SQL_BEFORE_GTIDS="<gtid_list>"`, for each domain specified in the gtid\_list, the replica will execute transactions up to the GTID found, and immediately stop processing events in that domain without executing the transaction of the specified GTID. Once all domains have stopped, the replica will stop. Events originating from domains that are not specified in the list are not replicated.
* `START SLAVE UNTIL SQL_AFTER_GTIDS="<gtid_list>"` is an alias to the default behavior of `START SLAVE UNTIL master_gtid_pos="<gtid_list>"`, the known behavior before MariaDB Enterprise Server 11.4.
* The replica will execute transactions originating from domain ids provided in the list, and will stop once all transactions provided in the `UNTIL` list have all been executed.
* An index is now created on the GTIDs of the binary log, which allows a connecting replica to find the position it should start from without the need to scan the whole binary log.
  * The new system variable `binlog_gtid_index` (default `ON`) can be used to disable the creation of indexes.
  * The new system variable `binlog_gtid_index_page_size` (default `4096`) defines the page size to use for the binary log GTID index.
  * The new system variable `binlog_gtid_index_span_min` (default `65536`) controls the sparseness of the binary log GTID index.
  * The new status variables `binlog_gtid_index_hit` and `binlog_gtid_index_miss` can be used for monitoring purposes. A miss is an indication that the index file is missing.
* GTID binlog events now include the thread ID (MENT-2180)
  * The thread ID and the corresponding statement can now be retrieved from binary logs
  * The output of mariadb-binlog also includes the thread ID
* Binary log filter options `binlog-do-db`, `binlog-ignore-db`, and `binlog-row-event-max-size` are now visible as system variables. ([MDEV-30188](https://jira.mariadb.org/browse/MDEV-30188))
  * For example:

```sql
SHOW GLOBAL VARIABLES WHERE
  Variable_name LIKE 'binlog_do_db' OR
  Variable_name LIKE 'binlog_ignore_db' OR
  Variable_name LIKE 'binlog_row_event_max_size';
```

```
+---------------------------+-------+
| Variable_name             | Value |
+---------------------------+-------+
| binlog_do_db              |       |
| binlog_ignore_db          |       |
| binlog_row_event_max_size | 8192  |
+---------------------------+-------+
```

* For all storage engines, [ALTER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table) is divided into two phases to prevent long-running DDL statements from causing replication lag on replicas: ([MDEV-11675](https://jira.mariadb.org/browse/MDEV-11675))
  * Enabled by setting [binlog\_alter\_two\_phase=1](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#binlog_alter_two_phase), which is not the default.
  * Two-phase `ALTER TABLE` is optimistic, so the operation begins on the replica server before it finishes on the primary server.
  * Two events are written to the binary log on the primary server: a `START ALTER` event when the operation starts, and either a `COMMIT ALTER` event or a `ROLLBACK ALTER` event when the operation finishes depending on whether it succeeds or fails.
* By default, replication uses Global Transaction IDs (GTID), which makes replicas crash-safe. ([MDEV-19801](https://jira.mariadb.org/browse/MDEV-19801))
  * This change impacts backward compatibility.
  * In previous releases, when [CHANGE MASTER](https://github.com/mariadb-corporation/docs-release-notes/blob/test/mariadb-enterprise-server-release-notes/mariadb-enterprise-server-11-4/change-master/README.md) TO was executed without explicitly specifying `MASTER_USE_GTID`, it would default to `MASTER_USE_GTID=no`.
  * Starting with this release, when [CHANGE MASTER TO](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/replication-statements/change-master-to) is executed without explicitly specifying MASTER\_USE\_GTID, it defaults to `MASTER_USE_GTID=slave_pos`. With `MASTER_USE_GTID=slave_pos`, the replica server uses the [gtid\_slave\_pos system variable](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/gtid) as the GTID position.
  * This change can cause new behavior to occur when performing the following operations:
    * Setting up a new replica with [CHANGE MASTER TO](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/replication-statements/change-master-to) without specifying `MASTER_USE_GTID`
    * Freshly starting a stopped replica with [START REPLICA](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/replication-statements/start-replica) if the replica configuration does not explicitly have `MASTER_USE_GTID` set.
    * Resetting a replica with [RESET REPLICA](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/replication-statements/reset-replica)
  * When `MASTER_LOG_FILE` and `MASTER_LOG_POS` are explicitly set, `MASTER_USE_GTID=no` is implicitly set.
* For mariadb-binlog, the start and stop positions can be specified as GTIDs: ([MDEV-4989](https://jira.mariadb.org/browse/MDEV-4989))

```bash
$ mariadb-binlog --start-position='0-1-1001,1-2-1000' \
 --stop-position='0-1-2000,1-2-1050' \
 mariadb-bin.000001
```

* The --start-position command-line option can set the starting GTID position as a comma-separated list of GTIDs. For each specified GTID domain, the GTID position is exclusive, so an event is only printed if its sequence number is greater than the sequence number specified for that domain.
* The --stop-position command-line option can set the ending GTID position as a comma-separated list of GTIDs. For each specified GTID domain, the GTID position is inclusive, so an event is only printed if its sequence number is greater than or equal to the sequence number specified for that domain.
* Both command-line options require each GTID in the comma-separated list to have a different domain ID.
* For [mariadb-binlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog), events can be filtered based on the domain IDs and server IDs in the event's GTID: ([MDEV-4989](https://jira.mariadb.org/browse/MDEV-4989), [MDEV-20119](https://jira.mariadb.org/browse/MDEV-20119))

```bash
$ mariadb-binlog --do-domain-ids='0,1' \
 --do-server-ids='1,2' \
 mariadb-bin.000001
```

* The --do-domain-ids command-line option can set domain IDs that should be read as a comma-separated list of domain IDs. If an event's GTID does not have one of the specified domain IDs, the event is not printed.
* The --ignore-domain-ids command-line option can set domain IDs that should be ignored as a comma-separated list of domain IDs. If an event's GTID has one of the specified domain IDs, the event is not printed.$ mariadb-binlog --start-position='0-1-1001,1-2-1000' \ --stop-position='0-1-2000,1-2-1050' mariadb-bin.000001
* The --start-position command-line option can set the starting GTID position as a comma-separated list of GTIDs. For each specified GTID domain, the GTID position is exclusive, so an event is only printed if its sequence number is greater than the sequence number specified for that domain.
* The --stop-position command-line option can set the ending GTID position as a comma-separated list of GTIDs. For each specified GTID domain, the GTID position is inclusive, so an event is only printed if its sequence number is greater than or equal to the sequence number specified for that domain.
* Both command-line options require each GTID in the comma-separated list to have a different domain ID.

## Galera Cluster

* The following changes pertain to Galera Cluster with MariaDB Enterprise Server 11.4:
* Automatic SST User Account Management with Galera (MENT-2144)
  * The State Snapshot Transfer (SST) method, needed to provide a full data copy to a new node, requires a dedicated account to access the remote server (donor) during the SST process.
  * MariaDB Enterprise Cluster (Galera) now creates the user internally for the time of an SST, which makes the need to have an account created manually obsolete. This removes the requirement to have a user and password provided via a configuration file. Having the user created by Galera also ensures that the needed privileges are set.
* New connection states in [SHOW \[FULL\] PROCESSLIST](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-processlist) and [information\_schema.PROCESSLIST](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-processlist-table) better reflect the state of the connection: ([MDEV-26352](https://jira.mariadb.org/browse/MDEV-26352))

| Connection State                | Description                                                                                                                                                                                                                                                                                                      |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| waiting to execute in isolation | The connection is executing a DDL statement with [wsrep\_osu\_method=TOI](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_osu_method), but the operation requires other concurrent operations to finish first, so the DDL statement can be executed in isolation. |
| waiting for TOI DDL             | Another connection is executing a DDL statement with [wsrep\_osu\_method=TOI](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_osu_method), so this connection must wait for the DDL statement to finish.                                                          |
| waiting for flow control        | The connection is committing a transaction, but transactions are currently paused due to flow control, so the connection is waiting for the cluster to catch up and unpause transactions.                                                                                                                        |
| waiting for certification       | The connection is committing a transaction, but it is waiting for the other cluster nodes to certify the transaction.                                                                                                                                                                                            |

* Node state changes can be saved to a machine-readable JSON file configured by the [wsrep\_status\_file system variable](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_status_file): ([MDEV-26971](https://jira.mariadb.org/browse/MDEV-26971))

```
[mariadb]
wsrep_status_file=galera_status.json
```

* The JSON file can be read by monitoring tools.
* When `wsrep_status_file` is set to a path, the node state changes are written to the specified file.
* When `wsrep_status_file` is set to `none`, this functionality is disabled.
* Progress reporting for MariaDB Enterprise Backup-based SST by configuring the progress option in the \[`sst`] option group: ([MDEV-26971](https://jira.mariadb.org/browse/MDEV-26971))

```
[mariadb]
wsrep_sst_method=mariadb-backup
wsrep_debug=1
[sst]
progress=1
rlimit=100m
```

* Progress reporting is only supported for MariaDB Enterprise Backup-based SST, so [wsrep\_sst\_method=mariadb-backup](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_sst_method) must be set.
* Progress reporting is only enabled when [wsrep\_debug=1](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_debug) is set.
* When `progress=1` is set, progress reporting goes to standard error (`stderr`).
* When `progress` is set to a path, progress reporting is written to the specified file.
* When `progress` is set to none, progress reporting is disabled.
* `rlimit` can be used to set a rate limit in bytes. The value can use a suffix to represent a unit: k for kilobytes, `m` for megabytes, `g` for gigabytes, and `t` for terabytes.
* The `pv` utility must be installed for SST progress reporting.
* When progress reporting is enabled, the following SST progress message is written to the MariaDB log during an SST:
* When `wsrep_status_file` is set to `none`, this functionality is disabled.
* Progress reporting for MariaDB Enterprise Backup-based SST by configuring the progress option in the \[sst] option group: ([MDEV-26971](https://jira.mariadb.org/browse/MDEV-26971))

```
[mariadb]
wsrep_sst_method=mariadb-backup
wsrep_debug=1
[sst]
progress=1
rlimit=100m
```

* Progress reporting is only supported for MariaDB Enterprise Backup-based SST, so [wsrep\_sst\_method=mariadb-backup](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_sst_method) must be set.
* Progress reporting is only enabled when [wsrep\_debug=1](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_debug) is set.
* When `progress=1` is set, progress reporting goes to standard error (`stderr`).
* When `progress` is set to a path, progress reporting is written to the specified file.
* When `progress` is set to none, progress reporting is disabled.
* rlimit can be used to set a rate limit in bytes. The value can use a suffix to represent a unit: `k` for kilobytes, `m` for megabytes, `g` for gigabytes, and `t` for terabytes.
* The `pv` utility must be installed for SST progress reporting.
* When progress reporting is enabled, the following SST progress message is written to the MariaDB log during an SST:

## Platforms

In alignment with [enterprise lifecycle](../enterprise-server-lifecycle.md), MariaDB Enterprise Server 11.4.4-2 is provided for:

Debian 11 (x86\_64, ARM64)

Debian 12 (x86\_64, ARM64)

Red Hat Enterprise Linux 8 (x86\_64, ARM64)

Red Hat Enterprise Linux 9 (x86\_64, ARM64, PPC64LE)

AlmaLinux 8 (x86\_64, ARM64)

AlmaLinux 9 (x86\_64, ARM64)

Rocky Linux 8 (x86\_64, ARM64)

Rocky Linux 9 (x86\_64, ARM64)

SUSE Linux Enterprise Server 15 (x86\_64, ARM64)

Ubuntu 20.04 (x86\_64, ARM64)

Ubuntu 22.04 (x86\_64, ARM64)

Ubuntu 24.04 (x86\_64, ARM64)

Microsoft Windows (x86\_64) (Without MariaDB Enterprise Cluster (Galera) support)

Red Hat UBI 8 (x86\_64, ARM64)

Red Hat UBI 8 is part of the Enterprise Server Docker Image. It does not support MariaDB Enterprise Cluster (Galera) or MariaDB ColumnStore.

Some components of MariaDB Enterprise Server might not support all platforms. For additional information, see [MariaDB Corporation Engineering Policies".](https://mariadb.com/engineering-policies)

## Installation Instructions

[Deploy MariaDB Enterprise with Repositories](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/architecture/topologies/single-node-topologies/enterprise-server)

[Deploy MariaDB Enterprise with Package Tarballs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/package-tarballs)

[Deploy MariaDB Enterprise with Docker](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/automated-mariadb-deployment-and-administration/docker-and-mariadb/deploy-mariadb-enterprise-server-with-docker)

## Upgrade Instructions

[Upgrade to MariaDB Enterprise Server 11.4](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/upgrading/upgrades/upgrade-to-mariadb-enterprise-server-11.4)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
