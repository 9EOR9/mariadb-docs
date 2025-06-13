# UNCOMPRESS

## Syntax

```
UNCOMPRESS(string_to_uncompress)
```

## Description

Uncompresses a string compressed by the `[COMPRESS()](compress.md)` function. If the\
argument is not a compressed value, the result is `NULL`. This function\
requires MariaDB to have been compiled with a compression library such\
as zlib. Otherwise, the return value is always `NULL`. The [have\_compress](../../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#have_compress) server system variable indicates whether a compression library is present.

## Examples

```
SELECT UNCOMPRESS(COMPRESS('a string'));
+----------------------------------+
| UNCOMPRESS(COMPRESS('a string')) |
+----------------------------------+
| a string                         |
+----------------------------------+

SELECT UNCOMPRESS('a string');
+------------------------+
| UNCOMPRESS('a string') |
+------------------------+
| NULL                   |
+------------------------+
```

<sub>_This page is licensed: GPLv2, originally from [fill\_help\_tables.sql](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)_</sub>

{% @marketo/form formId="4316" %}
