# Range Optimizer

Range optimizer is a part of MariaDB (and MySQL) optimizer that takes as input

* the table and index definition(s)
* the WHERE condition (or ON expression if the table is inner in an outer join)

and constructs list of ranges one can scan in an index to read the rows that match the WHERE condition, or a superset of it. It can also construct an "index\_merge" plan, where one needs ranges from two or more\
indexes to compute a union (formed from multiple condition disjunctions) and/or intersection (formed from multiple condition conjunctions).

## Basic example

Consider a table

```
create table t1 (
  key1 int,
  key2 varchar(100),
  ...
  index(key1),
  index(key2)
);
```

and query

```
-- Turn on optimizer trace so we can see the ranges:
set optimizer_trace=1; 
explain select * from t1 where key1<10 and key2='foo';
select * from information_schema.optimizer_trace\G
```

This shows the ranges that the optimizer was able to infer:

```
"range_scan_alternatives": [
                      {
                        "index": "key1",
                        "ranges": ["(NULL) < (key1) < (10)"],
                        ...
                      },
                      {
                        "index": "key2",
                        "ranges": ["(foo) <= (key2) <= (foo)"],
                        ...
                      }
                    ],
```

## Ranges are non-overlapping

Range optimizer produces a list of ranges without overlaps. Consider this WHERE clause where conditions do have overlaps:

```
select * from t1 where (key1 between 10 and 20  and key1 > 14)  or key1 in (17, 22, 33);
select * from information_schema.optimizer_trace\G
```

We get

```
...
                  "analyzing_range_alternatives": {
                    "range_scan_alternatives": [
                      {
                        "index": "key1",
                        "ranges": [
                          "(14) < (key1) <= (20)",
                          "(22) <= (key1) <= (22)",
                          "(33) <= (key1) <= (33)"
                        ],
```

## Ranges for multi-part indexes

Let's consider an index with multiple key parts. (note: due to [Extended Keys](extended-keys.md) optimization, an index may have more key parts than you've explicitly defined)

```
create table t2 (
  keypart1 int,
  keypart2 varchar(100),
  keypart3 int,
  index idx(keypart1, keypart2, keypart3)
);
```

Range optimizer will generate a _finite_ set of ranges over lexicographical ordering over `(keypart1, keypart2, ...)`.

Example:

```
select * from t2 where keypart1 in (1,2,3) and keypart2 between 'bar' and 'foo';
select * from information_schema.optimizer_trace\G
```

gives

```
"range_scan_alternatives": [
                      {
                        "index": "idx",
                        "ranges": [
                          "(1,bar) <= (keypart1,keypart2) <= (1,foo)",
                          "(2,bar) <= (keypart1,keypart2) <= (2,foo)",
                          "(3,bar) <= (keypart1,keypart2) <= (3,foo)"
                        ],
```

Compare with a similar query:

```
select * from t2 where keypart1 between 1 and 3 and keypart2 between 'bar' and 'foo';
select * from information_schema.optimizer_trace\G
```

this will generate just one bigger range:

```
"range_scan_alternatives": [
                      {
                        "index": "idx",
                        "ranges": ["(1,bar) <= (keypart1,keypart2) <= (3,foo)"],
                        ...
```

which includes for example rows like `(keypart1,keypart2)=(1,zzz)`. One could argue that the optimizer could be able to figure out that for condition `keypart1 between 1 and 3` the only possible values are 1, 2, 3 but this is not implemented.

### Not all comparisons produce ranges

Note that some keypart comparisons produce multi-part ranges while some do not.\
The governing rule is the same: the conditions together must produce an interval (or a finite number of intervals) in lexicographic order in the index.

Some examples:

```
where keypart1<= 10 and keypart2<'foo'
```

can use the second keypart:

```
"ranges": ["(NULL) < (keypart1,keypart2) < (10,foo)"],
```

but the interval will still include rows like `(keypart1, keypart2) = (8, 'zzzz')`

Non-inclusive bound on keypart1 prevents any use of keypart2. For

```
where keypart1< 10 keypart2<'foo';
```

we get

```
"ranges": ["(NULL) < (keypart1) < (10)"]
```

Non-agreeing comparison (less than and greater than) do not produce a multi-part range:

```
where keypart1<= 10 and keypart2>'foo';
```

gives

```
"ranges": ["(NULL) < (keypart1) <= (10)"],
```

A "Hole" in keyparts means higher keypart cannot be used.

```
where keypart1= 10 and keypart3<='foo';
```

gives

```
"ranges": ["(10) <= (keypart1) <= (10)"]
```

### Combinatorial blow-ups

For multi-part keys, range analyzer can produce ranges that are "tight", that is, they only include rows that\
will match the WHERE condition.\
On the other hand, some SQL constructs can produce very large (combinatorial) amounts of ranges.\
Consider a query

```
select * from t2 where keypart1 in (1,2,3,4) and keypart2 in ('a','b', 'c')
```

two IN-lists produce 3\*4 =12 ranges:

```
"range_scan_alternatives": [
                      {
                        "index": "idx",
                        "ranges": [
                          "(1,a) <= (keypart1,keypart2) <= (1,a)",
                          "(1,b) <= (keypart1,keypart2) <= (1,b)",
                          "(1,c) <= (keypart1,keypart2) <= (1,c)",
                          "(2,a) <= (keypart1,keypart2) <= (2,a)",
                          "(2,b) <= (keypart1,keypart2) <= (2,b)",
                          "(2,c) <= (keypart1,keypart2) <= (2,c)",
                          "(3,a) <= (keypart1,keypart2) <= (3,a)",
                          "(3,b) <= (keypart1,keypart2) <= (3,b)",
                          "(3,c) <= (keypart1,keypart2) <= (3,c)",
                          "(4,a) <= (keypart1,keypart2) <= (4,a)",
                          "(4,b) <= (keypart1,keypart2) <= (4,b)",
                          "(4,c) <= (keypart1,keypart2) <= (4,c)"
                        ],
```

if one adds `and keypart3 IN (1,2,3,4,5)`, the amount of ranges will be &#x33;_&#x34;_&#x35;=60 and so forth.\
See [optimizer\_max\_sel\_arg\_weight](optimizer_max_sel_arg_weight.md) on how to combat this.

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
