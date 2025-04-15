
# MaxScale 25.01 Contents

# Contents


## About MariaDB MaxScale


* [About MariaDB MaxScale](mariadb-maxscale-25-01-about/mariadb-maxscale-2501-maxscale-2501-about-mariadb-maxscale.md)
* [Changelog](mariadb-maxscale-2501-maxscale-2501-changelog.md)
* [Limitations](mariadb-maxscale-25-01-about/mariadb-maxscale-2501-maxscale-2501-limitations-and-known-issues-within-mariadb-maxscale.md)


## Getting Started


* [MariaDB MaxScale Installation Guide](mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-installation-guide.md)
* [Building MariaDB MaxScale from Source Code](mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-building-mariadb-maxscale-from-source-code.md)
* [Configuration Guide](mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-configuration-guide.md)
* [MaxGUI](mariadb-maxscale-25-01-getting-started/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-maxgui-guide.md)


## Upgrading MariaDB MaxScale


* [Upgrading MaxScale](mariadb-maxscale-25-01-upgrading/mariadb-maxscale-2501-maxscale-2501-upgrading-mariadb-maxscale.md)


## Reference


* [Hardening](mariadb-maxscale-25-01-reference/mariadb-maxscale-2501-maxscale-2501-securing-your-maxscale-deployment.md)
* [MaxCtrl - Command Line Admin Interface](mariadb-maxscale-25-01-reference/mariadb-maxscale-2501-maxscale-2501-maxctrl.md)
* [MaxScale REST API](mariadb-maxscale-25-01-rest-api/mariadb-maxscale-2501-maxscale-2501-rest-api.md)
* [Module Commands](mariadb-maxscale-25-01-reference/mariadb-maxscale-2501-maxscale-2501-module-commands.md)
* [Routing Hints](mariadb-maxscale-25-01-reference/mariadb-maxscale-2501-maxscale-2501-hint-syntax.md)
* [Settings](mariadb-maxscale-25-01-reference/mariadb-maxscale-2501-maxscale-2501-configuration-settings.md)


## Tutorials


The main tutorial for MariaDB MaxScale consist of setting up MariaDB MaxScale for the environment you are using with either a connection-based or a read/write-based configuration.


* [MariaDB MaxScale Tutorial](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-setting-up-mariadb-maxscale.md)


These tutorials are for specific use cases and module combinations.


* [Administration Tutorial](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-mariadb-maxscale-administration-tutorial.md)
* [Avro Router Tutorial](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-avrorouter-tutorial.md)
* [Connection Routing Tutorial](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-connection-routing-with-mariadb-maxscale.md)
* [Filter Tutorial](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-filters.md)
* [MariaDB Monitor Failover Tutorial](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-automatic-failover-with-mariadb-monitor.md)
* [Read Write Splitting Tutorial](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-read-write-splitting-with-mariadb-maxscale.md)
* [Simple Schema Sharding Tutorial](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-schemarouter-simple-sharding-with-two-servers.md)


Here are tutorials on monitoring and managing MariaDB MaxScale in cluster environments.


* [REST API Tutorial](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-rest-api-tutorial.md)


## Routers


The routing module is the core of a MariaDB MaxScale service. The router documentation
contains all module specific configuration options and detailed explanations
of their use.


* [Avrorouter](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-avrorouter-tutorial.md)
* [Binlogrouter](mariadb-maxscale-25-01-routers/mariadb-maxscale-2501-maxscale-2501-binlogrouter.md)
* [Cat](mariadb-maxscale-25-01-routers/mariadb-maxscale-2501-maxscale-2501-cat.md)
* [Diff](mariadb-maxscale-25-01-routers/mariadb-maxscale-2501-maxscale-2501-diff-router-for-comparing-servers.md)
* [KafkaCDC](mariadb-maxscale-25-01-routers/mariadb-maxscale-2501-maxscale-2501-kafkacdc.md)
* [KafkaImporter](mariadb-maxscale-25-01-routers/mariadb-maxscale-2501-maxscale-2501-kafkaimporter.md)
* [MirrorRouter](mariadb-maxscale-25-01-routers/mariadb-maxscale-2501-maxscale-2501-mirror.md)
* [Read Connection Router](mariadb-maxscale-25-01-routers/mariadb-maxscale-2501-maxscale-2501-readconnroute.md)
* [Read Write Split](mariadb-maxscale-25-01-routers/mariadb-maxscale-2501-maxscale-2501-readwritesplit.md)
* [Schemarouter](mariadb-maxscale-25-01-tutorials/mariadb-maxscale-2501-maxscale-2501-schemarouter-simple-sharding-with-two-servers.md)
* [SmartRouter](mariadb-maxscale-25-01-routers/mariadb-maxscale-2501-maxscale-2501-smartrouter.md)


## Filters


Here are detailed documents about the filters MariaDB MaxScale offers. They contain configuration guides and example use cases. Before reading these, you should have read the filter tutorial so that you know how they work and how to configure them.


* [Binlog Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-binlog-filter.md)
* [Cache](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-cache.md)
* [Comment Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-comment-filter.md)
* [Consistent Critical Read Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-consistent-critical-read-filter.md)
* [Hint Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-hintfilter.md)
* [LDIFilter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-ldi-filter.md)
* [Luafilter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-lua-filter.md)
* [Masking Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-masking.md)
* [Maxrows Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-maxrows.md)
* [Named Server Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-named-server-filter.md)
* [Prepared Statement Reuse Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-psreuse.md)
* [Optimistic Transaction Execution Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-optimistic-transaction-execution-filter.md)
* [Query Log All](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-query-log-all-filter.md)
* [Regex Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-regex-filter.md)
* [Rewrite Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-rewrite-filter.md)
* [Tee Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-tee-filter.md)
* [Throttle Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-throttle.md)
* [Top N Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-top-filter.md)
* [Transaction Performance Monitoring Filter](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-transaction-performance-monitoring-filter.md)
* [Wcar](mariadb-maxscale-25-01-filters/mariadb-maxscale-2501-maxscale-2501-workload-capture-and-replay.md)


## Monitors


Common options for all monitor modules.


* [Monitor Common](mariadb-maxscale-2501-maxscale-25-01-monitors/mariadb-maxscale-2501-maxscale-2501-common-monitor-parameters.md)


Module specific documentation.


* [Galera Monitor](mariadb-maxscale-2501-maxscale-25-01-monitors/mariadb-maxscale-2501-maxscale-2501-galera-monitor.md)
* [MariaDB Monitor](mariadb-maxscale-2501-maxscale-25-01-monitors/mariadb-maxscale-2501-maxscale-2501-mariadb-monitor.md)


## Protocols


Documentation for MaxScale protocol modules.


* [MariaDB](mariadb-maxscale-25-01-protocols/mariadb-maxscale-2501-maxscale-2501-mariadb-protocol-module.md)
* [Change Data Capture (CDC) Protocol](mariadb-maxscale-25-01-protocols/mariadb-maxscale-2501-maxscale-2501-change-data-capture-cdc-protocol.md)
* [Change Data Capture (CDC) Users](mariadb-maxscale-25-01-protocols/mariadb-maxscale-2501-maxscale-2501-change-data-capture-cdc-users.md)
* [NoSQL](mariadb-maxscale-25-01-protocols/mariadb-maxscale-2501-maxscale-2501-nosql-protocol-module.md)


The MaxScale CDC Connector provides a C++ API for consuming data from a CDC system.


* [CDC Connector](mariadb-maxscale-25-01-connectors/mariadb-maxscale-2501-maxscale-2501-maxscale-cdc-connector.md)


## Authenticators


A short description of the authentication module type can be found in the
[Authentication Modules](mariadb-maxscale-25-01-authenticators/mariadb-maxscale-2501-maxscale-2501-authentication-modules.md)
document.


* [MariaDB/MySQL Authenticator](mariadb-maxscale-25-01-authenticators/mariadb-maxscale-2501-maxscale-2501-mariadbmysql-authenticator.md)
* [GSSAPI Authenticator](mariadb-maxscale-25-01-authenticators/mariadb-maxscale-2501-maxscale-2501-gssapi-client-authenticator.md)
* [PAM Authenticator](mariadb-maxscale-25-01-authenticators/mariadb-maxscale-2501-maxscale-2501-pam-authenticator.md)
* [Ed25519 Authenticator](mariadb-maxscale-25-01-authenticators/mariadb-maxscale-2501-maxscale-2501-ed25519-authenticator.md)
