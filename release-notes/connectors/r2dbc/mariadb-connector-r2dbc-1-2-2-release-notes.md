# MariaDB Connector/R2DBC 1.2.2 Release Notes

## Overview

MariaDB Connector/R2DBC is a non-blocking interface between Java applications and MariaDB Server. MariaDB Connector/R2DBC enables the development of Java 8+ applications for MariaDB database products.

MariaDB Connector/R2DBC 1.2.2 was released on 2024-09-13. This release is of GA (generally available) maturity. It is compatible with MariaDB Connector/R2DBC 1.1 and is the maintenance path for version 1.1. This release is compatible with R2DBC 1.0.0 specification.

## Notable Changes

* To support the R2DBC 0.9.1 specification (used by Spring Boot 2.7) the maven artifact org.mariadb:r2dbc-mariadb-SPEC-0.9.1 has been added ([R2DBC-103](https://jira.mariadb.org/browse/R2DBC-103))
  * The artifact will be maintained until enterprise support ends for Spring boot 2.7
* A new option, skipPostCommands, permits disabling initial connection settings, and indicating that commands after connections must be skipped. This allows avoiding unnecessary commands on connection creation and, when using RDS proxy to not have session pinning. ([R2DBC-105](https://jira.mariadb.org/browse/R2DBC-105))
  * This option has to be used with care, because the connector expects the server to have:
    * Connection exchanges to be UTF8(mb3/mb4)
    * Autocommit set to true
    * Transaction isolation defaulting to REPEATABLE-READ
  * This option can only be enabled if the server's global options correspond to these defaults.

## Issues Fixed

When using connection redirection, error "Connection is closed. Cannot send anything" might be returned. ([R2DBC-104](https://jira.mariadb.org/browse/R2DBC-104))

## Resources

* [Download](https://mariadb.com/downloads/connectors/connectors-data-access/r2dbc-connector/)
* [Documentation](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/java-r2dbc-connector/README.md)
* [Install MariaDB Connector/R2DBC](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-native-r2dbc-api-of-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc)
* [Install MariaDB Connector/R2DBC with Spring Data](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-spring-data-framework-with-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc-spring-data)
* [Report Issues](https://jira.mariadb.org/browse/R2DBC)
* [Source code](https://github.com/mariadb-corporation/mariadb-connector-r2dbc/)

<sub>_This page is: Copyright © 2025 MariaDB. All rights reserved._</sub>

{% @marketo/form formid="4316" formId="4316" %}
