# LENGTHB

## Syntax

```
LENGTHB(str)
```

## Description

`LENGTHB()` returns the length of the given string, in bytes. When [Oracle mode](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/sql-functions/string-functions/broken-reference/README.md) is not set, this is a synonym for [LENGTH](length.md).

A multi-byte character counts as multiple bytes. This means that for a string containing five two-byte characters, `LENGTHB()` returns 10, whereas [CHAR\_LENGTH()](char_length.md) returns 5.

If `str` is not a string value, it is converted into a string. If `str` is `NULL`, the function returns `NULL`.

## Examples

When [Oracle mode](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/sql-functions/string-functions/broken-reference/README.md) from [MariaDB 10.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/what-is-mariadb-103) is not set:

```
SELECT CHAR_LENGTH('π'), LENGTH('π'), LENGTHB('π'), OCTET_LENGTH('π');
+-------------------+--------------+---------------+--------------------+
| CHAR_LENGTH('π')  | LENGTH('π')  | LENGTHB('π')  | OCTET_LENGTH('π')  |
+-------------------+--------------+---------------+--------------------+
|                 1 |            2 |             2 |                  2 |
+-------------------+--------------+---------------+--------------------+
```

In [Oracle mode from MariaDB 10.3](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/sql-functions/string-functions/broken-reference/README.md):

```
SELECT CHAR_LENGTH('π'), LENGTH('π'), LENGTHB('π'), OCTET_LENGTH('π');
+-------------------+--------------+---------------+--------------------+
| CHAR_LENGTH('π')  | LENGTH('π')  | LENGTHB('π')  | OCTET_LENGTH('π')  |
+-------------------+--------------+---------------+--------------------+
|                 1 |            1 |             2 |                  2 |
+-------------------+--------------+---------------+--------------------+
```

## See Also

* [CHAR\_LENGTH()](char_length.md)
* [LENGTH()](length.md)
* [OCTET\_LENGTH()](octet_length.md)

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
