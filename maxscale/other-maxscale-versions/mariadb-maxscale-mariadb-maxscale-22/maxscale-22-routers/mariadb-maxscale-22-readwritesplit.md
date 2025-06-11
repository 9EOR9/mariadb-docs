# Readwritesplit

This document provides a short overview of the **readwritesplit** router module\
and its intended use case scenarios. It also displays all router configuration\
parameters with their descriptions. A list of current limitations of the module\
is included and use examples are provided.

### Overview

The **readwritesplit** router is designed to increase the read-only processing\
capability of a cluster while maintaining consistency. This is achieved by\
splitting the query load into read and write queries. Read queries, which do not\
modify data, are spread across multiple nodes while all write queries will be\
sent to a single node.

The router is designed to be used with a traditional Master-Slave replication\
cluster. It automatically detects changes in the master server and will use the\
current master server of the cluster. With a Galera cluster, one can achieve a\
resilient setup and easy master failover by using one of the Galera nodes as a\
Write-Master node, where all write queries are routed, and spreading the read\
load over all the nodes.

### Configuration

Readwritesplit router-specific settings are specified in the configuration file\
of MariaDB MaxScale in its specific section. The section can be freely named but\
the name is used later as a reference in a listener section.

For more details about the standard service parameters, refer to the[Configuration Guide](../maxscale-22-getting-started/mariadb-maxscale-22-mariadb-maxscale-configuration-usage-scenarios.md).

### Optional parameters

#### `max_slave_connections`

**`max_slave_connections`** sets the maximum number of slaves a router session\
uses at any moment. The default is to use at most 255 slave connections per\
client connection. In older versions the default was to use all available slaves\
with no limit.

```
max_slave_connections=<max. number, or % of available slaves>
```

For example, if you have configured MaxScale with one master and three slaves\
and set `max_slave_connections=2`, for each client connection a connection to\
the master and two slave connections would be opened. The read query load\
balancing is then done between these two slaves and writes are sent to the\
master.

By tuning this parameter, you can control how dynamic the load balancing is at\
the cost of extra created connections. With a lower value of`max_slave_connections`, less connections per session are created and the set of\
possible slave servers is smaller. With a higher value in`max_slave_connections`, more connections are created which requires more\
resources but load balancing will almost always give the best single query\
response time and performance. Longer sessions are less affected by a high`max_slave_connections` as the relative cost of opening a connection is lower.

#### `max_slave_replication_lag`

**`max_slave_replication_lag`** specifies how many seconds a slave is allowed to\
be behind the master. If the lag is bigger than the configured value a slave\
can't be used for routing.

This feature is disabled by default.

```
max_slave_replication_lag=<allowed lag in seconds>
```

This applies to Master/Slave replication with MySQL monitor and`detect_replication_lag=1` options set. max\_slave\_replication\_lag must be\
greater than the monitor interval.

This option only affects Master-Slave clusters. Galera clusters do not have a\
concept of slave lag even if the application of write sets might have lag.

#### `use_sql_variables_in`

**`use_sql_variables_in`** specifies where should queries, which read session\
variable, be routed. The syntax for `use_sql_variable_in` is:

```
use_sql_variables_in=[master|all]
```

The default is to use SQL variables in all servers.

When value `all` is used, queries reading session variables can be routed to any\
available slave (depending on selection criteria). Queries modifying session\
variables are routed to all backend servers by default, excluding write queries\
with embedded session variable modifications, such as:

```
INSERT INTO test.t1 VALUES (@myid:=@myid+1)
```

In above-mentioned case the user-defined variable would only be updated in the\
master where the query would be routed to due to the `INSERT` statement.

**Note:** As of version 2.1 of MaxScale, all of the router options can also be\
defined as parameters. The values defined in _router\_options_ will have priority\
over the parameters.

```
[Splitter Service]
type=service
router=readwritesplit
servers=dbserv1, dbserv2, dbserv3
user=maxscale
passwd=96F99AA1315BDC3604B006F427DD9484
disable_sescmd_history=true
master_failure_mode=fail_on_write
```

#### `connection_keepalive`

Send keepalive pings to backend servers. This feature was introduced in MaxScale\
2.2.0 and is disabled by default.

The parameter value is the interval in seconds between each keepalive ping. A\
keepalive ping will be sent to a backend server if the connection is idle and it\
has not been used within `n` seconds where `n` is greater than or equal to the\
value of _connection\_keepalive_. The keepalive pings are only sent when the\
client executes a query.

This functionality allows the readwritesplit module to keep all backend\
connections alive even if they are not used. This is a common problem if the\
backend servers have a low _wait\_timeout_ value and the client connections live\
for a long time.

### Router options

**`router_options`** may include multiple **readwritesplit**-specific options.\
All the options are parameter-value pairs. All parameters listed in this section\
must be configured as a value in `router_options`.

Multiple options can be defined as a comma-separated list of parameter-value\
pairs.

```
router_options=<option>,<option>
```

For example, to set **`slave_selection_criteria`** an&#x64;**`disable_sescmd_history`**, write

```
router_options=slave_selection_criteria=LEAST_GLOBAL_CONNECTIONS,disable_sescmd_history=true
```

#### `slave_selection_criteria`

This option controls how the readwritesplit router chooses the slaves it\
connects to and how the load balancing is done. The default behavior is to route\
read queries to the slave server with the lowest amount of ongoing queries i.e.`LEAST_CURRENT_OPERATIONS`.

The option syntax:

```
router_options=slave_selection_criteria=<criteria>
```

Where `<criteria>` is one of the following values.

* `LEAST_GLOBAL_CONNECTIONS`, the slave with least connections from MariaDB MaxScale
* `LEAST_ROUTER_CONNECTIONS`, the slave with least connections from this service
* `LEAST_BEHIND_MASTER`, the slave with smallest replication lag
* `LEAST_CURRENT_OPERATIONS` (default), the slave with least active operations

The `LEAST_GLOBAL_CONNECTIONS` and `LEAST_ROUTER_CONNECTIONS` use the\
connections from MariaDB MaxScale to the server, not the amount of connections\
reported by the server itself.

`LEAST_BEHIND_MASTER` does not take server weights into account when choosing a\
server.

**Server Weights and `slave_selection_criteria`**

The following formula is used to calculate a score for a server when the`weightby` parameter is defined.

```
score = x / w
```

`x` is the absolute value of the chosen metric (queries, connections) and`w` is the weight of the server. The value of `w` is the relative weight\
of the server in relation to all the servers configured for the\
service. The server with the highest score that fulfills all other\
criteria is chosen as the target server.

Read the [configuration guide](../maxscale-22-getting-started/mariadb-maxscale-22-mariadb-maxscale-configuration-usage-scenarios.md#weightby)\
for a more detailed example on how the weights are calculated.

For `LEAST_CURRENT_OPERATIONS`, the metric is number of active queries on\
the candidate server, for `LEAST_GLOBAL_CONNECTIONS` and`LEAST_ROUTER_CONNECTIONS` it is the number of open connections and for`LEAST_BEHIND_MASTER` it is the number of seconds a server is behind the\
master.

**Interaction Between `slave_selection_criteria` and `max_slave_connections`**

Depending on the value of `max_slave_connections`, the slave selection criteria\
behave in different ways. Here are a few example cases of how the different\
criteria work with different amounts of slave connections.

* With `slave_selection_criteria=LEAST_GLOBAL_CONNECTIONS` and`max_slave_connections=1`, each session picks one slave and one master
* With `slave_selection_criteria=LEAST_CURRENT_OPERATIONS` and`max_slave_connections=100%`, each session picks one master and as many slaves\
  as possible
* With `slave_selection_criteria=LEAST_CURRENT_OPERATIONS` each read is load\
  balanced based on how many queries are active on a particular slave
* With `slave_selection_criteria=LEAST_GLOBAL_CONNECTIONS` each read is sent to\
  the slave with the least amount of connections

#### `max_sescmd_history`

**`max_sescmd_history`** sets a limit on how many session commands each session\
can execute before the session command history is disabled. The default is an\
unlimited number of session commands.

```
# Set a limit on the session command history
router_options=max_sescmd_history=1500
```

When a limitation is set, it effectively creates a cap on the session's memory\
consumption. This might be useful if connection pooling is used and the sessions\
use large amounts of session commands.

#### `disable_sescmd_history`

This option disables the session command history. This way no history is stored\
and if a slave server fails, the router will not try to replace the failed\
slave. Disabling session command history will allow long-lived connections\
without causing a constant growth in the memory consumption.

This option is only intended to be enabled if the value of`max_slave_connections` is lowered below the default value. This will allow a\
failed slave to be replaced with a standby slave server.

In versions 2.0 and older, the session command history is enabled by default.\
Starting with version 2.1, the session command history is disabled by default.

```
# Disable the session command history
router_options=disable_sescmd_history=true
```

#### `master_accept_reads`

**`master_accept_reads`** allows the master server to be used for reads. This is\
a useful option to enable if you are using a small number of servers and wish to\
use the master for reads as well.

By default, no reads are sent to the master.

```
# Use the master for reads
router_options=master_accept_reads=true
```

#### `strict_multi_stmt`

This option is disabled by default since MaxScale 2.2.1. In older versions, this\
option was enabled by default.

When a client executes a multi-statement query, it will be treated as if it were\
a DML statement and routed to the master. If the option is enabled, all queries\
after a multi-statement query will be routed to the master to guarantee a\
consistent session state.

If the feature is disabled, queries are routed normally after a multi-statement\
query.

**Warning:** Enable the strict mode only if you know that the clients will send\
statements that cause inconsistencies in the session state.

```
# Enable strict multi-statement mode
router_options=strict_multi_stmt=true
```

#### `strict_sp_calls`

Similar to `strict_multi_stmt`, this option allows all queries after a CALL\
operation on a stored procedure to be routed to the master. This option is\
disabled by default and was added in MaxScale 2.1.9.

All warnings and restrictions that apply to `strict_multi_stmt` also apply to`strict_sp_calls`.

#### `master_failure_mode`

This option controls how the failure of a master server is handled. By default,\
the router will close the client connection as soon as the master is lost.

The following table describes the values for this option and how they treat the\
loss of a master server.

| Value            | Description                                                                                                                     |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Value            | Description                                                                                                                     |
| fail\_instantly  | When the failure of the master server is detected, the connection will be closed immediately.                                   |
| fail\_on\_write  | The client connection is closed if a write query is received when no master is available.                                       |
| error\_on\_write | If no master is available and a write query is received, an error is returned stating that the connection is in read-only mode. |

These also apply to new sessions created after the master has failed. This means\
that in _fail\_on\_write_ or _error\_on\_write_ mode, connections are accepted as\
long as slave servers are available.

**Note:** If _master\_failure\_mode_ is set to _error\_on\_write_ and the connection\
to the master is lost, clients will not be able to execute write queries without\
reconnecting to MariaDB MaxScale once a new master is available.

#### `retry_failed_reads`

This option controls whether autocommit selects are retried in case of failure.\
This option is enabled by default.

When a simple autocommit select is being executed outside of a transaction and\
the slave server where the query is being executed fails, readwritesplit can\
retry the read on a replacement server. This makes the failure of a slave\
transparent to the client.

### Routing hints

The readwritesplit router supports routing hints. For a detailed guide on hint\
syntax and functionality, please read [this](../maxscale-22-reference/mariadb-maxscale-22-hint-syntax.md)\
document.

**Note**: Routing hints will always have the highest priority when a routing\
decision is made. This means that it is possible to cause inconsistencies in\
the session state and the actual data in the database by adding routing hints\
to DDL/DML statements which are then directed to slave servers. Only use routing\
hints when you are sure that they can cause no harm.

### Limitations

For a list of readwritesplit limitations, please read the[Limitations](../about-maxscale-22/mariadb-maxscale-22-limitations-and-known-issues-within-mariadb-maxscale.md) document.

### Examples

Examples of the readwritesplit router in use can be found in the[Tutorials](https://mariadb.com/kb/Tutorials) folder.

### Readwritesplit routing decisions

Here is a small explanation which shows what kinds of queries are routed to\
which type of server.

#### Routing to Master

Routing to master is important for data consistency and because majority of\
writes are written to binlog and thus become replicated to slaves.

The following operations are routed to master:

* write statements,
* all statements within an open transaction,
* stored procedure calls
* user-defined function calls
* DDL statements (`DROP`|`CREATE`|`ALTER TABLE` … etc.)
* `EXECUTE` (prepared) statements
* all statements using temporary tables

In addition to these, if the **readwritesplit** service is configured with the`max_slave_replication_lag` parameter, and if all slaves suffer from too much\
replication lag, then statements will be routed to the _Master_. (There might be\
other similar configuration parameters in the future which limit the number of\
statements that will be routed to slaves.)

#### Routing to Slaves

The ability to route some statements to slaves is important because it also\
decreases the load targeted to master. Moreover, it is possible to have multiple\
slaves to share the load in contrast to single master.

Queries which can be routed to slaves must be auto committed and belong to one\
of the following group:

* read-only database queries,
* read-only queries to system, or user-defined variables,
* `SHOW` statements
* system function calls.

#### Routing to every session backend

A third class of statements includes those which modify session data, such as\
session system variables, user-defined variables, the default database, etc. We\
call them session commands, and they must be replicated as they affect the\
future results of read and write operations. They must be executed on all\
servers that could execute statements on behalf of this client.

Session commands include for example:

* `SET` statements
* `USE``<dbname>`
* system/user-defined variable assignments embedded in read-only statements, such\
  as `SELECT (@myvar := 5)`
* `PREPARE` statements
* `QUIT`, `PING`, `STMT RESET`, `CHANGE USER`, etc. commands

**NOTE**: if variable assignment is embedded in a write statement it is routed\
to _Master_ only. For example, `INSERT INTO t1 values(@myvar:=5, 7)` would be\
routed to _Master_ only.

The router stores all of the executed session commands so that in case of a\
slave failure, a replacement slave can be chosen and the session command history\
can be repeated on that new slave. This means that the router stores each\
executed session command for the duration of the session. Applications that use\
long-running sessions might cause MariaDB MaxScale to consume a growing amount\
of memory unless the sessions are closed. This can be solved by setting a\
connection timeout on the application side.

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
