---
description: MariaDB Galera Cluster Replication quickstart guide
---

# MariaDB Galera Cluster Replication Guide

### Quickstart Guide: About Galera Replication

Galera Replication is a core technology enabling MariaDB Galera Cluster to provide a highly available and scalable database solution. It is characterized by its **virtually synchronous** replication, ensuring strong data consistency across all cluster nodes.

#### 1. What is Galera Replication?

Galera Replication is a **multi-primary replication solution** for database clustering. Unlike traditional asynchronous or semi-synchronous replication, Galera ensures that transactions are committed on all nodes (or fail on all) before the client receives a success confirmation. This mechanism eliminates data loss and minimizes replica lag, making all nodes active and capable of handling read and write operations.

#### 2. How Galera Replication Works

The core of Galera Replication revolves around the concept of **write sets** and the **`wsrep API`**:

* **Write Set Broadcasting:** When a client commits a transaction on any node in the cluster, that node (the "donor" for that specific transaction) captures the changes (the "write set") associated with that transaction. This write set is then **broadcasted to all other nodes** in the cluster.
* **Certification and Application:** Each receiving node performs a "certification" test to ensure that the incoming write set does not conflict with any concurrent transactions being committed locally.
  * If the write set passes certification, it is applied to the local database, and the transaction is committed on that node.
  * If a conflict is detected, the conflicting transaction (usually the one that was executed locally) is aborted, ensuring data consistency across the cluster.
* **Virtually Synchronous:** The term "virtually synchronous" means that while the actual data application might happen slightly after the commit on the initiating node, the commit order is globally consistent, and all successful transactions are guaranteed to be applied on all active nodes. A transaction is not truly considered committed until it has passed certification on all nodes.
* **`wsrep API`:** This API defines the interface between the Galera replication library (the "wsrep provider") and the database server (MariaDB). It allows the database to expose hooks for Galera to capture and apply transaction write sets.

#### 3. Key Characteristics

* **Multi-Primary (Active-Active):** All nodes in a Galera Cluster can be simultaneously used for both read and write operations.
* **Synchronous Replication (Virtual):** Data is consistent across all nodes at all times, preventing data loss upon node failures.
* **Automatic Node Provisioning (SST/IST):** When a new node joins or an existing node rejoins, Galera automatically transfers the necessary state to bring it up to date.
  * **State Snapshot Transfer (SST):** A full copy of the database is transferred from an existing node to the joining node.
  * **Incremental State Transfer (IST):** Only missing write sets are transferred if the joining node is not too far behind.
* **Automatic Membership Control:** Nodes automatically detect and manage cluster membership changes (nodes joining or leaving).

Galera Replication essentially transforms a set of individual MariaDB servers into a robust, highly available, and consistent distributed database system.

#### Further Resources:

* [MariaDB Galera Cluster Guide](https://mariadb.net/docs/galera-cluster/galera-cluster-quickstart-guides/mariadb-galera-cluster-guide)
* [Galera Cluster Documentation (Primary Site)](https://www.google.com/search?q=https://galeracluster.com/documentation/html_docs_galera/galera-overview.html\&authuser=1)
* [MariaDB documentation - Galera Cluster](https://mariadb.com/kb/en/galera-cluster/)
