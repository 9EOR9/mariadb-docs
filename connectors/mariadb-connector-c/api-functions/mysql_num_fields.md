# mysql\_num\_fields

## Syntax

```c
unsigned int mysql_num_fields(MYSQL_RES * );
```

* `MYSQL RES *` - A result set identifier returned by [mysql\_store\_result()](mysql_store_result.md) or [mysql\_use\_result()](mysql_use_result.md).

## Description

Returns number of fields in a specified result set.

## See also

* [mysql\_fetch\_field()](mysql_fetch_field.md)


{% @marketo/form formid="4316" %}
