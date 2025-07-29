# mysql\_set\_server\_option

## Syntax

```c
int mysql_set_server_option(MYSQL * mysql,
  enum enum_mysql_set_option);
```

* `mysql` - a mysql handle, which was previously allocated by [mysql\_init()](mysql_init.md) or [mysql\_real\_connect()](mysql_real_connect.md).
* `enum_mysql_set_option` - server option (see below)

## Description

Server option, which can be one of the following values:

| Option                              | Description                      |
| ----------------------------------- | -------------------------------- |
| `MYSQL_OPTION_MULTI_STATEMENTS_OFF` | Disables multi statement support |
| `MYSQL_OPTION_MULTI_STATEMENTS_ON`  | Enable multi statement support   |

Returns zero on success, non-zero on failure.

## See also

* [mysql\_real\_connect()](mysql_real_connect.md)

{% @marketo/form formId="4316" %}
