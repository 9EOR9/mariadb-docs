
# MBRWithin

## Syntax


```
MBRWithin(g1,g2)
```

## Description


Returns 1 or 0 to indicate whether the [Minimum Bounding Rectangle](mbr-definition.md) of g1 is within the Minimum Bounding Rectangle of g2. This tests the opposite relationship as [MBRContains()](mbrcontains.md).


## Examples


```
SET @g1 = GeomFromText('Polygon((0 0,0 3,3 3,3 0,0 0))');
SET @g2 = GeomFromText('Polygon((0 0,0 5,5 5,5 0,0 0))');
SELECT MBRWithin(@g1,@g2), MBRWithin(@g2,@g1);
+--------------------+--------------------+
| MBRWithin(@g1,@g2) | MBRWithin(@g2,@g1) |
+--------------------+--------------------+
|                  1 |                  0 |
+--------------------+--------------------+
```


GPLv2 fill_help_tables.sql

