
# Aurora Monitor

# Aurora Monitor


This module monitors the status of Aurora cluster replicas. These replicas do
not use the standard MySQL protocol replication but rely on a mechanism provided
by AWS to replicate changes.


# How Aurora Is Monitored


Each node in an Aurora cluster has the variable `@@aurora_server_id` which is
the unique identifier for that node. An Aurora replica stores information
relevant to replication in the `information_schema.replica_host_status`
table. The table contains information about the status of all replicas in the
cluster. The `server_id` column in this table holds the values of
`@@aurora_server_id` variables from all nodes. The `session_id` column contains
an unique string for all read-only replicas. For the master node, this value
will be `MASTER_SESSION_ID`. By executing the following query, we are able to
retrieve the `@@aurora_server_id` of the master node along with the
`@@aurora_server_id` of the current node.



```
SELECT @@aurora_server_id, server_id FROM information_schema.replica_host_status WHERE session_id = 'MASTER_SESSION_ID';
```



The node which returns a row with two identical fields is the master. All other
nodes are read-only replicas and will be labeled as slave servers.


In addition to replica status information, the
`information_schema.replica_host_status` table contains information about
replication lag between the master and the read-only nodes. This value is stored
in the `replica_lag_in_milliseconds` column. This can be used to detect read
replicas that are lagging behind the master node. This information can then be
used by the routing modules to route reads to up-to-date nodes.


# Configuring the Aurora Monitor


The Aurora monitor should connect directly to the unique endpoints of the Aurora
replicas. The cluster end point should not be included in the set of monitored
servers. Read the [Amazon RDS User Guide](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Aurora.html#Aurora.Overview.Endpoints)
for more information about how to retrieve the unique endpoints of your cluster.


The Aurora monitor requires no parameters apart from the standard monitor
parameters. It supports the monitor script functionality described in
[Monitor Common](mariadb-maxscale-25-common-monitor-parameters.md) documentation.


Here is an example Aurora monitor configuration.



```
[Aurora-Monitor]
type=monitor
module=auroramon
servers=cluster-1,cluster-2,cluster-3
user=aurora
password=borealis
monitor_interval=2500ms
```



The servers *cluster-1*, *cluster-2* and *cluster-3* are the unique Aurora
endpoints configured as MaxScale servers. The monitor will use the
*aurora*:*borealis* credentials to connect to each of the endpoint. The status
of the nodes is inspected every 2500 milliseconds.


CC BY-SA / Gnu FDL

