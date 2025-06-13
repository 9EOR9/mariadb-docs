# MariaDB Connector/R2DBC 1.2.1 Release Notes

## Overview

MariaDB Connector/R2DBC is a non-blocking interface between Java applications and MariaDB Server. MariaDB Connector/R2DBC enables the development of Java 8+ applications for MariaDB database products.

MariaDB Connector/R2DBC 1.2.1 was released on 2024-06-24. This release is of GA (generally available) maturity. It is compatible with MariaDB Connector/R2DBC 1.1 and is the maintenance path for version 1.1. This release is compatible with [R2DBC 1.0.0](https://r2dbc.io/spec/1.0.0.RELEASE/spec/html/) specification.

## Notable Changes

* Adding missing UUID Object support ([R2DBC-96](https://mariadb.com/))

## Issues Fixed

* NPE if No HaMode provided ([R2DBC-97](https://mariadb.com/))
* Correcting possible bug connecting if project contain a project.properties file ([R2DBC-98](https://mariadb.com/))
* No encoding set for ByteBuffer parameter ([R2DBC-99](https://mariadb.com/))
* Wrong default return type for MySQL JSON fields ([R2DBC-101](https://mariadb.com/))
* Avoid netty unneeded dependencies ([R2DBC-102](https://mariadb.com/))

## Resources

* [Download](https://mariadb.com/downloads/connectors/connectors-data-access/r2dbc-connector/)
* [Documentation](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/java-r2dbc-connector/README.md)
* [Install MariaDB Connector/R2DBC](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-native-r2dbc-api-of-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc)
* [Install MariaDB Connector/R2DBC with Spring Data](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-spring-data-framework-with-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc-spring-data)
* [Report Issues](https://jira.mariadb.org/browse/R2DBC)
* [Source code](https://github.com/mariadb-corporation/mariadb-connector-r2dbc/)

<sub>_This page is: Copyright © 2025 MariaDB. All rights reserved._</sub>

{% @marketo/form formid="4316" formId="4316" %}
