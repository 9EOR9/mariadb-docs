# MariaDB 10.2.2 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.2)[Release Notes](mariadb-1022-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-1022-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 27 Sep 2016

[MariaDB 10.2](what-is-mariadb-102.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.2](mariadb-1022-release-notes.md) is a [_**Beta**_](../../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**beta**_**&#x20;releases on production systems!**

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the first beta release in the [MariaDB 10.2](what-is-mariadb-102.md) series.

* [InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-versions) was merged from MySQL-5.7.14 (XtraDB is disabled in MariaDB-10.2.2 pending a similar merge)
  * Note that there have been numerous variable changes, both new variables and changes to defaults, for example [innodb\_strict\_mode](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) now defaults to ON.
  * InnoDB tables now support [spatial indexes](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/geometry/spatial-index).
* [ANALYZE TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/analyze-table) has been re-implemented so as not to lock the entire table when collecting engine independent statistics ([MDEV-7901](https://jira.mariadb.org/browse/MDEV-7901))
* The CONNECT engine now supports the [JDBC Table type](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect/connect-table-types/connect-jdbc-table-type-accessing-tables-from-another-dbms) ([MDEV-9765](https://jira.mariadb.org/browse/MDEV-9765))
* Internal CRC32 routines use the optimized implementation on Power8 — [MDEV-9872](https://jira.mariadb.org/browse/MDEV-9872)
* Old GPL client library is gone; now MariaDB Server comes with the LGPL Connector/C client library ([MDEV-9055](https://jira.mariadb.org/browse/MDEV-9055))
* Recursive Common Table Expressions ([MDEV-9864](https://jira.mariadb.org/browse/MDEV-9864))
* Further improvements and bugfixing for CHECK CONSTRAINT ([MDEV-7563](https://jira.mariadb.org/browse/MDEV-7563)) and DEFAULT with expressions ([MDEV-10134](https://jira.mariadb.org/browse/MDEV-10134))
* Optimizer improvement: conditions can be [pushed down into non-mergeable views/derived tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#optimizer_switch) ([MDEV-9197](https://jira.mariadb.org/browse/MDEV-9197))
* Support for `NO PAD` [collations](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets/supported-character-sets-and-collations), with 88 new `NO PAD` collations included in the server ([MDEV-9711](https://jira.mariadb.org/browse/MDEV-9711))
* Table cache can automatically partition itself as needed to reduce the contention ([MDEV-10296](https://jira.mariadb.org/browse/MDEV-10296))
* The thread pool now gives higher priority to connections that have an active transaction. This can be controlled with the new [thread\_pool\_prio\_kickup\_timer](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/buffers-caches-and-threads/thread-pool/thread-pool-system-status-variables) and [thread\_pool\_priority](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/buffers-caches-and-threads/thread-pool/thread-pool-system-status-variables) system variables. ([MDEV-10297](https://jira.mariadb.org/browse/MDEV-10297))
* Window functions support extended. All standard aggregate functions (except GROUP\_CONCAT) can be used as window functions. ([MDEV-9526](https://jira.mariadb.org/browse/MDEV-9526))
* New [window functions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/window-functions) added: [LEAD](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/window-functions/lead), [LAG](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/window-functions/lag), [NTH\_VALUE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/window-functions/nth_value), [FIRST\_VALUE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/window-functions/first_value), [LAST\_VALUE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/information-functions/last_value). ([MDEV-8091](https://jira.mariadb.org/browse/MDEV-8091))
* Performance improvements for faster computing of window functions. Multiple window functions with compatible sorting criteria are computed during the same pass. ([MDEV-10059](https://jira.mariadb.org/browse/MDEV-10059))
* Default [server\_id](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables) changed from `0` to `1`.
* New [innochecksum](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/administrative-tools/innochecksum) options.
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

**Do not use&#x20;**_**beta**_**&#x20;releases on production systems!**

For a complete list of changes made in [MariaDB 10.2.2](mariadb-1022-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-1022-changelog.md).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
