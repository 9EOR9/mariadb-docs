# BIT\_OR

## Syntax

```
BIT_OR(expr) [over_clause]
```

## Description

Returns the bitwise OR of all bits in `expr`. The calculation is performed with 64-bit ([BIGINT](../../../data-types/data-types-numeric-data-types/bigint.md)) precision. It is an [aggregate function](./), and so can be used with the [GROUP BY](../../data-manipulation/selecting-data/group-by.md) clause.

If no rows match, `BIT_OR` will return a value with all bits set to `0`. NULL values have no effect on the result unless all results are NULL, which is treated as no match.

`BIT_OR` can be used as a [window function](../special-functions/window-functions/) with the addition of the _over\_clause_.

## Examples

```
CREATE TABLE vals (x INT);

INSERT INTO vals VALUES(111),(110),(100);

SELECT BIT_AND(x), BIT_OR(x), BIT_XOR(x) FROM vals;
+------------+-----------+------------+
| BIT_AND(x) | BIT_OR(x) | BIT_XOR(x) |
+------------+-----------+------------+
|        100 |       111 |        101 |
+------------+-----------+------------+
```

As an [aggregate function](./):

```
CREATE TABLE vals2 (category VARCHAR(1), x INT);

INSERT INTO vals2 VALUES
  ('a',111),('a',110),('a',100),
  ('b','000'),('b',001),('b',011);

SELECT category, BIT_AND(x), BIT_OR(x), BIT_XOR(x) 
  FROM vals GROUP BY category;
+----------+------------+-----------+------------+
| category | BIT_AND(x) | BIT_OR(x) | BIT_XOR(x) |
+----------+------------+-----------+------------+
| a        |        100 |       111 |        101 |
| b        |          0 |        11 |         10 |
+----------+------------+-----------+------------+
```

No match:

```
SELECT BIT_OR(NULL);
+--------------+
| BIT_OR(NULL) |
+--------------+
|            0 |
+--------------+
```

## See Also

* [BIT\_AND](bit_and.md)
* [BIT\_XOR](bit_xor.md)

GPLv2 fill\_help\_tables.sql
