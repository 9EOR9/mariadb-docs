# extract\_schema\_from\_file\_name

## Syntax

```
sys.extract_schema_from_file_name(path)
```

## Description

`extract_schema_from_file_name` is a [stored function](../../../../../../../server-usage/stored-routines/stored-functions/) available with the [Sys Schema](../).

Given a file path, it returns the schema (database) name. The file name is assumed to be within the schema directory, and therefore the function will not return the expected result with partitions, or when tables are defined using the DATA\_DIRECTORY table option.

The function does not examine anything on disk. The return value, a VARCHAR(64), is determined solely from the provided path.

## Examples

```
SELECT sys.extract_schema_from_file_name('/usr/local/mysql/data/db/t1.ibd');
+----------------------------------------------------------------------+
| sys.extract_schema_from_file_name('/usr/local/mysql/data/db/t1.ibd') |
+----------------------------------------------------------------------+
| db                                                                   |
+----------------------------------------------------------------------+
```

## See also

* [extract\_table\_from\_file\_name()](extract_table_from_file_name.md)

CC BY-SA / Gnu FDL
