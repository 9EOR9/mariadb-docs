# MariaDB Monitor

* [MariaDB Monitor](mariadb-maxscale-24-mariadb-monitor.md#mariadb-monitor)
  * [Overview](mariadb-maxscale-24-mariadb-monitor.md#overview)
  * [Master selection](mariadb-maxscale-24-mariadb-monitor.md#master-selection)
  * [Configuration](mariadb-maxscale-24-mariadb-monitor.md#configuration)
  * [Common Monitor Parameters](mariadb-maxscale-24-mariadb-monitor.md#common-monitor-parameters)
  * [MariaDB Monitor optional parameters](mariadb-maxscale-24-mariadb-monitor.md#mariadb-monitor-optional-parameters)
    * [assume\_unique\_hostnames](mariadb-maxscale-24-mariadb-monitor.md#assume_unique_hostnames)
    * [detect\_replication\_lag](mariadb-maxscale-24-mariadb-monitor.md#detect_replication_lag)
    * [detect\_stale\_master](mariadb-maxscale-24-mariadb-monitor.md#detect_stale_master)
    * [detect\_stale\_slave](mariadb-maxscale-24-mariadb-monitor.md#detect_stale_slave)
    * [mysql51\_replication](mariadb-maxscale-24-mariadb-monitor.md#mysql51_replication)
    * [multimaster](mariadb-maxscale-24-mariadb-monitor.md#multimaster)
    * [ignore\_external\_masters](mariadb-maxscale-24-mariadb-monitor.md#ignore_external_masters)
    * [detect\_standalone\_master](mariadb-maxscale-24-mariadb-monitor.md#detect_standalone_master)
    * [failcount](mariadb-maxscale-24-mariadb-monitor.md#failcount)
    * [allow\_cluster\_recovery](mariadb-maxscale-24-mariadb-monitor.md#allow_cluster_recovery)
    * [enforce\_read\_only\_slaves](mariadb-maxscale-24-mariadb-monitor.md#enforce_read_only_slaves)
    * [maintenance\_on\_low\_disk\_space](mariadb-maxscale-24-mariadb-monitor.md#maintenance_on_low_disk_space)
  * [Cluster manipulation operations](mariadb-maxscale-24-mariadb-monitor.md#cluster-manipulation-operations)
    * [Operation details](mariadb-maxscale-24-mariadb-monitor.md#operation-details)
    * [Manual activation](mariadb-maxscale-24-mariadb-monitor.md#manual-activation)
    * [Automatic activation](mariadb-maxscale-24-mariadb-monitor.md#automatic-activation)
    * [Limitations and requirements](mariadb-maxscale-24-mariadb-monitor.md#limitations-and-requirements)
    * [External master support](mariadb-maxscale-24-mariadb-monitor.md#external-master-support)
    * [Configuration parameters](mariadb-maxscale-24-mariadb-monitor.md#configuration-parameters)
      * [auto\_failover](mariadb-maxscale-24-mariadb-monitor.md#auto_failover)
      * [auto\_rejoin](mariadb-maxscale-24-mariadb-monitor.md#auto_rejoin)
      * [switchover\_on\_low\_disk\_space](mariadb-maxscale-24-mariadb-monitor.md#switchover_on_low_disk_space)
      * [enforce\_simple\_topology](mariadb-maxscale-24-mariadb-monitor.md#enforce_simple_topology)
      * [replication\_user and replication\_password](mariadb-maxscale-24-mariadb-monitor.md#replication_user-and-replication_password)
      * [replication\_master\_ssl](mariadb-maxscale-24-mariadb-monitor.md#replication_master_ssl)
      * [failover\_timeout and switchover\_timeout](mariadb-maxscale-24-mariadb-monitor.md#failover_timeout-and-switchover_timeout)
      * [verify\_master\_failure and master\_failure\_timeout](mariadb-maxscale-24-mariadb-monitor.md#verify_master_failure-and-master_failure_timeout)
      * [servers\_no\_promotion](mariadb-maxscale-24-mariadb-monitor.md#servers_no_promotion)
      * [promotion\_sql\_file and demotion\_sql\_file](mariadb-maxscale-24-mariadb-monitor.md#promotion_sql_file-and-demotion_sql_file)
      * [handle\_events](mariadb-maxscale-24-mariadb-monitor.md#handle_events)
  * [Troubleshooting](mariadb-maxscale-24-mariadb-monitor.md#troubleshooting)
    * [Failover/switchover fails](mariadb-maxscale-24-mariadb-monitor.md#failoverswitchover-fails)
    * [Slave detection shows external masters](mariadb-maxscale-24-mariadb-monitor.md#slave-detection-shows-external-masters)
  * [Using the MariaDB Monitor With Binlogrouter](mariadb-maxscale-24-mariadb-monitor.md#using-the-mariadb-monitor-with-binlogrouter)

### Overview

MariaDB Monitor monitors a Master-Slave replication cluster. It probes the\
state of the backends and assigns server roles such as master and slave, which\
are used by the routers when deciding where to route a query. It can also modify\
the replication cluster by performing failover, switchover and rejoin. Backend\
server versions older than MariaDB/MySQL 5.5 are not supported. Failover and\
other similar operations require MariaDB 10.0.2 or later.

Up until MariaDB MaxScale 2.2.0, this monitor was called _MySQL Monitor_.

### Master selection

Only one backend can be master at any given time. A master must be running\
(successfully connected to by the monitor) and its _read\_only_-setting must be\
off. A master may not be replicating from another server in the monitored\
cluster unless the master is part of a multimaster group. Master selection\
prefers to select the server with the most slaves, possibly in multiple\
replication layers. Only slaves reachable by a chain of running relays or\
directly connected to the master count. When multiple servers are tied for\
master status, the server which appears earlier in the `servers`-setting of the\
monitor is selected.

Servers in a cyclical replication topology (multimaster group) are interpreted\
as having all the servers in the group as slaves. Even from a multimaster group\
only one server is selected as the overall master.

After a master has been selected, the monitor prefers to stick with the choice\
even if other potential masters with more slave servers are available. Only if\
the current master is clearly unsuitable does the monitor try to select another\
master. An existing master turns invalid if:

1. It is unwritable (read\_only is on).
2. It has been down for more than failcount monitor passes and has no running\
   slaves. Running slaves behind a downed relay count.
3. It did not previously replicate from another server in the cluster but it\
   is now replicating.
4. It was previously part of a multimaster group but is no longer, or the\
   multimaster group is replicating from a server not in the group.

Cases 1 and 2 cover the situations in which the DBA, an external script or even\
another MaxScale has modified the cluster such that the old master can no longer\
act as master. Cases 3 and 4 are less severe. In these cases the topology has\
changed significantly and the master should be re-selected, although the old\
master may still be the best choice.

The master change described above is different from failover and switchover\
described in section[Failover, switchover and auto-rejoin](mariadb-maxscale-24-mariadb-monitor.md#failover,-switchover-and-auto-rejoin).\
A master change only modifies the server roles inside MaxScale but does not\
modify the cluster other than changing the targets of read and write queries.\
Failover and switchover perform a master change on their own.

As a general rule, it's best to avoid situations where the cluster has multiple\
standalone servers, separate master-slave pairs or separate multimaster groups.\
Due to master invalidation rule 2, a standalone master can easily lose the\
master status to another valid master if it goes down. The new master probably\
does not have the same data as the previous one. Non-standalone masters are less\
vulnerable, as a single running slave or multimaster group member will keep the\
master valid even when down.

### Configuration

A minimal configuration for a monitor requires a set of servers for monitoring\
and a username and a password to connect to these servers.

```
[MyMonitor]
type=monitor
module=mariadbmon
servers=server1,server2,server3
user=myuser
password=mypwd
```

From MaxScale 2.2.1 onwards, the module name is `mariadbmon` instead of`mysqlmon`. The old name can still be used.

The `user` requires privileges depending on which monitor features are used.\
REPLICATION CLIENT (or REPLICATION SLAVE ADMIN for Server 10.5) allows the\
monitor to list replication connections, and is always required. See[Cluster manipulation operations](mariadb-maxscale-24-mariadb-monitor.md#cluster-manipulation-operations) for more\
information on required privileges.

```
MariaDB [(none)]> grant replication client on *.* to 'myuser'@'maxscalehost';
Query OK, 0 rows affected (0.00 sec)
```

### Common Monitor Parameters

For a list of optional parameters that all monitors support, read the[Monitor Common](mariadb-maxscale-24-common-monitor-parameters.md) document.

### MariaDB Monitor optional parameters

These are optional parameters specific to the MariaDB Monitor. Failover,\
switchover and rejoin-specific parameters are listed in their own[section](mariadb-maxscale-24-mariadb-monitor.md#cluster-manipulation-operations).

#### `assume_unique_hostnames`

Boolean, default: ON. When active, the monitor assumes that server hostnames and\
ports are consistent between the server definitions in the MaxScale\
configuration file and the "SHOW ALL SLAVES STATUS" outputs of the servers\
themselves. Specifically, the monitor assumes that if server A is replicating\
from server B, then A must have a slave connection with `Master_Host` and`Master_Port` equal to B's address and port in the configuration file. If this\
is not the case, e.g. an IP is used in the server while a hostname is given in\
the file, the monitor may misinterpret the topology. In MaxScale 2.4.1, the\
monitor attempts name resolution on the addresses if a simple string comparison\
does not find a match. Using exact matching addresses is, however, more\
reliable.

This setting must be ON to use any cluster operation features such as failover\
or switchover, because MaxScale uses the addresses and ports in the\
configuration file when issuing "CHANGE MASTER TO"-commands.

If the network configuration is such that the addresses MaxScale uses to connect\
to backends are different from the ones the servers use to connect to each\
other, `assume_unique_hostnames` should be set to OFF. In this mode, MaxScale\
uses server id:s it queries from the servers and the `Master_Server_Id` fields\
of the slave connections to deduce which server is replicating from which. This\
is not perfect though, since MaxScale doesn't know the id:s of servers it has\
never connected to (e.g. server has been down since MaxScale was started). Also,\
the `Master_Server_Id`-field may have an incorrect value if the slave connection\
has not been established. MaxScale will only trust the value if the monitor has\
seen the slave connection IO thread connected at least once. If this is not the\
case, the slave connection is ignored.

#### `detect_replication_lag`

Deprecated and unused as of MaxScale 2.3. Can be defined but is ignored.

Is effectively always on. The monitor uses the "Seconds\_Behind\_Master"-field of\
"SHOW SLAVE STATUS" to get the replication lag.

#### `detect_stale_master`

Deprecated and ignored.

#### `detect_stale_slave`

Boolean, default: ON. Treat running slaves servers without a running master as\
valid slave servers.

If a slave server does not have a live connection to the master, either because\
the master is _Down_ or because the slave cannot connect, replication is\
effectively paused. The slave may still have up-to-date data and may be usable\
for reading. _detect\_stale\_slave_ controls whether such a slave is marked _Slave_\
and used for query routing.

If this feature is disabled, a server is considered a valid slave only if it has\
a running master server and the replication connection is working properly. In a\
multi-level topology, each link would also need to be replicating properly.

```
detect_stale_slave=true
```

#### `mysql51_replication`

Deprecated and unused as of MaxScale 2.3. Can be defined but is ignored.

#### `multimaster`

Deprecated and unused as of MaxScale 2.3. Can be defined but is ignored.

#### `ignore_external_masters`

Boolean, default: OFF. Ignore any servers that are not monitored by this monitor\
but are a part of the replication topology.

An external server is a server not monitored by this monitor. If a server is\
replicating from an external server, it typically gains the _Slave of External_\
\&#xNAN;_Server_-status. If this setting is enabled, the status is not set.

#### `detect_standalone_master`

Boolean, default: ON. This setting controls whether a standalone server can be a\
master. A standalone server is a server from which no other server in the\
cluster is attempting to replicate from.

If disabled, a solitary server cannot gain _Master_-status. If MaxScale cannot\
connect to a slave but the slave was previously replicating, then the master is\
still assumed to have a slave, and this setting does not apply.

#### `failcount`

Number of consecutive monitor passes a master server must be down before it is\
considered failed. At this point, automatic failover is performed if enabled\
(`auto_failover=true`). If automatic failover is not on, the monitor will try to\
search for another server to fultill the master role. See section[Master selection](mariadb-maxscale-24-mariadb-monitor.md#master-selection)\
for more details. Changing the master may break replication as queries could be\
routed to a server without previous events. To prevent this, avoid having\
multiple valid master servers in the cluster.

The default value is 5 failures.

The worst-case delay between the master failure and the start of the failover\
can be estimated by summing up the timeout values and `monitor_interval` and\
multiplying that by `failcount`:

```
(monitor_interval + backend_connect_timeout) * failcount
```

#### `allow_cluster_recovery`

Deprecated and unused as of MaxScale 2.3. Can be defined but is ignored.

#### `enforce_read_only_slaves`

This feature is disabled by default. If set to ON, the monitor attempts to set\
the server `read_only` flag to ON on any slave server with `read_only` OFF. The\
flag is checked at every monitor iteration. The monitor user requires the\
SUPER-privilege for this feature to work. While the `read_only`-flag is ON, only\
users with the SUPER-privilege can write to the backend server. If temporary\
write access is required, this feature should be disabled before attempting to\
disable `read_only`. Otherwise the monitor would quickly re-enable it.

#### `maintenance_on_low_disk_space`

This feature is enabled by default. If a running server that is not the master\
or a relay master is out of disk space the server is set to maintenance mode.\
Such servers are not used for router sessions and are ignored when performing a\
failover or other cluster modification operation. See the general monitor\
parameters [disk\_space\_threshold](https://mariadb.com/kb/en/node:mariadb-maxscale-24-common-monitor-parameters#disk_space_threshold) and[disk\_space\_check\_interval](https://mariadb.com/kb/en/node:mariadb-maxscale-24-common-monitor-parameters#disk_space_check_interval)\
on how to enable disk space monitoring.

Once a server has been put to maintenance mode, the disk space situation\
of that server is no longer updated. The server will not be taken out of\
maintanance mode even if more disk space becomes available. The maintenance\
flag must be removed manually:

```
maxadmin clear server server2 Maint
maxctrl clear server server2 Maint
```

### Cluster manipulation operations

Starting with MaxScale 2.2.1, MariaDB Monitor supports replication cluster\
modification. The operations implemented are:

* _failover_, which replaces a failed master with a slave
* _switchover_, which swaps a running master with a slave
* _rejoin_, which directs servers to replicate from the master
* _reset-replication_ (added in MaxScale 2.3.0), which deletes binary logs and\
  resets gtid:s

See [operation details](mariadb-maxscale-24-mariadb-monitor.md#operation-details) for more information on the\
implementation of the commands.

The cluster operations require that the monitor user (`user`) has the following\
privileges:

* SUPER, to modify slave connections, set globals such as read\_only and kill\
  connections from other super-users
* SELECT on mysql.user, to see which users have SUPER
* REPLICATION CLIENT (REPLICATION SLAVE ADMIN in MariaDB Server 10.5), to list\
  slave connections
* RELOAD, to flush binary logs
* PROCESS, to check if the event\_scheduler process is running
* SHOW DATABASES and EVENT, to list and modify server events

```
GRANT super, replication client, reload, process, show databases, event on *.* to 'myuser'@'maxscalehost';
GRANT select on mysql.user to 'myuser'@'maxscalehost';
```

The privilege system was changed in MariaDB Server 10.5. The effects of this on\
the MaxScale monitor user are minor, as the SUPER-privilege contains many of the\
required privileges and is still required to kill connections from other\
super-users.

```
GRANT super, reload, process, show databases, event on *.* to 'myuser'@'maxscalehost';
GRANT select on mysql.user to 'myuser'@'maxscalehost';
```

In addition, the monitor needs to know which username and password a\
slave should use when starting replication. These are given in`replication_user` and `replication_password`.

The user can define files with SQL statements which are executed on any server\
being demoted or promoted by cluster manipulation commands. See the sections on`promotion_sql_file` and `demotion_sql_file` for more information.

The monitor can manipulate scheduled server events when promoting or demoting a\
server. See the section on `handle_events` for more information.

All cluster operations can be activated manually through MaxAdmin/MaxCtrl. See\
section [Manual activation](mariadb-maxscale-24-mariadb-monitor.md#manual-activation) for more details.

See [Limitations and requirements](mariadb-maxscale-24-mariadb-monitor.md#limitations-and-requirements) for\
information on possible issues with failover and switchover.

#### Operation details

**Failover** replaces a failed master with a running slave. It does the\
following:

1. Select the most up-to-date slave of the old master to be the new master. The\
   selection criteria is as follows in descending priority:
2. gtid\_IO\_pos (latest event in relay log)
3. gtid\_current\_pos (most processed events)
4. log\_slave\_updates is on
5. disk space is not low
6. If the new master has unprocessed relay log items, cancel and try again\
   later.
7. Prepare the new master:
8. Remove the slave connection the new master used to replicate from the\
   old master.
9. Disable the read\_only-flag.
10. Enable scheduled server events (if event handling is on). Only events\
    that were enabled on the old master are enabled.
11. Run the commands in `promotion_sql_file`.
12. Start replication from external master if one existed.
13. Redirect all other slaves to replicate from the new master:
14. STOP SLAVE and RESET SLAVE
15. CHANGE MASTER TO
16. START SLAVE
17. Check that all slaves are replicating.

Failover is considered successful if steps 1 to 3 succeed, as the cluster then\
has at least a valid master server.

**Switchover** swaps a running master with a running slave. It does the\
following:

1. Prepare the old master for demotion:
2. Stop any external replication.
3. Kill connections from super-users since read\_only does not affect\
   them.
4. Enable the read\_only-flag to stop writes.
5. Disable scheduled server events (if event handling is on).
6. Run the commands in `demotion_sql_file`.
7. Flush the binary log (FLUSH LOGS) so that all events are on disk.
8. Wait for the new master to catch up with the old master.
9. Promote new master and redirect slaves as in failover steps 3 and 4. Also\
   redirect the demoted old master.
10. Check that all slaves are replicating.

Similar to failover, switchover is considered successful if the new master was\
successfully promoted.

**Rejoin** joins a standalone server to the cluster or redirects a slave\
replicating from a server other than the master. A standalone server is joined\
by:

1. Run the commands in `demotion_sql_file`.
2. Enable the read\_only-flag.
3. Disable scheduled server events (if event handling is on).
4. Start replication: CHANGE MASTER TO and START SLAVE.

A server which is replicating from the wrong master is redirected simply with\
STOP SLAVE, RESET SLAVE, CHANGE MASTER TO and START SLAVE commands.

**Reset-replication** (added in MaxScale 2.3.0) deletes binary logs and resets\
gtid:s. This destructive command is meant for situations where the gtid:s in the\
cluster are out of sync while the actual data is known to be in sync. The\
operation proceeds as follows:

1. Reset gtid:s and delete binary logs on all servers:
2. Stop (STOP SLAVE) and delete (RESET SLAVE ALL) all slave connections.
3. Enable the read\_only-flag.
4. Disable scheduled server events (if event handling is on).
5. Delete binary logs (RESET MASTER).
6. Set the sequence number of gtid\_slave\_pos to zero. This also affects\
   gtid\_current\_pos.
7. Prepare new master:
8. Disable the read\_only-flag.
9. Enable scheduled server events (if event handling is on). Events are\
   only enabled if the cluster had a master server when starting the\
   reset-replication operation. Only events that were enabled on the previous\
   master are enabled on the new.
10. Direct other servers to replicate from the new master as in the other\
    operations.

#### Manual activation

Cluster operations can be activated manually through the REST API, MaxCtrl or\
MaxAdmin. The commands are only performed when MaxScale is in active mode. The\
commands generally match their automatic versions. The exception is _rejoin_, in\
which the manual command allows rejoining even when the joining server has empty\
gtid:s. This rule allows the user to force a rejoin on a server without binary\
logs.

All commands require the monitor instance name as the first parameter. Failover\
selects the new master server automatically and does not require additional\
parameters. Rejoin requires the name of the joining server as second parameter.\
Replication reset accepts the name of the new master server as second parameter.\
If not given, the current master is selected.

Switchover takes one to three parameters. If only the monitor name is given,\
switchover will autoselect both the slave to promote and the current master as\
the server to be demoted. If two parameters are given, the second parameter is\
interpreted as the slave to promote. If three parameters are given, the third\
parameter is interpreted as the current master. The user-given current master is\
compared to the master server currently deduced by the monitor and if the two\
are unequal, an error is given.

Example commands are below:

```
call command mariadbmon failover MyMonitor
call command mariadbmon rejoin MyMonitor OldMasterServ
call command mariadbmon reset-replication MyMonitor
call command mariadbmon reset-replication MyMonitor NewMasterServ
call command mariadbmon switchover MyMonitor
call command mariadbmon switchover MyMonitor NewMasterServ
call command mariadbmon switchover MyMonitor NewMasterServ OldMasterServ
```

The commands follow the standard module command syntax. All require the monitor\
configuration name (MyMonitor) as the first parameter. For switchover, the\
last two parameters define the server to promote (NewMasterServ) and the server\
to demote (OldMasterServ). For rejoin, the server to join (OldMasterServ) is\
required. Replication reset requires the server to promote (NewMasterServ).

It is safe to perform manual operations even with automatic failover, switchover\
or rejoin enabled since automatic operations cannot happen simultaneously\
with manual ones.

If a switchover or failover fails, automatic failover is disabled to prevent\
master changes to a possibly malfunctioning cluster. Automatic failover can be\
turned on manually via the REST API or MaxAdmin. Example commands are listed\
below.

```
maxadmin alter monitor MariaDB-Monitor auto_failover=true
maxctrl alter monitor MariaDB-Monitor auto_failover true
```

When a cluster modification is iniated via the REST-API, the URL path is of the\
form:

```
/v1/maxscale/modules/mariadbmon/<operation>?<monitor-instance>&<server-param1>&<server-param2>
```

* `<operation>` is the name of the command: failover, switchover, rejoin\
  or reset-replication.
* `<monitor-instance>` is the monitor section name from the MaxScale\
  configuration file.
* `<server-param1>` and `<server-param2>` are server parameters as described\
  above for MaxAdmin. Only switchover accepts both, failover doesn't need any\
  and both rejoin and reset-replication accept one.

Given a MaxScale configuration file like

```
[Cluster1]
type=monitor
module=mariadbmon
servers=server1, server2, server3, server 4
...
```

with the assumption that `server2` is the current master, then the URL\
path for making `server4` the new master would be:

```
/v1/maxscale/modules/mariadbmon/switchover?Cluster1&server4&server2
```

Example REST-API paths for other commands are listed below.

```
/v1/maxscale/modules/mariadbmon/failover?Cluster1
/v1/maxscale/modules/mariadbmon/rejoin?Cluster1&server3
/v1/maxscale/modules/mariadbmon/reset-replication?Cluster1&server3
```

#### Automatic activation

Failover can activate automatically if `auto_failover` is on. The activation\
begins when the master has been down at least `failcount` monitor iterations.\
Before modifying the cluster, the monitor checks that all prerequisites for the\
failover are fulfilled. If the cluster does not seem ready, an error is printed\
and the cluster is rechecked during the next monitor iteration.

Switchover can also activate automatically with the`switchover_on_low_disk_space`-setting. The operation begins if the master\
server is low on disk space but otherwise the operating logic is quite similar\
to automatic failover.

Rejoin stands for starting replication on a standalone server or redirecting a\
slave replicating from the wrong master (any server that is not the cluster\
master). The rejoined servers are directed to replicate from the current cluster\
master server, forcing the replication topology to a 1-master-N-slaves\
configuration.

A server is categorized as standalone if the server has no slave connections,\
not even stopped ones. A server is replicating from the wrong master if the\
slave IO thread is connected but the master server id seen by the slave does not\
match the cluster master id. Alternatively, the IO thread may be stopped or\
connecting but the master server host or port information differs from the\
cluster master info. These criteria mean that a STOP SLAVE does not yet set a\
slave as standalone.

With `auto_rejoin` active, the monitor will try to rejoin any servers matching\
the above requirements. Rejoin does not obey `failcount` and will attempt to\
rejoin any valid servers immediately. When activating rejoin manually, the\
user-designated server must fulfill the same requirements.

#### Limitations and requirements

Switchover and failover only understand simple topologies. They will not work if\
the cluster has multiple masters, relay masters, or if the topology is circular.\
The server cluster is assumed to be well-behaving with no significant\
replication lag and all commands that modify the cluster complete in a few\
seconds (faster than `backend_read_timeout` and `backend_write_timeout`).

The backends must all use GTID-based replication, and the domain id should not\
change during a switchover or failover. Master and slaves must have\
well-behaving GTIDs with no extra events on slave servers.

Failover cannot be performed if MaxScale was started only after the master\
server went down. This is because MaxScale needs reliable information on the\
gtid domain of the cluster and the replication topology in general to properly\
select the new master.

Failover may lose events. If a master goes down before sending new events to at\
least one slave, those events are lost when a new master is chosen. If the old\
master comes back online, the other servers have likely moved on with a\
diverging history and the old master can no longer join the replication cluster.

To reduce the chance of losing data, use[semisynchronous replication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/semisynchronous-replication).\
In semisynchronous mode, the master waits for a slave to receive an event before\
returning an acknowledgement to the client. This does not yet guarantee a clean\
failover. If the master fails after preparing a transaction but before receiving\
slave acknowledgement, it will still commit the prepared transaction as part of\
its crash recovery. Since the slaves may never have seen this transaction, the\
old master has diverged from the slaves. See[Configuring the Master Wait Point](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/semisynchronous-replication)\
for more information.

Even a controlled shutdown of the master may lose events. The server does not by\
default wait for all data to be replicated to the slaves when shutting down and\
instead simply closes all connections. Before shutting down the master with the\
intention of having a slave promoted, run _switchover_ first to ensure that all\
data is replicated. For more information on server shutdown, see[Binary Log Dump Threads and the Shutdown Process](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-threads).

Switchover requires that the cluster is "frozen" for the duration of the\
operation. This means that no data modifying statements such as INSERT or UPDATE\
are executed and the GTID position of the master server is stable. When\
switchover begins, the monitor sets the global _read\_only_ flag on the old\
master backend to stop any updates. _read\_only_ does not affect users with the\
SUPER-privilege so any such user can issue writes during a switchover. These\
writes have a high chance of breaking replication, because the write may not be\
replicated to all slaves before they switch to the new master. To prevent this,\
any users who commonly do updates should not have the SUPER-privilege. For even\
more security, the only SUPER-user session during a switchover should be the\
MaxScale monitor user.

When mixing rejoin with failover/switchover, the backends should hav&#x65;_&#x6C;og\_slave\_updates_ on. The rejoining server is likely lagging behind the rest\
of the cluster. If the current cluster master does not have binary logs from the\
moment the rejoining server lost connection, the rejoining server cannot\
continue replication. This is an issue if the master has changed and\
the new master does not have _log\_slave\_updates_ on.

If an automatic cluster operation such as auto-failover or auto-rejoin fails,\
all cluster modifying operations are disabled for `failcount` monitor iterations,\
after which the operation may be retried. Similar logic applies if the cluster is\
unsuitable for such operations, e.g. replication is not using GTID.

#### External master support

The monitor detects if a server in the cluster is replicating from an external\
master (a server that is not monitored by the monitor). If the replicating\
server is the cluster master server, then the cluster itself is considered to\
have an external master.

If a failover/switchover happens, the new master server is set to replicate from\
the cluster external master server. The usename and password for the replication\
are defined in `replication_user` and `replication_password`. The address and\
port used are the ones shown by `SHOW ALL SLAVES STATUS` on the old cluster\
master server. In the case of switchover, the old master also stops replicating\
from the external server to preserve the topology.

After failover the new master is replicating from the external master. If the\
failed old master comes back online, it is also replicating from the external\
server. To normalize the situation, either have _auto\_rejoin_ on or manually\
execute a rejoin. This will redirect the old master to the current cluster\
master.

#### Configuration parameters

**`auto_failover`**

Enable automated master failover. This parameter expects a boolean value and the\
default value is false.

When automatic failover is enabled, traditional MariaDB Master-Slave clusters\
will automatically elect a new master if the old master goes down and stays down\
a number of iterations given in `failcount`. Failover will not take place when\
MaxScale is configured as a passive instance. For details on how MaxScale\
behaves in passive mode, see the documentation on `failover_timeout` below.

The monitor user must have the SUPER and RELOAD privileges for failover to work.

**`auto_rejoin`**

Enable automatic joining of server to the cluster. This parameter expects a\
boolean value and the default value is false.

When enabled, the monitor will attempt to direct standalone servers and servers\
replicating from a relay master to the main cluster master server, enforcing a\
1-master-N-slaves configuration.

For example, consider the following event series.

1. Slave A goes down
2. Master goes down and a failover is performed, promoting Slave B
3. Slave A comes back

Slave A is still trying to replicate from the downed master, since it wasn't\
online during failover. If `auto_rejoin` is on, Slave A will quickly be\
redirected to Slave B, the current master.

**`switchover_on_low_disk_space`**

This feature is disabled by default. If enabled, the monitor will attempt to\
switchover a master server low on disk space with a slave. The switch is only\
done if a slave without disk space issues is found. If`maintenance_on_low_disk_space` is also enabled, the old master (now a slave)\
will be put to maintenance during the next monitor iteration.

For this parameter to have any effect, `disk_space_threshold` must be specified\
for the [server](../maxscale-24-getting-started/mariadb-maxscale-24-mariadb-maxscale-configuration-guide.md)\
or the [monitor](https://github.com/mariadb-corporation/docs-server/blob/test/maxscale/mariadb-maxscale-24/maxscale-24-monitors/node:mariadb-maxscale-24-common-monitor-parameters/README.md#disk_space_threshold).\
Also, [disk\_space\_check\_interval](https://github.com/mariadb-corporation/docs-server/blob/test/maxscale/mariadb-maxscale-24/maxscale-24-monitors/node:mariadb-maxscale-24-common-monitor-parameters/README.md#disk_space_check_interval)\
must be defined for the monitor.

```
switchover_on_low_disk_space=true
```

**`enforce_simple_topology`**

This setting tells the monitor to assume that the servers should be arranged in a\
1-master-N-slaves topology and the monitor should try to keep it that way. If`enforce_simple_topology` is enabled, the settings `assume_unique_hostnames`,`auto_failover` and `auto_rejoin` are also activated regardless of their individual\
settings.

This setting also allows the monitor to perform a failover to a cluster where the master\
server has not been seen \[Running]. This is usually the case when the master goes down\
before MaxScale is started. When using this feature, the monitor will guess the GTID\
domain id of the master from the slaves. For reliable results, the GTID:s of the cluster\
should be simple.

```
enforce_simple_topology=true
```

**`replication_user` and `replication_password`**

The username and password of the replication user. These are given as the values\
for `MASTER_USER` and `MASTER_PASSWORD` whenever a `CHANGE MASTER TO` command is\
executed.

Both `replication_user` and `replication_password` parameters must be defined if\
a custom replication user is used. If neither of the parameters is defined, the`CHANGE MASTER TO`-command will use the monitor credentials for the replication\
user.

The credentials used for replication must have the `REPLICATION SLAVE`\
privilege.

`replication_password` uses the same encryption scheme as other password\
parameters. If password encryption is in use, `replication_password` must be\
encrypted with the same key to avoid erroneous decryption.

**`replication_master_ssl`**

Type: bool Default: off

If set to ON, any `CHANGE MASTER TO`-command generated will set `MASTER_SSL=1` to enable\
encryption for the replication stream. This setting should only be enabled if the backend\
servers are configured for ssl. This typically means setting _ssl\_ca_, _ssl\_cert_ an&#x64;_&#x73;sl\_key_ in the server configuration file. Additionally, credentials for the replication\
user should require an encrypted connection (`e.g. ALTER USER repl@'%' REQUIRE SSL;`).

If the setting is left OFF, `MASTER_SSL` is not set at all, which will preserve existing\
settings when redirecting a slave connection.

**`failover_timeout` and `switchover_timeout`**

Time limit for failover and switchover operations. The default\
values are 90 seconds for both. `switchover_timeout` is also used as the time\
limit for a rejoin operation. Rejoin should rarely time out, since it is a\
faster operation than switchover.

The timeouts are specified as documented[here](../maxscale-24-getting-started/mariadb-maxscale-24-mariadb-maxscale-configuration-guide.md). If no explicit unit\
is provided, the value is interpreted as seconds in MaxScale 2.4. In subsequent\
versions a value without a unit may be rejected. Note that since the granularity\
of the timeouts is seconds, a timeout specified in milliseconds will be rejected,\
even if the duration is longer than a second.

If no successful failover/switchover takes place within the configured time\
period, a message is logged and automatic failover is disabled. This prevents\
further automatic modifications to the misbehaving cluster.

**`verify_master_failure` and `master_failure_timeout`**

Enable additional master failure verification for automatic failover.`verify_master_failure` is a boolean value (default: true) which enables this\
feature and `master_failure_timeout` defines the timeout (default: 10 seconds).

The master failure timeout is specified as documented[here](../maxscale-24-getting-started/mariadb-maxscale-24-mariadb-maxscale-configuration-guide.md). If no explicit unit\
is provided, the value is interpreted as seconds in MaxScale 2.4. In subsequent\
versions a value without a unit may be rejected. Note that since the granularity\
of the timeout is seconds, a timeout specified in milliseconds will be rejected,\
even if the duration is longer than a second.

Failure verification is performed by checking whether the slave servers are\
still connected to the master and receiving events. An event is either a change\
in the _Gtid\_IO\_Pos_-field of the `SHOW SLAVE STATUS` output or a heartbeat\
event. Effectively, if a slave has received an event within`master_failure_timeout` duration, the master is not considered down when\
deciding whether to failover, even if MaxScale cannot connect to the master.`master_failure_timeout` should be longer than the `Slave_heartbeat_period` of\
the slave connection to be effective.

If every slave loses its connection to the master (_Slave\_IO\_Running_ is not\
"Yes"), master failure is considered verified regardless of timeout. This allows\
faster failover when the master properly disconnects.

For automatic failover to activate, the `failcount` requirement must also be\
met.

**`servers_no_promotion`**

This is a comma-separated list of server names that will not be chosen for\
master promotion during a failover or autoselected for switchover. This does not\
affect switchover if the user selects the server to promote. Using this setting\
can disrupt new master selection for failover such that an nonoptimal server is\
chosen. At worst, this will cause replication to break. Alternatively, failover\
may fail if all valid promotion candidates are in the exclusion list.

```
servers_no_promotion=backup_dc_server1,backup_dc_server2
```

**`promotion_sql_file` and `demotion_sql_file`**

These optional settings are paths to text files with SQL statements in them.\
During promotion or demotion, the contents are read line-by-line and executed on\
the backend. Use these settings to execute custom statements on the servers to\
complement the built-in operations.

Empty lines or lines starting with '#' are ignored. Any results returned by the\
statements are ignored. All statements must succeed for the failover, switchover\
or rejoin to continue. The monitor user may require additional privileges and\
grants for the custom commands to succeed.

When promoting a slave to master during switchover or failover, the`promotion_sql_file` is read and executed on the new master server after its\
read-only flag is disabled. The commands are ran _before_ starting replication\
from an external master if any.

`demotion_sql_file` is ran on an old master during demotion to slave, before the\
old master starts replicating from the new master. The file is also ran before\
rejoining a standalone server to the cluster, as the standalone server is\
typically a former master server. When redirecting a slave replicating from a\
wrong master, the sql-file is not executed.

Since the queries in the files are ran during operations which modify\
replication topology, care is required. If `promotion_sql_file` contains data\
modification (DML) queries, the new master server may not be able to\
successfully replicate from an external master. `demotion_sql_file` should never\
contain DML queries, as these may not replicate to the slave servers before\
slave threads are stopped, breaking replication.

```
promotion_sql_file=/home/root/scripts/promotion.sql
demotion_sql_file=/home/root/scripts/demotion.sql
```

**`handle_events`**

This setting is on by default. If enabled, the monitor continuously queries the\
servers for enabled scheduled events and uses this information when performing\
cluster operations, enabling and disabling events as appropriate.

When a server is being demoted, any events with "ENABLED" status are set to\
"SLAVESIDE\_DISABLED". When a server is being promoted to master, events that are either\
"SLAVESIDE\_DISABLED" or "DISABLED" are set to "ENABLED" if the same event was also enabled\
on the old master server last time it was successfully queried. Events are considered\
identical if they have the same schema and name. When a standalone server is rejoined to\
the cluster, its events are also disabled since it is now a slave.

The monitor does not check whether the same events were disabled and enabled during a\
switchover or failover/rejoin. All events that meet the criteria above are altered.

The monitor does not enable or disable the event scheduler itself. For the\
events to run on the new master server, the scheduler should be enabled by the\
admin. Enabling it in the server configuration file is recommended.

Events running at high frequency may cause replication to break in a failover\
scenario. If an old master which was failed over restarts, its event scheduler\
will be on if set in the server configuration file. Its events will also\
remember their "ENABLED"-status and run when scheduled. This may happen before\
the monitor rejoins the server and disables the events. This should only be an\
issue for events running more often than the monitor interval or events that run\
immediately after the server has restarted.

### Troubleshooting

#### Failover/switchover fails

Before performing failover or switchover, the MariaDB Monitor first checks that\
prerequisites are fulfilled, printing any found errors. This should catch and\
explain most issues with failover or switchover not working. If the operations\
are attempted and still fail, then most likely one of the commands the monitor\
issued to a server failed or timed out. The log should explain which query failed.\
To print out all queries sent to the servers, start MaxScale with`--debug=enable-statement-logging`. This setting prints all queries sent to the\
backends by monitors and authenticators.

A typical reason for failure is that a command such as `STOP SLAVE` takes longer than the`backend_read_timeout` of the monitor, causing the connection to break. As of 2.3, the\
monitor will retry most such queries if the failure was caused by a timeout. The retrying\
continues until the total time for a failover or switchover has been spent. If the log\
shows warnings or errors about commands timing out, increasing the backend timeout\
settings of the monitor should help. Another settings to look at are `query_retries` and`query_retry_timeout`. These are general MaxScale settings described in the[Configuration guide](../maxscale-24-getting-started/mariadb-maxscale-24-mariadb-maxscale-configuration-guide.md). Setting`query_retries` to 2 is a reasonable first try.

#### Slave detection shows external masters

If a slave is shown in _maxadmin_ or _maxctrl_ as "Slave of External Server" instead of\
"Slave", the reason is likely that the "Master\_Host"-setting of the replication connection\
does not match the MaxScale server definition. As of 2.3.2, the MariaDB Monitor by default\
assumes that the slave connections (as shown by `SHOW ALL SLAVES STATUS`) use the exact\
same "Master\_Host" as used the MaxScale configuration file server definitions. This is\
controlled by the setting [assume\_unique\_hostnames](mariadb-maxscale-24-mariadb-monitor.md#assume_unique_hostnames).

### Using the MariaDB Monitor With Binlogrouter

Since MaxScale 2.2 it's possible to detect a replication setup\
which includes Binlog Server: the required action is to add the\
binlog server to the list of servers only if _master\_id_ identity is set.

For addition information read the[Replication Proxy](../maxscale-24-tutorials/mariadb-maxscale-24-mariadb-maxscale-as-a-binlog-server.md)\
tutorial.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
