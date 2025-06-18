# Galera Monitor

##

## Designing for MaxScale's Galera Monitor

MaxScale's [Galera Monitor (galeramon)](../../../mariadb-maxscale-23-02/mariadb-maxscale-23-02-monitors/mariadb-maxscale-2302-galera-monitor.md) monitors [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/en/mariadb-galera-cluster-quickstart/README.md) deployments.

This page contains topics that need to be considered when designing applications that use the Galera Monitor.

* [How do I allow SST donors to execute queries](maxscale-mariadb-monitor-usage-galera-monitor.md#using-sst-donors-for-queries-with-maxscales-galera-monitor)?

Additional information is available [here](../../../mariadb-maxscale-25/maxscale-25-monitors/mariadb-maxscale-25-galera-monitor.md).

## Understanding MaxScale's Galera Monitor

MaxScale's [Galera Monitor (galeramon)](../../../mariadb-maxscale-23-02/mariadb-maxscale-23-02-monitors/mariadb-maxscale-2302-galera-monitor.md) monitors [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/en/mariadb-galera-cluster-quickstart/README.md) deployments.

What Does the [Galera Monitor](../../../mariadb-maxscale-23-02/mariadb-maxscale-23-02-monitors/mariadb-maxscale-2302-galera-monitor.md) Support?

The Galera Monitor (galeramon) supports:

* Monitoring [MariaDB Enterprise Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/en/mariadb-galera-cluster-quickstart/README.md) deployments
* Monitoring [MariaDB Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/en/mariadb-galera-cluster-quickstart/README.md) deployments
* Query-based load balancing with the [Read/Write Split Router (readwritesplit)](../../mariadb-maxscale-21-06-routers/readwrite-split-router-usage/understanding-maxscales-readwrite-split-router.md)
* Connection-based load balancing with the Read Connection Router (readconnroute)

### Deploying Galera Monitor

* Deploy MaxScale with Galera Monitor and Read/Write Split Router
* Deploy MaxScale with Galera Monitor and Read Connection Router

## Using SST Donors for Queries with MaxScale's Galera Monitor

MaxScale's [Galera Monitor (galeramon)](../../../mariadb-maxscale-23-02/mariadb-maxscale-23-02-monitors/mariadb-maxscale-2302-galera-monitor.md) monitors [Galera Cluster](https://github.com/mariadb-corporation/docs-server/blob/test/en/mariadb-galera-cluster-quickstart/README.md).

By default, when a node is chosen as a donor for a State Snapshot Transfer (SST), Galera Monitor does not route any queries to it. However, some SST methods are non-blocking on the donor, so this default behavior is not always desired.

### Non-Blocking SST Methods

A cluster's SST method is defined by the [wsrep\_sst\_method](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_sst_method) system variable. When this system variable is set to mariabackup, the cluster uses [MariaDB Backup](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/backing-up-and-restoring-databases/mariabackup) to perform the SST. [MariaDB Backup](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/backing-up-and-restoring-databases/mariabackup) is a non-blocking backup method, so Galera Cluster allows the node to execute queries while acting as the SST donor.

### Configuring Availability of SST Donors

1. Configure the availability of SST donors by configuring the available\_when\_donor parameter for the Galera Monitor in maxscale.cnf.

For example:

```
[galera-cluster]
type                     = monitor
module                   = galeramon
...
available_when_donor     = true
```

2. Restart the MaxScale instance.

```
$ sudo systemctl restart maxscale
```

{% @marketo/form formId="4316" %}
