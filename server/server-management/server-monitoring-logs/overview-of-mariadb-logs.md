# Overview of MariaDB Logs

There are many variables in MariaDB that you can use to define what to log and when to log.

This article will give you an overview of the different logs and how to enable/disable logging to these.

Note that storage engines can have their logs too: for example, InnoDB keeps an [Undo Log](../../reference/storage-engines/innodb/innodb-undo-log.md) and a Redo Log which are used for rollback and crash recovery. However, this page only lists MariaDB server logs.

### [Error Log](error-log.md)

* Always enabled
* Usually a file in the data directory, but some distributions may move this to other locations.
* All critical errors are logged here.
* One can get warnings to be logged by setting [log\_warnings](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_warnings).
* With the [mysqld\_safe](../../clients-and-utilities/legacy-clients-and-utilities/mariadbd_safe.md) `--syslog` option one can duplicate the messages to the system's syslog.

### [General Query Log](general-query-log.md)

* Enabled with [--general-log](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#general_log)
* Logs all queries to a [file or table](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_output).
* Useful for debugging or auditing queries.
* The super user can disable logging to it for a connection by setting [SQL\_LOG\_OFF](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#sql_log_off) to 1.

### [Slow Query Log](slow-query-log/)

* Enabled by starting mysqld with [--slow-query-log](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#slow_query_log)
* Logs all queries to a [file or table](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_output).
* Useful to find queries that causes performance problems.
* Logs all queries that takes more than [long\_query\_time](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#long_query_time) to run.
* One can decide what to log with the options [--log-slow-admin-statements](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_slow_admin_statements), [--log-slow-slave-statements](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_slow_slave_statements), [log\_slow\_filter](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_slow_filter) or [log\_slow\_rate\_limit](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_slow_rate_limit).
* One can change what is logged by setting [log\_slow\_verbosity](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#log_slow_verbosity).
* One can disable it globally by setting [global.slow\_query\_log](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#slow_query_log) to 0
* In 10.1 one can disable it for a connection by setting [local.slow\_query\_log](../../ha-and-performance/optimization-and-tuning/system-variables/server-system-variables.md#slow_query_log) to 0.

### [Binary Log](binary-log/overview-of-the-binary-log.md)

* Enabled by starting mysqld with [--log-bin](../../ha-and-performance/standard-replication/replication-and-binary-log-system-variables.md)
* Used on machines that are, or may become, replication masters.
* Required for point-in-time recovery.
* Binary log files are mainly used by replication and can also be used with [mariadb-binlog](../../clients-and-utilities/mariadb-binlog/) to apply on a backup to get the database up to date.
* One can decide what to log with [--binlog-ignore-db=database\_name](../getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md) or [--binlog-do-db=database\_name](../getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options.md).
* The super user can disable logging for a connection by [setting SQL\_LOG\_BIN](../../reference/sql-statements/administrative-sql-statements/set-commands/set-sql_log_bin.md) to 0. However while this is 0, no changes done in this connection will be replicated to the slaves!
* For examples, see [Using and Maintaining the Binary Log](binary-log/using-and-maintaining-the-binary-log.md).

### Examples

If you know that your next query will be slow and you don't want to log it in the slow query log, do:

```
SET LOCAL SLOW_QUERY_LOG=0;
```

If you are a super user running a log batch job that you don't want to have logged (for example mariadb-dump), do:

```
SET LOCAL SQL_LOG_OFF=1, LOCAL SLOW_QUERY_LOG=0;
```

[mariadb-dump](../../clients-and-utilities/backup-restore-and-import-clients/mariadb-dump.md) (previously mysqldump) since [MariaDB 10.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1) will add this automatically to your dump file if you run it with the `--skip-log-queries` option.

## See Also

* [MariaDB audit plugin](../../reference/plugins/mariadb-audit-plugin/)

CC BY-SA / Gnu FDL
