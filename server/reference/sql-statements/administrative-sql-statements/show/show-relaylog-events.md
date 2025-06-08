# SHOW RELAYLOG EVENTS

The terms _master_ and _slave_ have historically been used in replication, and MariaDB has begun the process of adding _primary_ and _replica_ synonyms. The old terms will continue to be used to maintain backward compatibility - see [MDEV-18777](https://jira.mariadb.org/browse/MDEV-18777) to follow progress on this effort.

## Syntax

```
SHOW RELAYLOG ['connection_name'] EVENTS
    [IN 'log_name'] [FROM pos] [LIMIT [offset,] row_count]
    [ FOR CHANNEL 'channel_name']
```

## Description

On [replicas](../../../../ha-and-performance/standard-replication/), this command shows the events in the [relay log](../../../../server-management/server-monitoring-logs/binary-log/relay-log.md). If `'log_name'` is not specified, the first relay log is shown.

Syntax for the `LIMIT` clause is the same as for [SELECT ... LIMIT](../../data-manipulation/selecting-data/select.md#limit).

Using the `LIMIT` clause is highly recommended because the `SHOW RELAYLOG EVENTS` command returns the complete contents of the relay log, which can be quite large.

This command does not return events related to setting user and system variables. If you need those, use [mariadb-binlog](../../../../clients-and-utilities/logging-tools/mariadb-binlog/).

On the primary, this command does nothing.

Requires the [REPLICA MONITOR](../../account-management-sql-statements/grant.md#replica-monitor) privilege (>= [MariaDB 10.5.9](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1059-release-notes)), the [REPLICATION SLAVE ADMIN](../../account-management-sql-statements/grant.md#replication-slave-admin) privilege (>= [MariaDB 10.5.2](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1052-release-notes)) or the [REPLICATION SLAVE](../../account-management-sql-statements/grant.md#replication-slave) privilege (<= [MariaDB 10.5.1](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/mariadb-10-5-series/mariadb-1051-release-notes)).

#### connection\_name

If there is only one nameless primary, or the default primary (as specified by the [default\_master\_connection](../../../../ha-and-performance/standard-replication/replication-and-binary-log-system-variables.md) system variable) is intended, `connection_name` can be omitted. If provided, the `SHOW RELAYLOG` statement will apply to the specified primary. `connection_name` is case-insensitive.

**MariaDB starting with** [**10.7.0**](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-7-series/mariadb-1070-release-notes)

The `FOR CHANNEL` keyword was added for MySQL compatibility. This is identical as\
using the channel\_name directly after `SHOW RELAYLOG`.

CC BY-SA / Gnu FDL
