# MariaDB 10.6.1 Release Notes

The most recent release of [MariaDB 10.6](what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.1](https://downloads.mariadb.org/mariadb/10.6.1/)[Release Notes](mariadb-1061-release-notes.md)[Changelog](../changelogs/changelogs-mariadb-106-series/mariadb-1061-changelog.md)[Overview of 10.6](what-is-mariadb-106.md)

**Release date:** 21 May 2021

[MariaDB 10.6](what-is-mariadb-106.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.5](../mariadb-10-5-series/what-is-mariadb-105.md) with several entirely new features.

[MariaDB 10.6.1](mariadb-1061-release-notes.md) is a [_**Beta**_](../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

**For an overview of** [**MariaDB 10.6**](what-is-mariadb-106.md) **see the**[**What is MariaDB 10.6?**](what-is-mariadb-106.md) **page.**

[Register now for our MariaDB Community Server 10.6 webinar to be held 2021-06-29](https://go.mariadb.com/21Q3-WBN-GLBL-OSSG-Community-Server-10.6-2021-06-22_Registration-LP.html?utm_source=KB) and be one of the first to see the biggest features coming in MariaDB Community Server 10.6, with an exclusive opportunity to have your questions answered by MariaDB engineering and product leads.

Thanks, and enjoy MariaDB!

## Notable Changes

Notable changes of this release include:

### Atomic DDL

* [CREATE TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-table), [ALTER TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table), [RENAME TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/rename-table), [DROP TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/drop/drop-table), [DROP DATABASE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/drop/drop-database) and related DDL statements are now atomic. Either the statement is fully completed, or everything is reverted to it's original state. Note that when deleting multiple tables with DROP TABLE, only each individual drop is atomic, not the full list of tables). ([MDEV-23842](https://jira.mariadb.org/browse/MDEV-23842)).

### Replication, Galera and Binlog

* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/galera-cluster/README.md) updated to 26.4.8
* The delay between binary log purges can now be specified with much greater precision. The system variable [binlog\_expire\_logs\_seconds](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#binlog_expire_logs_seconds) is introduced as a form of alias for [expire\_logs\_days](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#expire_logs_days), which now accepts a precision of 1/1000000 days ([MDEV-19371](https://jira.mariadb.org/browse/MDEV-19371))
* Allow transition from unencrypted to TLS [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/galera/README.md) cluster communication without cluster downtime ([MDEV-22131](https://jira.mariadb.org/browse/MDEV-22131))
* DDL information logged on all [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/galera/README.md) cluster nodes if wsrep\_debug is set to SERVER and wsrep\_OSU\_method is 'TOI' ([MDEV-9609](https://jira.mariadb.org/browse/MDEV-9609))
* For the [mysqlbinlog / mariadb-binlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog/mariadb-binlog-options) `--base64-output` option, removed the deprecated `always` option, and changed the default to `auto` ([MDEV-25222](https://jira.mariadb.org/browse/MDEV-25222))

### Oracle Compatibility

* [ADD\_MONTHS()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/date-time-functions/add_months) added ([MDEV-20025](https://jira.mariadb.org/browse/MDEV-20025))
* [TO\_CHAR()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/to_char) added ([MDEV-20017](https://jira.mariadb.org/browse/MDEV-20017))
* [SYS\_GUID()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/miscellaneous-functions/sys_guid) added ([MDEV-24285](https://jira.mariadb.org/browse/MDEV-24285))
* MINUS is mapped to [EXCEPT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/joins-subqueries/except) in UNION ([MDEV-20021](https://jira.mariadb.org/browse/MDEV-20021))
* [ROWNUM](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/information-functions/rownum) function returns the current number of accepted rows in the current context ([MDEV-24089](https://jira.mariadb.org/browse/MDEV-24089))

### Character Sets

* The `utf8` [character set](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets) (and related collations) is now by default an alias for `utf8mb3` rather than the other way around. It can be set to imply `utf8mb4` by changing the value of the [old\_mode](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#old_mode) system variable ([MDEV-8334](https://jira.mariadb.org/browse/MDEV-8334))

### Clients

* For clients such as [mysql / mariadb](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/mariadb-client/mysql-command-line-client), the connection property specified via the command line (e.g. --port=3306) will now force its type ([MDEV-14974](https://jira.mariadb.org/browse/MDEV-14974))

## Changelog

For a complete list of changes made in [MariaDB 10.6.1](mariadb-1061-release-notes.md), with links to detailed\
information on each push, see the [changelog](../changelogs/changelogs-mariadb-106-series/mariadb-1061-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.6.1](mariadb-1061-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-6-1-now-available/).

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
