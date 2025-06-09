# MariaDB 10.5.9 Release Notes

The most recent release of [MariaDB 10.5](what-is-mariadb-105.md) is:[**MariaDB 10.5.28**](mariadb-10-5-28-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.5.28/)

[Download 10.5.9](https://downloads.mariadb.org/mariadb/10.5.9/)[Release Notes](mariadb-1059-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-1059-changelog.md)[Overview of 10.5](what-is-mariadb-105.md)

**Release date:** 22 Feb 2021

**Last month long-time MariaDB VP of Engineering, Rasmus Johansson, passed due to complications from cancer. His loss has been felt keenly by the whole MariaDB team. Our thoughts are with his family during this difficult time and this release is dedicated to his memory.**

[MariaDB 10.5](what-is-mariadb-105.md) is the current _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.4](broken-reference) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.5.9](mariadb-1059-release-notes.md) is a [_**Stable (GA)**_](../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.5**](what-is-mariadb-105.md) **see the**[**What is MariaDB 10.5?**](what-is-mariadb-105.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

### InnoDB

* [MDEV-24188](https://jira.mariadb.org/browse/MDEV-24188) - Hang in `buf_page_create()` after reusing a previously freed page
* [MDEV-24275](https://jira.mariadb.org/browse/MDEV-24275) - [InnoDB persistent stats](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/innodb-persistent-statistics) analyze forces full scan forcing lock crash
* [MDEV-24449](https://jira.mariadb.org/browse/MDEV-24449) - Corruption of system tablespace or last recovered page
* [MDEV-24109](https://jira.mariadb.org/browse/MDEV-24109) - InnoDB hangs with [innodb\_flush\_sync=OFF](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_flush_sync)
* [MDEV-24537](https://jira.mariadb.org/browse/MDEV-24537) - [innodb\_max\_dirty\_pages\_pct\_lwm=0](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_max_dirty_pages_pct_lwm) lost its special meaning
* Fixed bugs in the handling of freed pages - [MDEV-24569](https://jira.mariadb.org/browse/MDEV-24569), [MDEV-24695](https://jira.mariadb.org/browse/MDEV-24695), [MDEV-24765](https://jira.mariadb.org/browse/MDEV-24765), [MDEV-24864](https://jira.mariadb.org/browse/MDEV-24864)
* [MDEV-12227](https://jira.mariadb.org/browse/MDEV-12227) - Defer writes to the InnoDB temporary tablespace

### Galera

* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera-cluster/README.md) updated to 26.4.7
* [MDEV-23328](https://jira.mariadb.org/browse/MDEV-23328) - Server hang due to Galera lock conflict resolution
* [MDEV-23851](https://jira.mariadb.org/browse/MDEV-23851) - BF-BF Conflict issue because of UK GAP locks
* [MDEV-20717](https://jira.mariadb.org/browse/MDEV-20717) - Plugin system variables and activation options can break [mysqld --wsrep\_recover](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_recover)
* [MDEV-24469](https://jira.mariadb.org/browse/MDEV-24469) - Assertion `active() == false` failed with "XA START.."
* [MDEV-23647](https://jira.mariadb.org/browse/MDEV-23647) - Garbd can't initiate SST anymore in 10.5
* [MDEV-25179](https://jira.mariadb.org/browse/MDEV-25179) - [wsrep\_provider](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_provider) and [wsrep\_notify\_cmd](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_notify_cmd) system variables are now read-only

### Replication

* [MDEV-8134](https://jira.mariadb.org/browse/MDEV-8134) - relay-log is corrected to rotate past 999999
* [MDEV-23033](https://jira.mariadb.org/browse/MDEV-23033) - fixed slave applier for row-based events with FK constraints on virtual columns
* [MDEV-4633](https://jira.mariadb.org/browse/MDEV-4633) - Relay\_Log\_Space of Show-Slave-Status is made thread-safe
* [MDEV-10272](https://jira.mariadb.org/browse/MDEV-10272) - add master host/port info to slave thread exit messages
* [MDEV-23846](https://jira.mariadb.org/browse/MDEV-23846) - improves [mysqlbinlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog) error message issuing
* [MDEV-24087](https://jira.mariadb.org/browse/MDEV-24087) - replication of [S3](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/s3-storage-engine) ALTER PARTITION corrected
* [MDEV-23610](https://jira.mariadb.org/browse/MDEV-23610) - New privilege [REPLICA MONITOR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#replica-monitor) (also accessible as SLAVE MONITOR)

### ColumnStore

* MariaDB ColumnStore updated to 5.5.1
* MariaDB ColumnStore deb and rpm packages now have a version of `10.5.9-5.5.1` so one can see both the server version (10.5.9) and the plugin version (5.5.1) without needing to check the [Available Versions](broken-reference) table in the ColumnStore docs
* The MariaDB ColumnStore plugin is no longer provided for 32-bit x86 (i386) builds

### Misc

* MariaDB is fixed to build on the Apple M1 CPU
* MariaDB is fixed to build on AIX
* [MDEV-24122](https://jira.mariadb.org/browse/MDEV-24122) - anomalies in mysql.user tables on previously 5.7 MySQL versions corrected
* [MDEV-24093](https://jira.mariadb.org/browse/MDEV-24093) - Detect during [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) if `type_mysql_json.so` is needed and load it
* Binary tarballs now use WolfSSL v4.6.0 and pcre2-10.36
* [MDEV-23630](https://jira.mariadb.org/browse/MDEV-23630) - [mysqldump --system](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysqldump) option
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-27928](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-27928)

## Changelog

For a complete list of changes made in [MariaDB 10.5.9](mariadb-1059-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-1059-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.5.9](mariadb-1059-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-9-10-4-18-10-3-28-and-10-2-37-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
