# Partition Pruning and Selection

When a WHERE clause is related to the partitioning expression, the optimizer knows which partitions are relevant for the query. Other partitions will not be read. This optimization is called *partition pruning*.

[EXPLAIN PARTITIONS](../../clients-and-utilities/explain-analyzer.md) can be used to know which partitions will be read for a given query. A column called `partitions` will contain a comma-separated list of the accessed partitions. For example:

```
EXPLAIN PARTITIONS SELECT * FROM orders WHERE id < 15000000;
+------+-------------+--------+------------+-------+---------------+---------+---------+------+------+-------------+
| id | select_type | table | partitions | type | possible_keys | key | key_len | ref | rows | Extra |
+------+-------------+--------+------------+-------+---------------+---------+---------+------+------+-------------+
| 1 | SIMPLE | orders | p0,p1 | range | PRIMARY | PRIMARY | 4 | NULL | 2 | Using where |
+------+-------------+--------+------------+-------+---------------+---------+---------+------+------+-------------+
```

Sometimes the WHERE clause does not contain the necessary information to use partition pruning, or the optimizer cannot infer this information. However, we may know which partitions are relevant for the query. Since [MariaDB 10.0](/kb/en/what-is-mariadb-100/), we can force MariaDB to only access the specified partitions by adding a PARTITION clause. This feature is called *partition selection*. For example:

```
SELECT * FROM orders PARTITION (p3) WHERE user_id = 50;
SELECT * FROM orders PARTITION (p2,p3) WHERE user_id >= 40;
```

The PARTITION clause is supported for all DML statements:

* [SELECT](../../server-usage/replication-cluster-multi-master/standard-replication/selectively-skipping-replication-of-binlog-events.md)
* [INSERT](../../server-usage/programming-customizing-mariadb/views/inserting-and-updating-with-views.md)
* [UPDATE](../../reference/sql-statements-and-structure/sql-statements/data-manipulation/changing-deleting-data/update.md)
* [DELETE](../../reference/sql-statements-and-structure/sql-statements/data-manipulation/changing-deleting-data/delete.md)
* [REPLACE](../../clients-and-utilities/replace-utility.md)

#

# Partition Pruning and Triggers

In general, partition pruning is applied to statements contained in [triggers](../../server-usage/programming-customizing-mariadb/triggers-events/triggers/triggers-and-implicit-locks.md).

However, note that if a `BEFORE INSERT` or `BEFORE UPDATE` trigger is defined on a table, MariaDB doesn't know in advance if the columns used in the partitioning expression will be changed. For this reason, it is forced to lock all partitions.