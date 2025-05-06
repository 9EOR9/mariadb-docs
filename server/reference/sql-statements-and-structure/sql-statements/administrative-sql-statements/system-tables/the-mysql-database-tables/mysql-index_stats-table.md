
# mysql.index_stats Table

The `mysql.index_stats` table is one of three tables storing data used for [Engine-independent table statistics](../../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/engine-independent-table-statistics.md). The others are [mysql.column_stats](mysql-column_stats-table.md) and [mysql.table_stats](mysql-table_stats-table.md).


It is populated when the [ANALYZE TABLE](../../../table-statements/analyze-table.md) statement is run, although not by default. See [Collecting Statistics with the ANALYZE TABLE Statement](../../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/engine-independent-table-statistics.md#collecting-statistics-with-the-analyze-table-statement) for details.


It is possible to manually update the table and, unlike most system tables, there are some scenarios where this could be useful. See [Manual updates to statistics tables](../../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/engine-independent-table-statistics.md#manual-updates-to-statistics-tables) for details.


This table uses the [Aria](../../../../../storage-engines/aria/README.md) storage engine.


The `mysql.index_stats` table contains the following fields:



| Field | Type | Null | Key | Default | Description |
| --- | --- | --- | --- | --- | --- |
| Field | Type | Null | Key | Default | Description |
| db_name | varchar(64) | NO | PRI | NULL | Database the table is in. |
| table_name | varchar(64) | NO | PRI | NULL | Table name |
| index_name | varchar(64) | NO | PRI | NULL | Name of the index |
| prefix_arity | int(11) unsigned | NO | PRI | NULL | Index prefix length. 1 for the first keypart, 2 for the first two, and so on. InnoDB's extended keys are supported. |
| avg_frequency | decimal(12,4) | YES |  | NULL | Average number of records one will find for given values of (keypart1, keypart2, ..), provided the values will be found in the table. |



It is possible to manually update the table. See [Manual updates to statistics tables](../../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/engine-independent-table-statistics.md#manual-updates-to-statistics-tables) for details.


CC BY-SA / Gnu FDL

