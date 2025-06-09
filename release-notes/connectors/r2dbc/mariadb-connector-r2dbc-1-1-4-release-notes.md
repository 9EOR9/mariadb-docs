# MariaDB Connector/R2DBC 1.1.4 Release Notes

## Overview

MariaDB Connector/R2DBC is a non-blocking interface between Java applications and MariaDB Server. MariaDB Connector/R2DBC enables the development of Java 8+ applications for MariaDB database products.

MariaDB Connector/R2DBC 1.1.4 was released on 2023-03-27. This release is of GA (generally available) maturity. This release is compatible with [R2DBC 1.0.0](https://r2dbc.io/spec/1.0.0.RELEASE/spec/html/) specification.

## Notable Changes

* When MariaDB Connector/R2DBC 1.1.4 connects to a pre-existing TLS tunnel, host verification can be disabled. ([R2DBC-80](https://jira.mariadb.org/browse/R2DBC-80))
  * The behavior can be configured using the [sslTunnelDisableHostVerification Connection Parameter](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/mariadb-connector-r2dbc-connection-parameters), which defaults to false.
  * When the sslMode connection parameter is set to [SslMode.TUNNEL](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/mariadb-connector-r2dbc-connection-parameters), host verification can be disabled by setting sslTunnelDisableHostVerification to true.
  * For example:

```java
try {
     // Configure the Connection
     MariadbConnectionConfiguration conf = MariadbConnectionConfiguration.builder()
             .host("192.0.2.1")
             .port(8880) // tunnel port
             .username("db_user")
             .password("db_user_password")
             .database("test")
             .sslMode(SslMode.TUNNEL)
             .sslContextBuilderCustomizer(
                     sslContextBuilder -> sslContextBuilder
                             .protocols("TLSv1.3")
                             .keyManager(new File("/path/to/client/cert"), new File("/path/to/client/key")))
             .sslTunnelDisableHostVerification(true)
             .build();

     // Instantiate a Connection Factory
     MariadbConnectionFactory connFactory = new MariadbConnectionFactory(conf);

     MariadbConnection connection = connFactory.create().block();
     connection.close().block();

 } catch (java.lang.IllegalArgumentException e) {
     System.err.println("Issue encountered while getting connection");
     e.printStackTrace();
 }
```

* When the [useServerPrepStmts connection parameter](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/mariadb-connector-r2dbc-connection-parameters) is enabled, prepared statements can use the text protocol. ([R2DBC-85](https://jira.mariadb.org/browse/R2DBC-85))
  * To use the text protocol in this scenario, prefix the query string with /_text_/ when creating the prepared statement.
  * For example, to use the text protocol with the native R2DBC API:

```java
connection
     .createStatement("/*text*/ call some_proc(?)")
     .bind(0, "connr2dbc_user@example.edu")
     .execute()
     .flatMap(...);
```

*
  * Or to use the text protocol with Spring Data:

```java
@Query("/*text*/ call some_proc(:emailparam)")
List<User> findUsersWithEmailAddress(@Param("emailparam") String emailParam);
```

* MariaDB Connector/R2DBC 1.1.4 adds support for decoding TIMESTAMP and DATE "zero" date values ('0000-00-00') from MariaDB Xpand. ([R2DBC-83](https://jira.mariadb.org/browse/R2DBC-83))
  * In previous releases, when the connector received a "zero" date value from Xpand, the value could not be decoded and the following error would be raised:

```
wrong month 0
```

## Issues Fixed

* When the [useServerPrepStmts connection parameter](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/mariadb-connector-r2dbc-connection-parameters) is enabled, MEDIUMINT values are not properly decoded. ([R2DBC-76](https://jira.mariadb.org/browse/R2DBC-76))
  * In Connector/R2DBC 1.1.2 and 1.1.3, when the binary protocol is used, the last byte of a MEDIUMINT value is not read from a result-set, so remaining values from the same row are read incorrectly.
* When the Statement.returnGeneratedValues() method is called when connected to a version of MariaDB Server prior to 10.5, an error is raised. ([R2DBC-77](https://jira.mariadb.org/browse/R2DBC-77))
  * In previous releases, the following error would be raised:

```
Cannot invoke "Object.getClass()" because "obj" is null
```

* MariaDB Connector/R2DBC's internal statement parser improperly classifies user-defined variables in SELECT statements as named statement parameters. ([R2DBC-79](https://jira.mariadb.org/browse/R2DBC-79))
  * In previous releases, the @amount token in the query below would be classified as a named statement parameter, instead of a user-defined variable.

```sql
SELECT @amount := 10;
```

* Since a statement parameter does not exist with that name, the following error would be raised:

```
java.lang.IllegalStateException: Parameter at position 0 is not set.
```

* Starting with this release, the internal statement parser can distinguish between user-defined variables and named statement parameters.
* When a ConnectionFactory is used to construct a connection string from a ConnectionFactoryOptions instance, the restrictedAuth, rsaPublicKey, cachingRsaPublicKey, and allowPublicKeyRetrieval connection parameters are not properly parsed. ([R2DBC-81](https://jira.mariadb.org/browse/R2DBC-81))
* When a server does not advertise the CLIENT\_SESSION\_TRACK capability (such as old versions of MariaDB Server, MySQL, and MariaDB Xpand), the MariadbConnection.getTransactionIsolationLevel() and MariadbConnection.setTransactionIsolationLevel(IsolationLevel isolationLevel) methods do not properly get or set the transaction isolation level. ([R2DBC-82](https://jira.mariadb.org/browse/R2DBC-82))

## Resources

* [Download](https://mariadb.com/downloads/connectors/connectors-data-access/r2dbc-connector/)
* [Documentation](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/java-r2dbc-connector/README.md)
* [Install MariaDB Connector/R2DBC](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/native-r2dbc-api/install-mariadb-connector-r2dbc)
* [Install MariaDB Connector/R2DBC with Spring Data](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-r2dbc/spring-data-framework/install-mariadb-connector-r2dbc-spring-data)
* [Report Issues](https://jira.mariadb.org/browse/R2DBC)
* [Source code](https://github.com/mariadb-corporation/mariadb-connector-r2dbc/)

Copyright © 2025 MariaDB

{% @marketo/form formid="4316" formId="4316" %}
