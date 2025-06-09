# mysql\_affected\_rows

## Syntax

```c
my_ulonglong mysql_affected_rows(MYSQL * mysql);
```

`mysql` is a connection identifier, which was previously allocated by [mysql\_init()](mysql_init.md) or [mysql\_real\_connect()](mysql_real_connect.md).

## Description

Returns the number of affected rows by the last operation associated with mysql, if the operation was an "upsert" ([INSERT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements-and-structure/sql-statements/data-manipulation/inserting-loading-data/insert), [UPDATE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements-and-structure/sql-statements/data-manipulation/changing-deleting-data/update), [DELETE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements-and-structure/sql-statements/data-manipulation/changing-deleting-data/delete) or [REPLACE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements-and-structure/sql-statements/data-manipulation/changing-deleting-data/replace)) statement, or `UINT64_MAX` (0xffffffffffffffff) if the last query failed.

{% hint style="info" %}
When using [UPDATE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements-and-structure/sql-statements/data-manipulation/changing-deleting-data/update), MariaDB will not update columns where the new value is the same as the old value. This creates the possibility that mysql\_affected\_rows may not actually equal the number of rows matched, only the number of rows that were literally affected by the query.

The [REPLACE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements-and-structure/sql-statements/data-manipulation/changing-deleting-data/replace) statement first deletes the record with the same primary key and then inserts the new record. This function returns the number of deleted records in addition to the number of inserted records.
{% endhint %}

## See also

* [mysql\_num\_rows()](mysql_num_rows.md)

{% @marketo/form formid="4316" %}
