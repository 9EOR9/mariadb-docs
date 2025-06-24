# mariadb-backup and BACKUP STAGE Commands

The [BACKUP STAGE](../../../reference/sql-statements/administrative-sql-statements/backup-commands/backup-stage.md) commands are a set of commands to make it possible to make an efficient external backup tool. How mariadb-backup uses these commands depends on whether you are using the version that is bundled with MariaDB Community Server or the version that is bundled with MariaDB Enterprise Server.

## mariadb-backup and `BACKUP STAGE` Commands in MariaDB Community Server

The [BACKUP STAGE](../../../reference/sql-statements/administrative-sql-statements/backup-commands/backup-stage.md) commands are supported. However, the version of `mariadb-backup` that is bundled with MariaDB Community Server does not yet use the `BACKUP STAGE` commands in the most efficient way. mariadb-backup simply executes the following `BACKUP STAGE` commands to lock the database:

```sql
BACKUP STAGE START;
BACKUP STAGE BLOCK_COMMIT;
```

When the backup is complete, it executes the following `BACKUP STAGE` command to unlock the database:

```sql
BACKUP STAGE END;
```

If you would like to use a version of `mariadb-backup` that uses the [BACKUP STAGE](../../../reference/sql-statements/administrative-sql-statements/backup-commands/backup-stage.md) commands in the most efficient way, then your best option is to use MariaDB Backup that is bundled with MariaDB Enterprise Server.

### Tasks Performed Prior to `BACKUP STAGE` in MariaDB Community Server

* Copy some transactional tables.
  * InnoDB (i.e. `ibdataN` and file extensions `.ibd` and `.isl`)
* Copy the tail of some transaction logs.
  * The tail of the InnoDB redo log (i.e. `ib_logfileN` files) will be copied for InnoDB tables.

### `BACKUP STAGE START` in MariaDB Community Server

mariadb-backup from MariaDB Community Server does not currently perform any tasks in the `START` stage.

### `BACKUP STAGE FLUSH` in MariaDB Community Server

mariadb-backup from MariaDB Community Server does not currently perform any tasks in the `FLUSH` stage.

### `BACKUP STAGE BLOCK_DDL` in MariaDB Community Server

mariadb-backup from MariaDB Community Server does not currently perform any tasks in the `BLOCK_DDL` stage.

### `BACKUP STAGE BLOCK_COMMIT` in MariaDB Community Server

`mariadb-backup` from MariaDB Community Server performs the following tasks in the `BLOCK_COMMIT` stage:

* Copy other files.
  * i.e. file extensions `.frm`, `.isl`, `.TRG`, `.TRN`, `.opt`, `.par`
* Copy some transactional tables.
  * Aria (i.e. `aria_log_control` and file extensions `.MAD` and `.MAI`)
* Copy the non-transactional tables.
  * MyISAM (i.e. file extensions `.MYD` and `.MYI`)
  * MERGE (i.e. file extensions `.MRG`)
  * ARCHIVE (i.e. file extensions `.ARM` and `.ARZ`)
  * CSV (i.e. file extensions `.CSM` and `.CSV`)
* Create a MyRocks checkpoint using the rocksdb\_create\_checkpoint system variable.
* Copy the tail of some transaction logs.
  * The tail of the InnoDB redo log (i.e. `ib_logfileN` files) will be copied for InnoDB tables.
* Save the binary log position to xtrabackup\_binlog\_info.
* Save the Galera Cluster state information to xtrabackup\_galera\_info.

### `BACKUP STAGE END` in MariaDB Community Server

mariadb-backup from MariaDB Community Server performs the following tasks in the `END` stage:

* Copy the MyRocks checkpoint into the backup.

## mariadb-backup and `BACKUP STAGE` Commands in MariaDB Enterprise Server

The following sections describe how the MariaDB Backup version of mariadb-backup that is bundled with MariaDB Enterprise Server uses each [BACKUP STAGE](../../../reference/sql-statements/administrative-sql-statements/backup-commands/backup-stage.md) command in an efficient way.

### `BACKUP STAGE START` in MariaDB Enterprise Server

mariadb-backup from MariaDB Enterprise Server performs the following tasks in the `START` stage:

* Copy all transactional tables.
  * InnoDB (i.e. `ibdataN` and file extensions `.ibd` and `.isl`)
  * Aria (i.e. `aria_log_control` and file extensions `.MAD` and `.MAI`)
* Copy the tail of all transaction logs.
  * The tail of the InnoDB redo log (i.e. `ib_logfileN` files) will be copied for InnoDB tables.
  * The tail of the Aria redo log (i.e. `aria_log.N` files) will be copied for Aria tables.

### `BACKUP STAGE FLUSH` in MariaDB Enterprise Server

mariadb-backup from MariaDB Enterprise Server performs the following tasks in the `FLUSH` stage:

* Copy all non-transactional tables that are not in use. This list of used tables is found with SHOW OPEN TABLES.
  * MyISAM (i.e. file extensions `.MYD` and `.MYI`)
  * MERGE (i.e. file extensions `.MRG`)
  * ARCHIVE (i.e. file extensions `.ARM` and `.ARZ`)
  * CSV (i.e. file extensions `.CSM` and `.CSV`)
* Copy the tail of all transaction logs.
  * The tail of the InnoDB redo log (i.e. `ib_logfileN` files) will be copied for InnoDB tables.
  * The tail of the Aria redo log (i.e. `aria_log.N` files) will be copied for Aria tables.

### `BACKUP STAGE BLOCK_DDL` in MariaDB Enterprise Server

mariadb-backup from MariaDB Enterprise Server performs the following tasks in the `BLOCK_DDL` stage:

* Copy other files.
  * i.e. file extensions `.frm`, `.isl`, `.TRG`, `.TRN`, `.opt`, `.par`
* Copy the non-transactional tables that were in use during `BACKUP STAGE FLUSH`.
  * MyISAM (i.e. file extensions `.MYD` and `.MYI`)
  * MERGE (i.e. file extensions `.MRG`)
  * ARCHIVE (i.e. file extensions `.ARM` and `.ARZ`)
  * CSV (i.e. file extensions `.CSM` and `.CSV`)
* Check `ddl.log` for DDL executed before the `BLOCK DDL` stage.
  * The file names of newly created tables can be read from `ddl.log`.
  * The file names of dropped tables can also be read from `ddl.log`.
  * The file names of renamed tables can also be read from `ddl.log`, so the files can be renamed instead of re-copying them.
* Copy changes to system log tables.
  * mysql.general\_log
  * mysql.slow\_log
  * This is easy as these are append only.
* Copy the tail of all transaction logs.
  * The tail of the InnoDB redo log (i.e. `ib_logfileN` files) will be copied for InnoDB tables.
  * The tail of the Aria redo log (i.e. `aria_log.N` files) will be copied for Aria tables.

### `BACKUP STAGE BLOCK_COMMIT` in MariaDB Enterprise Server

mariadb-backup from MariaDB Enterprise Server performs the following tasks in the `BLOCK_COMMIT` stage:

* Create a MyRocks checkpoint using the rocksdb\_create\_checkpoint system variable.
* Copy changes to system log tables.
  * mysql.general\_log
  * mysql.slow\_log
  * This is easy as these are append only.
* Copy changes to statistics tables.
  * mysql.table\_stats
  * mysql.column\_stats
  * mysql.index\_stats
* Copy the tail of all transaction logs.
  * The tail of the InnoDB redo log (i.e. `ib_logfileN` files) will be copied for InnoDB tables.
  * The tail of the Aria redo log (i.e. `aria_log.N` files) will be copied for Aria tables.
* Save the binary log position to xtrabackup\_binlog\_info.
* Save the Galera Cluster state information to xtrabackup\_galera\_info.

### `BACKUP STAGE END` in MariaDB Enterprise Server

mariadb-backup from MariaDB Enterprise Server performs the following tasks in the `END` stage:

* Copy the MyRocks checkpoint into the backup.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
