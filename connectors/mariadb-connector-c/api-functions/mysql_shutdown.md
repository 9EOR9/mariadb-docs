# mysql\_shutdown

## Syntax

```c
int mysql_shutdown(MYSQL * mysql,
  enum mysql_enum_shutdown_level);
```

* `mysql` - a mysql handle, which was previously allocated by [mysql\_init()](mysql_init.md) or [mysql\_real\_connect()](mysql_real_connect.md).
* `mysql_enum_shutdown_level` - currently only one shutdown level, SHUTDOWN\_DEFAULT is supported.

## Description

Sends a shutdown message to the server. To shutdown the database server, the user for the current connection must have SHUTDOWN privileges.

Returns zero on success, non-zero on failure.

## See also

* [mysql\_kill()](mysql_kill.md)


{% @marketo/form formId="4316" %}
