
# Writing Plugins for MariaDB


## About


Generally speaking, writing plugins for MariaDB is very similar to writing plugins for MySQL.


## Authentication Plugins


See [Pluggable Authentication](../plugins/authentication-plugins/pluggable-authentication-overview.md).


## Storage Engine Plugins


Storage engines can extend `<code class="highlight fixed" style="white-space:pre-wrap">CREATE TABLE</code>` syntax with optional
index, field, and table attribute clauses. See
[Extending CREATE TABLE](../storage-engines/storage-engines-storage-engine-development/engine-defined-new-tablefieldindex-attributes.md) for more information.


See [Storage Engine Development](../storage-engines/storage-engines-storage-engine-development/README.md).


## Information Schema Plugins


Information Schema plugins can have their own [FLUSH](../sql-statements-and-structure/sql-statements/administrative-sql-statements/flush-commands/flush-tables-for-export.md) and [SHOW](../sql-statements-and-structure/sql-statements/administrative-sql-statements/show/show-procedure-code.md) statements. See 
[FLUSH and SHOW for Information Schema plugins](information-schema-plugins-show-and-flush-statements.md).


## Encryption Plugins


[Encryption plugins](encryption-plugin-api.md) in MariaDB are used for the [data at rest encryption](../../security/securing-mariadb/securing-mariadb-encryption/encryption-data-at-rest-encryption/data-at-rest-encryption-overview.md) feature. They are responsible for both key management and for the actual encryption and decryption of data.


## Function Plugins


Function plugins add new SQL functions to MariaDB. Unlike the old [UDF](../../server-usage/programming-customizing-mariadb/user-defined-functions/user-defined-functions-security.md) API, function plugins can do almost anything that a built-function can.


## Plugin Declaration Structure


The MariaDB plugin declaration differs from
the MySQL plugin declaration in the following ways:


1. it has no useless 'reserved' field (the very last field in the MySQL plugin declaration)
1. it has a 'maturity' declaration
1. it has a field for a text representation of the version field


MariaDB can load plugins that only have the MySQL plugin declaration but both `<code>PLUGIN_MATURITY</code>` and `<code>PLUGIN_AUTH_VERSION</code>` will show up as 'Unknown' in the
[INFORMATION_SCHEMA.PLUGINS table](../sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/plugins-table-information-schema.md).


For compiled-in (not dynamically loaded) plugins, the presence of the MariaDB plugin declaration is mandatory.


### Example Plugin Declaration


The MariaDB plugin declaration looks like this:


```
/* MariaDB plugin declaration */
maria_declare_plugin(example)
{
   MYSQL_STORAGE_ENGINE_PLUGIN, /* the plugin type (see include/mysql/plugin.h) */
   &example_storage_engine_info, /* pointer to type-specific plugin descriptor   */
   "EXAMPLEDB", /* plugin name */
   "John Smith",  /* plugin author */
   "Example of plugin interface", /* the plugin description */
   PLUGIN_LICENSE_GPL, /* the plugin license (see include/mysql/plugin.h) */
   example_init_func,   /* Pointer to plugin initialization function */
   example_deinit_func,  /* Pointer to plugin deinitialization function */
   0x0001 /* Numeric version 0xAABB means AA.BB version */,
   example_status_variables,  /* Status variables */
   example_system_variables,  /* System variables */
   "0.1 example",  /* String version representation */
   MariaDB_PLUGIN_MATURITY_EXPERIMENTAL /* Maturity (see include/mysql/plugin.h)*/
}
maria_declare_plugin_end;
```
