# ANALYZE TABLE

## Syntax

```sql
ANALYZE [NO_WRITE_TO_BINLOG | LOCAL] TABLE tbl_name [,tbl_name ...]
  [PERSISTENT FOR 
    { ALL
      | COLUMNS ([col_name [,col_name ...]]) INDEXES ([index_name [,index_name ...]])
    }
  ]
```

## Description

`ANALYZE TABLE` analyzes and stores the key distribution for a table ([index statistics](../../../ha-and-performance/optimization-and-tuning/optimization-and-indexes/index-statistics.md)). This statement works with [MyISAM](../../../server-usage/storage-engines/myisam-storage-engine/), [Aria](../../../server-usage/storage-engines/aria/) and [InnoDB](../../../server-usage/storage-engines/innodb/) tables. During the analysis, InnoDB will allow reads/writes, and MyISAM/Aria reads/inserts. For MyISAM tables, this statement is equivalent to using [myisamchk --analyze](../../../clients-and-utilities/myisam-clients-and-utilities/myisamchk.md).

`ANALYZE` uses histograms, which can provide a better selectivity than InnoDB statistics offer. InnoDB statistics work with a limited sample set and is therefore not as accurate as persistent statistics can be. For more information on how the analysis works within InnoDB, see [InnoDB Limitations](../../../server-usage/storage-engines/innodb/innodb-limitations.md#table-analysis).

MariaDB uses the stored key distribution to decide the order in which tables should be joined when you perform a join on something other than a constant. In addition, key distributions can be used when deciding which indexes to use for a specific table within a query.

This statement requires [SELECT and INSERT privileges](../account-management-sql-statements/grant.md) for the table.

By default, ANALYZE TABLE statements are written to the [binary log](../../../server-management/server-monitoring-logs/binary-log/) and will be [replicated](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/sql-statements/table-statements/broken-reference/README.md). The `NO_WRITE_TO_BINLOG` keyword (`LOCAL` is an alias) will ensure the statement is not written to the binary log.

`ANALYZE TABLE` statements are not logged to the binary log if [read\_only](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#read_only) is set. See also [Read-Only Replicas](../../../ha-and-performance/standard-replication/read-only-replicas.md).

{% tabs %}
{% tab title="Current" %}
`ANALYZE TABLE` is non-blocking and non-intrusive. A connection will start using new statistics for the query following the completion of the `ANALYZE TABLE`.
{% endtab %}

{% tab title="< 10.6.16" %}
`ANALYZE TABLE` is blocking and intrusive.
{% endtab %}
{% endtabs %}

`ANALYZE TABLE` is also supported for partitioned tables. You can use [`ALTER TABLE`](../data-definition/alter/alter-table/#analyze-partition) `... ANALYZE PARTITION` to analyze one or more partitions.

The [Aria](../../../server-usage/storage-engines/aria/) storage engine supports [progress reporting](../administrative-sql-statements/show/show-processlist.md) for the `ANALYZE TABLE` statement.

### Skipping Long CHAR/VARCHAR Columns

When using `ANALYZE TABLE PERSISTENT`  MariaDB, skip long `CHAR`/`VARCHAR` columns during statistics collection if they exceed the value of the `analyze_max_length` system variable.

This prevents excessive disk usage when analyzing tables with large text columns.

* If a column is longer than `analyze_max_length`, it is excluded from stats.
* If a long column is **explicitly specified** in `FOR COLUMNS()`, it is **still analyzed**, regardless of its size.

Example

```sql
SET GLOBAL analyze_max_length = 50000;
ANALYZE TABLE large_text_table PERSISTENT;
```

```sql
ANALYZE TABLE large_text_table PERSISTENT FOR COLUMNS(long_description);
```

```sql
CREATE TABLE product_data (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    description VARCHAR(50000), -- long column
    specs VARCHAR(1000)
);

-- Set limit
SET SESSION analyze_max_length = 10000;

-- Run analysis without explicitly selecting columns
ANALYZE TABLE product_data PERSISTENT;

-- 'description' will be skipped due to length > 10000

-- To include it anyway
ANALYZE TABLE product_data PERSISTENT FOR COLUMNS(description);

```

## Performance Impact

Note that analyzing tables with `ANALYZE` can have a performance impact and can use a lot of disk space for big tables. As column statistics usually do not change much over time, even when the table grows, there is no benefit to running `ANALYZE` very often.

Running `ANALYZE` is indicated:

* for newly populated tables,
* for tables that have additional columns added that are used in WHERE clauses,
* when a table has doubled in size,
* when you note that a query becomes slow because the table order has changed and you can see from [EXPLAIN](../administrative-sql-statements/analyze-and-explain-statements/explain.md) or [ANALYZE FORMAT=JSON](../administrative-sql-statements/analyze-and-explain-statements/analyze-format-json.md) that the selectivity is wrong for a table.

{% hint style="warning" %}
`ANALYZE` isn’t useful for table columns of type `UNIQUE`, `PRIMARY KEY`, `TIME`, or `CURRENT_TIME`. In `ANALYZE` queries, you should omit columns of those types.
{% endhint %}

## Engine-Independent Statistics / PERSISTENT FOR

`ANALYZE TABLE` supports [engine-independent statistics](../../../ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/engine-independent-table-statistics.md). See [Engine-Independent Table Statistics: Collecting Statistics with the ANALYZE TABLE Statement](../../../ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/engine-independent-table-statistics.md#collecting-statistics-with-the-analyze-table-statement) for more information.

Engine-independent statistics can be controlled (enabled and disabled) using the [use\_stat\_tables variable](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#use_stat_tables) and the [optimizer\_use\_condition\_selectivity variable](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#optimizer_use_condition_selectivity). InnoDB-persistent statistics are controlled with the [innodb\_stats\_persistent variable](../../../server-usage/storage-engines/innodb/innodb-system-variables.md#innodb_stats_persistent). Combining both kinds of statistics is possible.

The server relies on InnoDB statistics by default. That way, it can use some statistics even if `ANALYZE TABLE` is never run (or not often enough). This gives good enough results for the majority of queries. Some queries, however, need more statistical data so the optimizer can create a good plan. Slow queries indicate there aren't enough statistical data. Those queries can be accelerated by running `ANALYZE TABLE tbl PERSISTENT FOR ...`, where `tbl` indicates a table used by a slow query. You can also run `ANALYZE TABLE ... PERSISTENT FOR ALL`, but that has a significant performance impact.

## Useful Variables

The following overview indicates when a particular variable was introduced. When multiple versions are given, it means variable options (like the default value) changed between the indicated versions.

| Variable                                                                                                                                                  | Introduced in MariaDB version | Description                                                                                                                                                                                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [analyze\_sample\_percentage](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#analyze_sample_percentage)  | 10.4.3                        | Percentage of rows from the table ANALYZE TABLE will sample to collect table statistics. Set to 0 to let MariaDB decide what percentage of rows to sample.                                                                                                                                                          |
| [histogram\_type](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#histogram_type)                         | 10.4.3-11.0                   | Specifies the type of histograms created by ANALYZE. Options are #SINGLE\_PREC\_HB,DOUBLE\_PREC\_HB or JSON\_HB.                                                                                                                                                                                                    |
| [histogram\_size](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#histogram_size)                         | 10.7                          | Number of bytes or buckets (in case of JSON\_HB) used for storing the histogram. If set to 0, no histograms are created by ANALYZE.]]                                                                                                                                                                               |
| [log\_slow\_admin\_statements](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_slow_admin_statements) | 11.0.1                        | Log slow OPTIMIZE, ANALYZE, ALTER and other administrative statements to the slow log if it is open. Deprecated. Use [log\_slow\_filter](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_slow_filter) instead.                                                  |
| [log\_slow\_filter](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_slow_filter)                      | (all versions)                | Having admin in log\_slow\_filter will add slow ANALYZE\_TABLE statements to the slow log.                                                                                                                                                                                                                          |
| [sort\_buffer\_size](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#sort_buffer_size)                    | (all versions)                | For calculating the number of duplicates, ANALYZE TABLE uses a buffer of [sort\_buffer\_size](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#sort_buffer_size) bytes per column. You can slightly increase the speed of ANALYZE TABLE by increasing this variable. |

## Examples

```sql
-- update all engine-independent statistics for all columns and indexes
ANALYZE TABLE tbl PERSISTENT FOR ALL;

-- update specific columns and indexes:
ANALYZE TABLE tbl PERSISTENT FOR COLUMNS (col1,col2,...) INDEXES (idx1,idx2,...);

-- empty lists are allowed:
ANALYZE TABLE tbl PERSISTENT FOR COLUMNS (col1,col2,...) INDEXES ();
ANALYZE TABLE tbl PERSISTENT FOR COLUMNS () INDEXES (idx1,idx2,...);

-- the following will only update mysql.table_stats fields:
ANALYZE TABLE tbl PERSISTENT FOR COLUMNS () INDEXES ();

-- when use_stat_tables is set to 'COMPLEMENTARY' or 'PREFERABLY', 
-- a simple ANALYZE TABLE  collects engine-independent statistics for all columns and indexes.
SET SESSION use_stat_tables='COMPLEMENTARY';
ANALYZE TABLE tbl;
```

## See Also

* [This one trick can make MariaDB 30x faster!](https://mariadb.org/mariadb-30x-faster/) (mariadb.org blog)
* [Index Statistics](../../../ha-and-performance/optimization-and-tuning/optimization-and-indexes/index-statistics.md)
* [InnoDB Persistent Statistics](../../../ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/innodb-persistent-statistics.md)
* [Progress Reporting](../administrative-sql-statements/show/show-processlist.md)
* [Engine-independent Statistics](../../../ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/engine-independent-table-statistics.md)
* [Histogram-based Statistics](../../../ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/histogram-based-statistics.md)
* [ANALYZE Statement](../administrative-sql-statements/analyze-and-explain-statements/analyze-statement.md)

<sub>_This page is licensed: GPLv2, originally from_</sub> [<sub>_fill\_help\_tables.sql_</sub>](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)

{% @marketo/form formId="4316" %}
