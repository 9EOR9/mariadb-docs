# ALTER USER

### Syntax <a href="#syntax" id="syntax"></a>

```
ALTER USER [IF EXISTS] 
 user_specification [,user_specification] ...
  [REQUIRE {NONE | tls_option [[AND] tls_option] ...}]
  [WITH resource_option [resource_option] ...]
  [lock_option] [password_option] 

user_specification:
  username [authentication_option]

authentication_option:
  IDENTIFIED BY 'password' 
  | IDENTIFIED BY PASSWORD 'password_hash'
  | IDENTIFIED {VIA|WITH} authentication_rule [OR authentication_rule] ... 
 
authentication_rule:
  authentication_plugin
  | authentication_plugin {USING|AS} 'authentication_string'
  | authentication_plugin {USING|AS} PASSWORD('password')

tls_option
  SSL 
  | X509
  | CIPHER 'cipher'
  | ISSUER 'issuer'
  | SUBJECT 'subject'

resource_option
  MAX_QUERIES_PER_HOUR count
  | MAX_UPDATES_PER_HOUR count
  | MAX_CONNECTIONS_PER_HOUR count
  | MAX_USER_CONNECTIONS count
  | MAX_STATEMENT_TIME time

password_option:
  PASSWORD EXPIRE
  | PASSWORD EXPIRE DEFAULT
  | PASSWORD EXPIRE NEVER
  | PASSWORD EXPIRE INTERVAL N DAY

lock_option:
    ACCOUNT LOCK
  | ACCOUNT UNLOCK
}
```

### Description <a href="#description" id="description"></a>

The `ALTER USER` statement modifies existing MariaDB accounts. To use it, you must have the global [CREATE USER](https://mariadb.com/kb/en/grant/#global-privileges) privilege or the [UPDATE](https://mariadb.com/kb/en/grant/#table-privileges) privilege for the [mysql](https://mariadb.com/kb/en/the-mysql-database-tables/) database. The global [SUPER](https://mariadb.com/kb/en/grant/#global-privileges) privilege is also required if the [read\_only](https://mariadb.com/kb/en/server-system-variables/#read_only) system variable is enabled.

If any of the specified user accounts do not yet exist, an error results. If an error occurs, `ALTER USER` will still modify the accounts that do not result in an error. Only one error is produced for all users which have not been modified.

For renaming an existing account (user name and/or host), see [RENAME USER](https://mariadb.com/kb/en/rename-user/).

### IF EXISTS <a href="#if-exists" id="if-exists"></a>

When the `IF EXISTS` clause is used, MariaDB will return a warning instead of an error for each specified user that does not exist.

### Account Names <a href="#account-names" id="account-names"></a>

For `ALTER USER` statements, account names are specified as the `username` argument in the same way as they are for [CREATE USER](https://mariadb.com/kb/en/create-user/) statements. See [account names](https://mariadb.com/kb/en/create-user/#account-names) from the `CREATE USER` page for details on how account names are specified.

[CURRENT\_USER](https://mariadb.com/kb/en/current_user/) or `CURRENT_USER()` can also be used to alter the account logged into the current session. For example, to change the current user's password to `mariadb`:

```
ALTER USER CURRENT_USER() IDENTIFIED BY 'mariadb';
```

### Authentication Options <a href="#authentication-options" id="authentication-options"></a>

From [MariaDB 10.4](https://mariadb.com/kb/en/what-is-mariadb-104/), it is possible to use more than one authentication plugin for each user account. For example, this can be useful to slowly migrate users to the more secure ed25519 authentication plugin over time, while allowing the old mysql\_native\_password authentication plugin as an alternative for the transitional period. See [Authentication from MariaDB 10.4](https://mariadb.com/kb/en/authentication-from-mariadb-104/) for more.

When running `ALTER USER`, not specifying an authentication option in the IDENTIFIED VIA clause will remove that authentication method. (However this was not the case before [MariaDB 10.4.13](https://mariadb.com/kb/en/mariadb-10413-release-notes/), see [MDEV-21928](https://jira.mariadb.org/browse/MDEV-21928))

For example, a user is created with the ability to authenticate via both a password and unix\_socket:

```
CREATE USER 'bob'@'localhost' 
  IDENTIFIED VIA mysql_native_password USING PASSWORD('pwd') 
  OR unix_socket;

SHOW CREATE USER 'bob'@'localhost'\G
*************************** 1. row ***************************
CREATE USER for bob@localhost: CREATE USER `bob`@`localhost` 
  IDENTIFIED VIA mysql_native_password 
  USING '*975B2CD4FF9AE554FE8AD33168FBFC326D2021DD' 
  OR unix_socket
```

If the user's password is updated, but unix\_socket authentication is not specified in the `IDENTIFIED VIA` clause, unix\_socket authentication will no longer be permitted.

```
ALTER USER 'bob'@'localhost' IDENTIFIED VIA mysql_native_password 
  USING PASSWORD('pwd2');

SHOW CREATE USER 'bob'@'localhost'\G
*************************** 1. row ***************************
CREATE USER for bob@localhost: CREATE USER `bob`@`localhost` 
  IDENTIFIED BY PASSWORD '*38366FDA01695B6A5A9DD4E428D9FB8F7EB75512'
```

#### IDENTIFIED BY 'password' <a href="#identified-by-password" id="identified-by-password"></a>

The optional `IDENTIFIED BY` clause can be used to provide an account with a password. The password should be specified in plain text. It will be hashed by the [PASSWORD](https://mariadb.com/kb/en/password/) function prior to being stored to the [mysql.user](https://mariadb.com/kb/en/mysqluser-table/) table.

For example, if our password is `mariadb`, then we can set the account's password with:

```
ALTER USER foo2@test IDENTIFIED BY 'mariadb';
```

If you do not specify a password with the `IDENTIFIED BY` clause, the user will be able to connect without a password. A blank password is not a wildcard to match any password. The user must connect without providing a password if no password is set.

The only [authentication plugins](https://mariadb.com/kb/en/authentication-plugins/) that this clause supports are [mysql\_native\_password](https://mariadb.com/kb/en/authentication-plugin-mysql_native_password/) and [mysql\_old\_password](https://mariadb.com/kb/en/authentication-plugin-mysql_old_password/).

#### IDENTIFIED BY PASSWORD 'password\_hash' <a href="#identified-by-password-password_hash" id="identified-by-password-password_hash"></a>

The optional `IDENTIFIED BY PASSWORD` clause can be used to provide an account with a password that has already been hashed. The password should be specified as a hash that was provided by the [PASSWORD](https://mariadb.com/kb/en/password/)#function. It will be stored to the [mysql.user](https://mariadb.com/kb/en/mysqluser-table/) table as-is.

For example, if our password is `mariadb`, then we can find the hash with:

```
SELECT PASSWORD('mariadb');
+-------------------------------------------+
| PASSWORD('mariadb')                       |
+-------------------------------------------+
| *54958E764CE10E50764C2EECBB71D01F08549980 |
+-------------------------------------------+
```

And then we can set an account's password with the hash:

```
ALTER USER foo2@test 
  IDENTIFIED BY PASSWORD '*54958E764CE10E50764C2EECBB71D01F08549980';
```

If you do not specify a password with the `IDENTIFIED BY` clause, the user will be able to connect without a password. A blank password is not a wildcard to match any password. The user must connect without providing a password if no password is set.

The only [authentication plugins](https://mariadb.com/kb/en/authentication-plugins/) that this clause supports are [mysql\_native\_password](https://mariadb.com/kb/en/authentication-plugin-mysql_native_password/) and [mysql\_old\_password](https://mariadb.com/kb/en/authentication-plugin-mysql_old_password/).

#### IDENTIFIED {VIA|WITH} authentication\_plugin <a href="#identified-viawith-authentication_plugin" id="identified-viawith-authentication_plugin"></a>

The optional `IDENTIFIED VIA authentication_plugin` allows you to specify that the account should be authenticated by a specific [authentication plugin](https://mariadb.com/kb/en/authentication-plugins/). The plugin name must be an active authentication plugin as per [SHOW PLUGINS](https://mariadb.com/kb/en/show-plugins/). If it doesn't show up in that output, then you will need to install it with [INSTALL PLUGIN](https://mariadb.com/kb/en/install-plugin/) or [INSTALL SONAME](https://mariadb.com/kb/en/install-soname/).

For example, this could be used with the [PAM authentication plugin](https://mariadb.com/kb/en/authentication-plugin-pam/):

```
ALTER USER foo2@test IDENTIFIED VIA pam;
```

Some authentication plugins allow additional arguments to be specified after a `USING` or `AS` keyword. For example, the [PAM authentication plugin](https://mariadb.com/kb/en/authentication-plugin-pam/) accepts a [service name](https://mariadb.com/kb/en/authentication-plugin-pam/#configuring-the-pam-service):

```
ALTER USER foo2@test IDENTIFIED VIA pam USING 'mariadb';
```

The exact meaning of the additional argument would depend on the specific authentication plugin.

From [MariaDB 10.4](https://mariadb.com/kb/en/what-is-mariadb-104/), the `USING` or `AS` keyword can also be used to provide a plain-text password to a plugin if it's provided as an argument to the [PASSWORD()](https://mariadb.com/kb/en/password/) function. This is only valid for [authentication plugins](https://mariadb.com/kb/en/authentication-plugins/) that have implemented a hook for the [PASSWORD()](https://mariadb.com/kb/en/password/) function. For example, the [ed25519](https://mariadb.com/kb/en/authentication-plugin-ed25519/) authentication plugin supports this:

```
ALTER USER safe@'%' IDENTIFIED VIA ed25519 USING PASSWORD('secret');
```

### TLS Options <a href="#tls-options" id="tls-options"></a>

By default, MariaDB transmits data between the server and clients without encrypting it. This is generally acceptable when the server and client run on the same host or in networks where security is guaranteed through other means. However, in cases where the server and client exist on separate networks or they are in a high-risk network, the lack of encryption does introduce security concerns as a malicious actor could potentially eavesdrop on the traffic as it is sent over the network between them.

To mitigate this concern, MariaDB allows you to encrypt data in transit between the server and clients using the Transport Layer Security (TLS) protocol. TLS was formerly known as Secure Socket Layer (SSL), but strictly speaking the SSL protocol is a predecessor to TLS and, that version of the protocol is now considered insecure. The documentation still uses the term SSL often and for compatibility reasons TLS-related server system and status variables still use the prefix ssl\_, but internally, MariaDB only supports its secure successors.

See [Secure Connections Overview](https://mariadb.com/kb/en/secure-connections-overview/) for more information about how to determine whether your MariaDB server has TLS support.

You can set certain TLS-related restrictions for specific user accounts. For instance, you might use this with user accounts that require access to sensitive data while sending it across networks that you do not control. These restrictions can be enabled for a user account with the [CREATE USER](https://mariadb.com/kb/en/create-user/), [ALTER USER](https://mariadb.com/kb/en/alter-user/), or [GRANT](https://mariadb.com/kb/en/grant/) statements. The following options are available:

| Option                      | Description                                                                                                                                                                                                                                                                                                 |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `REQUIRE NONE`              | TLS is not required for this account, but can still be used.                                                                                                                                                                                                                                                |
| `REQUIRE SSL`               | The account must use TLS, but no valid X509 certificate is required. This option cannot be combined with other TLS options.                                                                                                                                                                                 |
| `REQUIRE X509`              | The account must use TLS and must have a valid X509 certificate. This option implies `REQUIRE SSL`. This option cannot be combined with other TLS options.                                                                                                                                                  |
| `REQUIRE ISSUER 'issuer'`   | The account must use TLS and must have a valid X509 certificate. Also, the Certificate Authority must be the one specified via the string `issuer`. This option implies `REQUIRE X509`. This option can be combined with the `SUBJECT`, and `CIPHER` options in any order.                                  |
| `REQUIRE SUBJECT 'subject'` | The account must use TLS and must have a valid X509 certificate. Also, the certificate's Subject must be the one specified via the string `subject`. This option implies `REQUIRE X509`. This option can be combined with the `ISSUER`, and `CIPHER` options in any order.                                  |
| `REQUIRE CIPHER 'cipher'`   | The account must use TLS, but no valid X509 certificate is required. Also, the encryption used for the connection must use a specific cipher method specified in the string `cipher`. This option implies `REQUIRE SSL`. This option can be combined with the `ISSUER`, and `SUBJECT` options in any order. |

The `REQUIRE` keyword must be used only once for all specified options, and the `AND` keyword can be used to separate individual options, but it is not required.

For example, you can alter a user account to require these TLS options with the following:

```
ALTER USER 'alice'@'%'
 REQUIRE SUBJECT '/CN=alice/O=My Dom, Inc./C=US/ST=Oregon/L=Portland' AND
 ISSUER '/C=FI/ST=Somewhere/L=City/ O=Some Company/CN=Peter Parker/emailAddress=p.parker@marvel.com'
 AND CIPHER 'SHA-DES-CBC3-EDH-RSA';
```

If any of these options are set for a specific user account, then any client who tries to connect with that user account will have to be configured to connect with TLS.

See [Securing Connections for Client and Server](https://mariadb.com/kb/en/securing-connections-for-client-and-server/) for information on how to enable TLS on the client and server.

### Resource Limit Options <a href="#resource-limit-options" id="resource-limit-options"></a>

It is possible to set per-account limits for certain server resources. The following table shows the values that can be set per account:

| Limit Type                 | Description                                                                                                                                                                                                                  |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `MAX_QUERIES_PER_HOUR`     | Number of statements that the account can issue per hour (including updates)                                                                                                                                                 |
| `MAX_UPDATES_PER_HOUR`     | Number of updates (not queries) that the account can issue per hour                                                                                                                                                          |
| `MAX_CONNECTIONS_PER_HOUR` | Number of connections that the account can start per hour                                                                                                                                                                    |
| `MAX_USER_CONNECTIONS`     | Number of simultaneous connections that can be accepted from the same account; if it is 0, `max_connections` will be used instead; if `max_connections` is 0, there is no limit for this account's simultaneous connections. |
| `MAX_STATEMENT_TIME`       | Timeout, in seconds, for statements executed by the user. See also [Aborting Statements that Exceed a Certain Time to Execute](https://mariadb.com/kb/en/aborting-statements/).                                              |

If any of these limits are set to `0`, then there is no limit for that resource for that user.

Here is an example showing how to set an account's resource limits:

```
ALTER USER 'someone'@'localhost' WITH
    MAX_USER_CONNECTIONS 10
    MAX_QUERIES_PER_HOUR 200;
```

The resources are tracked per account, which means `'user'@'server'`; not per user name or per connection.

The count can be reset for all users using [FLUSH USER\_RESOURCES](https://mariadb.com/kb/en/flush/), [FLUSH PRIVILEGES](https://mariadb.com/kb/en/flush/) or [mysqladmin reload](https://mariadb.com/kb/en/mysqladmin/).

Per account resource limits are stored in the [user](https://mariadb.com/kb/en/mysqluser-table/) table, in the [mysql](https://mariadb.com/kb/en/the-mysql-database-tables/) database. Columns used for resources limits are named `max_questions`, `max_updates`, `max_connections` (for `MAX_CONNECTIONS_PER_HOUR`), and `max_user_connections` (for `MAX_USER_CONNECTIONS`).

### Password Expiry <a href="#password-expiry" id="password-expiry"></a>

Besides automatic password expiry, as determined by [default\_password\_lifetime](https://mariadb.com/kb/en/server-system-variables/#default_password_lifetime), password expiry times can be set on an individual user basis, overriding the global setting, for example:

```
ALTER USER 'monty'@'localhost' PASSWORD EXPIRE INTERVAL 120 DAY;
ALTER USER 'monty'@'localhost' PASSWORD EXPIRE NEVER;
ALTER USER 'monty'@'localhost' PASSWORD EXPIRE DEFAULT;
```

See [User Password Expiry](https://mariadb.com/kb/en/user-password-expiry/) for more details.

### Account Locking <a href="#account-locking" id="account-locking"></a>

Account locking permits privileged administrators to lock/unlock user accounts. No new client connections will be permitted if an account is locked (existing connections are not affected). For example:

```
ALTER USER 'marijn'@'localhost' ACCOUNT LOCK;
```

See [Account Locking](https://mariadb.com/kb/en/account-locking/) for more details.

{% tabs %}
{% tab title="MariaDB < 10.4.7 / 10.5.8" %}
The _lock\_option_ and _password\_option_ clauses must occur in that order.
{% endtab %}
{% endtabs %}

### See Also <a href="#see-also" id="see-also"></a>

* [Authentication from MariaDB 10.4](https://mariadb.com/kb/en/authentication-from-mariadb-104/)
* [GRANT](https://mariadb.com/kb/en/grant/)
* [CREATE USER](https://mariadb.com/kb/en/create-user/)
* [DROP USER](https://mariadb.com/kb/en/drop-user/)
* [SET PASSWORD](https://mariadb.com/kb/en/set-password/)
* [SHOW CREATE USER](https://mariadb.com/kb/en/show-create-user/)
* [mysql.user table](https://mariadb.com/kb/en/mysqluser-table/)
* [Password Validation Plugins](https://mariadb.com/kb/en/password-validation-plugins/) - permits the setting of basic criteria for passwords
* [Authentication Plugins](https://mariadb.com/kb/en/authentication-plugins/) - allow various authentication methods to be used, and new ones to be developed.
