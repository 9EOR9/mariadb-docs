# SUBSTRING

## Syntax

```
SUBSTRING(str,pos), 
SUBSTRING(str FROM pos), 
SUBSTRING(str,pos,len),
SUBSTRING(str FROM pos FOR len)

SUBSTR(str,pos), 
SUBSTR(str FROM pos), 
SUBSTR(str,pos,len),
SUBSTR(str FROM pos FOR len)
```

## Description

The forms without a _`len`_ argument return a substring from string _`str`_ starting at position _`pos`_.

The forms with a _`len`_ argument return a substring _`len`_ characters long from string _`str`_, starting at position _`pos`_.

The forms that use _`FROM`_ are standard SQL syntax.

It is also possible to use a negative value for _`pos`_. In this case, the beginning of the substring is _`pos`_ characters from the end of the string, rather than the beginning. A negative value may be used for _`pos`_ in any of the forms of this function.

By default, the position of the first character in the string from which the substring is to be extracted is reckoned as 1. For [Oracle-compatibility](broken-reference), from [MariaDB 10.3.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1033-release-notes), when sql\_mode is set to 'oracle', position zero is treated as position 1 (although the first character is still reckoned as 1).

If any argument is `NULL`, returns `NULL`.

Prior to [MariaDB 11.8](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-11-8-series/what-is-mariadb-118), the optimizer could not take advantage of queries of the format [SUBSTR(col, 1, n) = const\_str](substring.md).

## Examples

```
SELECT SUBSTRING('Knowledgebase',5);
+------------------------------+
| SUBSTRING('Knowledgebase',5) |
+------------------------------+
| ledgebase                    |
+------------------------------+

SELECT SUBSTRING('MariaDB' FROM 6);
+-----------------------------+
| SUBSTRING('MariaDB' FROM 6) |
+-----------------------------+
| DB                          |
+-----------------------------+

SELECT SUBSTRING('Knowledgebase',3,7);
+--------------------------------+
| SUBSTRING('Knowledgebase',3,7) |
+--------------------------------+
| owledge                        |
+--------------------------------+

SELECT SUBSTRING('Knowledgebase', -4);
+--------------------------------+
| SUBSTRING('Knowledgebase', -4) |
+--------------------------------+
| base                           |
+--------------------------------+

SELECT SUBSTRING('Knowledgebase', -8, 4);
+-----------------------------------+
| SUBSTRING('Knowledgebase', -8, 4) |
+-----------------------------------+
| edge                              |
+-----------------------------------+

SELECT SUBSTRING('Knowledgebase' FROM -8 FOR 4);
+------------------------------------------+
| SUBSTRING('Knowledgebase' FROM -8 FOR 4) |
+------------------------------------------+
| edge                                     |
+------------------------------------------+
```

[Oracle mode from MariaDB 10.3.3](broken-reference):

```
SELECT SUBSTR('abc',0,3);
+-------------------+
| SUBSTR('abc',0,3) |
+-------------------+
|                   |
+-------------------+

SELECT SUBSTR('abc',1,2);
+-------------------+
| SUBSTR('abc',1,2) |
+-------------------+
| ab                |
+-------------------+

SET sql_mode='oracle';

SELECT SUBSTR('abc',0,3);
+-------------------+
| SUBSTR('abc',0,3) |
+-------------------+
| abc               |
+-------------------+

SELECT SUBSTR('abc',1,2);
+-------------------+
| SUBSTR('abc',1,2) |
+-------------------+
| ab                |
+-------------------+
```

## See Also

* [INSTR()](instr.md) - Returns the position of a string within a string
* [LOCATE()](locate.md) - Returns the position of a string within a string
* [SUBSTRING\_INDEX()](substring_index.md) - Returns a string based on substring

GPLv2 fill\_help\_tables.sql
