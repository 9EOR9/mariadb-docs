# MaxScale 23.08 Readconnroute

## Readconnroute

## Readconnroute

This document provides an overview of the **readconnroute** router module\
and its intended use case scenarios. It also displays all router\
configuration parameters with their descriptions.

* [Readconnroute](mariadb-maxscale-2308-readconnroute.md#readconnroute)
  * [Overview](mariadb-maxscale-2308-readconnroute.md#overview)
  * [Configuration](mariadb-maxscale-2308-readconnroute.md#configuration)
    * [router\_options](mariadb-maxscale-2308-readconnroute.md#router_options)
    * [master\_accept\_reads](mariadb-maxscale-2308-readconnroute.md#master_accept_reads)
    * [max\_replication\_lag](mariadb-maxscale-2308-readconnroute.md#max_replication_lag)
  * [Examples](mariadb-maxscale-2308-readconnroute.md#examples)
  * [Router Diagnostics](mariadb-maxscale-2308-readconnroute.md#router-diagnostics)
  * [Limitations](mariadb-maxscale-2308-readconnroute.md#limitations)

### Overview

The readconnroute router provides simple and lightweight load balancing across a\
set of servers.

Note that \*_readconnroute_ balances _connections_ and not _statements_. When a\
client connects, the router selects the server that matches the value of`router_options` and has the least number of connections. Once the connection is\
opened, it will not be changed for the duration of the session. If the\
connection between MaxScale and the server breaks, the connection can not be\
re-established and the client session will be closed. The fact that the server\
is fixed when the client connects also means that routing hints are ignored.

Connections from other MaxScale instances or connections done directly on a\
database are not taken into account. Only connections done through the same\
Maxscale instance are taken into account.

**Warning:** `readconnroute` will not prevent writes from being done even if you\
define `router_options=slave`. The client application is responsible for\
making sure that it only performs read-only queries in such\
cases. `readconnroute` is simple by design: it selects a server for each\
client connection and routes all queries there. If something more complex is\
required, the [readwritesplit](mariadb-maxscale-2308-readwritesplit.md) router is usually the right\
choice.

### Configuration

For more details about the standard service parameters, refer to the[Configuration Guide](../../../../../en/maxscale-2308-getting-started-mariadb-maxscale-configuration-guide/).

#### `router_options`

* Type: [enum\_mask](../../../../../en/maxscale-2308-getting-started-mariadb-maxscale-configuration-guide/#enumerations)
* Mandatory: No
* Dynamic: Yes
* Values: `master`, `slave`, `synced`, `running`
* Default: `running`

**`router_options`** can contain a comma separated list of valid server\
roles. These roles are used as the valid types of servers the router will\
form connections to when new sessions are created.

Examples:

```
router_options=slave
router_options=master,slave
```

Here is a list of all possible values for the `router_options`.

| Role    | Description                                                                                                                                                                                                                  |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Role    | Description                                                                                                                                                                                                                  |
| master  | A server assigned as a primary by one of MariaDB MaxScale monitors. Depending on the monitor implementation, this could be a primary server of a Primary-Replica replication cluster or a Write-Primary of a Galera cluster. |
| slave   | A server assigned as a replica of a primary. If all replicas are down, but the primary is still available, then the router will use the primary.                                                                             |
| synced  | A Galera cluster node which is in a synced state with the cluster.                                                                                                                                                           |
| running | A server that is up and running. All servers that MariaDB MaxScale can connect to are labeled as running.                                                                                                                    |

If no `router_options` parameter is configured in the service definition,\
the router will use the default value of `running`. This means that it will\
load balance connections across all running servers defined in the `servers`\
parameter of the service.

When a connection is being created and the candidate server is being chosen, the\
list of servers is processed in from first entry to last. This means that if two\
servers with equal rank and number of connections are found, the one that's\
listed first in the _servers_ parameter for the service is chosen.

When using `router_options=slave`, only servers with the `Slave` status are\
used. If there are no servers with the `Slave` status but there is a `Master`\
status, it will be used as the fallback server. Note that the use of`router_options=slave` does not prevent writes from being done and the client\
application is responsible for making sure that no writes are done on a `Slave`\
server.

#### `master_accept_reads`

* Type: [boolean](../../../../../en/maxscale-2308-getting-started-mariadb-maxscale-configuration-guide/#booleans)
* Mandatory: No
* Dynamic: Yes
* Default: true

This option can be used to prevent queries from being sent to the current primary.\
If `router_options` does not contain `master`, the readconnroute instance is\
usually meant for reading. Setting `master_accept_reads=false` excludes the primary\
from server selection (and thus from receiving reads).

If `router_options` contains `master`, the setting of `master_accept_reads` has no effect.

By default `master_accept_reads=true`.

#### `max_replication_lag`

* Type: [duration](../../../../../en/maxscale-2308-getting-started-mariadb-maxscale-configuration-guide/#durations)
* Mandatory: No
* Dynamic: Yes
* Default: 0s

The maximum acceptable replication lag. The value is in seconds and is specified\
as documented [here](../../../../../en/maxscale-2308-getting-started-mariadb-maxscale-configuration-guide/#durations). The\
default value is `0s`, which means that the lag is ignored.

The replication lag of a server must be less than the configured value in order\
for it to be used for routing. To configure the router to not allow any lag, use\
the smallest duration larger than 0, that is, `max_replication_lag=1s`.

### Examples

The most common use for the readconnroute is to provide either a read or\
write port for an application. This provides a more lightweight routing\
solution than the more complex readwritesplit router but requires the\
application to be able to use distinct write and read ports.

To configure a read-only service that tolerates primary failures, we first\
need to add a new section in to the configuration file.

```
[Read-Service]
type=service
router=readconnroute
servers=replica1,replica2,replica3
router_options=slave
```

Here the `router_options` designates replicas as the only valid server\
type. With this configuration, the queries are load balanced across the\
replica servers.

For more complex examples of the readconnroute router, take a look at the\
examples in the [Tutorials](https://mariadb.com/kb/Tutorials) folder.

### Router Diagnostics

The `router_diagnostics` output for readconnroute has the following fields.

* `queries`: Number of queries executed through this service.

### Limitations

* Sending of binary data with `LOAD DATA LOCAL INFILE` is not supported.
* The router will never reconnect to the server it initially connected to.

CC BY-SA / Gnu FDL
