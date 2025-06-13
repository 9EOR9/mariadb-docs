# LIMIT

## Description

Use the `LIMIT` clause to restrict the number of returned rows. When you use a single\
integer _n_ with `LIMIT`, the first _n_ rows will be returned. Use the [ORDER BY](order-by.md)\
clause to control which rows come first. You can also select a number of rows after an offset\
using either of the following:

```
LIMIT offset, row_count
LIMIT row_count OFFSET offset
```

When you provide an offset _m_ with a limit _n_, the first _m_ rows will be ignored, and the\
following _n_ rows will be returned.

Executing an [UPDATE](../changing-deleting-data/update.md) with the `LIMIT` clause is not safe for replication. `LIMIT 0` is an exception to this rule (see [MDEV-6170](https://jira.mariadb.org/browse/MDEV-6170)).

There is a [LIMIT ROWS EXAMINED](../../../../ha-and-performance/optimization-and-tuning/query-optimizations/limit-rows-examined.md) optimization which provides the\
means to terminate the execution of [SELECT](select.md) statements which examine too\
many rows, and thus use too many resources. See [LIMIT ROWS EXAMINED](../../../../ha-and-performance/optimization-and-tuning/query-optimizations/limit-rows-examined.md).

### Multi-Table Updates

Until [MariaDB 10.3.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1031-release-notes), it was not possible to use `LIMIT` (or [ORDER BY](order-by.md)) in a multi-table [UPDATE](../changing-deleting-data/update.md) statement. This restriction was lifted in [MariaDB 10.3.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1032-release-notes).

### GROUP\_CONCAT

Starting from [MariaDB 10.3.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1033-release-notes), it is possible to use `LIMIT` with [GROUP\_CONCAT()](../../../sql-functions/aggregate-functions/group_concat.md).

## Examples

```
CREATE TABLE members (name VARCHAR(20));
INSERT INTO members VALUES('Jagdish'),('Kenny'),('Rokurou'),('Immaculada');

SELECT * FROM members;
+------------+
| name       |
+------------+
| Jagdish    |
| Kenny      |
| Rokurou    |
| Immaculada |
+------------+
```

Select the first two names (no ordering specified):

```
SELECT * FROM members LIMIT 2;
+---------+
| name    |
+---------+
| Jagdish |
| Kenny   |
+---------+
```

All the names in alphabetical order:

```
SELECT * FROM members ORDER BY name;
+------------+
| name       |
+------------+
| Immaculada |
| Jagdish    |
| Kenny      |
| Rokurou    |
+------------+
```

The first two names, ordered alphabetically:

```
SELECT * FROM members ORDER BY name LIMIT 2;
+------------+
| name       |
+------------+
| Immaculada |
| Jagdish    |
+------------+
```

The third name, ordered alphabetically (the first name would be offset zero, so the third is offset two):

```
SELECT * FROM members ORDER BY name LIMIT 2,1;
+-------+
| name  |
+-------+
| Kenny |
+-------+
```

From [MariaDB 10.3.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1032-release-notes), `LIMIT` can be used in a multi-table update:

```
CREATE TABLE warehouse (product_id INT, qty INT);
INSERT INTO warehouse VALUES (1,100),(2,100),(3,100),(4,100);

CREATE TABLE store (product_id INT, qty INT);
INSERT INTO store VALUES (1,5),(2,5),(3,5),(4,5);

UPDATE warehouse,store SET warehouse.qty = warehouse.qty-2, store.qty = store.qty+2 
  WHERE (warehouse.product_id = store.product_id AND store.product_id  >= 1) 
    ORDER BY store.product_id DESC LIMIT 2;

SELECT * FROM warehouse;
+------------+------+
| product_id | qty  |
+------------+------+
|          1 |  100 |
|          2 |  100 |
|          3 |   98 |
|          4 |   98 |
+------------+------+

SELECT * FROM store;
+------------+------+
| product_id | qty  |
+------------+------+
|          1 |    5 |
|          2 |    5 |
|          3 |    7 |
|          4 |    7 |
+------------+------+
```

From [MariaDB 10.3.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1033-release-notes), `LIMIT` can be used with [GROUP\_CONCAT](../../../sql-functions/aggregate-functions/group_concat.md), so, for example, given the following table:

```
CREATE TABLE d (dd DATE, cc INT);

INSERT INTO d VALUES ('2017-01-01',1);
INSERT INTO d VALUES ('2017-01-02',2);
INSERT INTO d VALUES ('2017-01-04',3);
```

the following query:

```
SELECT SUBSTRING_INDEX(GROUP_CONCAT(CONCAT_WS(":",dd,cc) ORDER BY cc DESC),",",1) FROM d;
+----------------------------------------------------------------------------+
| SUBSTRING_INDEX(GROUP_CONCAT(CONCAT_WS(":",dd,cc) ORDER BY cc DESC),",",1) |
+----------------------------------------------------------------------------+
| 2017-01-04:3                                                               |
+----------------------------------------------------------------------------+
```

can be more simply rewritten as:

```
SELECT GROUP_CONCAT(CONCAT_WS(":",dd,cc) ORDER BY cc DESC LIMIT 1) FROM d;
+-------------------------------------------------------------+
| GROUP_CONCAT(CONCAT_WS(":",dd,cc) ORDER BY cc DESC LIMIT 1) |
+-------------------------------------------------------------+
| 2017-01-04:3                                                |
+-------------------------------------------------------------+
```

## See Also

* [OFFSET ... FETCH](select-offset-fetch.md) Like limit, but also support `WITH TIES`
* [ROWNUM() function](../../../sql-functions/secondary-functions/information-functions/rownum.md)
* [SELECT](select.md)
* [UPDATE](../changing-deleting-data/update.md)
* [DELETE](../changing-deleting-data/delete.md)
* [Joins and Subqueries](joins-subqueries/)
* [ORDER BY](order-by.md)
* [GROUP BY](group-by.md)
* [Common Table Expressions](common-table-expressions/)
* [SELECT WITH ROLLUP](select-with-rollup.md)
* [SELECT INTO OUTFILE](select-into-outfile.md)
* [SELECT INTO DUMPFILE](select-into-dumpfile.md)
* [FOR UPDATE](for-update.md)
* [LOCK IN SHARE MODE](lock-in-share-mode.md)
* [Optimizer Hints](optimizer-hints.md)
* [SELECT ... OFFSET ... FETCH](select-offset-fetch.md)

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
