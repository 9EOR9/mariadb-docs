# mysql\_stmt\_fetch

## Syntax

```c
int mysql_stmt_fetch(MYSQL_STMT * stmt);
```

* `stmt` - a statement handle, which was previously allocated by [mysql\_stmt\_init()](mysql_stmt_init.md).

## Description

Fetch the result from a prepared statement into the buffer bound by mysql\_stmt\_bind\_result(). Returns `0` for success, `MYSQL_NO_DATA` if the end of the result set has been reached, or `MYSQL_DATA_TRUNCATED` if one or more values are truncated.

{% hint style="info" %}
Note that all columns must be bound by the application before calling mysql\_stmt\_fetch().

Data are transferred unbuffered without calling [mysql\_stmt\_store\_result()](mysql_stmt_store_result.md) which can decrease performance (but reduces memory cost).
{% endhint %}

## See Also

* [mysql\_stmt\_prepare()](mysql_stmt_prepare.md)
* [mysql\_stmt\_bind\_result()](mysql_stmt_bind_result.md)
* [mysql\_stmt\_execute()](mysql_stmt_execute.md)


{% @marketo/form formid="4316" %}
