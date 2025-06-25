# MariaDB 5.3.0 Release Notes

The most recent release in the [MariaDB 5.3 series](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) is:[**MariaDB 5.3.12**](mariadb-5312-release-notes.md)

[Download](https://downloads.askmonty.org/mariadb/5.3.0) |**Release Notes** |[Changelog](../../changelogs/changelogs-mariadb-53-series/mariadb-530-changelog.md) |[Overview of 5.3](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md)

**Release date:** 26 July 2011

[MariaDB 5.3.0](mariadb-530-release-notes.md) is a [Beta release](../../../mariadb-release-criteria.md). In general this means that there are no known serious bugs, except for those marked as feature requests. [MariaDB 5.3](changes-improvements-in-mariadb-5-3.md) radically improves performance for subqueries as well as for joins and single-table queries over large data sets.

**For a detailed description of** [**MariaDB 5.3**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) **see the** [**What is MariaDB 5.3**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) **page.**

For a list of every change made in [MariaDB 5.3.0](mariadb-530-release-notes.md), including the various bugs that were fixed and links to detailed information on each push, see the [MariaDB 5.3.0 Changelog](../../changelogs/changelogs-mariadb-53-series/mariadb-530-changelog.md). These changes are compared against [MariaDB 5.2](../release-notes-mariadb-5-2-series/changes-improvements-in-mariadb-5-2.md), and it is worth noting that [MariaDB 5.3](changes-improvements-in-mariadb-5-3.md) is based on the MySQL 5.1 releases.

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

Be notified of new releases automatically by adding the[releases rss feed](https://montyprogram.com/news/feed/mariadb_releases/) to\
your favorite feed reader or by [subscribing](https://mariadb.org) to the\
announce 'at' mariadb.org announcement list (this is a low traffic,\
announce-only list).

A few highlights (**for a more detailed list, please see the** [**What is MariaDB 5.3**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) **page**) in [MariaDB 5.3.0](mariadb-530-release-notes.md) follow:

## Subquery optimizations

One of the major performance improvements in [MariaDB 5.3.0](mariadb-530-release-notes.md) is that subqueries are finally usable in practice. It is no longer necessary to rewrite subqueries manually into joins or separate queries. The optimizer of [MariaDB 5.3](changes-improvements-in-mariadb-5-3.md) will do this, and more automatically. EXPLAIN for derived tables and materialized views is instantaneous. Both derived tables and views can be optimized by indexes created on the fly.

## Join & disk access optimizations

MariaDB now supports many join optimizations, including utilizing the Block Nested Loop algorithm that can be used for outer joins, Classic Hash Join which can be used for equi-joins, and Batch Key Access joins are supported providing the benefits of ordered retrievals for primary and secondary keys provided by the new implementation of Multi-Range-Read (MRR) optimizations. MariaDB also features Index Condition Pushdown.

## NoSQL-style interfaces

NoSQL is all the rage these days and [MariaDB 5.3.0](mariadb-530-release-notes.md) ships with the [HandlerSocket](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/nosql/handlersocket) plugin.

## Dynamic columns

[Dynamic columns](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/nosql/dynamic-columns) allows you to have a different set of "virtual columns" for each row in your table. You can at any time add or remove columns from a row.

## Group commit for the binary log

[MariaDB 5.3](changes-improvements-in-mariadb-5-3.md) implements group commit which works when using XtraDB with the binary log enabled.

## Microsoft Windows performance improvements

Microsoft Windows performance improvements from MySQL 5.5 have been backported, including benefits to the XtraDB storage engine.

{% @marketo/form formid="4316" formId="4316" %}
