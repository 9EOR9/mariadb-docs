# REPAIR TABLE

## Syntax

<= [MariaDB 11.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-11-4-series/what-is-mariadb-114)

```
REPAIR [NO_WRITE_TO_BINLOG | LOCAL] TABLE
    tbl_name [, tbl_name] ...
    [QUICK] [EXTENDED] [USE_FRM]
```

> \= [MariaDB 11.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115)

```
REPAIR [NO_WRITE_TO_BINLOG | LOCAL] TABLE
    tbl_name [, tbl_name] ...
    [QUICK] [EXTENDED] [USE_FRM] [FORCE]
```

## Description

`REPAIR TABLE` repairs a possibly corrupted table. By default,\
it has the same effect as

```
myisamchk --recover tbl_name
```

or

```
aria_chk --recover tbl_name
```

See [aria\_chk](../../../clients-and-utilities/aria-clients-and-utilities/aria_chk.md) and [myisamchk](../../../clients-and-utilities/myisam-clients-and-utilities/myisamchk.md) for more.

`REPAIR TABLE` works for [Archive](../../storage-engines/archive/), [Aria](../../storage-engines/aria/), [CSV](../../storage-engines/csv/) and [MyISAM](../../storage-engines/myisam-storage-engine/) tables. For [InnoDB](../../storage-engines/innodb/), see [recovery modes](../../storage-engines/innodb/innodb-troubleshooting/innodb-recovery-modes.md). For CSV, see also [Checking and Repairing CSV Tables](../../storage-engines/csv/checking-and-repairing-csv-tables.md). For Archive, this statement also improves compression. If the storage engine does not support this statement, a warning is issued.

This statement requires [SELECT and INSERT privileges](../account-management-sql-statements/grant.md) for the table.

By default, `REPAIR TABLE` statements are written to the [binary log](../../../server-management/server-monitoring-logs/binary-log/) and will be [replicated](broken-reference). The `NO_WRITE_TO_BINLOG` keyword (`LOCAL` is an alias) will ensure the statement is not written to the binary log.

From [MariaDB 10.3.19](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-3-series/mariadb-10319-release-notes), `REPAIR TABLE` statements are not logged to the binary log if [read\_only](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#read_only) is set. See also [Read-Only Replicas](../../../ha-and-performance/standard-replication/read-only-replicas.md).

When an index is recreated, the storage engine may use a configurable buffer in the process. Incrementing the buffer speeds up the index creation. [Aria](../../storage-engines/aria/) and [MyISAM](../../storage-engines/myisam-storage-engine/) allocate a buffer whose size is defined by [aria\_sort\_buffer\_size](../../storage-engines/aria/aria-system-variables.md) or [myisam\_sort\_buffer\_size](../../storage-engines/myisam-storage-engine/myisam-system-variables.md), also used for [ALTER TABLE](../data-definition/alter/alter-table.md).

### QUICK

When specified, `REPAIR TABLE` will not modify the data file, only attempting to repair the index file. The same behavior can be achieved with [myisamchk --recover --quick](../../../clients-and-utilities/myisam-clients-and-utilities/myisamchk.md#repairing-tables).

### EXTENDED

Creates the index row by row rather than sorting and creating a single index. Similar to [myisamchk --safe-recover](../../../clients-and-utilities/myisam-clients-and-utilities/myisamchk.md#repairing-tables).

### USE\_FRM

For use only when the index file is missing or its header corrupted. MariaDB then attempts to recreate it using the .frm file. There is no equivalent [myisamchk](../../../clients-and-utilities/myisam-clients-and-utilities/myisamchk.md) option.

**MariaDB starting with** [**11.5**](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115)

### FORCE

The FORCE argument was added in [MariaDB 11.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115) to allow one to first run internal repair to fix damaged blocks and then follow it with ALTER TABLE ([MDEV-33449](https://jira.mariadb.org/browse/MDEV-33449)).

### Partitioned Tables

`REPAIR TABLE` is also supported for [partitioned tables](../../../server-management/partitioning-tables/) with the [ALTER TABLE ... REPAIR PARTITION](../data-definition/alter/alter-table.md) statement. However, the `USE_FRM` option cannot be used with this statement on a partitioned table. See [Repairing Partitions](../../../server-management/partitioning-tables/partitioning-overview.md#repairing-partitions) for details.

### Progress Reporting

The [Aria](../../storage-engines/aria/) storage engine supports [progress reporting](../../mariadb-internals/using-mariadb-with-your-programs-api/progress-reporting.md) for this statement.

## See Also

* [mariadb-check](../../../clients-and-utilities/mariadb-check.md)
* [aria\_chk](../../../clients-and-utilities/aria-clients-and-utilities/aria_chk.md)
* [myisamchk](../../../clients-and-utilities/myisam-clients-and-utilities/myisamchk.md)

GPLv2 fill\_help\_tables.sql
