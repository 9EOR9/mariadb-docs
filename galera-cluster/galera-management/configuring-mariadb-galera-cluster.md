# Configuring MariaDB Galera Cluster

A number of options need to be set in order for Galera Cluster to work when using MariaDB. These should be set in the [MariaDB option file](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/getting-installing-and-upgrading-mariadb/configuring-mariadb-with-option-files).

## Mandatory Options

Several options are mandatory, which means that they _must_ be set in order for Galera Cluster to be enabled or to work properly with MariaDB. The mandatory options are:

* `[wsrep_provider](../reference/galera-cluster-system-variables.md#wsrep_provider)` — Path to the Galera library
* `[wsrep_cluster_address](../reference/galera-cluster-system-variables.md#wsrep_cluster_address)` — See [Galera Cluster address format and usage](galera-cluster-address.md)
* `[binlog_format=ROW](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables)` — See [Binary Log Formats](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log/binary-log-formats)
* `[wsrep_on=ON](../reference/galera-cluster-system-variables.md#wsrep_on)` — Enable wsrep replication
* `[default_storage_engine=InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables#default_storage_engine)` — This is the default value, or alternately `[wsrep_replicate_myisam=1](../reference/galera-cluster-system-variables.md#wsrep_replicate_myisam)` (before [MariaDB 10.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-10-6-series/what-is-mariadb-106)) or `[galera-cluster-system-variables/#wsrep_mode=REPLICATE_ARIA,REPLICATE_MYISAM](../reference/galera-cluster-system-variables.md#wsrep_mode%3DREPLICATE_ARIA%2CREPLICATE_MYISAM)` ([MariaDB 10.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/release-notes-mariadb-10-6-series/what-is-mariadb-106) and later)
* `[innodb_doublewrite=1](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_doublewrite)` — This is the default value, and should not be changed.

## Performance-related Options

These are optional optimizations that can be made to improve performance.

* `[innodb_flush_log_at_trx_commit=0](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_flush_log_at_trx_commit)` — This is not usually recommended in the case of standard MariaDB. However, it is a safer, recommended option with Galera Cluster, since inconsistencies can always be fixed by recovering from another node.
* `[innodb_autoinc_lock_mode=2](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_autoinc_lock_mode)` — This tells InnoDB to use interleaved method. Interleaved is the fastest and most scalable lock mode, and should be used when BINLOG\_FORMAT is set to ROW.\
  Setting the auto-increment lock mode for InnoDB to interleaved, you’re allowing slaves threads to operate in parallel.
* `[wsrep_slave_threads=4](../reference/galera-cluster-system-variables.md#wsrep_slave_threads)`\
  — This makes state transfers quicker for new nodes. You should start with four slave threads per CPU core.\
  The logic here is that, in a balanced system, four slave threads can typically saturate a CPU core. However, I/O performance can increase this figure several times over. For example, a single-core ThinkPad R51 with a 4200 RPM drive can use thirty-two slave threads. The value should not be set higher than [wsrep\_cert\_deps\_distance](../reference/galera-cluster-status-variables.md#wsrep_cert_deps_distance).

## Writing Replicated Write Sets to the Binary Log

Like with [MariaDB replication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication), write sets that are received by a node with [Galera Cluster's certification-based replication](../readme/about-galera-replication.md) are not written to the [binary log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log) by default. If you would like a node to write its replicated write sets to the [binary log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log), then you will have to set `[log_slave_updates=ON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables#log_slave_updates)`. This is especially helpful if the node is a replication master. See [Using MariaDB Replication with MariaDB Galera Cluster: Configuring a Cluster Node as a Replication Master](../high-availability/using-mariadb-replication-with-mariadb-galera-cluster/using-mariadb-replication-with-mariadb-galera-cluster-using-mariadb-replica.md).

## Replication Filters

Like with [MariaDB replication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication), [replication filters](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-filters) can be used to filter write sets from being replicated by [Galera Cluster's certification-based replication](../readme/about-galera-replication.md). However, they should be used with caution because they may not work as you'd expect.

The following replication filters are honored for [InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb) DML, but not DDL:

* `[binlog_do_db](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options)`
* `[binlog_ignore_db](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options)`
* `[replicate_wild_do_table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables)`
* `[replicate_wild_ignore_table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables)`

The following replication filters are honored for DML and DDL for tables that use both the [InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb) and [MyISAM](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/myisam-storage-engine) storage engines:

* `[replicate_do_table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables)`
* `[replicate_ignore_table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/standard-replication/replication-and-binary-log-system-variables)`

However, it should be kept in mind that if replication filters cause inconsistencies that lead to replication errors, then nodes may abort.

See also [MDEV-421](https://jira.mariadb.org/browse/MDEV-421) and [MDEV-6229](https://jira.mariadb.org/browse/MDEV-6229).

## Network Ports

Galera Cluster needs access to the following ports:

* Standard MariaDB Port (default: 3306) - For MySQL client connections and [State Snapshot Transfers](state-snapshot-transfers-ssts-in-galera-cluster/introduction-to-state-snapshot-transfers-ssts.md) that use the `mysqldump` method. This can be changed by setting `[port](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables#port)`.
* Galera Replication Port (default: 4567) - For Galera Cluster replication traffic, multicast replication uses both UDP transport and TCP on this port. Can be changed by setting `[wsrep_node_address](../reference/galera-cluster-system-variables.md#wsrep_node_address)`.
* Galera Replication Listening Interface (default: `0.0.0.0:4567`) needs to be set using [gmcast.listen\_addr](../reference/wsrep_provider_options.md#gmcastlisten_addr), either
  * in [wsrep\_provider\_options](../reference/galera-cluster-system-variables.md#wsrep_provider_options): `wsrep_provider_options='gmcast.listen_addr=tcp://<IP_ADDR>:<PORT>;'`
  * or in [wsrep\_cluster\_address](../reference/galera-cluster-system-variables.md#wsrep_cluster_address)
* IST Port (default: 4568) - For Incremental State Transfers. Can be changed by setting `[ist.recv_addr](https://galeracluster.com/library/documentation/galera-parameters.html#ist-recv-addr)` in `[wsrep_provider_options](../reference/galera-cluster-system-variables.md#wsrep_provider_options)`.
* SST Port (default: 4444) - For all [State Snapshot Transfer](state-snapshot-transfers-ssts-in-galera-cluster/introduction-to-state-snapshot-transfers-ssts.md) methods other than `mysqldump`. Can be changed by setting `[wsrep_sst_receive_address](../reference/galera-cluster-system-variables.md#wsrep_sst_receive_address)`.

## Mutiple Galera Cluster Instances on One Server

If you want to run multiple Galera Cluster instances on one server, then you can do so by starting each instance with `[mysqld_multi](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysqld_multi)`, or if you are using [systemd](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/systemd), then you can use the relevant [systemd method for interacting with multiple MariaDB instances](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/systemd#interacting-with-multiple-mariadb-server-processes).

You need to ensure that each instance is configured with a different `[datadir](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables#datadir)`.

You also need to ensure that each instance is configured with different [network ports](configuring-mariadb-galera-cluster.md#network-ports).

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
