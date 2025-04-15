# Disks Plugin

The `DISKS` plugin creates the [DISKS](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-disks-table.md) table in the [INFORMATION_SCHEMA](../../../server-usage/programming-customizing-mariadb/views/information-schema-views-table.md) database. This table shows metadata about disks on the system.

Before [MariaDB 10.4.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-104-series/mariadb-1047-release-notes), [MariaDB 10.3.17](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-10-3-series/mariadb-10317-release-notes) and [MariaDB 10.2.26](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-102-series/mariadb-10226-release-notes), this plugin did **not** check [user privileges](../../sql-statements-and-structure/sql-statements/account-management-sql-commands/grant.md). When it is enabled, **any** user can query the `INFORMATION_SCHEMA.DISKS` table and see all the information it provides.

Since [MariaDB 10.4.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-104-series/mariadb-1047-release-notes), [MariaDB 10.3.17](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-10-3-series/mariadb-10317-release-notes) and [MariaDB 10.2.26](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-102-series/mariadb-10226-release-notes) , it required the [FILE privilege](../../sql-statements-and-structure/sql-statements/account-management-sql-commands/grant.md).

The plugin only works on Linux.

#

# Installing the Plugin

Although the plugin's shared library is distributed with MariaDB by default, the plugin is not actually installed by MariaDB by default. There are two methods that can be used to install the plugin with MariaDB.

The first method can be used to install the plugin without restarting the server. You can install the plugin dynamically by executing [INSTALL SONAME](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/install-soname.md) or [INSTALL PLUGIN](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/install-plugin.md). For example:

```
INSTALL SONAME 'disks';
```

The second method can be used to tell the server to load the plugin when it starts up. The plugin can be installed this way by providing the [--plugin-load](/en/mysqld-options/#-plugin-load) or the [--plugin-load-add](/en/mysqld-options/#-plugin-load-add) options. This can be specified as a command-line argument to [mysqld](/en/mysqld-options/) or it can be specified in a relevant server [option group](../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md). For example:

```
[mariadb]
...
plugin_load_add = disks
```

#

# Uninstalling the Plugin

You can uninstall the plugin dynamically by executing [UNINSTALL SONAME](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/uninstall-soname.md) or [UNINSTALL PLUGIN](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/uninstall-plugin.md). For example:

```
UNINSTALL SONAME 'disks';
```

If you installed the plugin by providing the [--plugin-load](/en/mysqld-options/#-plugin-load) or the [--plugin-load-add](/en/mysqld-options/#-plugin-load-add) options in a relevant server [option group](../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md#option-groups) in an [option file](../../../server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files.md), then those options should be removed to prevent the plugin from being loaded the next time the server is restarted.

#

# Example

```
SELECT * FROM information_schema.DISKS;

+-----------+-------+----------+---------+-----------+
| Disk | Path | Total | Used | Available |
+-----------+-------+----------+---------+-----------+
| /dev/vda1 | / | 26203116 | 2178424 | 24024692 |
| /dev/vda1 | /boot | 26203116 | 2178424 | 24024692 |
| /dev/vda1 | /etc | 26203116 | 2178424 | 24024692 |
+-----------+-------+----------+---------+-----------+
```

#

# Versions

| Version | Status | Introduced |
| --- | --- | --- |
| Version | Status | Introduced |
| 1.1 | Stable | [MariaDB 10.4.7](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-104-series/mariadb-1047-release-notes), [MariaDB 10.3.17](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-10-3-series/mariadb-10317-release-notes), [MariaDB 10.2.26](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-102-series/mariadb-10226-release-notes), [MariaDB 10.1.41](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-101-series/mariadb-10141-release-notes) |
| 1.0 | Beta | [MariaDB 10.3.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-10-3-series/mariadb-1036-release-notes), [MariaDB 10.2.14](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-102-series/mariadb-10214-release-notes), [MariaDB 10.1.32](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server/release-notes-mariadb-101-series/mariadb-10132-release-notes) |

#

# Options

#

## `disks`

* Description: Controls how the server should treat the plugin when the server starts up.

 * Valid values are:

 * `OFF` - Disables the plugin without removing it from the [mysql.plugins](/en/mysqlplugin-table/) table.
 * `ON` - Enables the plugin. If the plugin cannot be initialized, then the server will still continue starting up, but the plugin will be disabled.
 * `FORCE` - Enables the plugin. If the plugin cannot be initialized, then the server will fail to start with an error.
 * `FORCE_PLUS_PERMANENT` - Enables the plugin. If the plugin cannot be initialized, then the server will fail to start with an error. In addition, the plugin cannot be uninstalled with [UNINSTALL SONAME](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/uninstall-soname.md) or [UNINSTALL PLUGIN](../../sql-statements-and-structure/sql-statements/administrative-sql-statements/plugin-sql-statements/uninstall-plugin.md) while the server is running.
 * See [Plugin Overview: Configuring Plugin Activation at Server Startup](../plugin-overview.md#configuring-plugin-activation-at-server-startup) for more information.
* Commandline: `--disks=value`
* Data Type: `enumerated`
* Default Value: `ON`
* Valid Values: `OFF`, `ON`, `FORCE`, `FORCE_PLUS_PERMANENT`