# mysql\_row\_seek

## Syntax

```c
MYSQL_ROW_OFFSET mysql_row_seek(MYSQL_RES * result,
    MYSQL_ROW_OFFSET offset);
```

* `result` - a result set identifier returned by [mysql\_store\_result()](mysql_store_result.md).
* `offset` - row offset. This value can be obtained either by `mysql_row_seek()` or [mysql\_row\_tell()](mysql_row_tell.md)

## Description

Positions the row cursor to an aribtrary row in a result set which was obtained by [mysql\_store\_result()](mysql_store_result.md). Returns the previous row offset.

{% hint style="info" %}
This function will not work if the result set was obtained by [mysql\_use\_result()](mysql_use_result.md).
{% endhint %}

## See also

* [mysql\_store\_result()](mysql_store_result.md)
* [mysql\_row\_tell()](mysql_row_tell.md)

{% @marketo/form formId="4316" %}
