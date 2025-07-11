# MariaDB MaxScale

* Q: What is MariaDB MaxScale and its function in a database architecture?\
  A: MariaDB MaxScale is an advanced database proxy, intelligent query router, and robust load balancer developed by MariaDB plc. It operates as an intermediary layer between client applications and MariaDB database servers, providing significantly enhanced scalability, high availability, security, and overall manageability for the database infrastructure.
* Q: What are the core functionalities and features of MariaDB MaxScale?\
  A: Core functionalities of MariaDB MaxScale include automatic database failover management, efficient read-write splitting for optimizing workloads, intelligent connection routing based on various criteria (such as query type, username, or regular expressions), comprehensive query filtering and logging, schema-based sharding capabilities, Change Data Capture (CDC) for data streaming, and a powerful database firewall for enhanced security.
* Q: How does MariaDB MaxScale improve database high availability and resilience?\
  A: MariaDB MaxScale continuously monitors the health and status of backend database servers (e.g., a MariaDB Enterprise Cluster or a primary/replica replication setup). In the event of a primary server failure, MaxScale can automatically promote a replica to become the new primary or seamlessly switch traffic to another available master in a cluster, thereby minimizing downtime for connected applications.
* Q: What is the licensing model for MariaDB MaxScale? Is it open source?\
  A: MariaDB MaxScale is distributed under the Business Source License (BSL) 1.1. The BSL allows free usage of MaxScale with up to two MariaDB backend database servers. For deployments involving more than two backend servers, or for certain commercial uses restricted by the BSL, a commercial subscription from MariaDB plc is necessary. Code licensed under BSL typically converts to an open-source license (like GPL) after a defined period, usually three years.
* Q: Can MariaDB MaxScale be used effectively with databases other than MariaDB?\
  A: While MariaDB MaxScale is primarily designed, optimized, and tested for use with MariaDB Server and its various configurations (like MariaDB Enterprise Cluster and MariaDB Xpand), its underlying architecture allows it to potentially support other databases that are compliant with the MySQL network protocol. However, its most advanced features and integrations are best leveraged when used in conjunction with MariaDB databases.

{% @marketo/form formId="4316" %}
