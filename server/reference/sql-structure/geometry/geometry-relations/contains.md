# CONTAINS

## Syntax

```sql
Contains(g1,g2)
```

## Description

Returns `1` or `0` to indicate whether a geometry `g1` completely contains geometry `g2`. CONTAINS() is based on the original MySQL implementation and uses object bounding rectangles, while [ST\_CONTAINS()](st-contains.md) uses object shapes.

This tests the opposite relationship to [Within()](within.md).

GPLv2 fill\_help\_tables.sql

{% @marketo/form formId="4316" %}
