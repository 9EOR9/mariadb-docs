# Metadata Locking

MariaDB supports metadata locking. This means that when a transaction (including [XA transactions](xa-transactions.md)) uses a table, it locks its metadata until the end of transaction. Non-transactional tables are also locked, as well as views and objects which are related to locked tables/views (stored functions, triggers, etc). When a connection tries to use a DDL statement (like an [ALTER TABLE](../data-definition/alter/alter-table.md)) which modifies a table that is locked, that connection is queued, and has to wait until it's unlocked. Using savepoints and performing a partial rollback does not release metadata locks.

[LOCK TABLES ... WRITE](lock-tables.md) are also queued. Some wrong statements which produce an error may not need to wait for the lock to be freed.

The metadata lock's timeout is determined by the value of the [lock\_wait\_timeout](../../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#lock_wait_timeout) server system variable (in seconds). However, note that its default value is 31536000 (1 year, MariaDB <= 10.2.3), or 86400 (1 day, MariaDB >= 10.2.4). If this timeout is exceeded, the following error is returned:

```
ERROR 1205 (HY000): Lock wait timeout exceeded; try restarting transaction
```

If the [metadata\_lock\_info](../../plugins/other-plugins/metadata-lock-info-plugin.md) plugin is installed, the [Information Schema](../administrative-sql-statements/system-tables/information-schema/) [metadata\_lock\_info](../administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-metadata_lock_info-table.md) table stores information about existing metadata locks.

**MariaDB starting with** [**10.5.2**](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1052-release-notes)

From [MariaDB 10.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/what-is-mariadb-105), the [Performance Schema metadata\_locks](../administrative-sql-statements/system-tables/performance-schema/performance-schema-tables/performance-schema-metadata_locks-table.md) table contains metadata lock information.

## Example

Let's use the following MEMORY (non-transactional) table:

```
CREATE TABLE t (a INT) ENGINE = MEMORY;
```

Connection 1 starts a transaction, and INSERTs a row into t:

```
START TRANSACTION;

INSERT INTO t SET a=1;
```

`t`'s metadata is now locked by connection 1. Connection 2 tries to alter `t`, but has to wait:

```
ALTER TABLE t ADD COLUMN b INT;
```

Connection 2's prompt is blocked now.

Now connection 1 ends the transaction:

```
COMMIT;
```

...and connection 2 finally gets the output of its command:

```
Query OK, 1 row affected (35.23 sec)
Records: 1  Duplicates: 0  Warnings: 0
```

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
