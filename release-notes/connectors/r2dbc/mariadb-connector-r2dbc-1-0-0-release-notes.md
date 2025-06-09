# MariaDB Connector/R2DBC 1.0.0 Release Notes

## Overview

MariaDB Connector/R2DBC is a non-blocking interface between Java applications and MariaDB Server. MariaDB Connector/R2DBC enables the development of Java 8+ applications for MariaDB database products.

MariaDB Connector/R2DBC 1.0.0 was released on 2020-12-11. It is the first generally available (GA) release of MariaDB Connector/R2DBC. This release is compatible with [R2DBC 0.8.3](https://r2dbc.io/spec/0.8.3.RELEASE/spec/html/) specification.

## Notable Changes

* MariaDB Connector/R2DBC now supports R2DBC specification version 0.8.3.

## Issues Fixed

* Connector releases row before client use. ([R2DBC-14](https://jira.mariadb.org/browse/R2DBC-14))
* Row buffer reading position is sometimes incorrect.
* Retained buffer is not released. ([R2DBC-12](https://jira.mariadb.org/browse/R2DBC-12))
* Batching on statement use parameters is not added. ([R2DBC-11](https://jira.mariadb.org/browse/R2DBC-11))

## Resources

* [Download](https://mariadb.com/downloads/connectors/connectors-data-access/r2dbc-connector/)
* [Documentation](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/java-r2dbc-connector/README.md)
* [Install MariaDB Connector/R2DBC](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-native-r2dbc-api-of-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc)
* [Install MariaDB Connector/R2DBC with Spring Data](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-spring-data-framework-with-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc-spring-data)
* [Report Issues](https://jira.mariadb.org/browse/R2DBC)
* [Source code](https://github.com/mariadb-corporation/mariadb-connector-r2dbc/)

Copyright © 2025 MariaDB
