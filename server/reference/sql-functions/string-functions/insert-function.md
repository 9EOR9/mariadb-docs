
# INSERT Function

## Syntax


```
INSERT(str,pos,len,newstr)
```

## Description


Returns the string `str`, with the substring beginning at position `pos`
and `len` characters long replaced by the string `newstr`. Returns the
original string if `pos` is not within the length of the string.
Replaces the rest of the string from position `pos` if `len` is not within
the length of the rest of the string. Returns NULL if any argument is
NULL.


## Examples


```
SELECT INSERT('Quadratic', 3, 4, 'What');
+-----------------------------------+
| INSERT('Quadratic', 3, 4, 'What') |
+-----------------------------------+
| QuWhattic                         |
+-----------------------------------+

SELECT INSERT('Quadratic', -1, 4, 'What');
+------------------------------------+
| INSERT('Quadratic', -1, 4, 'What') |
+------------------------------------+
| Quadratic                          |
+------------------------------------+

SELECT INSERT('Quadratic', 3, 100, 'What');
+-------------------------------------+
| INSERT('Quadratic', 3, 100, 'What') |
+-------------------------------------+
| QuWhat                              |
+-------------------------------------+
```


<sub>_This page is licensed: GPLv2, originally from [fill\_help\_tables.sql](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)_</sub>


{% @marketo/form formId="4316" %}
