# mariadb-slap

## mariadb-slap

`mariadb-slap` is a tool for load-testing MariaDB. It allows you to emulate multiple concurrent connections, and run a set of queries multiple times.

Prior to [MariaDB 10.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/what-is-mariadb-105), the client was called `mysqlslap`. It can still be accessed under this name, via a symlink in Linux, or an alternate binary in Windows.

It returns a benchmark including the following information:

* Average number of seconds to run all queries
* Minimum number of seconds to run all queries
* Maximum number of seconds to run all queries
* Number of clients running queries
* Average number of queries per client

### Using mariadb-slap

The command to use `mariadb-slap` and the general syntax is:

```
mariadb-slap [options]
```

#### Options

`mariadb-slap` supports the following options:

| Option                                      | Description                                                                                                                                                                                                                                                                 |
| ------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Option                                      | Description                                                                                                                                                                                                                                                                 |
| -a, --auto-generate-sql                     | Generate SQL statements automatically when they are not supplied in files or via command options.                                                                                                                                                                           |
| --auto-generate-sql-add-autoincrement       | Add an [AUTO\_INCREMENT](../reference/data-types/auto_increment.md) column to auto-generated tables.                                                                                                                                                                        |
| --auto-generate-sql-execute-number=num      | Specify how many queries to generate automatically.                                                                                                                                                                                                                         |
| --auto-generate-sql-guid-primary            | Add GUID based primary keys to auto-generated tables.                                                                                                                                                                                                                       |
| --auto-generate-sql-load-type=name          | Specify the test load type. The allowable values are read (scan tables), write (insert into tables), key (read primary keys), update (update primary keys), or mixed (half inserts, half scanning selects). The default is mixed.                                           |
| --auto-generate-sql-secondary-indexes=num   | Number of secondary indexes to add to auto-generated tables. By default, none are added.                                                                                                                                                                                    |
| --auto-generate-sql-unique-query-number=num | Number of unique queries to generate for automatic tests. For example, if you run a key test that performs 1000 selects, you can use this option with a value of 1000 to run 1000 unique queries, or with a value of 50 to perform 50 different selects. The default is 10. |
| --auto-generate-sql-unique-write-number=num | Number of unique queries to generate for auto-generate-sql-write-number.                                                                                                                                                                                                    |
| --auto-generate-sql-write-number=num        | Number of row inserts to perform for each thread. The default is 100.                                                                                                                                                                                                       |
| --commit=num                                | Number of statements to execute before committing. The default is 0.                                                                                                                                                                                                        |
| -C, --compress                              | Use compression in server/client protocol if both support it.                                                                                                                                                                                                               |
| -c name, --concurrency=name                 | Number of clients to simulate for query to run.                                                                                                                                                                                                                             |
| --create=name                               | File or string containing the statement to use for creating the table.                                                                                                                                                                                                      |
| --create-schema=name                        | Schema to run tests in.                                                                                                                                                                                                                                                     |
| --csv\[=name]                               | Generate comma-delimited output to named file or to standard output if no file is named.                                                                                                                                                                                    |
| -                                           |                                                                                                                                                                                                                                                                             |

## , --debug\[=options] | For debug builds, write a debugging log. A typical debug\_options string is d:t:o,file\_name. The default is d:t:o,/tmp/mariadb-slap.trace. |

\| --debug-check | Check memory and open file usage at exit. |\
\| -T, --debug-info | Print some debug info at exit. |\
\| --default-auth=name | Default authentication client-side plugin to use. |\
\| --defaults-extra-file=name | Read this file after the global files are read. Must be given as the first option. |\
\| --defaults-file=name | Only read default options from the given file name Must be given as the first option. |\
\| -F name, --delimiter=name | Delimiter to use in SQL statements supplied in file or command line. |\
\| --detach=num | Detach (close and reopen) connections after the specified number of requests. The default is 0 (connections are not detached). |\
\| -e name, --engine=name | Comma separated list of storage engines to use for creating the table. The test is run for each engine. You can also specify an option for an engine after a #:#, for example memory:max\_row=2300. |\
\| -?, --help | Display help and exit. |\
\| -h name, --host=name | Connect to the MariaDB server on the given host. |\
\| --init-command=name | SQL Command to execute when connecting to the MariaDB server. Will automatically be re-executed when reconnecting. Added in [MariaDB 5.5.34](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/mariadb-5534-release-notes). |\
\| -i num, --iterations=num | Number of times to run the tests. |\
\| --no-defaults | Don't read default options from any option file. Must be given as the first option. |\
\| --no-drop | Do not drop any schema created during the test after the test is complete. |\
\| -x name, --number-char-cols=name | Number of [VARCHAR](../reference/data-types/string-data-types/varchar.md) columns to create in table if specifying --auto-generate-sql. |\
\| -y name, --number-int-cols=name | Number of [INT](../reference/data-types/numeric-data-types/int.md) columns to create in table if specifying --auto-generate-sql. |\
\| --number-of-queries=num | Limit each client to approximately this number of queries. Query counting takes into account the statement delimiter. For example, if you invoke as follows, mariadb-slap --delimiter=";" --number-of-queries=10 --query="use test;insert into t values(null)", the #;

## delimiter is recognized so that each instance of the query string counts as two queries. As a result, 5 rows (not 10) are inserted. |

\| --only-print | Do not connect to the databases, but instead print out what would have been done. |\
\| -p\[password], --password\[=password] | Password to use when connecting to server. If password is not given it's asked from the command line. Specifying a password on the command line should be considered insecure. You can use an option file to avoid giving the password on the command line. |\
\| -W, --pipe | On Windows, connect to the server via a named pipe. This option applies only if the server supports named-pipe connections. |\
\| --plugin-dir=name | Directory for client-side plugins. |\
\| -P num, --port=num | Port number to use for connection. |\
\| --post-query=name | Query to run or file containing query to execute after tests have completed. This execution is not counted for timing purposes. |\
\| --post-system=name | system() string to execute after tests have completed. This execution is not counted for timing purposes. |\
\| --pre-query=name | Query to run or file containing query to execute before running tests. This execution is not counted for timing purposes. |\
\| --pre-system=name | system() string to execute before running tests. This execution is not counted for timing purposes. |\
\| --print-defaults | Print the program argument list and exit. Must be given as the first option. |\
\| --protocol=name | The protocol to use for connection (tcp, socket, pipe, memory). |\
\| -q name, --query=name | Query to run or file containing query to run. |\
\| --shared-memory-base-name | Shared-memory name to use for Windows connections using shared memory to a local server (started with the --shared-memory option). Case-sensitive. |\
\| -s, --silent | Run program in silent mode - no output. |\
\| -S, --socket=name | For connections to localhost, the Unix socket file to use, or, on Windows, the name of the named pipe to use. |\
\| --ssl | Enables [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). TLS is also enabled even without setting this option when certain other TLS options are set. The --ssl option will not enable [verifying the server certificate](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#server-certificate-verification) by default. In order to verify the server certificate, the user must specify the --ssl-verify-server-cert option. |\
\| --ssl-ca=name | Defines a path to a PEM file that should contain one or more X509 certificates for trusted Certificate Authorities (CAs) to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. See [Secure Connections Overview: Certificate Authorities (CAs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-authorities-cas) for more information. This option implies the --ssl option. |\
\| --ssl-capath=name | Defines a path to a directory that contains one or more PEM files that should each contain one X509 certificate for a trusted Certificate Authority (CA) to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. The directory specified by this option needs to be run through the [openssl rehash](https://www.openssl.org/docs/man1.1.1/man1/rehash.html) command. See [Secure Connections Overview: Certificate Authorities (CAs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-authorities-cas) for more information. This option is only supported if the client was built with OpenSSL or yaSSL. If the client was built with GnuTLS or Schannel, then this option is not supported. See [TLS and Cryptography Libraries Used by MariaDB](../security/securing-mariadb/securing-mariadb-encryption/tls-and-cryptography-libraries-used-by-mariadb.md) for more information about which libraries are used on which platforms. This option implies the --ssl option. |\
\| --ssl-cert=name | Defines a path to the X509 certificate file to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. This option implies the --ssl option. |\
\| --ssl-cipher=name | List of permitted ciphers or cipher suites to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option implies the --ssl option. |\
\| --ssl-crl=name | Defines a path to a PEM file that should contain one or more revoked X509 certificates to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. See [Secure Connections Overview: Certificate Revocation Lists (CRLs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-revocation-lists-crls) for more information. This option is only supported if the client was built with OpenSSL or Schannel. If the client was built with yaSSL or GnuTLS, then this option is not supported. See [TLS and Cryptography Libraries Used by MariaDB](../security/securing-mariadb/securing-mariadb-encryption/tls-and-cryptography-libraries-used-by-mariadb.md) for more information about which libraries are used on which platforms. |\
\| --ssl-crlpath=name | Defines a path to a directory that contains one or more PEM files that should each contain one revoked X509 certificate to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. The directory specified by this option needs to be run through the [openssl rehash](https://www.openssl.org/docs/man1.1.1/man1/rehash.html) command. See [Secure Connections Overview: Certificate Revocation Lists (CRLs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-revocation-lists-crls) for more information. This option is only supported if the client was built with OpenSSL. If the client was built with yaSSL, GnuTLS, or Schannel, then this option is not supported. See [TLS and Cryptography Libraries Used by MariaDB](../security/securing-mariadb/securing-mariadb-encryption/tls-and-cryptography-libraries-used-by-mariadb.md) for more information about which libraries are used on which platforms. |\
\| --ssl-key=name | Defines a path to a private key file to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. This option implies the --ssl option. |\
\| --ssl-verify-server-cert | Enables [server certificate verification](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#server-certificate-verification). This option is disabled by default. |\
\| -u, --user=name | User for login if not current user. |\
\| -v, --verbose | More verbose output; you can use this multiple times to get even more verbose output. |\
\| -V, --version | Output version information and exit. |

#### Option Files

In addition to reading options from the command-line, `mariadb-slap` can also read options from [option files](../server-management/install-and-upgrade-mariadb/configuring-mariadb-with-option-files.md). If an unknown option is provided to `mariadb-slap` in an option file, then it is ignored.

The following options relate to how MariaDB command-line tools handles option files. They must be given as the first argument on the command-line:

| Option                    | Description                                                                         |
| ------------------------- | ----------------------------------------------------------------------------------- |
| Option                    | Description                                                                         |
| --print-defaults          | Print the program argument list and exit.                                           |
| --no-defaults             | Don't read default options from any option file.                                    |
| --defaults-file=#         | Only read default options from the given file #.                                    |
| --defaults-extra-file=#   | Read this file after the global files are read.                                     |
| --defaults-group-suffix=# | In addition to the default option groups, also read option groups with this suffix. |

`mariadb-slap` is linked with [MariaDB Connector/C](../../kb/en/about-mariadb-connector-c/). However, MariaDB Connector/C does not yet handle the parsing of option files for this client. That is still performed by the server option file parsing code. See [MDEV-19035](https://jira.mariadb.org/browse/MDEV-19035) for more information.

**Option Groups**

`mariadb-slap` reads options from the following [option groups](../server-management/install-and-upgrade-mariadb/configuring-mariadb-with-option-files.md#option-groups) from [option files](../server-management/install-and-upgrade-mariadb/configuring-mariadb-with-option-files.md):

| Group             | Description                                                                                                                                                                                                                              |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Group             | Description                                                                                                                                                                                                                              |
| \[mysqlslap]      | Options read by mariadb-slap, which includes both MariaDB Server and MySQL Server.                                                                                                                                                       |
| \[mariadb-slap]   | Options read by mariadb-slap. Available starting with [MariaDB 10.4.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-1046-release-notes). |
| \[client]         | Options read by all MariaDB and MySQL [client programs](../../kb/en/clients-utilities/), which includes both MariaDB and MySQL clients. For example, mysqldump.                                                                          |
| \[client-server]  | Options read by all MariaDB [client programs](../../kb/en/clients-utilities/) and the MariaDB Server. This is useful for options like socket and port, which is common between the server and the clients.                               |
| \[client-mariadb] | Options read by all MariaDB [client programs](../../kb/en/clients-utilities/).                                                                                                                                                           |

### Examples

Create a table with data, and then query it with 40 simultaneous connections 100 times each.

```
mariadb-slap 
 --delimiter=";" 
 --create="CREATE TABLE t (a int);INSERT INTO t VALUES (5)"
 --query="SELECT * FROM t"
 --concurrency=40
 --iterations=100

Benchmark
	Average number of seconds to run all queries: 0.010 seconds
	Minimum number of seconds to run all queries: 0.009 seconds
	Maximum number of seconds to run all queries: 0.020 seconds
	Number of clients running queries: 40
	Average number of queries per client: 1
```

Using files to store the create and query SQL. Each file can contain multiple statements separated by the specified delimiter.

```
mariadb-slap
 --create=define.sql
 --query=query.sql
 --concurrency=10
 --iterations=20
 --delimiter=";"

Benchmark
	Average number of seconds to run all queries: 0.002 seconds
	Minimum number of seconds to run all queries: 0.002 seconds
	Maximum number of seconds to run all queries: 0.004 seconds
	Number of clients running queries: 10
	Average number of queries per client: 1
```

CC BY-SA / Gnu FDL
