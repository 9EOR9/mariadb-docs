# MariaDB 10.3.1 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.1)[Release Notes](mariadb-1031-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-1031-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 29 Aug 2017

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

[MariaDB 10.3](what-is-mariadb-103.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.3.1](mariadb-1031-release-notes.md) is an [_**Alpha**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.3**](what-is-mariadb-103.md) **see the**[**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the second alpha release in the [MariaDB 10.3](what-is-mariadb-103.md) series.

Notable changes of this release include:

### Syntax / General Features

* Update [InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-versions) to 5.7.19
* [ALTER SEQUENCE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sequences/alter-sequence)
* [SETVAL()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sequences/sequence-functions/setval)
* [SHOW CREATE SEQUENCE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-create-sequence)
* [CHR()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/chr) function ([MDEV-12685](https://jira.mariadb.org/browse/MDEV-12685))
* The [DELETE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/delete) statement can now delete from the table that is used in a subquery in the `WHERE` clause ([MDEV-12137](https://jira.mariadb.org/browse/MDEV-12137))
* Stored routine parameters can now use [ROW TYPE OF](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/programmatic-compound-statements/declare-variable#type-of-row-type-of) ([MDEV-13581](https://jira.mariadb.org/browse/MDEV-13581))
* The server now [supports the PROXY protocol](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/server-client-software/client-libraries/proxy-protocol-support) - see also the new [proxy\_protocol\_networks](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#proxy_protocol_networks) system variable ([MDEV-11159](https://jira.mariadb.org/browse/MDEV-11159))
* Reset old history of records and redo log format changes ([MDEV-12288](https://jira.mariadb.org/browse/MDEV-12288), [MDEV-13536](https://jira.mariadb.org/browse/MDEV-13536), [Revision #bae0844f657](https://github.com/MariaDB/server/commit/bae0844f657))

### Optimizer

* New [optimizer switch](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/optimizer-switch) setting, `split_grouping_derived=on` (see [description](https://github.com/MariaDB/server/commit/b14e2b044b))

### Compatibility

* Functions that used to only return 64-bit now can return 32-bit results ([MDEV-12619](https://jira.mariadb.org/browse/MDEV-12619)).

### Logging

* Disable logging of certain statements to the [general log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/general-query-log) or the [slow query log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/slow-query-log) with the [log\_disabled\_statements](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#log_disabled_statements) and [log\_slow\_disabled\_statements](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#log_slow_disabled_statements) system variables.
* A new option to [log\_slow\_filter](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#log_slow_filter), `filsort_priority_queue` (renamed to `filesort_priority_queue` in [MariaDB 10.3.2](mariadb-1032-release-notes.md)).

### Global-Transaction ID

* New system variable [gtid\_pos\_auto\_engines](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/gtid#gtid_pos_auto_engines) for improving performance if a server is using multiple different storage engines in different transactions ([MDEV-12179](https://jira.mariadb.org/browse/MDEV-12179))

### Other Variables

* New status variables [Rpl\_transactions\_multi\_engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-status-variables#rpl_transactions_multi_engine), [Transactions\_gtid\_foreign\_engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-status-variables), [Transactions\_multi\_engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-status-variables) and [Com\_alter\_sequence](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-status-variables#com_alter_sequence) .
* [session variables tracking](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#session_track_system_variables) is enabled by default ([MDEV-11825](https://jira.mariadb.org/browse/MDEV-11825))
* Remove deprecated variables [innodb\_file\_format](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables), [innodb\_file\_format\_check](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables), [innodb\_file\_format\_max](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) and [innodb\_large\_prefix](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables).

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

For a complete list of changes made in [MariaDB 10.3.1](mariadb-1031-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-1031-changelog.md).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
