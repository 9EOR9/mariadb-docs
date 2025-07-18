# LAST\_INSERT\_ID

## Syntax

```sql
LAST_INSERT_ID(), LAST_INSERT_ID(expr)
```

## Description

`LAST_INSERT_ID()` (no arguments) returns the first automatically generated value successfully inserted for an [AUTO\_INCREMENT](../../../data-types/auto_increment.md) column as a result of the most recently executed `INSERT`\
statement. The value of `LAST_INSERT_ID()` remains unchanged if no rows are successfully inserted.

If one gives an argument to `LAST_INSERT_ID()`, then it will return the value of the expression and\
the next call to `LAST_INSERT_ID()` will return the same value. The value is also sent to the client\
and can be accessed by the [mysql\_insert\_id](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/api-functions/mysql_insert_id) function.

For example, after inserting a row that generates an `AUTO_INCREMENT` value, you can get the value like this:

```sql
SELECT LAST_INSERT_ID();
+------------------+
| LAST_INSERT_ID() |
+------------------+
|                9 |
+------------------+
```

You can also use `LAST_INSERT_ID()` to delete the last inserted row:

```sql
DELETE FROM product WHERE id = LAST_INSERT_ID();
```

If no rows were successfully inserted, `LAST_INSERT_ID()` returns 0.

You can also use [INSERT...RETURNING](../../../sql-statements/data-manipulation/inserting-loading-data/insertreturning.md) for this purpose.

The value of `LAST_INSERT_ID()` will be consistent across all versions if all rows in the [INSERT](../../../sql-statements/data-manipulation/inserting-loading-data/insert.md) or [UPDATE](../../../sql-statements/data-manipulation/changing-deleting-data/update.md) statement were successful.

The currently executing statement does not affect the value of `LAST_INSERT_ID()`. Suppose that you generate an `AUTO_INCREMENT` value with one statement, and then refer to `LAST_INSERT_ID()` in a\
multiple-row `INSERT` statement that inserts rows into a table with its own `AUTO_INCREMENT` column. The value of `LAST_INSERT_ID()` will remain stable in the second statement; its value for the second and later rows is not affected by the earlier row insertions. (However, if you mix references to `LAST_INSERT_ID()` and `LAST_INSERT_ID(`<kbd>`expr`</kbd>`)`, the effect is undefined.)

If the previous statement returned an error, the value of `LAST_INSERT_ID()` is undefined. For transactional tables, if the statement is rolled back due to an error, the value of `LAST_INSERT_ID()` is left undefined. For manual [ROLLBACK](../../../sql-statements/transactions/rollback.md), the value of `LAST_INSERT_ID()` is not restored to that before the transaction; it remains as it was at the point of the `ROLLBACK`.

Within the body of a stored routine (procedure or function) or a trigger, the value of `LAST_INSERT_ID()` changes the same way as for statements executed outside the body of these kinds of objects. The\
effect of a stored routine or trigger upon the value of `LAST_INSERT_ID()` that is seen by following statements depends on the kind of routine:

* If a [stored procedure](../../../../server-usage/stored-routines/stored-procedures/) executes statements that change the value of `LAST_INSERT_ID()`, the new value will be seen by statements that follow the procedure call.
* For [stored functions](../../../../server-usage/stored-routines/stored-functions/) and [triggers](../../../../server-usage/triggers-events/triggers/) that change the value, the value is restored when the function or trigger ends, so following statements will not see a changed value.

## Examples

```sql
CREATE TABLE t (
  id INTEGER UNSIGNED AUTO_INCREMENT PRIMARY KEY, 
  f VARCHAR(1)) 
ENGINE = InnoDB;

INSERT INTO t(f) VALUES('a');

SELECT LAST_INSERT_ID();
+------------------+
| LAST_INSERT_ID() |
+------------------+
|                1 |
+------------------+

INSERT INTO t(f) VALUES('b');

INSERT INTO t(f) VALUES('c');

SELECT LAST_INSERT_ID();
+------------------+
| LAST_INSERT_ID() |
+------------------+
|                3 |
+------------------+

INSERT INTO t(f) VALUES('d'),('e');

SELECT LAST_INSERT_ID();
+------------------+
| LAST_INSERT_ID() |
+------------------+
|                4 |
+------------------+

SELECT * FROM t;
+----+------+
| id | f    |
+----+------+
|  1 | a    |
|  2 | b    |
|  3 | c    |
|  4 | d    |
|  5 | e    |
+----+------+

SELECT LAST_INSERT_ID(12);
+--------------------+
| LAST_INSERT_ID(12) |
+--------------------+
|                 12 |
+--------------------+

SELECT LAST_INSERT_ID();
+------------------+
| LAST_INSERT_ID() |
+------------------+
|               12 |
+------------------+

INSERT INTO t(f) VALUES('f');

SELECT LAST_INSERT_ID();
+------------------+
| LAST_INSERT_ID() |
+------------------+
|                6 |
+------------------+

SELECT * FROM t;
+----+------+
| id | f    |
+----+------+
|  1 | a    |
|  2 | b    |
|  3 | c    |
|  4 | d    |
|  5 | e    |
|  6 | f    |
+----+------+

SELECT LAST_INSERT_ID(12);
+--------------------+
| LAST_INSERT_ID(12) |
+--------------------+
|                 12 |
+--------------------+

INSERT INTO t(f) VALUES('g');

SELECT * FROM t;
+----+------+
| id | f    |
+----+------+
|  1 | a    |
|  2 | b    |
|  3 | c    |
|  4 | d    |
|  5 | e    |
|  6 | f    |
|  7 | g    |
+----+------+
```

## See Also

* [mysql\_insert\_id](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c/api-functions/mysql_insert_id)
* [AUTO\_INCREMENT](../../../data-types/auto_increment.md)
* [AUTO\_INCREMENT handling in InnoDB](../../../../server-usage/storage-engines/innodb/auto_increment-handling-in-innodb.md)
* [Sequences](../../../sql-structure/sequences/) - an alternative to auto\_increment
* [INSERT...RETURNING](../../../sql-statements/data-manipulation/inserting-loading-data/insertreturning.md)

<sub>_This page is licensed: GPLv2, originally from_</sub> [<sub>_fill\_help\_tables.sql_</sub>](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)

{% @marketo/form formId="4316" %}
