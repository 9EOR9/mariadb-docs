# MBRContains

## Syntax

```sql
MBRContains(g1,g2)
```

## Description

Returns 1 or 0 to indicate whether the [Minimum Bounding Rectangle](mbr-definition.md) of g1 contains the Minimum Bounding Rectangle of g2. This tests the opposite relationship as [MBRWithin()](mbrwithin.md).

## Examples

```sql
SET @g1 = GeomFromText('Polygon((0 0,0 3,3 3,3 0,0 0))');

SET @g2 = GeomFromText('Point(1 1)');

SELECT MBRContains(@g1,@g2), MBRContains(@g2,@g1);
+----------------------+----------------------+
| MBRContains(@g1,@g2) | MBRContains(@g2,@g1) |
+----------------------+----------------------+
|                    1 |                    0 |
+----------------------+----------------------+
```

## See Also

* [MBRWithin](mbrwithin.md)

<sub>_This page is licensed: GPLv2, originally from [fill\_help\_tables.sql](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)_</sub>

{% @marketo/form formId="4316" %}
