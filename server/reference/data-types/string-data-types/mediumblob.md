
# MEDIUMBLOB

## Syntax


```
MEDIUMBLOB
```

## Description


A [BLOB](blob.md) column with a maximum
length of 16,777,215 (224 - 1) bytes.
Each MEDIUMBLOB value is stored using a three-byte length prefix that
indicates the number of bytes in the value.


`LONG VARBINARY` is a synonym for `MEDIUMBLOB`


## EXAMPLES


### MEDIUMBLOB


Example of MEDIUMBLOB:


```
CREATE TABLE mediumblob_example (
   description VARCHAR(20),
   example MEDIUMBLOB
) DEFAULT CHARSET=latin1; -- One byte per char makes the examples clearer
```

```
INSERT INTO mediumblob_example VALUES
   ('Normal foo', 'foo'),
   ('Trailing spaces foo', 'foo      '),
   ('NULLed', NULL),
   ('Empty', ''),
   ('Maximum', RPAD('', 16777215, CHAR(7)));
```

```
SELECT description, LENGTH(example) AS length
   FROM mediumblob_example;
```

```
+---------------------+----------+
| description         | length   |
+---------------------+----------+
| Normal foo          |        3 |
| Trailing spaces foo |        9 |
| NULLed              |     NULL |
| Empty               |        0 |
| Maximum             | 16777215 |
+---------------------+----------+
```

### Data Too Long


When SQL_MODE is strict (the default) a value is considered "too long" when its length exceeds the size of the data type, and an error is generated.


Example of data too long behavior for MEDIUMBLOB:


```
TRUNCATE mediumblob_example;
```

```
INSERT INTO mediumblob_example VALUES
   ('Overflow', RPAD('', 16777216, CHAR(7)));
```

```
ERROR 1406 (22001): Data too long for column 'example' at row 1
```

## See Also


* [BLOB](blob.md)
* [BLOB and TEXT Data Types](blob-and-text-data-types.md)
* [Data Type Storage Requirements](../data-type-storage-requirements.md)

