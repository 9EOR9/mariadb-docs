
# mariadb-show

Shows the structure of a MariaDB database (databases, tables, columns and indexes).


Prior to [MariaDB 10.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-10-5-series/what-is-mariadb-105), the client was called `mysqlshow`. It can still be accessed under this name, via a symlink in Linux, or an alternate binary in Windows.


You can also use [SHOW DATABASES](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-databases.md), [SHOW TABLES](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-tables.md), [SHOW COLUMNS](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-columns.md), [SHOW INDEX](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-index.md) and [SHOW TABLE STATUS](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-table-status.md), as well as the [Information Schema](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/information-schema/README.md) tables ([TABLES](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-tables-table.md), [COLUMNS](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-columns-table.md), [STATISTICS](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-statistics-table.md)), to get similar functionality.


## Using mariadb-show


```
mariadb-show [OPTIONS] [database [table [column]]]
```

The output displays only the names of those databases, tables, or columns for which you have some privileges.


If no database is given then all matching databases are shown. If no table is given, then all matching tables in database are shown. If no column is given, then all matching columns and column types in table are shown.


If the last argument contains a shell or SQL wildcard (*,?,% or _) then only
what's matched by the wildcard is shown. If a database name contains any underscores, those should be escaped with a backslash (some Unix shells require two) to get a list of the proper tables or columns. “*” and “?” characters are converted into SQL “%” and “_” wildcard characters. This might cause some confusion when you try to display the columns for a table with a “_” in the name, because in this case, mariadb-show shows you only the table names that match the pattern. This is easily fixed by adding an extra “%” last on the command line as a separate argument.


### Options


`mariadb-show` supports the following options:



| Option | Description |
| --- | --- |
| Option | Description |
| -c name, --character-sets-dir=name | Directory for [character set](../reference/data-types/string-data-types/character-sets/README.md) files. |
| -C, --compress | Use compression in server/client protocol if both support it. |
| --count | Show number of rows per table (may be slow for non-[MyISAM](../reference/storage-engines/myisam-storage-engine/README.md) tables). |
| -

# [name], --debug[=name] | Output debug log. Typical is d:t:o,filename, the default is d:t:o. |
| --debug-check | Check memory and open file usage at exit. |
| --debug-info | Print some debug info at exit. |
| --default-auth=name | Default authentication client-side plugin to use. |
| --default-character-set=name | Set the default [character set](../reference/data-types/string-data-types/character-sets/README.md). |
| --defaults-extra-file=name | Read the file name after the global files are read. Must be given as the first option. |
| --defaults-file=name | Only read default options from the given file name. Must be given as the first option. |
| --defaults-group-suffix=suffix | In addition to the given groups, also read groups with this suffix. |
| -?, --help | Display help and exit. |
| -h name, --host=name | Connect to the MariaDB server on the given host. |
| -k, --keys | Show indexes for table. |
| --no-defaults | Don't read default options from any option file. Must be given as the first option. |
| -p[password], --password[=password] | Password to use when connecting to server. If password is not given, it's solicited on the command line. Specifying a password on the command line should be considered insecure. You can use an option file to avoid giving the password on the command line. |
| -W, --pipe | On Windows, connect to the server via a named pipe. This option applies only if the server supports named-pipe connections. |
| --plugin-dir=name | Directory for client-side plugins. |
| -P num, --port=num | Port number to use for connection or 0 for default to, in order of preference, my.cnf, $MYSQL_TCP_PORT, /etc/services, built-in default (3306). |
| --print-defaults | Print the program argument list and exit. Must be given as the first option. |
| --protocol=name | The protocol to use for connection (tcp, socket, pipe, memory). |
| --shared-memory-base-name=name | On Windows, the shared-memory name to use, for connections made using shared memory to a local server. The default value is MYSQL. The shared-memory name is case sensitive. The server must be started with the --shared-memory option to enable shared-memory connections. |
| -t, --show-table-type | Show table type column, as in [SHOW FULL TABLES](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-tables.md). The type is BASE TABLE or VIEW. |
| -S name, --socket=name | For connections to localhost, the Unix socket file to use, or, on Windows, the name of the named pipe to use. |
| --ssl | Enables [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/README.md). TLS is also enabled even without setting this option when certain other TLS options are set. Starting with [MariaDB 10.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/what-is-mariadb-102), the --ssl option will not enable [verifying the server certificate](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#server-certificate-verification) by default. In order to verify the server certificate, the user must specify the --ssl-verify-server-cert option. |
| --ssl-ca=name | Defines a path to a PEM file that should contain one or more X509 certificates for trusted Certificate Authorities (CAs) to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/README.md). This option requires that you use the absolute path, not a relative path. See [Secure Connections Overview: Certificate Authorities (CAs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-authorities-cas) for more information. This option implies the --ssl option. |
| --ssl-capath=name | Defines a path to a directory that contains one or more PEM files that should each contain one X509 certificate for a trusted Certificate Authority (CA) to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/README.md). This option requires that you use the absolute path, not a relative path. The directory specified by this option needs to be run through the [openssl rehash](https://www.openssl.org/docs/man1.1.1/man1/rehash.html) command. See [Secure Connections Overview: Certificate Authorities (CAs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-authorities-cas) for more information. This option is only supported if the client was built with OpenSSL. If the client was built with yaSSL, GnuTLS, or Schannel, then this option is not supported. See [TLS and Cryptography Libraries Used by MariaDB](../security/securing-mariadb/securing-mariadb-encryption/tls-and-cryptography-libraries-used-by-mariadb.md) for more information about which libraries are used on which platforms. This option implies the --ssl option. |
| --ssl-cert=name | Defines a path to the X509 certificate file to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/README.md). This option requires that you use the absolute path, not a relative path. This option implies the --ssl option. |
| --ssl-cipher=name | List of permitted ciphers or cipher suites to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/README.md). This option implies the --ssl option. |
| --ssl-key=name | Defines a path to a private key file to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/README.md). This option requires that you use the absolute path, not a relative path. This option implies the --ssl option. |
| --ssl-crl=name | Defines a path to a PEM file that should contain one or more revoked X509 certificates to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/README.md). This option requires that you use the absolute path, not a relative path. See [Secure Connections Overview: Certificate Revocation Lists (CRLs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-revocation-lists-crls) for more information. This option is only supported if the client was built with OpenSSL or Schannel. If the client was built with yaSSL or GnuTLS, then this option is not supported. See [TLS and Cryptography Libraries Used by MariaDB](../security/securing-mariadb/securing-mariadb-encryption/tls-and-cryptography-libraries-used-by-mariadb.md) for more information about which libraries are used on which platforms. This option implies the --ssl option. |
| --ssl-crlpath=name | Defines a path to a directory that contains one or more PEM files that should each contain one revoked X509 certificate to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/README.md). This option requires that you use the absolute path, not a relative path. The directory specified by this option needs to be run through the [openssl rehash](https://www.openssl.org/docs/man1.1.1/man1/rehash.html) command. See [Secure Connections Overview: Certificate Revocation Lists (CRLs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-revocation-lists-crls) for more information. This option is only supported if the client was built with OpenSSL. If the client was built with yaSSL, GnuTLS, or Schannel, then this option is not supported. See [TLS and Cryptography Libraries Used by MariaDB](../security/securing-mariadb/securing-mariadb-encryption/tls-and-cryptography-libraries-used-by-mariadb.md) for more information about which libraries are used on which platforms. This option implies the --ssl option. |
| --ssl-verify-server-cert | Enables (or disables) [server certificate verification](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#server-certificate-verification). This option is disabled by default. |
| -i, --status | Shows a lot of extra information about each table. See the [INFORMATION_SCHEMA.TABLES](../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-tables-table.md) table for more details on the returned information. |
| --tls-version=name | This option accepts a comma-separated list of TLS protocol versions. A TLS protocol version will only be enabled if it is present in this list. All other TLS protocol versions will not be permitted. See [Secure Connections Overview: TLS Protocol Versions](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#tls-protocol-versions) for more information. This option was added in [MariaDB 10.4.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-1046-release-notes). |
| -u, --user=name | User for login if not current user. |
| -v, --verbose | More verbose output; you can use this multiple times to get even more verbose output. |
| -V, --version | Output version information and exit. |



### Option Files


In addition to reading options from the command-line, `mariadb-show` can also read options from [option files](../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md). If an unknown option is provided to `mariadb-show` in an option file, then it is ignored.


The following options relate to how MariaDB command-line tools handles option files. They must be given as the first argument on the command-line:



| Option | Description |
| --- | --- |
| Option | Description |
| --print-defaults | Print the program argument list and exit. |
| --no-defaults | Don't read default options from any option file. |
| --defaults-file=# | Only read default options from the given file #. |
| --defaults-extra-file=# | Read this file after the global files are read. |
| --defaults-group-suffix=# | In addition to the default option groups, also read option groups with this suffix. |



In [MariaDB 10.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/what-is-mariadb-102) and later, `mariadb-show` is linked with [MariaDB Connector/C](/kb/en/about-mariadb-connector-c/). However, MariaDB Connector/C does not yet handle the parsing of option files for this client. That is still performed by the server option file parsing code. See [MDEV-19035](https://jira.mariadb.org/browse/MDEV-19035) for more information.


#### Option Groups


`mariadb-show` reads options from the following [option groups](../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md#option-groups) from [option files](../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md):



| Group | Description |
| --- | --- |
| Group | Description |
| [mysqlshow] | Options read by mysqlshow, which includes both MariaDB Server and MySQL Server. |
| [mariadb-show] | Options read by mariadb-show. Available starting with [MariaDB 10.4.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-1046-release-notes). |
| [client] | Options read by all MariaDB and MySQL [client programs](/kb/en/clients-utilities/), which includes both MariaDB and MySQL clients. For example, mysqldump. |
| [client-server] | Options read by all MariaDB [client programs](/kb/en/clients-utilities/) and the MariaDB Server. This is useful for options like socket and port, which is common between the server and the clients. |
| [client-mariadb] | Options read by all MariaDB [client programs](/kb/en/clients-utilities/). |



## Examples


Getting a list of databases:


```
bin/mariadb-show
+--------------------+
|     Databases      |
+--------------------+
| information_schema |
| test               |
+--------------------+
```

Getting a list of tables in the `test` database:


```
bin/mariadb-show test
Database: test
+---------+
| Tables  |
+---------+
| author  |
| book    |
| city    |
| country |
+---------+
```

Getting a list of columns in the `test`.`book` table:


```
bin/mariadb-show test book
Database: test  Table: book
+-----------+-----------------------+-------------------+------+-----+---------+----------------+--------------------------------+---------+
| Field     | Type                  | Collation         | Null | Key | Default | Extra          | Privileges                      | Comment |
+-----------+-----------------------+-------------------+------+-----+---------+----------------+--------------------------------+---------+
| id        | mediumint(8) unsigned |                   | NO   | PRI |         | auto_increment | select,insert,update,references |         |
| title     | varchar(200)          | latin1_swedish_ci | NO   |     |         |                | select,insert,update,references |         |
| author_id | smallint(5) unsigned  |                   | NO   | MUL |         |                | select,insert,update,references |         |
+-----------+-----------------------+-------------------+------+-----+---------+----------------+--------------------------------+---------+
```


CC BY-SA / Gnu FDL

