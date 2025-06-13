# Understanding Monitors in MaxScale

In MariaDB MaxScale, monitors perform the following tasks:

* Deciding whether a server is up or down.
* Deciding whether a server is the primary server or a replica server.
* Performing automatic failover when the primary server fails (for certain kinds of deployments).

## Monitors Supported by MaxScale

MaxScale supports different monitors for different kinds of deployments:

| Deployment Type                                                                                               | Monitor                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Deployment Type                                                                                               | Monitor                                                                                                                   |
| [MariaDB Replication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication) | [MariaDB Monitor (mariadbmon)](maxscale-mariadb-monitor-usage-mariadb-monitor/understanding-maxscales-mariadb-monitor.md) |
| [Galera Cluster](../../../../../en/mariadb-galera-cluster-quickstart/)                                        | [Galera Monitor (galeramon)](maxscale-mariadb-monitor-usage-galera-monitor.md#understanding-maxscales-galera-monitor)     |
| [Multi-Node Enterprise ColumnStore](../../../../../en/mariadb-columnstore/)                                   | MariaDB Monitor (mariadbmon)                                                                                              |
| ColumnStore 1.2                                                                                               | ColumnStore Monitor (csmon)                                                                                               |
| Xpand                                                                                                         | [Xpand Monitor (xpandmon)](../../../../../en/mariadb-maxscale-2208-xpand-monitor/)                                        |
| Amazon Aurora                                                                                                 | Aurora Monitor (auroramon)                                                                                                |

<sub>_This page is: Copyright © 2025 MariaDB. All rights reserved._</sub>

{% @marketo/form formId="4316" %}
