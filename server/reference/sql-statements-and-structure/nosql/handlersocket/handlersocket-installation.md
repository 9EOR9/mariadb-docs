
# HandlerSocket Installation

After MariaDB is installed, use the [INSTALL PLUGIN](../../sql-statements/administrative-sql-statements/plugin-sql-statements/install-plugin.md) command (as the root user) to install
the HandlerSocket plugin. This command only needs to be run once, like so:


```
INSTALL PLUGIN handlersocket SONAME 'handlersocket.so';
```

After installing the plugin, [SHOW PROCESSLIST](../../sql-statements/administrative-sql-statements/show/show-processlist.md) you first need to configure some settings. All [HandlerSocket configuration options](handlersocket-configuration-options.md) are placed in the [mysqld] section of your my.cnf file.


At least the [handlersocket_address](handlersocket-configuration-options.md#handlersocket_address), [handlersocket_port](handlersocket-configuration-options.md#handlersocket_port) and [handlersocket_port_wr](handlersocket-configuration-options.md#handlersocket_port_wr) options need to be set. For example:


```
handlersocket_address="127.0.0.1"
handlersocket_port="9998"
handlersocket_port_wr="9999"
```

After updating the configuration options, restart MariaDB.


On the client side, to make use of the plugin you will need to install the
appropriate client library (i.e. libhsclient for C++ applications and
perl-Net-HandlerSocket for perl applications).

