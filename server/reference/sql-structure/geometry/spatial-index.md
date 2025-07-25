# SPATIAL INDEX

## Description

On [MyISAM](../../../server-usage/storage-engines/myisam-storage-engine/), [Aria](../../../server-usage/storage-engines/aria/) and [InnoDB](../../../server-usage/storage-engines/innodb/) tables, MariaDB can create spatial indexes (an R-tree index) using syntax similar to that for creating regular indexes, but extended with the `SPATIAL` keyword.\
Currently, columns in spatial indexes must be declared `NOT NULL`.

Spatial indexes can be created when the table is created, or added after the fact like so:

* with [CREATE TABLE](../../sql-statements/data-definition/create/create-table.md):

```sql
CREATE TABLE geom (g GEOMETRY NOT NULL, SPATIAL INDEX(g));
```

* with [ALTER TABLE](../../sql-statements/data-definition/alter/alter-table/):

```sql
ALTER TABLE geom ADD SPATIAL INDEX(g);
```

* with [CREATE INDEX](../../sql-statements/data-definition/create/create-index.md):

```sql
CREATE SPATIAL INDEX sp_index ON geom (g);
```

`SPATIAL INDEX` creates an `R-tree` index. For storage\
engines that support non-spatial indexing of spatial columns, the engine\
creates a `B-tree` index. A `B-tree` index on spatial values is useful for\
exact-value lookups, but not for range scans.

For more information on indexing spatial columns, see [CREATE INDEX](../../sql-statements/data-definition/create/create-index.md).

To drop spatial indexes, use [ALTER TABLE](../../sql-statements/data-definition/alter/alter-table/) or [DROP INDEX](../../sql-statements/data-definition/drop/drop-index.md):

* with [ALTER TABLE](../../sql-statements/data-definition/alter/alter-table/):

```sql
ALTER TABLE geom DROP INDEX g;
```

* with [DROP INDEX](../../sql-statements/data-definition/drop/drop-index.md):

```sql
DROP INDEX sp_index ON geom;
```

### Data-at-Rest Encyption

Before [MariaDB 10.4.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-1043-release-notes), InnoDB's spatial indexes could not be [encrypted](../../../security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/). If an InnoDB table was encrypted and if it contained spatial indexes, then those indexes would be unencrypted.

In [MariaDB 10.4.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-1043-release-notes) and later, if [innodb\_checksum\_algorithm](../../storage-engines/innodb/innodb-system-variables.md#innodb_checksum_algorithm) is set to `full_crc32` or `strict_full_crc32`, and if the table does not use [ROW\_FORMAT=COMPRESSED](../../storage-engines/innodb/innodb-row-formats/innodb-row-formats-overview.md), then InnoDB spatial indexes will be encrypted if the table is encrypted.

See [MDEV-12026](https://jira.mariadb.org/browse/MDEV-12026) for more information.

<sub>_This page is licensed: GPLv2, originally from_</sub> [<sub>_fill\_help\_tables.sql_</sub>](https://github.com/MariaDB/server/blob/main/scripts/fill_help_tables.sql)

{% @marketo/form formId="4316" %}
