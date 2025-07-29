# mysql\_refresh

## Syntax

```c
int mysql_refresh(MYSQL * mysql,
  unsigned int options);
```

* `mysql` - a mysql handle, which was previously allocated by [mysql\_init()](mysql_init.md) or [mysql\_real\_connect()](mysql_real_connect.md).
* `options` - a bit masked composed integer. See below.

## Description

Flushes different types of information stored on the server. The bit-masked parameter options specify which kind of information will be flushed. `options` can be any combination of the following:

| Option              | Description                                         |
| ------------------- | --------------------------------------------------- |
| REFRESH\_GRANT      | Refresh grant tables.                               |
| REFRESH\_LOG        | Flush logs.                                         |
| REFRESH\_TABLES     | Flush table cache.                                  |
| REFRESH\_HOSTS      | Flush host cache.                                   |
| REFRESH\_STATUS     | Reset status variables.                             |
| REFRESH\_THREADS    | Flush thread cache.                                 |
| REFRESH\_SLAVE      | Reset master server information and restart slaves. |
| REFRESH\_MASTER     | Remove binary log files.                            |
| REFRESH\_READ\_LOCK |                                                     |
| REFRESH\_FAST       |                                                     |

Returns zero on success, otherwise nonzero.

{% hint style="info" %}
To combine different values in the options parameter, use the OR operator '|'. The function `mysql_reload()` is an alias for `mysql_refresh()`.
{% endhint %}

{% @marketo/form formId="4316" %}
