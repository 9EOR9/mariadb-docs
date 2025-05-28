# Archive

The `ARCHIVE` storage engine is a storage engine that uses gzip to compress rows. It is mainly used for storing large amounts of data, without indexes, with only a very small footprint.

A table using the `ARCHIVE` storage engine is stored in two files on disk. There's a table definition file with an extension of .frm, and a data file with the extension .ARZ. At times during optimization, a .ARN file will appear.

New rows are inserted into a compression buffer and are flushed to disk when needed. SELECTs cause a flush. Sometimes, rows created by multi-row inserts are not visible until the statement is complete.

`ARCHIVE` allows a maximum of one key. The key must be on an `[AUTO_INCREMENT](../../data-types/auto_increment.md)` column, and can be a `PRIMARY KEY` or a non-unique key. However, it has a limitation: it is not possible to insert a value which is lower than the next `AUTO_INCREMENT` value.

## Installing the Plugin

Although the plugin's shared library is distributed with MariaDB by default, the plugin is not actually installed by MariaDB by default. There are two methods that can be used to install the plugin with MariaDB.

The first method can be used to install the plugin without restarting the server. You can install the plugin dynamically by executing `[INSTALL SONAME](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/install-soname.md)` or `[INSTALL PLUGIN](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/install-plugin.md)`. For example:

```
INSTALL SONAME 'ha_archive';
```

The second method can be used to tell the server to load the plugin when it starts up. The plugin can be installed this way by providing the `[--plugin-load](../../../server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md)` or the `[--plugin-load-add](../../../server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md)` options. This can be specified as a command-line argument to `[mysqld](../../../server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md)` or it can be specified in a relevant server [option group](../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md). For example:

```
[mariadb]
...
plugin_load_add = ha_archive
```

## Uninstalling the Plugin

You can uninstall the plugin dynamically by executing `[UNINSTALL SONAME](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/uninstall-soname.md)` or `[UNINSTALL PLUGIN](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/uninstall-plugin.md)`. For example:

```
UNINSTALL SONAME 'ha_archive';
```

If you installed the plugin by providing the `[--plugin-load](../../../server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md)` or the `[--plugin-load-add](../../../server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md)` options in a relevant server [option group](../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md), then those options should be removed to prevent the plugin from being loaded the next time the server is restarted.

## Characteristics

* Supports [INSERT](../../sql-statements/data-manipulation/inserting-loading-data/insert.md) and [SELECT](../../sql-statements/data-manipulation/selecting-data/select.md), but not [DELETE](../../sql-statements/data-manipulation/changing-deleting-data/delete.md), [UPDATE](../../sql-statements/data-manipulation/changing-deleting-data/update.md) or [REPLACE](../../sql-statements/data-manipulation/changing-deleting-data/replace.md).
* Data is compressed with zlib as it is inserted, making it very small.
* Data is slow the select, as it needs to be uncompressed, and, besides the [query cache](../../../ha-and-performance/optimization-and-tuning/buffers-caches-and-threads/query-cache.md), there is no cache.
* Supports AUTO\_INCREMENT (since MariaDB/MySQL 5.1.6), which can be a unique or a non-unique index.
* Since MariaDB/MySQL 5.1.6, selects scan past BLOB columns unless they are specifically requested, making these queries much more efficient.
* Does not support [spatial](../../sql-structure/geometry/spatial-index.md) data types.
* Does not support [transactions](../../sql-statements-and-structure/sql-statements/transactions/).
* Does not support foreign keys.
* Does not support [virtual columns](../../sql-statements/data-definition/create/generated-columns.md).
* No storage limit.
* Supports row locking.
* Supports [table discovery](../storage-engines-storage-engine-development/table-discovery.md), and the server can access ARCHIVE tables even if the corresponding `.frm` file is missing.
* [OPTIMIZE TABLE](../../../ha-and-performance/optimization-and-tuning/optimizing-tables/optimize-table.md) and [REPAIR TABLE](../../sql-statements/table-statements/repair-table.md) can be used to compress the table in its entirety, resulting in slightly better compression.
* With MariaDB, it is possible to upgrade from the MySQL 5.0 format without having to dump the tables.
* [INSERT DELAYED](../../sql-statements/data-manipulation/inserting-loading-data/insert-delayed.md) is supported.
* Running many SELECTs during the insertions can deteriorate the compression, unless only multi-rows INSERTs and INSERT DELAYED are used.
