# VALUES / VALUE

## Syntax

```
VALUE(col_name)
```

## Description

In an [INSERT ... ON DUPLICATE KEY UPDATE](../../../sql-statements/data-manipulation/inserting-loading-data/insert-on-duplicate-key-update.md) statement, you can use the `VALUES(col_name)` function in the [UPDATE](../../../sql-statements/data-manipulation/changing-deleting-data/update.md) clause to refer to column values from the [INSERT](../../../sql-statements/data-manipulation/inserting-loading-data/insert.md) portion of the statement. In other words, `VALUES(col_name)` in the `UPDATE` clause refers to the value of col\_name that would be inserted, had no duplicate-key conflict occurred. This function is especially useful in multiple-row inserts.

The `VALUES()` function is meaningful only in `INSERT ... ON DUPLICATE KEY UPDATE` statements and returns `NULL` otherwise.

This function was renamed to `VALUE()`, because it's incompatible with the standard Table Value Constructors syntax.

The `VALUES()` function can still be used but only in `INSERT ... ON DUPLICATE KEY UPDATE` statements; it's a syntax error otherwise.

## Examples

```
INSERT INTO t (a,b,c) VALUES (1,2,3),(4,5,6)
    ON DUPLICATE KEY UPDATE c=VALUE(a)+VALUE(b);
```

GPLv2 fill\_help\_tables.sql
