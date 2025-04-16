
# CONNECT XCOL Table Type

`XCOL` tables are based on another table or view, like `[PROXY](connect-proxy-table-type.md)` tables. This type can be
used when the object table has a column that contains a list of values.


Suppose we have a *'children'* table that can be displayed as:



| name | childlist |
| --- | --- |
| name | childlist |
| Sophie | Vivian, Antony |
| Lisbeth | Lucy,Charles,Diana |
| Corinne |  |
| Claude | Marc |
| Janet | Arthur, Sandra, Peter, John |



We can have a different view on these data, where each child will be associated
with his/her mother by creating an `XCOL` table by:


```
CREATE TABLE xchild (
  mother char(12) NOT NULL,
  child char(12) DEFAULT NULL flag=2
) ENGINE=CONNECT table_type=XCOL tabname='chlist'
option_list='colname=child';
```

The `COLNAME` option specifies the name of the column receiving the list
items. This will return from:


```
select * from xchild;
```

The requested view:



| mother | child |
| --- | --- |
| mother | child |
| Sophia | Vivian |
| Sophia | Antony |
| Lisbeth | Lucy |
| Lisbeth | Charles |
| Lisbeth | Diana |
| Corinne | NULL |
| Claude | Marc |
| Janet | Arthur |
| Janet | Sandra |
| Janet | Peter |
| Janet | John |



Several things should be noted here:


* When the original children field is void, what happens depends on the NULL specification of the "multiple" column. If it is nullable, like here, a void string will generate a NULL value. However, if the column is not nullable, no row will be generated at all.
* Blanks after the separator are ignored.
* No copy of the original data was done. Both tables use the same source data.
* Specifying the column definitions in the `CREATE TABLE` statement is optional.


The "multiple" column *child* can be used as any other column. For instance:


```
select * from xchild where substr(child,1,1) = 'A';
```

This will return:



| Mother | Child |
| --- | --- |
| Mother | Child |
| Sophia | Antony |
| Janet | Arthur |



If a query does not involve the "multiple" column, no row multiplication will
be done. For instance:


```
select mother from xchild;
```

This will just return all the mothers:



| mother |
| --- |
| mother |
| Sophia |
| Lisbeth |
| Corinne |
| Claude |
| Janet |



The same occurs with other types of select statements, for instance:


```
select count(*) from xchild;      -- returns 5
select count(child) from xchild;  -- returns 10
select count(mother) from xchild; -- returns 5
```

Grouping also gives different result:


```
select mother, count(*) from xchild group by mother;
```

Replies:



| mother | count(*) |
| --- | --- |
| mother | count(*) |
| Claude | 1 |
| Corinne | 1 |
| Janet | 1 |
| Lisbeth | 1 |
| Sophia | 1 |



While the query:


```
select mother, count(child) from xchild group by mother;
```

Gives the more interesting result:



| mother | count(child) |
| --- | --- |
| mother | count(child) |
| Claude | 1 |
| Corinne | 0 |
| Janet | 4 |
| Lisbeth | 3 |
| Sophia | 2 |



Some more options are available for this table type:



| Option | Description |
| --- | --- |
| Option | Description |
| Sep_char | The separator character used in the "multiple" column, defaults to the comma. |
| Mult | Indicates the max number of multiple items. It is used to internally calculate the max size of the table and defaults to 10. (To be specified in OPTION_LIST). |



## Using Special Columns with XCOL


Special columns can be used in XCOL tables. The mostly useful one is ROWNUM that gives the rank of the value in the list of values. For instance:


```
CREATE TABLE xchild2 (
rank int NOT NULL SPECIAL=ROWID,
mother char(12) NOT NULL,
child char(12) NOT NULL flag=2
) ENGINE=CONNECT table_type=XCOL tabname='chlist' option_list='colname=child';
```

This table will be displayed as:



| rank | mother | child |
| --- | --- | --- |
| rank | mother | child |
| 1 | Sophia | Vivian |
| 2 | Sophia | Antony |
| 1 | Lisbeth | Lucy |
| 2 | Lisbeth | Charles |
| 3 | Lisbeth | Diana |
| 1 | Claude | Marc |
| 1 | Janet | Arthur |
| 2 | Janet | Sandra |
| 3 | Janet | Peter |
| 4 | Janet | John |



To list only the first child of each mother you can do:


```
SELECT mother, child FROM xchild2 where rank = 1 ;
```

returning:



| mother | child |
| --- | --- |
| mother | child |
| Sophia | Vivian |
| Lisbeth | Lucy |
| Claude | Marc |
| Janet | Arthur |



However, note the following pitfall: trying to get the names of all mothers having more than 2 children cannot be done by:


```
SELECT mother FROM xchild2 where rank > 2;
```

This is because with no row multiplication being done, the rank value is always 1. The correct way to obtain this result is longer but cannot use the ROWNUM column:


```
SELECT mother FROM xchild2 group by mother having count(child) > 2;
```

## XCOL tables based on specified views


Instead of specifying a source table name via the TABNAME option, it is possible to retrieve data from a
“view” whose definition is given in a new option SRCDEF . For instance:


```
create table xsvars engine=connect table_type=XCOL
srcdef='show variables like "optimizer_switch"'
option_list='Colname=Value';
```

Then, for instance:


```
select value from xsvars limit 10;
```

This will display something like:



| value |
| --- |
| value |
| index_merge=on |
| index_merge_union=on |
| index_merge_sort_union=on |
| index_merge_intersection=on |
| index_merge_sort_intersection=off |
| engine_condition_pushdown=off |
| index_condition_pushdown=on |
| derived_merge=on |
| derived_with_keys=on |
| firstmatch=on |



Note: All XCOL tables are read only.

