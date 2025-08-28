# Delayed Retrying of Failed Queries with MaxScale's Read/Write Split Router

The [Read/Write Split Router (readwritesplit)](../../maxscale-archive/archive/mariadb-maxscale-23-02/mariadb-maxscale-23-02-routers/mariadb-maxscale-2302-readwritesplit.md) routes write queries to the primary server and load balances read-only queries between one or more replica servers. If a server fails, then the router may need to retry failed queries on a different server. The retry may need to be delayed in some cases, such as when [automatic failover](../../maxscale-archive/archive/mariadb-maxscale-21-06/mariadb-maxscale-2106-maxscale-21-06-monitors/maxscale-mariadb-monitor-usage/maxscale-mariadb-monitor-usage-mariadb-monitor/using-automatic-failover-with-maxscales-mariadb-monitor.md) is in progress.

## Configuring Delayed Retries for Failed Queries

1. Configure delayed retries for failed queries by configuring several parameters for the Read/Write Split Router in `maxscale.cnf`.

| Parameter               | Description                                                                                                                                                                                                                                                           |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| delayed\_retry          | • When this parameter is enabled, failed queries will not immediately return an error to the client. Instead, the router will retry the query if a different server becomes available before the timeout is reached. • This parameter is disabled by default.         |
| delayed\_retry\_timeout | • The maximum amount of time to wait until returning an error if a query fails. • The value can be followed by any of the following units: h, m, s, and ms, for specifying durations in hours, minutes, seconds, and milliseconds. • The default value is 10 seconds. |

For example:

```
[split-router]
type                     = service
router                   = readwritesplit
...
delayed_retry            = true
delayed_retry_timeout    = 30s
```

2. Restart the MaxScale instance.

```
$ sudo systemctl restart maxscale
```

<sub>_This page is: Copyright © 2025 MariaDB. All rights reserved._</sub>

{% @marketo/form formId="4316" %}
