# mysql.plugin Table

**System tables should not normally be edited directly. Use the related SQL statements instead.**

The `mysql.plugin` table can be queried to get information about installed [plugins](../../../../plugins/).

This table only contains information about [plugins](../../../../plugins/) that have been installed via the following methods:

* The [INSTALL SONAME](../../plugin-sql-statements/install-soname.md) statement.
* The [INSTALL PLUGIN](../../plugin-sql-statements/install-plugin.md) statement.
* The [mariadb-plugin](../../../../../clients-and-utilities/administrative-tools/mariadb-plugin.md) utility.

This table does not contain information about:

* Built-in plugins.
* Plugins loaded with the [--plugin-load-add](../../../../../server-management/starting-and-stopping-mariadb/mariadbd-options.md) option.
* Plugins loaded with the [--plugin-load](../../../../../server-management/starting-and-stopping-mariadb/mariadbd-options.md) option.

This table only contains enough information to reload the plugin when the server is restarted, which means it only contains the plugin name and the plugin library.

This table uses the [Aria](../../../../storage-engines/aria/) storage engine.

The `mysql.plugin` table contains the following fields:

| Field | Type         | Null | Key | Default | Description                 |
| ----- | ------------ | ---- | --- | ------- | --------------------------- |
| Field | Type         | Null | Key | Default | Description                 |
| name  | varchar(64)  | NO   | PRI |         | Plugin name.                |
| dl    | varchar(128) | NO   |     |         | Name of the plugin library. |

## Example

```
SELECT * FROM mysql.plugin;
+---------------------------+------------------------+
| name                      | dl                     |
+---------------------------+------------------------+
| spider                    | ha_spider.so           |
| spider_alloc_mem          | ha_spider.so           |
| METADATA_LOCK_INFO        | metadata_lock_info.so  |
| OQGRAPH                   | ha_oqgraph.so          |
| cassandra                 | ha_cassandra.so        |
| QUERY_RESPONSE_TIME       | query_response_time.so |
| QUERY_RESPONSE_TIME_AUDIT | query_response_time.so |
| LOCALES                   | locales.so             |
| sequence                  | ha_sequence.so         |
+---------------------------+------------------------+
```

CC BY-SA / Gnu FDL
