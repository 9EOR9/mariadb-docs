# mariadb-backup Overview

**mariadb-backup** is an open source tool provided by MariaDB for performing physical online backups of [InnoDB](../../storage-engines/innodb/), [Aria](../../storage-engines/aria/) and [MyISAM](../../storage-engines/myisam-storage-engine/) tables. For InnoDB, “hot online” backups are possible. It was originally forked from [Percona XtraBackup](../../../clients-and-utilities/legacy-clients-and-utilities/backing-up-and-restoring-databases-percona-xtrabackup/) 2.3.8. It is available on Linux and Windows.

This tool provides a production-quality, nearly non-blocking method for performing full backups on running systems. While partial backups with mariadb-backup are technically possible, they require many steps and cannot be restored directly onto existing servers containing other data.

## Backup Support for MariaDB-Exclusive Features

[MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) introduced features that are exclusive to MariaDB, such as [InnoDB Page Compression](../../storage-engines/innodb/innodb-page-compression.md) and [Data-at-Rest Encryption](../../../security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/data-at-rest-encryption-overview.md). These exclusive features have been very popular with MariaDB users. However, existing backup solutions from the MySQL ecosystem, such as [Percona XtraBackup](../../../clients-and-utilities/legacy-clients-and-utilities/backing-up-and-restoring-databases-percona-xtrabackup/), did not support full backup capability for these features.

To address the needs of our users, we decided to develop a backup solution that would fully support these popular MariaDB-exclusive features. We did this by creating mariadb-backup, which is based on the well-known and commonly used backup tool called [Percona XtraBackup](../../../clients-and-utilities/legacy-clients-and-utilities/backing-up-and-restoring-databases-percona-xtrabackup/). mariadb-backup was originally extended from version 2.3.8.

### Supported Features

mariadb-backup supports all of the main features of [Percona XtraBackup](../../../clients-and-utilities/legacy-clients-and-utilities/backing-up-and-restoring-databases-percona-xtrabackup/) 2.3.8, plus:

* Backup/Restore of tables using [Data-at-Rest Encryption](../../../security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/data-at-rest-encryption-overview.md).
* Backup/Restore of tables using [InnoDB Page Compression](../../storage-engines/innodb/innodb-page-compression.md).
* [mariabackup SST method](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/galera-management/state-snapshot-transfers-ssts-in-galera-cluster/mariabackup-sst-method) with Galera Cluster.
* Microsoft Windows support.
* Backup/Restore of tables using the [MyRocks](../../storage-engines/myrocks/) storage engine starting with [MariaDB 10.2.16](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10216-release-notes) and [MariaDB 10.3.8](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1038-release-notes). See [Files Backed up by mariadb-backup: MyRocks Data Files](files-backed-up-by-mariabackup.md#myrocks-data-files) for more information.

#### Supported Features in MariaDB Enterprise Backup

Features were ported from the Enterprise Server to [MariaDB 10.11.8](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-11-series/mariadb-10-11-8-release-notes) - prior to that they were not available.

[MariaDB Backup](./) supports some additional features, such as:

* Minimizes locks during the backup to permit more concurrency and to enable faster backups.
  * This relies on the usage of [BACKUP STAGE](../../../reference/sql-statements/administrative-sql-statements/backup-commands/backup-stage.md) commands and DDL logging.
  * This includes no locking during the copy phase of [`ALTER TABLE`](../../../reference/sql-statements/data-definition/alter/alter-table.md) statements, which tends to be the longest phase of these statements.
* Provides optimal backup support for all storage engines that store things on local disk.

### Differences Compared to Percona XtraBackup

* Percona XtraBackup requires more locks to run than MariaDB. In addition, any running ALTER TABLE will block Percona XtraBackup until it completes.
* Percona XtraBackup copies its [InnoDB redo log](../../storage-engines/innodb/innodb-redo-log.md) files to the file `xtrabackup_logfile`, while Mariabackup uses the file  [ib\_logfile0](files-created-by-mariabackup.md#ib_logfile0).
* Percona XtraBackup's [libgcrypt-based encryption of backups](https://www.percona.com/doc/percona-xtrabackup/2.3/backup_scenarios/encrypted_backup.html) is not supported by Mariabackup.
* There is no symbolic link from `mariabackup` to [innobackupex](https://www.percona.com/doc/percona-xtrabackup/2.3/innobackupex/innobackupex_option_reference.html), as there is for [xtrabackup](https://www.percona.com/doc/percona-xtrabackup/2.3/xtrabackup_bin/xbk_option_reference.html). Instead, `mariabackup` has the [--innobackupex](mariabackup-options.md#-innobackupex) command-line option to enable innobackupex-compatible options.
* The [--compact](https://www.percona.com/doc/percona-xtrabackup/2.3/xtrabackup_bin/xbk_option_reference.html#cmdoption-xtrabackup-compact) and [--rebuild_indexes](https://www.percona.com/doc/percona-xtrabackup/2.3/xtrabackup_bin/xbk_option_reference.html#cmdoption-xtrabackup-rebuild-indexes) options are not supported.
* Support for [--stream=tar](https://www.percona.com/doc/percona-xtrabackup/2.3/howtos/recipes_ibkx_stream.html) was removed from Mariabackup in [MariaDB 10.1.24](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10124-release-notes).
* The [xbstream](https://www.percona.com/doc/percona-xtrabackup/2.3/xbstream/xbstream.html) utility has been renamed to `mbstream`. However, to select this output format when creating a backup, Mariabackup's [--stream](mariabackup-options.md#-stream) option still expects the `xbstream` value.
* Mariabackup does not support [lockless binlog](https://www.percona.com/doc/percona-xtrabackup/2.3/advanced/lockless_bin-log.html).

#### Difference in Versioning Schemes

Each Percona XtraBackup release has two version numbers--the Percona XtraBackup version number and the version number of the MySQL Server release that it is based on. For example:

```bash
xtrabackup version 2.2.8 based on MySQL server 5.6.22
```

Each mariadb-backup release only has one version number, and it is the same as the version number of the MariaDB Server release that it is based on. For example:

```bash
mariabackup based on MariaDB server 10.2.15-MariaDB Linux (x86_64)
```

See [Compatibility of mariadb-backup Releases with MariaDB Server Releases](mariabackup-overview.md#compatibility-of-mariabackup-releases-with-mariadb-server-releases) for more information on mariadb-backup versions.

## Compatibility of mariadb-backup Releases with MariaDB Server Releases

It is not generally possible, or supported, to prepare a backup in a different MariaDB version than the database version at the time when backup was taken. For example, if you backup [MariaDB 10.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104), you should use mariabackup version 10.4, rather than e.g 10.5.

A MariaDB Server version can often be backed up with most other mariadb-backup releases in the same release series. For example, [MariaDB 10.2.21](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10221-release-notes) and [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes) are both in the [MariaDB 10.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/what-is-mariadb-102) release series, so MariaDB Server from [MariaDB 10.2.21](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10221-release-notes) could be backed up by mariadb-backup from [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), or vice versa.

However, occasionally, a MariaDB Server or mariadb-backup release will include bug fixes that will break compatibility with previous releases. For example, the fix for [MDEV-13564](https://jira.mariadb.org/browse/MDEV-13564) changed the [InnoDB redo log](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/storage-engines/innodb/innodb-redo-log.md) format in [MariaDB 10.2.19](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10219-release-notes) which broke compatibility with previous releases. To be safest, a MariaDB Server release should generally be backed up with the mariadb-backup release that has the same version number.

mariadb-backup from [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) releases may also be able to back up MariaDB Server from [MariaDB 5.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5) and [MariaDB 10.0](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0) releases in many cases. However, this is not fully supported. See [MDEV-14936](https://jira.mariadb.org/browse/MDEV-14936) for more information.

## Installing mariadb-backup

### Installing on Linux

The `mariabackup` executable is included in [binary tarballs](../../../server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/installing-mariadb-binary-tarballs.md) on Linux.

#### Installing with a Package Manager

mariadb-backup can also be installed via a package manager on Linux. In order to do so, your system needs to be configured to install from one of the MariaDB repositories.

You can configure your package manager to install it from MariaDB Corporation's MariaDB Package Repository by using the [MariaDB Package Repository setup script](../../../server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/mariadb-package-repository-setup-and-usage.md).

You can also configure your package manager to install it from MariaDB Foundation's MariaDB Repository by using the [MariaDB Repository Configuration Tool](https://downloads.mariadb.org/mariadb/repositories/).

**Installing with yum/dnf**

On RHEL, CentOS, Fedora, and other similar Linux distributions, it is highly recommended to install the relevant [RPM package](../../../server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/rpm/) from MariaDB's\
repository using [yum](../../getting-installing-and-upgrading-mariadb/binary-packages/rpm/yum.md) or [dnf](https://en.wikipedia.org/wiki/DNF_(software)). Starting with RHEL 8 and Fedora 22, `yum` has been replaced by `dnf`, which is the next major version of `yum`. However, `yum` commands still work on many systems that use `dnf`. For example:

```bash
sudo yum install MariaDB-backup
```

**Installing with apt-get**

On Debian, Ubuntu, and other similar Linux distributions, it is highly recommended to install the relevant [DEB package](../../../server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/installing-mariadb-deb-files.md) from MariaDB's\
repository using [apt-get](https://wiki.debian.org/apt-get). For example:

```bash
sudo apt-get install mariadb-backup
```

**Installing with zypper**

On SLES, OpenSUSE, and other similar Linux distributions, it is highly recommended to install the relevant [RPM package](../../../server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/rpm/) from MariaDB's repository using [zypper](../../getting-installing-and-upgrading-mariadb/binary-packages/rpm/installing-mariadb-with-zypper.md). For example:

```bash
sudo zypper install MariaDB-backup
```

### Installing on Windows

The `mariabackup` executable is included in [MSI](../../../server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/installing-mariadb-msi-packages-on-windows.md) and [ZIP](../../../server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/installing-mariadb-windows-zip-packages.md) packages on Windows.

When using the [Windows MSI installer](../../../server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/installing-mariadb-msi-packages-on-windows.md), `mariabackup` can be installed by selecting _Backup utilities_:

![mariadb\_backup\_windows](../../../.gitbook/assets/mariadb_backup_windows.png)

## Using mariadb-backup

The command to use `mariabackup` and the general syntax is:

```bash
mariabackup <options>
```

For in-depth explanations on how to use mariadb-backup, see:

* [Full Backup and Restore with mariadb-backup](full-backup-and-restore-with-mariabackup.md)
* [Incremental Backup and Restore with mariadb-backup](incremental-backup-and-restore-with-mariabackup.md)
* [Partial Backup and Restore with mariadb-backup](partial-backup-and-restore-with-mariabackup.md)
* [Restoring Individual Tables and Partitions with mariadb-backup](restoring-individual-tables-and-partitions-with-mariabackup.md)
* [Setting up a Replication Slave with mariadb-backup](setting-up-a-replica-with-mariabackup.md)
* [Using Encryption and Compression Tools With mariadb-backup](using-encryption-and-compression-tools-with-mariabackup.md)

### Options

Options supported by mariadb-backup can be found [here](mariabackup-options.md).

`mariabackup` will currently silently ignore unknown command-line options, so be extra careful about accidentally including typos in options or accidentally using options from later `mariabackup` versions. The reason for this is that `mariabackup` currently treats command-line options and options from [option files](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md) equivalently. When it reads from these [option files](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), it has to read a lot of options from the [server option groups](mariabackup-overview.md#server-option-groups) read by [mysqld](../../getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md). However, `mariabackup` does not know about many of the options that it normally reads in these option groups. If `mariabackup` raised an error or warning when it encountered an unknown option, then this process would generate a large amount of log messages under normal use. Therefore, `mariabackup` is designed to silently ignore the unknown options instead. See [MDEV-18215](https://jira.mariadb.org/browse/MDEV-18215) about that.

### Option Files

In addition to reading options from the command-line, mariadb-backup can also read options from [option files](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md).

The following options relate to how MariaDB command-line tools handles option files. They must be given as the first argument on the command-line:

| Option                    | Description                                                                         |
| ------------------------- | ----------------------------------------------------------------------------------- |
| Option                    | Description                                                                         |
| --print-defaults          | Print the program argument list and exit.                                           |
| --no-defaults             | Don't read default options from any option file.                                    |
| --defaults-file=#         | Only read default options from the given option file.                               |
| --defaults-extra-file=#   | Read this file after the global files are read.                                     |
| --defaults-group-suffix=# | In addition to the default option groups, also read option groups with this suffix. |

#### Server Option Groups

mariadb-backup reads server options from the following [option groups](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) from [option files](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md):

| Group             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Group             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \[mariabackup]    | Options read by mariadb-backup. Available starting with [MariaDB 10.1.31](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10131-release-notes) and [MariaDB 10.2.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10213-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| \[mariadb-backup] | Options read by mariadb-backup. Available starting with [MariaDB 10.4.14](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-10414-release-notes) and [MariaDB 10.5.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1054-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \[xtrabackup]     | Options read by mariadb-backup and [Percona XtraBackup](../../../clients-and-utilities/legacy-clients-and-utilities/backing-up-and-restoring-databases-percona-xtrabackup/percona-xtrabackup-overview.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| \[server]         | Options read by MariaDB Server. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \[mysqld]         | Options read by mysqld, which includes both MariaDB Server and MySQL Server.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| \[mysqld-X.Y]     | Options read by a specific version of mysqld, which includes both MariaDB Server and MySQL Server. For example, \[mysqld-10.4]. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \[mariadb]        | Options read by MariaDB Server. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \[mariadb-X.Y]    | Options read by a specific version of MariaDB Server. For example, \[mariadb-10.4]. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \[mariadbd]       | Options read by MariaDB Server. Available starting with [MariaDB 10.4.14](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-10414-release-notes) and [MariaDB 10.5.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1054-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| \[mariadbd-X.Y]   | Options read by a specific version of MariaDB Server. For example, \[mariadbd-10.4]. Available starting with [MariaDB 10.4.14](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-10414-release-notes) and [MariaDB 10.5.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1054-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| \[client-server]  | Options read by all MariaDB [client programs](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/clients-utilities/README.md) and the MariaDB Server. This is useful for options like socket and port, which is common between the server and the clients. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| \[galera]         | Options read by MariaDB Server, but only if it is compiled with [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/galera/README.md) support. In [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) and later, all builds on Linux are compiled with [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/galera/README.md) support. When using one of these builds, options from this option group are read even if the [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/galera/README.md) functionality is not enabled. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes) on systems compiled with [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/galera/README.md) support. |

#### Client Option Groups

mariadb-backup reads client options from the following [option groups](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) from [option files](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md):

| Group             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Group             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \[mariabackup]    | Options read by mariadb-backup. Available starting with [MariaDB 10.1.31](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10131-release-notes) and [MariaDB 10.2.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10213-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| \[mariadb-backup] | Options read by mariadb-backup. Available starting with [MariaDB 10.4.14](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-10414-release-notes) and [MariaDB 10.5.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1054-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \[xtrabackup]     | Options read by mariadb-backup and [Percona XtraBackup](../../../clients-and-utilities/legacy-clients-and-utilities/backing-up-and-restoring-databases-percona-xtrabackup/percona-xtrabackup-overview.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| \[client]         | Options read by all MariaDB and MySQL [client programs](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/clients-utilities/README.md), which includes both MariaDB and MySQL clients. For example, mysqldump.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \[client-server]  | Options read by all MariaDB [client programs](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/clients-utilities/README.md) and the MariaDB Server. This is useful for options like socket and port, which is common between the server and the clients. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes). |
| \[client-mariadb] | Options read by all MariaDB [client programs](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/clients-utilities/README.md). Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                             |

### Authentication and Privileges

Mariabackup needs to authenticate with the database server when it performs a backup operation (i.e. when the [--backup](mariabackup-options.md#-backup) option is specified). For most use cases, the user account that performs the backup needs to have the following [global privileges](../../../reference/sql-statements/account-management-sql-statements/grant.md#global-privileges) on the database server.

In 10.5 and later the required privileges are:

```sql
CREATE USER 'mariabackup'@'localhost' IDENTIFIED BY 'mypassword';
GRANT RELOAD, PROCESS, LOCK TABLES, BINLOG MONITOR ON *.* TO 'mariabackup'@'localhost';
```

Prior to 10.5, the required privileges are:

```sql
CREATE USER 'mariabackup'@'localhost' IDENTIFIED BY 'mypassword';
GRANT RELOAD, PROCESS, LOCK TABLES, REPLICATION CLIENT ON *.* TO 'mariabackup'@'localhost';
```

If your database server is also using the [MyRocks](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/storage-engines/myrocks/README.md) storage engine, then the user account that performs the backup will also need the `SUPER` [global privilege](../../../reference/sql-statements/account-management-sql-statements/grant.md#global-privileges). This is because Mariabackup creates a checkpoint of this data by setting the [rocksdb_create_checkpoint](../../../reference/storage-engines/myrocks/myrocks-system-variables.md#rocksdb_create_checkpoint) system variable, which requires this privilege. See [MDEV-20577](https://jira.mariadb.org/browse/MDEV-20577) for more information.

`CONNECTION ADMIN` is also required where [-kill-long-queries-timeout](mariabackup-options.md#-kill-long-queries-timeout) is greater than 0, and [--no-lock](mariabackup-options.md#-no-lock) isn't applied in order to [KILL](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/kill.md) queries. Prior to 10.5 a `SUPER` privilege is required instead of `CONNECTION ADMIN`.

`REPLICA MONITOR` (or alias `SLAVE MONITOR`) is also required where [--galera-info](mariabackup-options.md#-galera-info) or [--slave-info](mariabackup-options.md#-slave-info) is specified.

To use the [--history](mariabackup-options.md#-history) option, the backup user also needs to have the following privileges granted:

```sql
GRANT CREATE, INSERT ON mysql.mariadb_backup_history TO 'mariabackup'@'localhost';
```

Prior to [MariaDB 10.11](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-11-series/what-is-mariadb-1011), the necessary permissions to use [--history](mariabackup-options.md#-history) were:

```sql
GRANT CREATE, INSERT ON PERCONA_SCHEMA.* TO 'mariabackup'@'localhost';
```

If you're upgrading from an older version and you want to use the new default table without losing your backup history, you can move and rename the current table in this way:

```sql
RENAME TABLE PERCONA_SCHEMA.xtrabackup_history TO mysql.mariadb_backup_history;
```

The user account information can be specified with the [--user](mariabackup-options.md#-user) and [--password](mariabackup-options.md#-p-password) command-line options. For example:

```bash
$ mariabackup --backup \
   --target-dir=/var/mariadb/backup/ \
   --user=mariabackup --password=mypassword
```

The user account information can also be specified in a supported [client option group](mariabackup-overview.md#client-option-groups) in an [option file](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md). For example:

```bash
[mariabackup]
user=mariabackup
password=mypassword
```

mariadb-backup does not need to authenticate with the database server when preparing or restoring a backup.

### File System Permissions

mariadb-backup has to read MariaDB's files from the file system. Therefore, when you run mariadb-backup as a specific operating system user, you should ensure that user account has sufficient permissions to read those files.

If you are using Linux and if you installed MariaDB with a package manager, then MariaDB's files will probably be owned by the `mysql` user and the `mysql` group.

### Using mariadb-backup with Data-at-Rest Encryption

mariadb-backup supports [Data-at-Rest Encryption](../../../security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/data-at-rest-encryption-overview.md).

mariadb-backup will query the server to determine which [key management and encryption plugin](../../../security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/key-management-and-encryption-plugins/encryption-key-management.md) is being used, and then it will load that plugin itself, which means that mariadb-backup needs to be able to load the key management and encryption plugin's shared library.

mariadb-backup will also query the server to determine which [encryption keys](../../../security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/key-management-and-encryption-plugins/encryption-key-management.md#using-multiple-encryption-keys) it needs to use.

In other words, mariadb-backup is able to figure out a lot of encryption-related information on its own, so normally one doesn't need to provide any extra options to backup or restore encrypted tables.

mariadb-backup backs up encrypted and unencrypted tables as they are on the original server. If a table is encrypted, then the table will remain encrypted in the backup. Similarly, if a table is unencrypted, then the table will remain unencrypted in the backup.

The primary reason that mariadb-backup needs to be able to encrypt and decrypt data is that it needs to apply [InnoDB redo log](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/storage-engines/innodb/innodb-redo-log.md) records to make the data consistent when the backup is prepared. As a consequence, mariadb-backup does not perform many encryption or decryption operations when the backup is initially taken. MariaDB performs more encryption and decryption operations when the backup is prepared. This means that some encryption-related problems (such as using the wrong encryption keys) may not become apparent until the backup is prepared.

### Using mariadb-backup for Galera SSTs

The `mariabackup` SST method uses the [mariadb-backup](./) utility for performing SSTs. See [mariabackup SST method](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/galera-management/state-snapshot-transfers-ssts-in-galera-cluster/mariabackup-sst-method) for more information.

## Files Backed up by mariadb-backup

mariadb-backup backs up many different files in order to perform its backup operation. See [Files Backed up by mariadb-backup](files-backed-up-by-mariabackup.md) for a list of these files.

## Files Created by mariadb-backup

mariadb-backup creates several different types of files during the backup and prepare phases. See [Files Created by mariadb-backup](files-created-by-mariabackup.md) for a list of these files.

## Binary logs

mariadb-backup can store the the binary log position in the backup. See [--binlog-info](mariabackup-options.md#-binlog-info). This can be used for point-in-time recovery and to use the backup to setup a slave with the correct binlog position.

## Known Issues

### Unsupported Server Option Groups

Prior to [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes), mariadb-backup doesn't read server options from all [option groups](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md#option-groups) supported by the server. In those versions, it only looks for server options in the following server option groups:

| Group          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Group          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| \[xtrabackup]  | Options read by Percona XtraBackup and mariadb-backup.                                                                                                                                                                                                                                                                                                                                                                                                      |
| \[mariabackup] | Options read by Percona XtraBackup and mariadb-backup. Available starting with [MariaDB 10.1.31](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10131-release-notes) and [MariaDB 10.2.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10213-release-notes). |
| \[mysqld]      | Options read by mysqld, which includes both MariaDB Server and MySQL Server.                                                                                                                                                                                                                                                                                                                                                                             |

Those versions do not read server options from the following option groups supported by the server:

| Group            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Group            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \[server]        | Options read by MariaDB Server. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \[mysqld-X.Y]    | Options read by a specific version of mysqld, which includes both MariaDB Server and MySQL Server. For example, \[mysqld-5.5] Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| \[mariadb]       | Options read by MariaDB Server. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \[mariadb-X.Y]   | Options read by a specific version of MariaDB Server. For example, \[mariadb-10.3] Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \[client-server] | Options read by all MariaDB [client programs](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/clients-utilities/README.md) and the MariaDB Server. This is useful for options like socket and port, which is common between the server and the clients. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| \[galera]        | Options read by MariaDB Server, but only if it is compiled with [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/galera/README.md) support. In [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) and later, all builds on Linux are compiled with [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/galera/README.md) support. When using one of these builds, options from this option group are read even if the [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/galera/README.md) functionality is not enabled. Available starting with [MariaDB 10.1.38](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10138-release-notes), [MariaDB 10.2.22](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10222-release-notes), and [MariaDB 10.3.13](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10313-release-notes) on systems compiled with [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/kb/en/galera/README.md) support. |

See [MDEV-18347](https://jira.mariadb.org/browse/MDEV-18347) for more information.

### No Default Datadir

Prior to [MariaDB 10.1.36](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10136-release-notes), [MariaDB 10.2.18](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10218-release-notes), and [MariaDB 10.3.10](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10310-release-notes), if you were performing a [--copy-back](mariabackup-options.md#-copy-back) operation, and if you did not explicitly specify a value for the [datadir](mariabackup-options.md#datadir) option either on the command line or one of the supported [server option groups](mariabackup-overview.md#server-option-group) in an [option file](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md), then Mariabackup would not default to the server's default `datadir`. Instead, Mariabackup would fail with an error. For example:

```bash
Error: datadir must be specified.
```

The solution is to explicitly specify a value for the [datadir](mariabackup-options.md#datadir) option either on the command line or in one of the supported [server option groups](mariabackup-overview.md#server-option-groups) in an [option file](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md). For example:

```bash
[mysqld]
datadir=/var/lib/mysql
```

In [MariaDB 10.1.36](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10136-release-notes), [MariaDB 10.2.18](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10218-release-notes), and [MariaDB 10.3.10](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10310-release-notes) and later, Mariabackup will default to the server's default [datadir](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#datadir) value.

See [MDEV-12956](https://jira.mariadb.org/browse/MDEV-12956) for more information.

### Concurrent DDL and Backup Issues

Prior to [MariaDB 10.2.19](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10219-release-notes) and [MariaDB 10.3.10](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10310-release-notes), if concurrent DDL was executed while the backup was taken, then that could cause various kinds of problems to occur.

One example is that if DDL caused any tablespace IDs to change (such as [TRUNCATE TABLE](../../../reference/sql-statements-and-structure/sql-statements/table-statements/truncate-table.md) or [RENAME TABLE](../../../reference/sql-statements-and-structure/sql-statements/data-definition/rename-table.md)), then that could cause the effected tables to be inconsistent in the backup. In this scenario, you might see errors about mismatched tablespace IDs when the backup is prepared.

For example, the errors might look like this:

```bash
2018-12-07 07:49:32 7f51b3184820  InnoDB: Error: table 'DB1/TAB_TEMP'
InnoDB: in InnoDB data dictionary has tablespace id 1355633,
InnoDB: but a tablespace with that id does not exist. There is
InnoDB: a tablespace of name DB1/TAB_TEMP and id 1354713, though. Have
InnoDB: you deleted or moved .ibd files?
InnoDB: Please refer to
InnoDB: http://dev.mysql.com/doc/refman/5.6/en/innodb-troubleshooting-datadict.html
InnoDB: for how to resolve the issue.
```

Or they might look like this:

```bash
2018-07-12 21:24:14 139666981324672 [Note] InnoDB: Ignoring data file 'db1/tab1.ibd' with space ID 200485, since the redo log references db1/tab1.ibd with space ID 200484.
```

Some of the problems related to concurrent DDL are described below.

Problems solved by setting [--lock-ddl-per-table](mariabackup-options.md#-lock-ddl-per-table) (Mariabackup command-line option added in [MariaDB 10.2.9](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1029-release-notes)):

* If a table is dropped during the backup, then it might still exists after the backup is prepared.
* If a table exists when the backup starts, but it is dropped before the backup copies it, then the tablespace file can't be copied, so the backup would fail.

Problems solved by setting [innodb_log_optimize_ddl=OFF](../../../reference/storage-engines/innodb/innodb-system-variables.md#innodb_log_optimize_ddl) (MariaDB Server system variable added in [MariaDB 10.2.17](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10217-release-notes) and removed in 10.6.0):

* If the backup noticed concurrent DDL, then it might fail with "ALTER TABLE or OPTIMIZE TABLE was executed during backup".

Problems solved by [innodb_safe_truncate=ON](../../../reference/storage-engines/innodb/innodb-system-variables.md#innodb_safe_truncate) (MariaDB Server system variable in [MariaDB 10.2.19](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10219-release-notes) and removed in 10.3.0):

* If a table is created during the backup, then it might not exist in the backup after prepare.
* If a table is renamed during the backup after the tablespace file was copied, then the table may not exist after the backup is prepared.
* If a table is dropped and created under the same name during the backup after the tablespace file was copied, then the table will have the wrong tablespace ID when the backup is prepared.

Note that, with the removal of `innodb_log_optimize_ddl` and `innodb_safe_truncate`, the above problems were definitely solved.

Problems solved by other bug fixes:

* If [--lock-ddl-per-table](mariabackup-options.md#-lock-ddl-per-table) is used and if a table is concurrently being dropped or renamed, then Mariabackup can fail to acquire the MDL lock.

These problems are only fixed in [MariaDB 10.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/what-is-mariadb-102) and later, so it is not recommended to execute concurrent DDL when using mariadb-backup with [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1).

See [MDEV-13563](https://jira.mariadb.org/browse/MDEV-13563), [MDEV-13564](https://jira.mariadb.org/browse/MDEV-13564), [MDEV-16809](https://jira.mariadb.org/browse/MDEV-16809), and [MDEV-16791](https://jira.mariadb.org/browse/MDEV-16791) for more information.

### Manual Restore with Pre-existing InnoDB Redo Log files

Prior to [MariaDB 10.2.10](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10210-release-notes), Mariabackup users could run into issues if they restored a backup by manually copying the files from the backup into the [datadir](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#datadir) while the directory still contained pre-existing [InnoDB redo log](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/storage-engines/innodb/innodb-redo-log.md) files. The backup itself did not contain [InnoDB redo log](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/storage-engines/innodb/innodb-redo-log.md) files with the traditional `ib_logfileN` file names, so the pre-existing log files would remain in the [datadir](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#datadir). If the server were started with these pre-existing log files, then it could perform crash recovery with them, which could cause the database to become inconsistent or corrupt.

In these MariaDB versions, this problem could be avoided by not restoring the backup by manually copying the files and instead restoring the backup by using Mariabackup and providing the [--copy-back](mariabackup-options.md#-copy-back) option, since Mariabackup deletes pre-existing [InnoDB redo log](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/storage-engines/innodb/innodb-redo-log.md) files from the [datadir](../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#datadir) during the restore process.

In [MariaDB 10.2.10](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10210-release-notes) and later, Mariabackup prevents this issue by creating an empty [InnoDB redo log](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/storage-engines/innodb/innodb-redo-log.md) file called [ib_logfile0](files-created-by-mariabackup.md#ib_logfile0) as part of the [--prepare](mariabackup-options.md#-prepare) stage. That way, if the backup is manually restored, any pre-existing [InnoDB redo log](https://github.com/mariadb-corporation/docs-server/blob/test/server/reference/storage-engines/innodb/innodb-redo-log.md) files would get overwritten by the empty one.

See [MDEV-13311](https://jira.mariadb.org/browse/MDEV-13311) for more information.

### Too Many Open Files

If mariadb-backup uses more file descriptors than the system is configured to allow, then users can see errors like the following:

```
2019-02-12 09:48:38 7ffff7fdb820  InnoDB: Operating system error number 23 in a file operation.
InnoDB: Error number 23 means 'Too many open files in system'.
InnoDB: Some operating system error numbers are described at
InnoDB: http://dev.mysql.com/doc/refman/5.6/en/operating-system-error-codes.html
InnoDB: Error: could not open single-table tablespace file ./db1/tab1.ibd
InnoDB: We do not continue the crash recovery, because the table may become
InnoDB: corrupt if we cannot apply the log records in the InnoDB log to it.
InnoDB: To fix the problem and start mysqld:
InnoDB: 1) If there is a permission problem in the file and mysqld cannot
InnoDB: open the file, you should modify the permissions.
InnoDB: 2) If the table is not needed, or you can restore it from a backup,
InnoDB: then you can remove the .ibd file, and InnoDB will do a normal
InnoDB: crash recovery and ignore that table.
InnoDB: 3) If the file system or the disk is broken, and you cannot remove
InnoDB: the .ibd file, you can set innodb_force_recovery > 0 in my.cnf
InnoDB: and force InnoDB to continue crash recovery here.
```

Prior to [MariaDB 10.1.39](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10139-release-notes), [MariaDB 10.2.24](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10224-release-notes), and [MariaDB 10.3.14](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10314-release-notes), mariadb-backup would actually ignore the error and continue the backup. In some of those cases, mariadb-backup would even report a successful completion of the backup to the user. In later versions, mariadb-backup will properly throw an error and abort when this error is encountered. See [MDEV-19060](https://jira.mariadb.org/browse/MDEV-19060) for more information.

When this error is encountered, one solution is to explicitly specify a value for the [open-files-limit](mariabackup-options.md#-open-files-limit) option either on the command line or in one of the supported [server option groups](mariabackup-overview.md#server-option-groups) in an [option file](../../../server-management/install-and-upgrade-mariadb/configuring-mariadb/configuring-mariadb-with-option-files.md). For example:

```bash
[mariabackup]
open_files_limit=65535
```

An alternative solution is to set the soft and hard limits for the user account that runs Mariabackup by adding new limits to [/etc/security/limits.conf](https://linux.die.net/man/5/limits.conf). For example, if Mariabackup is run by the `mysql` user, then you could add lines like the following:

```bash
mysql soft nofile 65535
mysql hard nofile 65535
```

After the system is rebooted, the above configuration should set new open file limits for the `mysql` user, and the user's `ulimit` output should look like the following:

```bash
$ ulimit -Sn
65535
$ ulimit -Hn
65535
```

## Versions

| mariadb-backup/Server Version                                                                                                                                                                                                                                                                                                                                                 | Maturity |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| mariadb-backup/Server Version                                                                                                                                                                                                                                                                                                                                                 | Maturity |
| [MariaDB 10.2.10](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10210-release-notes)+, [MariaDB 10.1.26](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10126-release-notes)+ | Stable   |
| [MariaDB 10.2.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-1027-release-notes)+, [MariaDB 10.1.25](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10125-release-notes)    | Beta     |
| [MariaDB 10.1.23](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10123-release-notes)                                                                                                                                                                                        | Alpha    |

## See Also

* [mariadb-dump/mysqldump](../../../clients-and-utilities/legacy-clients-and-utilities/mysqldump.md)
* [How to backup with MariaDB](https://www.youtube.com/watch?v=xB4ImmmzXqU) (video)
* [MariaDB point-in-time recovery](https://www.youtube.com/watch?v=ezHmnNmmcDo) (video)
* [mariadb-backup and Restic](https://www.youtube.com/watch?v=b-KFj8GfvzE) (video)
* [MariaDB Backup](./). An updated version of mariabackup.
* [Percona Xtrabackup 2.3 documentation](https://www.percona.com/doc/percona-xtrabackup/2.3/index.html/)

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
