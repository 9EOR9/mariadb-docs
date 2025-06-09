# format\_bytes

## Syntax

```
sys.format_bytes(double)
```

## Description

`format_bytes` is a [stored function](../../../../../../server-usage/stored-routines/stored-functions/) available with the [Sys Schema](../).

Given a byte count, returns a string consisting of a value and the units in a human-readable format. The units will be in bytes, KiB (kibibytes), MiB (mebibytes), GiB (gibibytes), TiB (tebibytes), or PiB (pebibytes).

The binary prefixes (kibi, mebi, gibi, tebi and pebi) were created in December 1998 by the International Electrotechnical Commission to avoid possible ambiguity, as the widely-used prefixes kilo, mega, giga, tera and peta can be used to refer to both the power-of-10 decimal system multipliers and the power-of-two binary system multipliers.

From [MariaDB 11.8](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-8-series/what-is-mariadb-118), the built-in [FORMAT\_BYTES](https://mariadb.com/kb/en/miscellaneous-functions-format_byte) function can instead be used. The functions are similar, except that FORMAT\_BYTES also displays exbibytes.

## Examples

```
SELECT sys.format_bytes(1000),sys.format_bytes(1024);
+------------------------+------------------------+
| sys.format_bytes(1000) | sys.format_bytes(1024) |
+------------------------+------------------------+
| 1000 bytes             | 1.00 KiB               |
+------------------------+------------------------+

SELECT sys.format_bytes(1000000),sys.format_bytes(1048576);
+---------------------------+---------------------------+
| sys.format_bytes(1000000) | sys.format_bytes(1048576) |
+---------------------------+---------------------------+
| 976.56 KiB                | 1.00 MiB                  |
+---------------------------+---------------------------+

SELECT sys.format_bytes(1000000000),sys.format_bytes(1073741874);
+------------------------------+------------------------------+
| sys.format_bytes(1000000000) | sys.format_bytes(1073741874) |
+------------------------------+------------------------------+
| 953.67 MiB                   | 1.00 GiB                     |
+------------------------------+------------------------------+

SELECT sys.format_bytes(1000000000000),sys.format_bytes(1099511627776);
+---------------------------------+---------------------------------+
| sys.format_bytes(1000000000000) | sys.format_bytes(1099511627776) |
+---------------------------------+---------------------------------+
| 931.32 GiB                      | 1.00 TiB                        |
+---------------------------------+---------------------------------+

SELECT sys.format_bytes(1000000000000000),sys.format_bytes(1125899906842624);
+------------------------------------+------------------------------------+
| sys.format_bytes(1000000000000000) | sys.format_bytes(1125899906842624) |
+------------------------------------+------------------------------------+
| 909.49 TiB                         | 1.00 PiB                           |
+------------------------------------+------------------------------------+
```

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
