# MariaDB Connector/R2DBC 1.3.0 Release Notes

## Overview

MariaDB Connector/R2DBC is a non-blocking interface between Java applications and MariaDB Server. MariaDB Connector/R2DBC enables the development of Java 8+ applications for MariaDB database products.

MariaDB Connector/R2DBC 1.3.0 was released on 2024-10-24. This release is of GA (generally available) maturity. It is compatible with MariaDB Connector/R2DBC 1.2 and is the maintenance path for version 1.2. This release is compatible with [R2DBC](https://r2dbc.io/spec/1.0.0.RELEASE/spec/html/) 1.0.0 specification.

## Notable Changes

* Support of the PARSEC Authentication Plugin which is provided starting with MariaDB Server 11.6. See the [PARSEC Authentication Plugin documentation](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-parsec) for more details ([R2DBC-106](https://jira.mariadb.org/browse/R2DBC-106))
  * This requires Java 15+ (to use Java native ed25519 Algorithm implementation). For previous versions of Java, this will require adding BouncyCastle as a dependency.

## Resources

* [Download](https://mariadb.com/downloads/connectors/connectors-data-access/r2dbc-connector/)
* [Documentation](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc)
* [Install MariaDB Connector/R2DBC](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-native-r2dbc-api-of-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc)
* [Install MariaDB Connector/R2DBC with Spring Data](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-spring-data-framework-with-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc-spring-data)
* [Report Issues](https://jira.mariadb.org/browse/R2DBC)
* [Source code](https://github.com/mariadb-corporation/mariadb-connector-r2dbc/)

<sub>_This page is: Copyright © 2025 MariaDB. All rights reserved._</sub>

{% @marketo/form formid="4316" formId="4316" %}
