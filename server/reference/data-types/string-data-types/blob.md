# BLOB

## Syntax

```
BLOB[(M)]
```

## Description

A `BLOB` column with a maximum length of `65,535` (`216 - 1`) bytes. Each`BLOB` value is stored using a two-byte length prefix that indicates the\
number of bytes in the value.

An optional length `M` can be given for this type. If this is done,\
MariaDB creates the column as the smallest `BLOB` type large enough to\
hold values _`M`_ bytes long.

BLOBS can also be used to store [dynamic columns](../../sql-statements-and-structure/nosql/dynamic-columns.md).

`BLOB` and `TEXT` columns can both be assigned a [DEFAULT](../../sql-statements/data-definition/create/create-table.md#default) value.

### Indexing

On a column that uses the `BLOB` data type, setting a unique index is now possible.

#### Note

In previous releases, setting a unique index on a column that uses the `BLOB` data type was not possible. Index would only guarantee the uniqueness of a fixed number of characters.

### Oracle Mode

In [Oracle mode](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/compatibility-and-differences/sql_modeoracle), `BLOB` is a synonym for `LONGBLOB`.

## EXAMPLES

### BLOB

Example of BLOB:

```
CREATE TABLE blob_example (
   description VARCHAR(20),
   example BLOB
) DEFAULT CHARSET=latin1; -- One byte per char makes the examples clearer
```

```
INSERT INTO blob_example VALUES
   ('Normal foo', 'foo'),
   ('Trailing spaces foo', 'foo      '),
   ('NULLed', NULL),
   ('Empty', ''),
   ('Maximum', RPAD('', 65535, CHAR(7)));
```

```
SELECT description, LENGTH(example) AS length
   FROM blob_example;

+---------------------+--------+
| description         | length |
+---------------------+--------+
| Normal foo          |      3 |
| Trailing spaces foo |      9 |
| NULLed              |   NULL |
| Empty               |      0 |
| Maximum             |  65535 |
+---------------------+--------+
```

## Data Too Long

When SQL\_MODE is strict (the default) a value is considered "too long" when its length exceeds the size of the data type, and an error is generated.

Example of data too long behavior for BLOB:

```
TRUNCATE blob_example;

INSERT INTO blob_example VALUES
   ('Overflow', RPAD('', 65536, CHAR(7)));

ERROR 1406 (22001): Data too long for column 'example' at row 1
```

## See Also

* [BLOB and TEXT Data Types](blob-and-text-data-types.md)
* [Data Type Storage Requirements](../data-type-storage-requirements.md)
* [Oracle mode from MariaDB 10.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/compatibility-and-differences/sql_modeoracle)

GPLv2 fill\_help\_tables.sql
