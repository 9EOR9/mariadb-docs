# CONV

## Syntax

```
CONV(N,from_base,to_base)
```

## Description

Converts numbers between different number bases. Returns a string\
representation of the number _`N`_, converted from base _`from_base`_\
to base _`to_base`_.

Returns `NULL` if any argument is `NULL`, or if the second or third argument are not in the allowed range.

The argument _`N`_ is interpreted as an integer, but may be specified as an\
integer or a string. The minimum base is 2 and the maximum base is 36 (prior to [MariaDB 11.4.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-11-4-series/mariadb-11-4-0-release-notes)) or 62 (from [MariaDB 11.4.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-11-4-series/mariadb-11-4-0-release-notes)). If _`to_base`_ is a negative number, _`N`_ is regarded as a signed number.\
Otherwise, _`N`_ is treated as unsigned. `CONV()` works with 64-bit\
precision.

Some shortcuts for this function are also available: [BIN()](../string-functions/bin.md), [OCT()](oct.md), [HEX()](../string-functions/hex.md), [UNHEX()](../string-functions/unhex.md). Also, MariaDB allows [binary](../../sql-structure/sql-language-structure/binary-literals.md) literal values and [hexadecimal](../../sql-structure/sql-language-structure/hexadecimal-literals.md) literal values.

## Examples

```
SELECT CONV('a',16,2);
+----------------+
| CONV('a',16,2) |
+----------------+
| 1010           |
+----------------+

SELECT CONV('6E',18,8);
+-----------------+
| CONV('6E',18,8) |
+-----------------+
| 172             |
+-----------------+

SELECT CONV(-17,10,-18);
+------------------+
| CONV(-17,10,-18) |
+------------------+
| -H               |
+------------------+

SELECT CONV(12+'10'+'10'+0xa,10,10);
+------------------------------+
| CONV(12+'10'+'10'+0xa,10,10) |
+------------------------------+
| 42                           |
+------------------------------+
```

GPLv2 fill\_help\_tables.sql
