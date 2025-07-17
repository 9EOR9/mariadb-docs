# Connector/R2DBC 1.2.0 Release Notes

## Overview

MariaDB Connector/R2DBC is a non-blocking interface between Java applications and MariaDB Server. MariaDB Connector/R2DBC enables the development of Java 8+ applications for MariaDB database products.

MariaDB Connector/R2DBC 1.2.0 was released on 2024-02-23. This release is of GA (generally available) maturity. It is compatible with MariaDB Connector/R2DBC 1.1 and will therefore also be the maintenance path for version 1.1. This release is compatible with [R2DBC 1.0.0](https://r2dbc.io/spec/1.0.0.RELEASE/spec/html/) specification.

## Notable Changes

* New timezone option ([R2DBC-93](https://jira.mariadb.org/browse/R2DBC-93))
  * The new timezone option can have 3 types of values:
    * disabled (default) : connector doesn't change timezone
    * auto : connector will set timezone connection variable to java default timezone
    * : connector will set connection variable to the specified timezone. Compared to auto, this avoids having some additional exchange with the server at connection creation
    * Examples:

r2dbc:mariadb://user:pwd@localhost:3306/db?timezone=+5:00r2dbc:mariadb://user:pwd@localhost:3306/db?timezone=autor2dbc:mariadb://user:pwd@localhost:3306/db?timezone=America/New\_York

* The recommended setting for timezone is auto.
* Add support for connection redirection ([R2DBC-66](https://jira.mariadb.org/browse/R2DBC-66))
  * With MariaDB Community Server 11.3.1 a new global variable redirect\_url value has been added, supported format:

```
{mariadb/mysql}://[<user>[:<password>]@]<host>[:<port>]/
```

* When set, all existing connections will be redirected to the designated URL values when appropriate. A connection will only be redirected when no transaction is active.
* Example for enabling the redirection:

```sql
SET @@global.redirect_url="mariadb://somehost:3306/"
```

* The redirection feature is enabled by default. It can be disabled by setting the new option permitRedirect to FALSE, which will result in ignoring the redirection URL.

## Issues Fixed

* Properly end connection (in place of RST TCP packet) ([R2DBC-92](https://jira.mariadb.org/browse/R2DBC-92))
* Failover High availability mode r2dbc:mariadb:\[sequential|loadbalancing]:... wrongly parsed ([R2DBC-86](https://jira.mariadb.org/browse/R2DBC-86))
* Compatibility with [mariadb 11.1.1](../../community-server/old-releases/release-notes-mariadb-11-1-series/mariadb-11-1-1-release-notes.md) ([R2DBC-87](https://jira.mariadb.org/browse/R2DBC-87))
* Java 8 compatibility regression ([R2DBC-88](https://jira.mariadb.org/browse/R2DBC-88))
* Ensure respecting server collation ([R2DBC-91](https://jira.mariadb.org/browse/R2DBC-91))
* Session tracking wrong implementation when multiple system variable changes ([R2DBC-94](https://jira.mariadb.org/browse/R2DBC-94))

## Resources

* [Download](https://mariadb.com/downloads/connectors/connectors-data-access/r2dbc-connector/)
* [Documentation](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/java-r2dbc-connector/README.md)
* [Install MariaDB Connector/R2DBC](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/native-r2dbc-api/install-mariadb-connector-r2dbc)
* [Install MariaDB Connector/R2DBC with Spring Data](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/spring-data-framework/install-mariadb-connector-r2dbc-spring-data)
* [Report Issues](https://jira.mariadb.org/browse/R2DBC)
* [Source code](https://github.com/mariadb-corporation/mariadb-connector-r2dbc/)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
