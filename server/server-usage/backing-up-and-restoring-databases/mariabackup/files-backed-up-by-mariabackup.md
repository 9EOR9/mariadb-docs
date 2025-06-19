# Files Backed Up By mariadb-backup

## Files Included in Backup

mariadb-backup backs up the files listed below.

### InnoDB Data Files

mariadb-backup backs up the following InnoDB data files:

* [InnoDB system tablespace](../../storage-engines/innodb/innodb-tablespaces/innodb-system-tablespaces.md)
* [InnoDB file-per-table tablespaces](../../storage-engines/innodb/innodb-tablespaces/innodb-file-per-table-tablespaces.md)

### MyRocks Data Files

<<<<<<< HEAD
Starting with [MariaDB 10.2.16](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10216-release-notes) and [MariaDB 10.3.8](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1038-release-notes), mariadb-backup will back up tables that use the [MyRocks](../../storage-engines/myrocks/) storage engine. This data data is located in the directory defined by the `[rocksdb_datadir](../../../reference/storage-engines/myrocks/myrocks-system-variables.md#rocksdb_datadir)` system variable. mariadb-backup backs this data up by performing a checkpoint using the `[rocksdb_create_checkpoint](../../../reference/storage-engines/myrocks/myrocks-system-variables.md#rocksdb_create_checkpoint)` system variable.
=======
Starting with [MariaDB 10.2.16](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-2-series/mariadb-10216-release-notes) and [MariaDB 10.3.8](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-1038-release-notes), Mariabackup will back up tables that use the [MyRocks](../../storage-engines/myrocks/) storage engine. This data data is located in the directory defined by the [rocksdb_datadir](../../../reference/storage-engines/myrocks/myrocks-system-variables.md#rocksdb_datadir) system variable. Mariabackup backs this data up by performing a checkpoint using the [rocksdb_create_checkpoint](../../../reference/storage-engines/myrocks/myrocks-system-variables.md#rocksdb_create_checkpoint) system variable.
>>>>>>> 2f4a7af992d60113345320299a7c689ee31815c1

mariadb-backup does not currently support [partial backups](partial-backup-and-restore-with-mariabackup.md) for MyRocks.

### Other Data Files

mariadb-backup also backs up files with the following extensions:

* `frm`
* `isl`
* `MYD`
* `MYI`
* `MAD`
* `MAI`
* `MRG`
* `TRG`
* `TRN`
* `ARM`
* `ARZ`
* `CSM`
* `CSV`
* `opt`
* `par`

## Files Excluded From Backup

mariadb-backup does **not** back up the files listed below.

* [InnoDB Temporary Tablespaces](../../storage-engines/innodb/innodb-tablespaces/innodb-temporary-tablespaces.md)
* [Binary logs](../../../server-management/server-monitoring-logs/binary-log/)
* [Relay logs](../../../server-management/server-monitoring-logs/binary-log/relay-log.md)

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
