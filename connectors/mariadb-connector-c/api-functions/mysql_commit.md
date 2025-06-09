# mysql\_commit

## Syntax

```c
my_bool mysql_commit(MYSQL * mysql);
```

* `mysql` - a mysql handle, which was previously allocated by [mysql\_init()](mysql_init.md) or [mysql\_real\_connect()](mysql_real_connect.md).

## Description

Commits the current transaction for the specified database connection. Returns zero on success, nonzero if an error occurred.

{% hint style="info" %}
Executing mysql\_commit() will not affected the behaviour of [autocommit](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#autocommit). This means, any update or insert statements following mysql\_commit() will be rolled back when the connection gets closed.
{% endhint %}

## See also

* [mysql\_rollback()](mysql_rollback.md)


{% @marketo/form formid="4316" %}
