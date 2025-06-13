# PASSWORD

## Syntax

```
PASSWORD(str)
```

## Description

The PASSWORD() function is used for hashing passwords for use in authentication by the MariaDB server. It is not intended for use in other applications.

Calculates and returns a hashed password string from the plaintext password _str_. Returns an empty string (>= [MariaDB 10.0.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/mariadb-1004-release-notes)) if the argument was NULL.

The return value is a nonbinary string in the connection [character set and collation](../../../data-types/string-data-types/character-sets/), determined by the values of the [character\_set\_connection](../../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#character_set_connection) and [collation\_connection](../../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#collation_connection) system variables.

This is the function that is used for hashing MariaDB passwords for storage in the Password column of the [user table](../../../sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-user-table.md) (see [privileges](../../../sql-statements/account-management-sql-statements/grant.md)), usually used with the [SET PASSWORD](../../../sql-statements/account-management-sql-statements/set-password.md) statement. It is not intended for use in other applications.

Until [MariaDB 10.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/what-is-mariadb-103), the return value is 41-bytes in length, and the first character is always '\*'. From [MariaDB 10.4](broken-reference), the function takes into account the authentication plugin where applicable (A [CREATE USER](../../../sql-statements/account-management-sql-statements/create-user.md) or [SET PASSWORD](../../../sql-statements/account-management-sql-statements/set-password.md) statement). For example, when used in conjunction with a user authenticated by the [ed25519 plugin](../../../plugins/authentication-plugins/authentication-plugin-ed25519.md), the statement will create a longer hash:

```
CREATE USER edtest@localhost IDENTIFIED VIA ed25519 USING PASSWORD('secret');

CREATE USER edtest2@localhost IDENTIFIED BY 'secret';

SELECT CONCAT(user, '@', host, ' => ', JSON_DETAILED(priv)) FROM mysql.global_priv
  WHERE user LIKE 'edtest%'\G
*************************** 1. row ***************************
CONCAT(user, '@', host, ' => ', JSON_DETAILED(priv)): edtest@localhost => {
...
    "plugin": "ed25519",
    "authentication_string": "ZIgUREUg5PVgQ6LskhXmO+eZLS0nC8be6HPjYWR4YJY",
...
}
*************************** 2. row ***************************
CONCAT(user, '@', host, ' => ', JSON_DETAILED(priv)): edtest2@localhost => {
...
    "plugin": "mysql_native_password",
    "authentication_string": "*14E65567ABDB5135D0CFD9A70B3032C179A49EE7",
...
}
```

The behavior of this function is affected by the value of the [old\_passwords](../../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#old_passwords) system variable. If this is set to `1` (`0` is default), MariaDB reverts to using the [mysql\_old\_password authentication plugin](../../../plugins/authentication-plugins/authentication-plugin-mysql_old_password.md) by default for newly created users and passwords.

## Examples

```
SELECT PASSWORD('notagoodpwd');
+-------------------------------------------+
| PASSWORD('notagoodpwd')                   |
+-------------------------------------------+
| *3A70EE9FC6594F88CE9E959CD51C5A1C002DC937 |
+-------------------------------------------+
```

```
SET PASSWORD FOR 'bob'@'%.loc.gov' = PASSWORD('newpass');
```

## See Also

* [Password Validation Plugins](../../../plugins/password-validation-plugins/) - permits the setting of basic criteria for passwords
* [OLD\_PASSWORD()](old_password.md) - pre-MySQL 4.1 password function

<sub>_This page is licensed: GPLv2, originally from [fill\_help\_tables.sql](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)_</sub>

{% @marketo/form formId="4316" %}
