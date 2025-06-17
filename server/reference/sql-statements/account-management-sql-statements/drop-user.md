# DROP USER

## Syntax

```sql
DROP USER [IF EXISTS] user_name [, user_name] ...
```

## Description

The `DROP USER` statement removes one or more MariaDB accounts. It removes\
privilege rows for the account from all grant tables. To use this statement,\
you must have the global [CREATE USER](grant.md#create-user) privilege\
or the [DELETE](grant.md#table-privileges) privilege for the mysql database.\
Each account is named using the same format as for the `CREATE USER`\
statement; for example, `'jeffrey'@'localhost'`. If you specify\
only the user name part of the account name, a host name part of `'%'` is\
used. For additional information about specifying account names, see[CREATE USER](create-user.md).

Note that, if you specify an account that is currently connected, it will not\
be deleted until the connection is closed. The connection will not be\
automatically closed.

If any of the specified user accounts do not exist, `ERROR 1396 (HY000)`\
results. If an error occurs, `DROP USER` will still drop the accounts that do\
not result in an error. Only one error is produced for all users which have not\
been dropped:

```sql
ERROR 1396 (HY000): Operation DROP USER failed for 'u1'@'%','u2'@'%'
```

Failed `CREATE` or `DROP` operations, for both users and roles, produce the\
same error code.

#### IF EXISTS

If the `IF EXISTS` clause is used, MariaDB will return a note instead of an error if the user does not exist.

## Examples

```sql
DROP USER bob;

DROP USER foo2@localhost,foo2@'127.%';
```

`IF EXISTS`:

```sql
DROP USER bob;
ERROR 1396 (HY000): Operation DROP USER failed for 'bob'@'%'

DROP USER IF EXISTS bob;
Query OK, 0 rows affected, 1 warning (0.00 sec)

SHOW WARNINGS;
+-------+------+---------------------------------------------+
| Level | Code | Message                                     |
+-------+------+---------------------------------------------+
| Note  | 1974 | Can't drop user 'bob'@'%'; it doesn't exist |
+-------+------+---------------------------------------------+
```

## See Also

* [CREATE USER](create-user.md)
* [ALTER USER](alter-user.md)
* [GRANT](grant.md)
* [SHOW CREATE USER](../administrative-sql-statements/show/show-create-user.md)
* [mysql.user table](../administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-user-table.md)

<sub>_This page is licensed: GPLv2, originally from_</sub> [<sub>_fill\_help\_tables.sql_</sub>](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)

{% @marketo/form formId="4316" %}
