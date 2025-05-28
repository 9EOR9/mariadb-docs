---
icon: earth-africa
---

# ST\_SYMDIFFERENCE

## Syntax

```sql
ST_SYMDIFFERENCE(g1,g2)
```

## Description

Returns a geometry that represents the portions of geometry _`g1`_ and geometry _`g2`_ that don't intersect.

## Examples

```sql
SET @g1 = ST_GEOMFROMTEXT('LINESTRING(10 20, 10 40)');

SET @g2 = ST_GEOMFROMTEXT('LINESTRING(10 15, 10 25)');

SELECT ASTEXT(ST_SYMDIFFERENCE(@g1,@g2));
+----------------------------------------------+
| ASTEXT(ST_SYMDIFFERENCE(@g1,@g2))            |
+----------------------------------------------+
| MULTILINESTRING((10 15,10 20),(10 25,10 40)) |
+----------------------------------------------+

SET @g2 = ST_GeomFromText('LINESTRING(10 20, 10 41)');

SELECT ASTEXT(ST_SYMDIFFERENCE(@g1,@g2));
+-----------------------------------+
| ASTEXT(ST_SYMDIFFERENCE(@g1,@g2)) |
+-----------------------------------+
| LINESTRING(10 40,10 41)           |
+-----------------------------------+
```

CC BY-SA / Gnu FDL
