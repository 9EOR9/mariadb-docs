# SHUTDOWN

## Syntax

```
SHUTDOWN [WAIT FOR ALL { SLAVES | REPLICAS } ]
```

## Description

The `SHUTDOWN` command shuts the server down.

## WAIT FOR ALL REPLICAS / SLAVES

The `WAIT FOR ALL SLAVES` option was first added in [MariaDB 10.4.4](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/mariadb-1044-release-notes). `WAIT FOR ALL REPLICAS` has been a synonym since [MariaDB 10.5.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1051-release-notes).

When a primary server is shutdown and it goes through the normal shutdown process, the primary kills client threads in random order. By default, the primary also considers its binary log dump threads to be regular client threads. As a consequence, the binary log dump threads can be killed while client threads still exist, and this means that data can be written on the primary during a normal shutdown that won't be replicated. This is true even if [semi-synchronous replication](../../../ha-and-performance/standard-replication/semisynchronous-replication.md) is being used.

This problem can be solved by shutting down the server with the [SHUTDOWN](shutdown.md) command and by providing the `WAIT FOR ALL REPLICAS`/`WAIT FOR ALL SLAVES` option to the command. For example:

```
SHUTDOWN WAIT FOR ALL REPLICAS;
```

When the `WAIT FOR ALL REPLICAS` option is provided, the server only kills its binary log dump threads after all client threads have been killed, and it only completes the shutdown after the last [binary log](../../../server-management/server-monitoring-logs/binary-log/) has been sent to all connected replicas.

See [Replication Threads: Binary Log Dump Threads and the Shutdown Process](../../../ha-and-performance/standard-replication/replication-threads.md#binary-log-dump-threads-and-the-shutdown-process) for more information.

## Required Permissions

One must have a `SHUTDOWN` privilege (see [GRANT](../account-management-sql-statements/grant.md)) to use this command. It is the same privilege one needs to use the [mariadb-admin shutdown](../../../clients-and-utilities/mariadb-admin.md#mariadb-admin-commands) command.

## Shutdown for Upgrades

If you are doing a shutdown to [migrate to another major version of MariaDB](https://mariadb.com/kb/en/upgrading-between-major-mariadb-version), please ensure that the [innodb\_fast\_shutdown](../../storage-engines/innodb/innodb-system-variables.md#innodb_fast_shutdown) variable is not 2 (fast crash shutdown). The default of this variable is 1.

## Example

The following example shows how to create an [event](../../../server-usage/triggers-events/event-scheduler/) which turns off the server at a certain time:

```
CREATE EVENT `test`.`shutd`
    ON SCHEDULE
        EVERY 1 DAY
        STARTS '2014-01-01 20:00:00'
    COMMENT 'Shutdown Maria when the office is closed'
DO BEGIN
    SHUTDOWN;
END;
```

## Other Ways to Stop mariadbd

You can use the [mariadb-admin shutdown](../../../clients-and-utilities/mariadb-admin.md) command to take down mariadbd cleanly.

You can also use the system kill command on Unix with signal SIGTERM (15)

```
kill -SIGTERM pid-of-mariadbd-process
```

You can find the process number of the server process in the file that ends with `.pid` in your data directory.

The above is identical to `mariadb-admin shutdown`.

On windows you should use:

```
NET STOP MariaDB
```

## See Also

* [mariadb-admin shutdown](../../../clients-and-utilities/mariadb-admin.md).
* [InnoDB fast shutdown option](../../storage-engines/innodb/innodb-system-variables.md#innodb_fast_shutdown)

CC BY-SA / Gnu FDL
