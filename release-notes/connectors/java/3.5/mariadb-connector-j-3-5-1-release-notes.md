# MariaDB Connector/J 3.5.1 Release Notes

{% include "../../../.gitbook/includes/latest-java.md" %}

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/java8-connector)[Release Notes](mariadb-connector-j-3-5-1-release-notes.md)[Changelog](../changelogs/3.5/mariadb-connector-j-3-5-1-changelog.md)[Connector/J Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-j/README.md)

**Release date:** 20 Nov 2024

MariaDB Connector/J 3.5.1 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

**For an overview of MariaDB Connector/J see the**[**About MariaDB Connector/J**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-j/README.md) **page**

The MariaDB Connector/J 3.5 release series is replacing the maintenance releases for the 3.4 release series, as the new release series is fully compatible with 3.4.

## Notable changes

### PARSEC Authentication - [CONJ-1193](https://jira.mariadb.org/browse/CONJ-1193)

Support of the PARSEC Authentication Plugin which is provided starting with MariaDB Server 11.6. See [parsec](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-parsec) documentation for more details.

This requires java 15+ (to use java native ed25519 Algorithm implementation). For previous versions of java, this will require adding BouncyCastle as dependency.

_While initially documented in 3.5.0, this feature was not in the released version._

### New High Availability Mode With Loadbalancing For Reads - [CONJ-1207](https://jira.mariadb.org/browse/CONJ-1207)

When running a multi-master cluster (i.e. MariaDB Cluster with Galera), writing to more than one node can lead to optimistic locking errors ("deadlocks") in some use cases. Writing concurrently to multiple nodes also doesn't result in performance improvements, due to having to synchronously replicate to all nodes.\
The new high availability mode “Load-balance-read” permits the use of masters in a failover manner (try first master, the next one if the first master fails) while distributing the load on replicas.

Example of connection string:

```java
jdbc:mariadb:load-balance-read://127.0.0.5,127.0.0.6,address=(host=127.0.0.7)(type=replica),address=(host=127.0.0.8)(type=replica)/DB
```

Equivalent of:

```java
jdbc:mariadb:load-balance-read://address=(host=127.0.0.5)(type=primary),address=(host=127.0.0.6)(type=primary),address=(host=127.0.0.7)(type=replica),address=(host=127.0.0.8)(type=replica)/DB
```

In the example the hosts 127.0.0.5, 127.0.0.6 will be used for writes, in a failover manner. 127.0.0.6,127.0.0.7 are of type replica, read load balancing will be used.

### Permit bulk for INSERT ON DUPLICATE KEY UPDATE commands for 11.5.1+ servers - [CONJ-1208](https://jira.mariadb.org/browse/CONJ-1208)

Since [MDEV-30366](https://jira.mariadb.org/browse/MDEV-30366), the server can return appropriate detailed answers. This was implemented, but not for specific INSERT ON DUPLICATE KEY UPDATE commands.

## Bugs Fixed

* [CONJ-1053](https://jira.mariadb.org/browse/CONJ-1053) waffle-jna dependency is not declared optional in the module description
* [CONJ-1196](https://jira.mariadb.org/browse/CONJ-1196) setObject on java.util.Date is en/decode as java.sql.Date and truncates hour/minutes/seconds/ms while it must be en/decode like a java.sql.Timestamp
* [CONJ-1211](https://jira.mariadb.org/browse/CONJ-1211) JDBC 4.3 enquoteIdentifier missing validation
  * An identifier containing only number must be quoted, even if `alwaysQuote` parameter is set to false
  * Length validation must be done (< 64 characters).
* [CONJ-1213](https://jira.mariadb.org/browse/CONJ-1213) SQL commands ending with semicolon and trailing space are not using bulk

## Changelog

For a complete list of changes made in MariaDB Connector/J 3.5.1, with links to detailed\
information on each push, see the [changelog](../changelogs/3.5/mariadb-connector-j-3-5-1-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
