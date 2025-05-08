# Authentication with gssapi

## Overview

The gssapi [authentication plugin](../../reference/plugins/authentication-plugins/authentication-plugin-gssapi.md) validates user credentials against a GSSAPI-based authentication service, like Kerberos or NTLM.

## Install Package

The gssapi [authentication plugin](../../reference/plugins/authentication-plugins/authentication-plugin-gssapi.md) requires an additional package to be installed on Linux.\
On CentOS, RHEL, and Rocky Linux:

```
$ sudo yum install MariaDB-gssapi-server
```

On Debian and Ubuntu:

```
$ sudo apt install mariadb-plugin-gssapi-server
```

On SLES:

```
$ sudo zypper install MariaDB-gssapi-server
```

## Configure

The gssapi [authentication plugin](../../reference/plugins/authentication-plugins/authentication-plugin-gssapi.md) requires some system variables to be configured, including:

* gssapi\_keytab\_path
* gssapi\_principal\_name

For example:

```
[mariadb]
...
gssapi_keytab_path=KEYTAB_PATH
gssapi_principal_name=PRINCIPAL_NAME
```

## Install Plugin

The gssapi [authentication plugin](../../reference/plugins/authentication-plugins/authentication-plugin-gssapi.md) must be installed before it can be used.

To install with the INSTALL SONAME statement:

```
INSTALL SONAME 'gssapi';
```

To install in a configuration file with the plugin\_load\_add [option](https://mariadb.com/kb/en/option):

```
[mariadb]
...
plugin_load_add = auth_gssapi
```

## Create User

To create a user account that uses the gssapi [authentication plugin](../../reference/plugins/authentication-plugins/authentication-plugin-gssapi.md), specify the plugin in the CREATE USER statement:

```
CREATE USER 'USER'@'192.0.2.%'
   IDENTIFIED VIA gssapi;
```

An optional realm can be specified:

```
CREATE USER 'USER'@'192.0.2.%'
   IDENTIFIED VIA gssapi USING 'USER@DOMAIN';
```

Copyright © 2025 MariaDB
