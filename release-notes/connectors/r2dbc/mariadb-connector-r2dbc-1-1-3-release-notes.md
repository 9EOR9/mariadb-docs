# MariaDB Connector/R2DBC 1.1.3 Release Notes

## Overview

MariaDB Connector/R2DBC is a non-blocking interface between Java applications and MariaDB Server. MariaDB Connector/R2DBC enables the development of Java 8+ applications for MariaDB database products.

MariaDB Connector/R2DBC 1.1.3 was released on 2022-12-23. This release is of GA (generally available) maturity. This release is compatible with [R2DBC 1.0.0](https://r2dbc.io/spec/1.0.0.RELEASE/spec/html/) specification.

## Notable Changes

* To support the R2DBC 1.0.0 specification, the following implementation has been added or changed:
  * Result.getRowsUpdated() now returns Mono. Prior to this release, Result.getRowsUpdated() returned Mono.
* The default Netty hostname verifier is now used. Prior to this release, a custom hostname verifier was used. ([R2DBC-74](https://jira.mariadb.org/browse/R2DBC-74))
* Add SSL Tunnel mode:
  * New sslMode option tunnel (or TUNNEL) enables use of a preexisting SSL tunnel. ([R2DBC-69](https://jira.mariadb.org/browse/R2DBC-69))
  * New option sslContextBuilderCustomizer supports customizing SSL Context Builder. ([R2DBC-69](https://jira.mariadb.org/browse/R2DBC-69))

## Issues Fixed

* When subscriber cancellation occurs before the response ends, the connection might stall. ([R2DBC-68](https://jira.mariadb.org/browse/R2DBC-68))
* When a query returns a multi-row resultset, an IllegalReferenceCountException exception occurs in the TextRowDecoder.setPosition() call. ([R2DBC-65](https://jira.mariadb.org/browse/R2DBC-65))
* SSL host name verification does not properly close the socket when verification fails. An error is returned for SSL host name, and the connector fails with a socket close error. ([R2DBC-70](https://jira.mariadb.org/browse/R2DBC-70))
* When a connection error occurs, the connection is not always properly closed. ([R2DBC-71](https://jira.mariadb.org/browse/R2DBC-71))
* Pipelining PREPARE + EXECUTE can result in a buffer leak when PREPARE fails. ([R2DBC-73](https://jira.mariadb.org/browse/R2DBC-73))
* When a socket unexpectedly closes, parameters that are transformed as Byte Buffer may not be released. This causes the following error when setting the Netty error to the maximum. ([R2DBC-72](https://jira.mariadb.org/browse/R2DBC-72))

```
LEAK: ByteBuf.release() was not called before it's garbage-collected.
```

* During failover, the redo buffer is not released before it is garbage collected. ([R2DBC-75](https://jira.mariadb.org/browse/R2DBC-75))

## Resources

* [Download](https://mariadb.com/downloads/connectors/connectors-data-access/r2dbc-connector/)
* [Documentation](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/java-r2dbc-connector/README.md)
* [Install MariaDB Connector/R2DBC](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-native-r2dbc-api-of-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc)
* [Install MariaDB Connector/R2DBC with Spring Data](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/using-the-spring-data-framework-with-mariadb-connector-r2dbc/install-mariadb-connector-r2dbc-spring-data)
* [Report Issues](https://jira.mariadb.org/browse/R2DBC)
* [Source code](https://github.com/mariadb-corporation/mariadb-connector-r2dbc/)

Copyright © 2025 MariaDB
