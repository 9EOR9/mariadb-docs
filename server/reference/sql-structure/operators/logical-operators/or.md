# ||

## Syntax

```
OR, ||
```

## Description

Logical OR. When both operands are non-NULL, the result is 1 if any\
operand is non-zero, and 0 otherwise. With a NULL operand, the result\
is 1 if the other operand is non-zero, and NULL otherwise. If both\
operands are NULL, the result is NULL.

For this operator, [short-circuit evaluation](../operator-precedence.md#short-circuit-evaluation) can be used.

Note that, if the `PIPES_AS_CONCAT` [SQL\_MODE](../../../../server-management/variables-and-modes/sql-mode.md) is set, `||` is used as a string concatenation operator. This means that `a || b` is the same as `CONCAT(a,b)`. See [CONCAT()](../../sql-statements/built-in-functions/string-functions/concat.md) for details.

### Oracle Mode

In [Oracle mode](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/sql-structure/operators/logical-operators/broken-reference/README.md), `||` ignores [null](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/sql-statements-and-structure/operators/logical-operators/null/README.md).

## Examples

```
SELECT 1 || 1;
+--------+
| 1 || 1 |
+--------+
|      1 |
+--------+

SELECT 1 || 0;
+--------+
| 1 || 0 |
+--------+
|      1 |
+--------+

SELECT 0 || 0;
+--------+
| 0 || 0 |
+--------+
|      0 |
+--------+

SELECT 0 || NULL;
+-----------+
| 0 || NULL |
+-----------+
|      NULL |
+-----------+

SELECT 1 || NULL;
+-----------+
| 1 || NULL |
+-----------+
|         1 |
+-----------+
```

In [Oracle mode](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/sql-structure/operators/logical-operators/broken-reference/README.md):

```
SELECT 0 || NULL;
+-----------+
| 0 || NULL |
+-----------+
| 0         |
+-----------+
```

## See Also

## See Also

* [Operator Precedence](../operator-precedence.md)
* [Oracle mode](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/sql-structure/operators/logical-operators/broken-reference/README.md)

<sub>_This page is licensed: GPLv2, originally from_</sub> [<sub>_fill\_help\_tables.sql_</sub>](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)

{% @marketo/form formId="4316" %}
