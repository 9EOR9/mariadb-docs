# SQL Error Log System Variables and Options

This page documents system variables and options related to the [SQL\_Error\_Log Plugin](../../../server-management/server-monitoring-logs/sql-error-log-plugin.md). See [Server System Variables](server-system-variables.md) for a complete list of system variables and instructions on setting them.

See also the [Full list of MariaDB options, system and status variables](../../../server-management/variables-and-modes/full-list-of-mariadb-options-system-and-status-variables.md).

## Options

#### `sql_error_log`

* Description: Controls how the server should treat the plugin when the server starts up.
  * Valid values are:
    * `OFF` - Disables the plugin without removing it from the [mysql.plugins](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-plugin-table.md) table.
    * `ON` - Enables the plugin. If the plugin cannot be initialized, then the server will still continue starting up, but the plugin will be disabled.
    * `FORCE` - Enables the plugin. If the plugin cannot be initialized, then the server will fail to start with an error.
    * `FORCE_PLUS_PERMANENT` - Enables the plugin. If the plugin cannot be initialized, then the server will fail to start with an error. In addition, the plugin cannot be uninstalled with [UNINSTALL SONAME](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/uninstall-soname.md) or [UNINSTALL PLUGIN](../../../reference/sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/uninstall-plugin.md) while the server is running.
  * See [Plugin Overview: Configuring Plugin Activation at Server Startup](../../../reference/plugins/plugin-overview.md#configuring-plugin-activation-at-server-startup) for more information.
* Commandline: `--sql-error-log=value`
* Data Type: `enumerated`
* Default Value: `ON`
* Valid Values: `OFF`, `ON`, `FORCE`, `FORCE_PLUS_PERMANENT`

## System Variables

#### `sql_error_log_filename`

* Description: The name (and optionally path) of the logfile containing the errors. Rotation will use a naming convention such as `sql_error_log_filename.001`. If no path is specified, the log file will be written to the [data directory](server-system-variables.md#datadir).
* Commandline: `--sql-error-log-filename=value`
* Scope: Global
* Dynamic: No
* Data Type: `string`
* Default Value: `sql_errors.log`

#### `sql_error_log_rate`

* Description: The logging sampling rate. Setting to `10`, for example, means that one in ten errors will be logged. If set to zero, logging is disabled. The default, `1`, logs every error.
* Commandline: `--sql-error-log-rate=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `1`

#### `sql_error_log_rotate`

* Description: Setting to #1`forces log rotation.`
* Commandline: `--sql-error-log-rate[={0|1}]`
* Scope: Global
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `OFF`

#### `sql_error_log_rotations`

* Description: Number of rotations before the log is removed. When rotated, the current log file is stored and a new, empty, log is created. Any rotations older than this setting are removed.
* Commandline: `--sql-error-log-rotations=#`
* Scope: Global
* Dynamic: Yes
* Data Type: `numeric`
* Default Value: `9`
* Range: `1` to `999`

#### `sql_error_log_size_limit`

* Description: The log file size limit in bytes. After reaching this size, the log file is rotated.
* Commandline: `--sql-error-log-size-limit=#`
* Scope: Global
* Dynamic: No
* Data Type: `numeric`
* Default Value: `1000000`
* Range: `100` to `9223372036854775807`

#### `sql_error_log_warnings`

* Description: If set, log warnings in addition to errors.
* Commandline: `--sql-error-log-warnings={0,1}`
* Scope: Global
* Dynamic: Yes
* Data Type: `boolean`
* Default Value: `OFF`
* Introduced: [MariaDB 10.11.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-10-11-series/mariadb-10-11-5-release-notes)

#### `sql_error_log_with_db_and_thread_info`

* Description: If enabled, it prints the database name and the thread ID in the log in addition to already existing columns.
* Commandline: `--sql-error-log-with-db-and-thread-info=value`
* Scope: Global
* Dynamic: No
* Data Type: `boolean`
* Default Value: `OFF`
* Introduced: [MariaDB 10.6.17](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-10-6-series/mariadb-10-6-17-release-notes), [MariaDB 10.11.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-10-11-series/mariadb-10-11-7-release-notes), [MariaDB 11.0.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-0-series/mariadb-11-0-5-release-notes), [MariaDB 11.1.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-1-series/mariadb-11-1-4-release-notes), [MariaDB 11.2.3](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-2-series/mariadb-11-2-3-release-notes)

CC BY-SA / Gnu FDL
