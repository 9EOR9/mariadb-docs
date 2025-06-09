# MariaDB 10.3.6 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.6)[Release Notes](mariadb-1036-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-1036-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 16 Apr 2018

[MariaDB 10.3](what-is-mariadb-103.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.3.6](mariadb-1036-release-notes.md) is a [_**RC**_](../../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**non-GA**_**&#x20;releases on production systems!**

**For an overview of** [**MariaDB 10.3**](what-is-mariadb-103.md) **see the**[**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

Notable changes of this release include:

* Added the [DISKS plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-disks-table), for monitoring the disk space situation.
* [TRIM](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/trim), [LTRIM](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/ltrim), [RTRIM](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/rtrim), [LPAD](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/lpad) and [RPAD](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/rpad) now return NULL if returning an empty result when [SQL\_MODE=Oracle](broken-reference) - [MDEV-15739](https://jira.mariadb.org/browse/MDEV-15739), [MDEV-15664](https://jira.mariadb.org/browse/MDEV-15664).
* [innodb\_fast\_shutdown](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) now has a new mode, `3`, which skips the rollback of connected transactions - [MDEV-15832](https://jira.mariadb.org/browse/MDEV-15832)
* The max value of the [max\_prepared\_stmt\_count](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#max_prepared_stmt_count) system variable has been increased from 1048576 to 4294967295
* The [proxy\_protocol\_networks](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#proxy_protocol_networks) variable can now be modified without restarting the server - [MDEV-15501](https://jira.mariadb.org/browse/MDEV-15501)
* The Information Schema is optimized to use much less memory when selecting from [INFORMATION\_SCHEMA.TABLES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-tables-table) or any other table with many [VARCHAR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/varchar) or [TEXT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/text) columns - [MDEV-14275](https://jira.mariadb.org/browse/MDEV-14275)
* Added new status variables to count the usage of user defined aggregate functions: [Feature\_custom\_aggregate\_functions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-status-variables#feature_custom_aggregate_functions) - [MDEV-14592](https://jira.mariadb.org/browse/MDEV-14592)
* Windows binaries now use high-precision timer when available - [MDEV-15694](https://jira.mariadb.org/browse/MDEV-15694). This makes much less probable for two queries to have the same `CURRENT_TIMESTAMP(6)` value, for example.
* [System versioning](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/system-versioned-tables) is not allowed for tables in the mysql database - [MDEV-14790](https://jira.mariadb.org/browse/MDEV-14790)
* The [Information Schema Columns table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-columns-table) now displays [system versioning](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/system-versioned-tables) info in the EXTRA column - [MDEV-15062](https://jira.mariadb.org/browse/MDEV-15062)
* New Galera system variable, [wsrep\_reject\_queries](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_reject_queries) for rejecting client connection queries.
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.3](what-is-mariadb-103.md) for Debian 7 Wheezy

**Do not use&#x20;**_**non-GA**_**&#x20;releases on production systems!**

For a complete list of changes made in [MariaDB 10.3.6](mariadb-1036-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-1036-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.6](mariadb-1036-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-3-6-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
