# MariaDB 10.2.3 Release Notes

The most recent release of [MariaDB 10.2](../what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](../mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.3)[Release Notes](./)[Changelog](../../../../changelogs/changelogs-mariadb-102-series/mariadb-1023-changelog.md)[Overview of 10.2](../what-is-mariadb-102.md)

**Release date:** 24 Dec 2016

[MariaDB 10.2](../what-is-mariadb-102.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.1](../../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.3](./) is a [_**Beta**_](../../../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**beta**_**&#x20;releases on production systems!**

**For an overview of** [**MariaDB 10.2**](../what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](../what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the second beta release in the [MariaDB 10.2](../what-is-mariadb-102.md) series.

* [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 9.4
* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/what-is-mariadb-galera-cluster/README.md) updated to 25.3.19
* [Packages](https://downloads.mariadb.org/mariadb/repositories/) for Debian 9 "stretch" amd64 and x86 and Debian 8 "jessie" ppc64el added
* Fix for FULLTEXT index crash ([MDEV-11233](https://jira.mariadb.org/browse/MDEV-11233)).

### Replication

* New variable [read\_binlog\_speed\_limit](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables) permits restricting the speed at which the slave reads the binlog from the master ([MDEV-11064](https://jira.mariadb.org/browse/MDEV-11064)) — Tencent Game DBA Team, developed by chouryzhou.
* [Delayed replication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/delayed-replication) is supported ([MDEV-7145](https://jira.mariadb.org/browse/MDEV-7145))
* [Compression of events in the binary log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log/compressing-events-to-reduce-size-of-the-binary-log) is supported ([MDEV-11065](https://jira.mariadb.org/browse/MDEV-11065)) — Tencent Game DBA Team, developed by vinchen.

### Statements

* [JSON functions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions) added ([MDEV-9143](https://jira.mariadb.org/browse/MDEV-9143)).
* Oracle-style [EXECUTE IMMEDIATE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/prepared-statements/execute-immediate) statement ([MDEV-10585](https://jira.mariadb.org/browse/MDEV-10585)).
* [PREPARE Statement](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/prepared-statements/prepare-statement)/Dynamic SQL now understand most expressions ([MDEV-10866](https://jira.mariadb.org/browse/MDEV-10866), [MDEV-10709](https://jira.mariadb.org/browse/MDEV-10709)).

### Triggers

* Multiple [triggers](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/triggers-events/triggers) per table ([MDEV-6112](https://jira.mariadb.org/browse/MDEV-6112))
* The FOLLOWS/PRECEDES clauses have been added to the [CREATE TRIGGER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/triggers-events/triggers/create-trigger) statement.
* Multiple triggers are now counted in the Executed\_triggers status variable ([MDEV-10915](https://jira.mariadb.org/browse/MDEV-10915)).
* [SHOW TRIGGERS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-triggers) and [SHOW CREATE TRIGGER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-create-trigger) now include the date and time the trigger was created.
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Notes

**Do not use&#x20;**_**beta**_**&#x20;releases on production systems!**

## Changelog

For a complete list of changes made in [MariaDB 10.2.3](./), with links to detailed\
information on each push, see the [changelog](../../../../changelogs/changelogs-mariadb-102-series/mariadb-1023-changelog.md).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
