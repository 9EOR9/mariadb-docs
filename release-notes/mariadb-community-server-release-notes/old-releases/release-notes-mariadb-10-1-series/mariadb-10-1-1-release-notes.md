# MariaDB 10.1.1 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.1)[Release Notes](mariadb-10-1-1-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-1-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 17 October 2014

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.1](mariadb-10-1-1-release-notes.md) is an [_**Alpha**_](../../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**alpha**_**&#x20;releases on production systems!**

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the second alpha release in the [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) series.

Notable changes of this release include:

* [Triggers can now be run on the slave](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/running-triggers-on-the-replica-for-row-based-events) for row-based events.
* [Default roles](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/set-default-role) allow roles to be enabled automatically when a user connects.
* InnoDB: merged the Facebook/Kakao defragmentation patch (see [Defragmenting InnoDB Tablespaces](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimizing-tables/defragmenting-innodb-tablespaces)) which uses [OPTIMIZE TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimizing-tables/optimize-table) to defragment InnoDB tablespaces).
* [Performance Schema](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/performance-schema) tables no longer use `.frm` files.
* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) is merged into MariaDB server, [MariaDB 10.1.1](mariadb-10-1-1-release-notes.md) binaries automatically support Galera out of the box.
* InnoDB: report progress of inplace alter table (Kakao patch).
* [Statements that exceed a certain execution time](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/aborting-statements) can now be aborted.
* [PREPARE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/prepared-statements/prepare-statement) statement now supports [out parameters](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/prepared-statements/out-parameters-in-prepare).
* [Compound statements can be used outside of stored programs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/programmatic-compound-statements/using-compound-statements-outside-of-stored-programs).
* The [engine\_condition\_pushdown optimizer\_switch flag](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/optimizer-switch) has been deprecated. Engine condition pushdown is now always enabled for all engines that support it.
* New Information Schema table [SYSTEM\_VARIABLES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-system_variables-table) shows for every system variable its session and global variable values as well as various metadata.
* [Information Schema plugins can now support SHOW and FLUSH statements](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/broken-reference/README.md). New statements in this release:
  * [SHOW QUERY\_RESPONSE\_TIME](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-query_response_time)
  * [FLUSH QUERY\_RESPONSE\_TIME](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/query-response-time-plugin)
  * [SHOW LOCALES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-locales)
* Two new columns added to the [CLIENT\_STATISTICS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-client_statistics-table) and [USER\_STATISTICS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-user_statistics-table) Information Schema tables (`TOTAL_SSL_CONNECTIONS` and `MAX_STATEMENT_TIME_EXCEEDED`).
* MariaDB can execute [UNION ALL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/joins-subqueries/union) without a temporary table. (MySQL 5.7 patch)
* `@@sql_log_slow` is now a session variable, not global.
* Merge with [MariaDB 10.0.14](../release-notes-mariadb-10-0-series/mariadb-10014-release-notes.md)
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) for both Ubuntu 13.10 "Saucy" and Mint 16 "Petra".
* With the recent release of CentOS 7 and RHEL 7, we are pleased to now provide packages for both distributions. Instructions for how to enable the repositories can be found by visiting the "[Installing MariaDB with YUM](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/rpm/yum)" page and the [repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/).

**Do not use&#x20;**_**alpha**_**&#x20;releases on production systems!**

For a complete list of changes made in [MariaDB 10.1.1](mariadb-10-1-1-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-1-changelog.md).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
