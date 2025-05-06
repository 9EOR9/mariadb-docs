# FETCH

## Syntax

```
FETCH cursor_name INTO var_name [, var_name] ...
```

## Description

This statement fetches the next row (if a row exists) using the\
specified [open](open.md) [cursor](./), and advances the cursor pointer.

`var_name` can be a [local variable](../declare-variable.md), but _not_ a [user-defined variable](../../../reference/sql-statements-and-structure/sql-language-structure/user-defined-variables.md).

If no more rows are available, a No Data condition occurs with`SQLSTATE` value `02000`. To detect this condition, you can set up a\
handler for it (or for a `NOT FOUND` condition).

See [Cursor Overview](cursor-overview.md) for an example.

## See Also

* [Cursor Overview](cursor-overview.md)
* [DECLARE CURSOR](declare-cursor.md)
* [OPEN cursor\_name](open.md)
* [CLOSE cursor\_name](close.md)
* [Cursors in Oracle mode](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/compatibility-and-differences/sql_modeoracle)

GPLv2 fill\_help\_tables.sql
