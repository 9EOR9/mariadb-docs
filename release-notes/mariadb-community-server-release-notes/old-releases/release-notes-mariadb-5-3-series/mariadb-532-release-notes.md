# MariaDB 5.3.2 Release Notes

The most recent release in the [MariaDB 5.3 series](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) is:[**MariaDB 5.3.12**](mariadb-5312-release-notes.md)

[Download](https://downloads.askmonty.org/mariadb/5.3.2) |**Release Notes** |[Changelog](../../../changelogs/changelogs-mariadb-53-series/mariadb-532-changelog.md) |[Overview of 5.3](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md)

**Release date:** 14 Oct 2011

[MariaDB 5.3.2](mariadb-532-release-notes.md) is a [Beta release](../../../mariadb-release-criteria.md). In general this means\
that there are no known serious bugs, except for those marked as feature\
requests. [MariaDB 5.3](changes-improvements-in-mariadb-5-3.md) radically improves performance for subqueries as well as\
for joins and single-table queries over large data sets.

**For a detailed description of** [**MariaDB 5.3**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) **see the** [**What is MariaDB 5.3**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-3-series/broken-reference/README.md) **page.**

Compared to [MariaDB 5.3.0](mariadb-530-release-notes.md) and 5.3.1, [MariaDB 5.3.2](mariadb-532-release-notes.md) is mainly a bug-fix release. It is the\
third beta release of the 5.3 series and fixes bugs found in the initial 5.3.0 and\
5.3.1 beta releases.

For a list of every change made in [MariaDB 5.3.2](mariadb-532-release-notes.md), with links to detailed\
information on each push, see the[MariaDB 5.3.2 Changelog](../../../changelogs/changelogs-mariadb-53-series/mariadb-532-changelog.md). It is worth noting that[MariaDB 5.3](changes-improvements-in-mariadb-5-3.md) is built on [MariaDB 5.2](../release-notes-mariadb-5-2-series/changes-improvements-in-mariadb-5-2.md),[MariaDB 5.1](../release-notes-mariadb-5-1-series/changes-improvements-in-mariadb-5-1.md), and MySQL 5.1.

In most respects [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/mariadb/README.md) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

Be notified of new releases automatically by adding the[releases rss feed](https://montyprogram.com/news/feed/mariadb_releases/) to\
your favorite feed reader or by [subscribing](https://mariadb.org) to the\
announce 'at' mariadb.org announcement list (this is a low traffic,\
announce-only list).

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

## User Feedback plugin

[MariaDB 5.3.2](mariadb-532-release-notes.md)-beta introduces the [User Feedback plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/feedback-plugin). This plugin is disabled by default. If enabled, it submits anonymous basic MariaDB usage information. This information will be used by the developers to track trends in MariaDB usage to better guide development efforts.

If you would like to help make MariaDB better, please add `--plugin-load=feedback.so` to your my.cnf file! On Windows, add "feedback=ON" to your my.ini file, or click the checkbox during installation of the MSI package.

See the [User Feedback plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/feedback-plugin) page for more information.

## Subquery Cache

Starting in [MariaDB 5.3.2](mariadb-532-release-notes.md)-beta, the [Subquery cache](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/subquery-optimizations/subquery-cache) is on by default. In previous versions of MariaDB the cache was off by default.

The goal of the subquery cache is to optimize the evaluation of correlated subqueries by storing results together with correlation parameters in a cache and avoiding re-execution of the subquery in cases where the result is already in the cache.

See the [Subquery cache](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/subquery-optimizations/subquery-cache) page for more information.

{% @marketo/form formid="4316" formId="4316" %}
