---
icon: question
---

# mariadb-upgrade

## mariadb-upgrade

`mariadb-upgrade` is a tool that checks and updates your tables to the latest version.

Prior to [MariaDB 10.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/what-is-mariadb-105), the client was called `mysql_upgrade`. It can still be accessed under this name, via a symlink in Linux, or an alternate binary in Windows.

You should run `mariadb-upgrade` after upgrading from one major MySQL/MariaDB release to another, such as [from MySQL 5.0 to MariaDB 10.4](../server-management/install-and-upgrade-mariadb/migrating-to-mariadb/moving-from-mysql/migrating-to-mariadb-from-mysql-obsolete-articles/upgrading-to-mariadb-from-mysql-50-or-older.md) or [MariaDB 10.4](broken-reference) to [MariaDB 10.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/what-is-mariadb-105). You also have to use `mariadb-upgrade` after a direct "horizontal" migration, for example from MySQL 5.5.40 to [MariaDB 5.5.40](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/mariadb-5540-release-notes). It's also safe to run `mariadb-upgrade` for minor upgrades, as if there are no incompatibilities nothing is changed.

It needs to be run as a user with write access to the data directory.

**MariaDB starting with** [**10.5.14**](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-10514-release-notes)

Starting from `mariadb-upgrade` 2.0, the user running the upgrade tool must have write access to `datadir/mysql_upgrade_info`, so that the tool can write the current MariaDB version into the file. `mariadb-upgrade` (or `mysql_upgrade`) was updated in [MariaDB 10.2.42](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10242-release-notes), [MariaDB 10.3.33](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10333-release-notes), [MariaDB 10.4.23](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-10423-release-notes), [MariaDB 10.5.14](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-10514-release-notes), [MariaDB 10.6.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1066-release-notes), [MariaDB 10.7.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series/mariadb-1072-release-notes) and newer.

`mariadb-upgrade` is run after starting the new MariaDB server. Running it before you shut down the old version will not hurt anything and will allow you to make sure it works and figure out authentication for it ahead of time.

It is recommended to make a [backup](broken-reference/) of all the databases before running `mariadb-upgrade`.

In most cases, `mariadb-upgrade` should just take a few seconds. The main work of `mariadb-upgrade` is to:

* Update the system tables in the `mysql` database to the latest version (normally just add new fields to a few tables).
* Check that all tables are up to date (runs [CHECK TABLE table\_name FOR UPGRADE](../reference/sql-statements/table-statements/check-table.md)). For tables that are not up to date, runs [ALTER TABLE table\_name FORCE](../reference/sql-statements/data-definition/alter/alter-table.md) on the table to update it. A table is not up to date if:
* The table uses an index for which there has been a [collation](../reference/data-types/string-data-types/character-sets/) change (rare)
* A format change in the storage engine requires an update (very rare)

### Using mariadb-upgrade

```
mariadb-upgrade [--force] [--user=# --password=# 
  --host=hostname --port=# --socket=#
  --protocol=tcp|socket|pipe|memory 
  --verbose] [OTHER_OPTIONS]
```

`mariadb-upgrade` is mainly a framework to call [mariadb-check](mariadb-check.md). `mariadb-upgrade` works by doing the following operations:

```
# Find out path to datadir
echo "show variables like 'datadir'" | mysql
mariadb-check --no-defaults --check-upgrade --auto-repair --databases mysql
mysql_fix_privilege_tables
mariadb-check --no-defaults --all-databases --fix-db-names --fix-table-names
mariadb-check --no-defaults --check-upgrade --all-databases --auto-repair
```

The connect options given to `mariadb-upgrade` are passed along to [mariadb-check](mariadb-check.md) and [mysql](mariadb-client/mysql-command-line-client.md).

The `mysql_fix_privilege_tables` script is not actually called; it's included as part of `mariadb-upgrade`

If you have a problem with `mariadb-upgrade` try run it in very verbose mode:

```
mariadb-upgrade --verbose --verbose other-options
```

`mariadb-upgrade` also saves the MariaDB version number in a file named `mysql_upgrade_info` in the [data directory](../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#datadir). This is used to quickly check whether all tables have been checked for this release so that table-checking can be skipped. For this reason,`mariadb-upgrade` needs to be run as a user with write access to the data directory. To ignore this file and perform the check regardless, use the `--force` option.

#### Options

`mariadb-upgrade` supports the following options:

| Option | Description |
| - | - |
| -?, --help | Display this help message and exit. |
| --basedir=path | Old option accepted for backward compatibility but ignored. |
| --character-sets-dir=path| Old option accepted for backward compatibility but ignored. |
| check-if-upgrade-is-needed | Do a quick check if upgrade is needed. Returns 0 if yes, 1 if no. From version 2.0. |
| --compress=name| Old option accepted for backward compatibility but ignored. |
| --datadir=name | Old option accepted for backward compatibility but ignored. |
| ## \[name], --debug\[=name] | For debug builds, output debug log. |
| --debug-check | Check memory and open file usage at exit. |
| -T, --debug-info | Print some debug info at exit. |
| --default-character-set=name | Old option accepted for backward compatibility but ignored. |
| -f, --force | Force execution of mariadb-check even if mariadb-upgrade has already been executed for the current version of MariaDB. Ignores mysql\_upgrade\_info. |
| -h, --host=name | Connect to MariaDB on the given host. |
| -p, --password\[=name] | Password to use when connecting to server. If password is not given, it's solicited on the command line (which should be considered insecure). You can use an option file to avoid giving the password on the command line. |
| -P, --port=name | Port number to use for connection or 0 for default to, in order of preference, my.cnf, the MYSQL\_TCP\_PORT [environment variable](../server-management/install-and-upgrade-mariadb/configuring-mariadb/mariadb-environment-variables.md), /etc/services, built-in default (3306). |
| --protocol=name | The protocol to use for connection (tcp, socket, pipe, memory). |
| --silent | Print less information. |
| -S, --socket=name | For connections to localhost, the Unix socket file to use, or, on Windows, the name of the named pipe to use. |
| --ssl | Enables [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). TLS is also enabled even without setting this option when certain other TLS options are set. Starting with [MariaDB 10.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/what-is-mariadb-102), the --ssl option will not enable [verifying the server certificate](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#server-certificate-verification) by default. In order to verify the server certificate, the user must specify the --ssl-verify-server-cert option. |
| --ssl-ca=name | Defines a path to a PEM file that should contain one or more X509 certificates for trusted Certificate Authorities (CAs) to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. See [Secure Connections Overview: Certificate Authorities (CAs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-authorities-cas) for more information. This option implies the --ssl option. |
| --ssl-capath=name | Defines a path to a directory that contains one or more PEM files that should each contain one X509 certificate for a trusted Certificate Authority (CA) to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. The directory specified by this option needs to be run through the [openssl rehash](https://www.openssl.org/docs/man1.1.1/man1/rehash.html) command. See [Secure Connections Overview: Certificate Authorities (CAs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-authorities-cas) for more information. This option is only supported if the client was built with OpenSSL or yaSSL. If the client was built with GnuTLS or Schannel, then this option is not supported. See [TLS and Cryptography Libraries Used by MariaDB](../security/securing-mariadb/securing-mariadb-encryption/tls-and-cryptography-libraries-used-by-mariadb.md) for more information about which libraries are used on which platforms. This option implies the --ssl option. |
| --ssl-cert=name | Defines a path to the X509 certificate file to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. This option implies the --ssl option. |
| --ssl-cipher=name | List of permitted ciphers or cipher suites to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option implies the --ssl option. |
| --ssl-crl=name | Defines a path to a PEM file that should contain one or more revoked X509 certificates to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. See [Secure Connections Overview: Certificate Revocation Lists (CRLs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-revocation-lists-crls) for more information. This option is only supported if the client was built with OpenSSL or Schannel. If the client was built with yaSSL or GnuTLS, then this option is not supported. See [TLS and Cryptography Libraries Used by MariaDB](../security/securing-mariadb/securing-mariadb-encryption/tls-and-cryptography-libraries-used-by-mariadb.md) for more information about which libraries are used on which platforms. |
| --ssl-crlpath=name | Defines a path to a directory that contains one or more PEM files that should each contain one revoked X509 certificate to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. The directory specified by this option needs to be run through the [openssl rehash](https://www.openssl.org/docs/man1.1.1/man1/rehash.html) command. See [Secure Connections Overview: Certificate Revocation Lists (CRLs)](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#certificate-revocation-lists-crls) for more information. This option is only supported if the client was built with OpenSSL. If the client was built with yaSSL, GnuTLS, or Schannel, then this option is not supported. See [TLS and Cryptography Libraries Used by MariaDB](../security/securing-mariadb/securing-mariadb-encryption/tls-and-cryptography-libraries-used-by-mariadb.md) for more information about which libraries are used on which platforms. |
| --ssl-key=name | Defines a path to a private key file to use for [TLS](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/). This option requires that you use the absolute path, not a relative path. This option implies the --ssl option. |
| --ssl-verify-server-cert | Enables [server certificate verification](../security/securing-mariadb/securing-mariadb-encryption/data-in-transit-encryption/secure-connections-overview.md#server-certificate-verification). This option is disabled by default. |
| -t, --tmpdir=name | Directory for temporary files. |
| -s, --upgrade-system-tables | Only upgrade the system tables in the mysql database. Tables in other databases are not checked or touched. |
| -u, --user=name | User for login if not current user. |
| -v, --verbose | Display more output about the process, using it twice will print connection arguments; using it 3 times will print out all [CHECK](../reference/sql-statements/table-statements/check-table.md), [RENAME](../reference/sql-statements/data-definition/rename-table.md) and [ALTER TABLE](../reference/sql-statements/data-definition/alter/alter-table.md) commands used during the check phase; using it 4 times will also write out all [mariadb-check](mariadb-check.md) commands used. |
| -V, --version | Output version information and exit. |
| -k, --version-check | Run this program only if its 'server version' matches the version of the server to which it's connecting check. Note: the 'server version' of the program is the version of the MariaDB server with which it was built/distributed. (Defaults to on; use --skip-version-check to disable.) |
| --write-binlog | All commands including those run by [mariadb-check](mariadb-check.md) are written to the [binary log](../server-management/server-monitoring-logs/binary-log/). Disabled by default. Before [MariaDB 10.0.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/mariadb-1006-release-notes) and [MariaDB 5.5.34](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/mariadb-5534-release-notes), this was enabled by default, and --skip-write-binlog should be used when commands should not be sent to replication slaves. |

### mariadb-upgrade 2.0

`mariadb-upgrate/mysql_upgrade 2.0` was introduced in [MariaDB 10.2.42](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10242-release-notes), [MariaDB 10.3.33](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10333-release-notes), [MariaDB 10.4.23](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-10423-release-notes), [MariaDB 10.5.14](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-10514-release-notes), [MariaDB 10.6.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-6-series/mariadb-1066-release-notes), [MariaDB 10.7.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series/mariadb-1072-release-notes).

Previously the tool first ran the upgrade process and then created the `datadir/mysql_upgrade_info` file. If the file could not be created because of permissions (`mariadb-upgrade` did not have rights to create the file), `mariadb-upgrad` gave an error, but this was often ignored.\
One effect of not being able to create the `mysql_upgrade_info` file was that every new `mariadb-upgrade` run would have to do a full upgrade check, which can take a while if there are a lot of tables.

`mariadb-upgrade` 2.0 fixes the following issues:

* The `datadir/mysql_upgrade_info` is now created at the start of the upgrade process and locked. This ensures that two `mariadb-upgrade` processes cannot be run in parallel, which can cause deadlocks ([MDEV-27068](https://jira.mariadb.org/browse/MDEV-27068)). One side-effect of this is that `mariadb-upgrade` has to have write access to `datadir`, which means it has to be run as as the user that installed MariaDB, normally 'mysql' or 'root' .
* One can use `mariadb-upgrade --force --force` to force the upgrade to be run, even if there was no version change or if one doesn't have write access to `datadir`. Note that if this option is used, the next `mariadb-upgrade` run will assume that there is a major version change and the upgrade must be done (again).
* The upgrade will only be done if there is a major server version change (10.4.X -> 10.5.X). This will avoid unnecessary upgrades.
* New option added: `--check-if-upgrade-is-needed`. If this is used, `mariadb-upgrade` will return 0 if there has been a major version change and one should run `mariadb-upgrade`. If not upgrade is need, 1 will be returned.
* `--verbose` writes more information, including from which version to which version the upgrade will be done.
* Better messages when there is no need to run `mariadb-upgrade`.

#### Option Files

In addition to reading options from the command-line, `mariadb-upgrade` can also read options from [option files](../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md). If an unknown option is provided to `mariadb-upgrade` in an option file, then it is ignored.

The following options relate to how MariaDB command-line tools handles option files. They must be given as the first argument on the command-line:

| Option| Description |
| - | - |
| --print-defaults| Print the program argument list and exit. |
| --no-defaults | Don't read default options from any option file.|
| --defaults-file=# | Only read default options from the given file #.|
| --defaults-extra-file=# | Read this file after the global files are read. |
| --defaults-group-suffix=# | In addition to the default option groups, also read option groups with this suffix. |

In [MariaDB 10.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/what-is-mariadb-102) and later, `mariadb-upgrade` is linked with [MariaDB Connector/C](../../kb/en/about-mariadb-connector-c/). However, MariaDB Connector/C does not yet handle the parsing of option files for this client. That is still performed by the server option file parsing code. See [MDEV-19035](https://jira.mariadb.org/browse/MDEV-19035) for more information.

**Option Groups**

`mariadb-upgrade` reads options from the following [option groups](../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) from [option files](../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md):

| Group| Description |
| - | - |
| [mysql\_upgrade]| Options read by mariadb-upgrade, which includes both MariaDB Server and MySQL Server. |
| [mariadb-upgrade] | Options read by mariadb-upgrade. Available starting with [MariaDB 10.4.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-1046-release-notes). |
| [client]| Options read by all MariaDB and MySQL [client programs](../../kb/en/clients-utilities/), which includes both MariaDB and MySQL clients. For example, mysqldump. |
| [client-server] | Options read by all MariaDB [client programs](../../kb/en/clients-utilities/) and the MariaDB Server. This is useful for options like socket and port, which is common between the server and the clients.|
| [client-mariadb]| Options read by all MariaDB [client programs](../../kb/en/clients-utilities/).|

### Differences Between mysql\_upgrade in MariaDB and MySQL

This is as of [MariaDB 5.1.50](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/mariadb-5150-release-notes):

* MariaDB will convert long [table names](../reference/sql-structure/sql-language-structure/identifier-names.md) properly.
* MariaDB will convert [InnoDB](../reference/storage-engines/innodb/) tables (no need to do a dump/restore or `[ALTER TABLE](../reference/sql-statements-and-structure/sql-statements/data-definition/alter/alter-table.md)`).
* MariaDB will convert old archive tables to the new 5.1 format.
* "mysql\_upgrade --verbose" will run "mariadb-check --verbose" so that you get more information of what is happening. Running with 3 times --verbose will in [MariaDB 10.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0) print out all CHECK, RENAME and ALTER TABLE commands executed.
* The [mysql.event table](../reference/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-event-table.md) is upgraded live; no need to restart the server to use events if the event table has changed ([MariaDB 10.0.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/mariadb-10022-release-notes) and [MariaDB 10.1.9](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10-1-9-release-notes)).
* More descriptive output.

### Speeding Up mariadb-upgrade

* If you are sure that all your tables are up to date with the current version, then you can run `mariadb-upgrade ---upgrade-system-tables`, which will only fix your system tables in the mysql database to be compatible with the latest version.

The main reason to run `mariadb-upgrade` on all your tables is to allow it to check that:

* There has not been any change in table formats between versions.
* This has not happened since [MariaDB 5.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/changes-improvements-in-mariadb-5-1).
* If some of the tables are using an index for which we have changed sort order.
* This has not happened since [MariaDB 5.5](broken-reference).

If you are 100% sure this applies to you, you can just run `mariadb-upgrade` with the `---upgrade-system-tables` option.

### Symptoms of Not Having Run mariadb-upgrade When It Was Needed

* Errors in the [error log](../server-management/server-monitoring-logs/error-log.md) that some system tables don't have all needed columns.
* Updates or searches may not find the record they are attempting to update or search for.
* [CHECKSUM TABLE](../reference/sql-statements/table-statements/checksum-table.md) may report the wrong checksum for [MyISAM](../reference/storage-engines/myisam-storage-engine/) or [Aria](../reference/storage-engines/aria/) tables.
* The error message "Cannot load from mysql.proc. The table is probably corrupted."

To fix issues like this, run `mariadb-upgrade`, [mariadb-check](mariadb-check.md), [CHECK TABLE](../reference/sql-statements/table-statements/check-table.md) and if needed [REPAIR TABLE](../reference/sql-statements/table-statements/repair-table.md) on the wrong table.

### Other Uses

* `mariadb-upgrade` will re-create any missing tables in the [mysql database](../reference/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/). It will not touch any data in existing tables.

### See Also

* [mariadb-check](mariadb-check.md)
* [CHECK TABLE](../reference/sql-statements/table-statements/check-table.md)
* [REPAIR TABLE](../reference/sql-statements/table-statements/repair-table.md)
* [Downgrading between Major Versions of MariaDB](../server-management/install-and-upgrade-mariadb/downgrading-between-major-versions-of-mariadb.md)

CC BY-SA / Gnu FDL
