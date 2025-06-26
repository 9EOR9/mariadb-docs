# MariaDB Connector/R2DBC 1.0.1 Release Notes

## Overview

MariaDB Connector/R2DBC is a non-blocking interface between Java applications and MariaDB Server. MariaDB Connector/R2DBC enables the development of Java 8+ applications for MariaDB database products.

MariaDB Connector/R2DBC 1.0.1 was released on 2021-03-11. This release is compatible with [R2DBC 0.8.4](https://r2dbc.io/spec/0.8.4.RELEASE/spec/html/) specification.

## Notable Changes

* MariaDB Connector/R2DBC now supports R2DBC specification version 0.8.4.

## Issues Fixed

* Ensure autocommit initial state. ([R2DBC-16](https://jira.mariadb.org/browse/R2DBC-16))
* New option autocommit that defaults to true
* Transaction in query flux might not be persisted. ([R2DBC-17](https://jira.mariadb.org/browse/R2DBC-17))
* Data with size bigger than 16Mb correction. ([R2DBC-19](https://jira.mariadb.org/browse/R2DBC-19))

## Resources

* [Download](https://mariadb.com/downloads/connectors/connectors-data-access/r2dbc-connector/)
* [Documentation](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/java-r2dbc-connector/README.md)
* [Install MariaDB Connector/R2DBC](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-native-r2dbc-api-of-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc)
* [Install MariaDB Connector/R2DBC with Spring Data](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-spring-data-framework-with-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc-spring-data)
* [Report Issues](https://jira.mariadb.org/browse/R2DBC)
* [Source code](https://github.com/mariadb-corporation/mariadb-connector-r2dbc/)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
