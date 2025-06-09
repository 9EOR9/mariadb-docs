# mysql\_fetch\_field\_direct

## Syntax

```c
MYSQL_FIELD * mysql_fetch_field_direct(MYSQL_RES * res,
                                       unsigned int fieldnr);
```

* `res` - a result set identifier returned by [mysql\_store\_result()](mysql_store_result.md) or [mysql\_use\_result()](mysql_use_result.md).
* `fieldnr` - the field number. This value must be within the range from 0 to number of fields - 1

## Description

Returns a pointer to a MYSQL\_FIELD structure which contains field information from the specified result set.

{% hint style="info" %}
The total number of fields can be obtained by mysql\_field\_count()
{% endhint %}

## See also

* [mysql\_fetch\_field()](mysql_fetch_field.md)
* [mysql\_field\_count()](mysql_field_count.md)

{% @marketo/form formid="4316" %}
