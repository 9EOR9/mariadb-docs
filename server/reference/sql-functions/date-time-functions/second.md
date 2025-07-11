
# SECOND

## Syntax


```
SECOND(time)
```

## Description


Returns the second for a given `time` (which can include [microseconds](microseconds-in-mariadb.md)), in the range 0 to 59, or `NULL` if not given a valid time value.


## Examples


```
SELECT SECOND('10:05:03');
+--------------------+
| SECOND('10:05:03') |
+--------------------+
|                  3 |
+--------------------+

SELECT SECOND('10:05:01.999999');
+---------------------------+
| SECOND('10:05:01.999999') |
+---------------------------+
|                         1 |
+---------------------------+
```


<sub>_This page is licensed: GPLv2, originally from [fill\_help\_tables.sql](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)_</sub>


{% @marketo/form formId="4316" %}
