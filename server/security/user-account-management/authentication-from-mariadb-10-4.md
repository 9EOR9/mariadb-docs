
# Authentication from MariaDB 10.4

[MariaDB 10.4](../../../release-notes/mariadb-community-server/what-is-mariadb-104.md) introduced a number of changes to the authentication process, intended to make things easier and more intuitive.


For Windows, see [Authentication Plugin - GSSAPI](../../reference/plugins/authentication-plugins/authentication-plugin-gssapi.md).


## Overview


There are four **new main features in 10.4** relating to authentication:


* It is possible to use more than one [authentication plugin](../../reference/plugins/authentication-plugins/README.md) for each user account. For example, this can be useful to slowly migrate users to the more secure [ed25519](../../reference/plugins/authentication-plugins/authentication-plugin-ed25519.md) authentication plugin over time, while allowing the old [mysql_native_password](../../reference/plugins/authentication-plugins/authentication-plugin-mysql_native_password.md) authentication plugin as an alternative for the transitional period.
* The `<code>root@localhost</code>` user account created by [mariadb-install-db](../../server-management/getting-installing-and-upgrading-mariadb/mariadb-install-db-exe.md) is created with the ability to use two [authentication plugins](../../reference/plugins/authentication-plugins/README.md).

  * First, it is configured to try to use the [unix_socket](../../reference/plugins/authentication-plugins/authentication-plugin-unix-socket.md) authentication plugin. This allows the `<code>root@localhost</code>` user to login without a password via the local Unix socket file defined by the [socket](../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#socket) system variable, as long as the login is attempted from a process owned by the operating system `<code>root</code>` user account.
  * Second, if authentication fails with the [unix_socket](../../reference/plugins/authentication-plugins/authentication-plugin-unix-socket.md) authentication plugin, then it is configured to try to use the [mysql_native_password](../../reference/plugins/authentication-plugins/authentication-plugin-mysql_native_password.md) authentication plugin. However, an invalid password is initially set, so in order to authenticate this way, a password must be set with [SET PASSWORD](../../reference/sql-statements-and-structure/sql-statements/account-management-sql-commands/set-password.md).
  * However, just using the [unix_socket](../../reference/plugins/authentication-plugins/authentication-plugin-unix-socket.md) authentication plugin may be fine for many users, and it is very secure. You may want to try going without password authentication to see how well it works for you. Remember, the best way to keep your password safe is not to have one!
* All user accounts, passwords, and global privileges are now stored in the [mysql.global_priv](../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-global_priv-table.md) table. The [mysql.user](../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-user-table.md) table still exists and has exactly the same set of columns as before, but it’s now a view that references the [mysql.global_priv](../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-global_priv-table.md) table. Tools that analyze the [mysql.user](../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-user-table.md) table should continue to work as before. From [MariaDB 10.4.13](../../../release-notes/mariadb-community-server/release-notes-mariadb-10-4-series/mariadb-10413-release-notes.md), the dedicated `<code>mariadb.sys</code>` user is created as the definer of this view. Previously `<code>root</code>` was the definer, which resulted in privilege problems when this username was changed.
* [MariaDB 10.4](../../../release-notes/mariadb-community-server/what-is-mariadb-104.md) adds supports for [User Password Expiry](user-password-expiry.md), which is not active by default.


## Description


As a result of the above changes, the open-for-everyone all-powerful root account is finally gone. And installation scripts will no longer demand that you “PLEASE REMEMBER TO SET A PASSWORD FOR THE MariaDB root USER !”, because the root account is securely created automatically.


Two all-powerful accounts are created by default — root and the OS user that owns the data directory, typically mysql. They are created as:


```
CREATE USER root@localhost IDENTIFIED VIA unix_socket OR mysql_native_password USING 'invalid'
CREATE USER mysql@localhost IDENTIFIED VIA unix_socket OR mysql_native_password USING 'invalid'
```

Using unix_socket means that if you are the system root user, you can login as root@locahost without a password. This technique was pioneered by Otto Kekäläinen in Debian MariaDB packages and has been successfully [used in Debian](../../server-management/getting-installing-and-upgrading-mariadb/troubleshooting-installation-issues/installation-issues-on-debian-and-ubuntu/differences-in-mariadb-in-debian-and-ubuntu.md) since as early as [MariaDB 10.0](../../../release-notes/mariadb-community-server/old-releases/release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md).


It is based on a simple fact that asking the system root for a password adds no extra security — root has full access to all the data files and all process memory anyway. But not asking for a password means, there is no root password to forget (no need for the numerous tutorials on “how to reset MariaDB root password”). And if you want to script some tedious database work, there is no need to store the root password in plain text for the script to use (no need for debian-sys-maint user).


Still, some users may wish to log in as MariaDB root without using sudo. Hence the old authentication method — conventional MariaDB password — is still available. By default it is disabled (“invalid” is not a valid password hash), but one can set the password with a usual [SET PASSWORD](../../reference/sql-statements-and-structure/sql-statements/account-management-sql-commands/set-password.md) statement. And still retain the password-less access via sudo.


If you install MariaDB locally (say from a tarball), you would not want to use sudo to be able to login. This is why MariaDB creates a second all-powerful user with the same name as a system user that owns the data directory. In local (not system-wide) installations, this will be the user who installed MariaDB — they automatically get convenient password-less root-like access, because they can access all the data files anyway.


Even if MariaDB is installed system-wide, you may not want to run your database maintenance scripts as system root — now you can run them as system mysql user. And you will know that they will never destroy your entire system, even if you make a typo in a shell script.


However, seasoned MariaDB DBAs who are used to the old ways do need to make some changes. See the examples below for common tasks.


## Cookbook


After installing MariaDB system-wide the first thing you’ve got used to doing is logging in into the unprotected root account and protecting it, that is, setting the root password:


```
$ sudo dnf install MariaDB-server
$ mariadb -uroot
...
MariaDB> set password = password("XH4VmT3_jt");
```

This is not only unnecessary now, it will simply not work — there is no unprotected root account. To login as root use


```
$ sudo dnf install MariaDB-server
$ sudo mariadb
```

Note that it implies you are connecting via the unix socket, not tcp. If you happen to have `<code>protocol=tcp</code>` in a system-wide `<code>/etc/my.cnf</code>` file, use `<code>sudo mariadb --protocol=socket</code>`.


After installing MariaDB locally you’ve also used to connect to the unprotected root account using `<code>mariadb -uroot</code>`. This will not work either, simply use `<code>mariadb</code>` without specifying a username.


If you've forgotten your root password, no problem — you can still connect using sudo and change the password. And if you've also removed unix_socket authentication, to restore access do as follows:


* restart MariaDB with [--skip-grant-tables](https://mariadb.com/kb/en/mariadb-options/#-skip-grant-tables)
* login into the unprotected server
* run [FLUSH PRIVILEGES](../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/flush-commands/flush-tables-for-export.md) (note, before 10.4 this would’ve been the last step, not anymore). This disables `<code>--skip-grant-tables</code>` and allows you to change the stored authentication method
* run [SET PASSWORD](../../reference/sql-statements-and-structure/sql-statements/account-management-sql-commands/set-password.md) FOR root@localhost to change the root password.


To view inside privilege tables, the old mysql.user table still exists. You can select from it as before, although you cannot update it anymore. It doesn’t show alternative authentication plugins and this was one of the reasons for switching to the mysql.global_priv table — complex authentication rules did not fit into rigid structure of a relational table. You can select from the new table, for example:


```
select concat(user, '@', host, ' => ', json_detailed(priv)) from mysql.global_priv;
```

## Reverting to the Previous Authentication Method for root@localhost


If you don't want the `<code>root@localhost</code>` user account created by [mariadb-install-db](../../server-management/getting-installing-and-upgrading-mariadb/mariadb-install-db-exe.md) to use [unix_socket](../../reference/plugins/authentication-plugins/authentication-plugin-unix-socket.md) authentication by default, then there are a few ways to revert to the previous [mysql_native_password](../../reference/plugins/authentication-plugins/authentication-plugin-mysql_native_password.md) authentication method for this user account.


### Configuring mariadb-install-db to Revert to the Previous Authentication Method


One way to revert to the previous [mysql_native_password](../../reference/plugins/authentication-plugins/authentication-plugin-mysql_native_password.md) authentication method for the `<code>root@localhost</code>` user account is to execute [mariadb-install-db](../../server-management/getting-installing-and-upgrading-mariadb/mariadb-install-db-exe.md) with a special option. If [mariadb-install-db](../../server-management/getting-installing-and-upgrading-mariadb/mariadb-install-db-exe.md) is executed while `<code>--auth-root-authentication-method=normal</code>` is specified, then it will create the default user accounts using the default behavior of [MariaDB 10.3](../../../release-notes/mariadb-community-server/what-is-mariadb-103.md) and before.


This means that the `<code>root@localhost</code>` user account will use [mysql_native_password](../../reference/plugins/authentication-plugins/authentication-plugin-mysql_native_password.md) authentication by default. There are some other differences as well. See [mariadb-install-db: User Accounts Created by Default](../../server-management/getting-installing-and-upgrading-mariadb/mariadb-install-db-exe.md#user-accounts-created-by-default) for more information.


For example, the option can be set on the command-line while running [mariadb-install-db](../../server-management/getting-installing-and-upgrading-mariadb/mariadb-install-db-exe.md):


```
mariadb-install-db --user=mysql --datadir=/var/lib/mysql --auth-root-authentication-method=normal
```

The option can also be set in an [option file](../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md) in an [option group](../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md#option-groups) supported by [mariadb-install-db](../../server-management/getting-installing-and-upgrading-mariadb/mariadb-install-db-exe.md). For example:


```
[mysql_install_db]
auth_root_authentication_method=normal
```

If the option is set in an [option file](../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md) and if [mariadb-install-db](../../server-management/getting-installing-and-upgrading-mariadb/mariadb-install-db-exe.md) is executed, then [mariadb-install-db](../../server-management/getting-installing-and-upgrading-mariadb/mariadb-install-db-exe.md) will read this option from the [option file](../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md), and it will automatically set this option.


### Altering the User Account to Revert to the Previous Authentication Method


If you have already installed MariaDB, and if the `<code>root@localhost</code>` user account is already using [unix_socket](../../reference/plugins/authentication-plugins/authentication-plugin-unix-socket.md) authentication, then you can revert to the old [mysql_native_password](../../reference/plugins/authentication-plugins/authentication-plugin-mysql_native_password.md) authentication method for the user account by executing the following:


```
ALTER USER root@localhost IDENTIFIED VIA mysql_native_password USING PASSWORD("verysecret")
```

## See Also


* [Authentication from MariaDB 10 4 video tutorial](https://www.youtube.com/watch?v=aWFG4uLbimM)
* [Authentication in MariaDB 10.4 — understanding the changes (mariadb.org)](https://mariadb.org/authentication-in-mariadb-10-4/)

