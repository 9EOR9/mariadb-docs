# MariaDB 5.5.21 Release Notes

The most recent release in the [MariaDB 5.5](broken-reference) series is:[**MariaDB 5.5.68**](mariadb-5568-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/5.5.68/)

[Download](https://downloads.askmonty.org/mariadb/5.5.21) |**Release Notes** |[Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5521-changelog.md) |[Overview of 5.5](broken-reference)

**Release date:** 16 Mar 2012

[MariaDB 5.5.21](mariadb-5521-release-notes.md) is a [_**Beta**_](../../../mariadb-release-criteria.md) release. In general this means that there are no known serious bugs, except for those marked as feature requests. This is the second release of the [MariaDB 5.5](broken-reference) series and includes features left out of the 5.5.20-alpha release, and various bug fixes.

**For a description of** [**MariaDB 5.5**](broken-reference) **see the**[**What is MariaDB 5.5**](broken-reference) **page.**

For a list of changes made in [MariaDB 5.5.21](mariadb-5521-release-notes.md)-beta, with links to detailed\
information on each push, see the[MariaDB 5.5.21 Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5521-changelog.md).

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

**Note:** _There are no RPM packages of_ [_MariaDB 5.5.21_](mariadb-5521-release-notes.md) _available at this time._

## Includes MySQL 5.5.21

This version of MariaDB includes MySQL 5.5.21. See [Changes in MySQL 5.5.21](https://dev.mysql.com/doc/refman/5.5/en/news-5-5-21.html) for what changed between this and previous MySQL versions.

## Security fix

* A fix is included for a COM\_BINLOG\_DUMP crash on invalid data. See [MDEV-3910](https://jira.mariadb.org/browse/MDEV-3910) for details.

## Threadpool

[MariaDB 5.5.21](mariadb-5521-release-notes.md) is the first release to feature the new [threadpool](https://kb.askmonty.org/en/thread-pool-in-mariadb-55). This is comparable in functionality to the closed-source feature in MySQL Enterprise.

Preliminary benchmarks of the new threadpool code are available [here](https://kb.askmonty.org/en/threadpool-benchmarks).

For our Windows users, pool-of-threads is now the default scheduler on Windows Vista (and higher). It is not the default on Linux/Unix yet as we don't feel we have had enough time to thoroughly test various corner cases.

## Updated SphinxSE

[SphinxSE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/sphinx-storage-engine) has been updated to version 2.0.4 (the latest upstream version) in [MariaDB 5.5.21](mariadb-5521-release-notes.md).

## LIMIT ROWS EXAMINED

In 5.5.21 there is a new `LIMIT ROWS EXAMINED` optimization which provides\
the means to terminate the\
execution of `[SELECT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements-and-structure/sql-statements/data-manipulation/selecting-data/select)` statements which examine too many rows, and\
thus use too many resources. This is achieved through an extension of the`[LIMIT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements-and-structure/sql-statements/data-manipulation/selecting-data/select#limit)` clause —`LIMIT ROWS EXAMINED <number_of_rows>`. Whenever possible the\
semantics of `LIMIT ROWS EXAMINED` is the same as that of normal `LIMIT`\
(for instance for aggregate functions).

More information is available on the `[LIMIT ROWS EXAMINED](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/replication-cluster-multi-master/optimization-and-tuning/query-optimizations/limit-rows-examined)` page.

## INSTALL SONAME

[MariaDB 5.5.21](mariadb-5521-release-notes.md) includes a new `INSTALL SONAME` statement. This statement is a variant of [INSTALL PLUGIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/plugin-sql-statements/install-plugin). It installs **all** plugins from a given `plugin_library`.

See the [INSTALL SONAME](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/plugin-sql-statements/install-soname) page for details.

## Extended Keys support for XtraDB and InnoDB

In 5.5.21 there is a new "extended keys" optimization which, when enabled,\
makes use of existing components of InnoDB/XtraDB keys to generate more\
efficient execution plans. Using these components in many cases allows the\
server to generate execution plans which employ index-only look-ups.

See the [Extended Keys](broken-reference) page for more information.

## Non-blocking Client Library

MariaDB, starting with version 5.5.21 supports [non-blocking operations in the client-library](broken-reference). This allows an application to start a query or other operation against the database, and then continue to do other work (in the same thread) while the request is sent over the network, the query is processed in the server, and the result travels back. As parts of the result become ready, the application can — at its leisure — call back into the library to continue processing, repeating this until the operation is completed.

Non-blocking operation is implemented entirely within the client library. This means no special server support is necessary and non-blocking operation works with any version of the MariaDB or MySQL server, the same as the normal blocking API. It also means that it is not possible to have two queries running at the same time on the same connection (this is a protocol limitation). But a single thread can have any number of non-blocking queries running at the same time, each using its own MYSQL connection object.

See [Non-Blocking Client Library](broken-reference) for details.

## mysql\_real\_connect() Changes

In MySQL, and in MariaDB versions before 5.5.21, `mysql_real_connect()`\
removes from the `MYSQL` object any options set with `mysql_option()` when\
it fails. Beginning with [MariaDB 5.5.21](mariadb-5521-release-notes.md), options are preserved by a failing`mysql_real_connect()`; use `mysql_close()`, as normal, to clear them.

This only has effect if the `MYSQL` object is reused after a`mysql_real_connect()` failure (which is unusual). No real-life\
incompatibilities are expected from this change (it is unlikely that an\
application would rely on options being automatically removed between\
connection attempts).

## Selectively skipping replication of binlog events

Normally, all changes that are logged as events in the binlog are also\
replicated to all slaves (though still subject to filtering by`--replicate-do-xxx`, `--replicate-ignore-xxx`,\
and similar options). However, sometimes it may be desirable to have certain\
events be logged into the binlog, but not be replicated to all or a subset of\
slaves, where the distinction between events that should be replicated or not\
is under the control of the application making the changes.

This could be useful if an application does some replication external to the\
server outside of the built-in replication, or if it has some data that should\
not be replicated for whatever reason.

This is possible with two new system variables introduced in [MariaDB 5.5.21](mariadb-5521-release-notes.md): `@@skip_replication` and `--replicate-events-marked-for-skip`.

See [Selectively skipping replication of binlog events](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/selectively-skipping-replication-of-binlog-events) for details.

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
