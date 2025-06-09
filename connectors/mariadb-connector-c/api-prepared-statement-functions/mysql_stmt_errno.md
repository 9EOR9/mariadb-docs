# mysql\_stmt\_errno

## Syntax

```c
unsigned int mysql_stmt_errno(MYSQL_STMT * stmt);
```

* `stmt` - a statement handle, which was previously allocated by [mysql\_stmt\_init()](mysql_stmt_init.md).

## Description

Returns the [error code](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/mariadb-internals/using-mariadb-with-your-programs-api/error-codes/mariadb-error-code-reference) for the most recently invoked statement function that can succeed or fail. Zero means no error occurred.

{% hint style="info" %}
Client error messages are listed in errmsg.h header file, server error messages are listed in mysqld\_error.h header file of the server source distribution.
{% endhint %}

## See Also

* [mysql\_stmt\_error()](mysql_stmt_error.md),
* [mysql\_stmt\_sqlstate()](mysql_stmt_sqlstate.md)


{% @marketo/form formid="4316" %}
