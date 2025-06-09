# MariaDB 10.2.37 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download 10.2.37](https://downloads.mariadb.org/mariadb/10.2.37/)[Release Notes](mariadb-10237-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10237-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 22 Feb 2021

**Last month long-time MariaDB VP of Engineering, Rasmus Johansson, passed due to complications from cancer. His loss has been felt keenly by the whole MariaDB team. Our thoughts are with his family during this difficult time and this release is dedicated to his memory.**

[MariaDB 10.2](what-is-mariadb-102.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.37](mariadb-10237-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

### InnoDB

* [MDEV-24188](https://jira.mariadb.org/browse/MDEV-24188) - Hang in buf\_page\_create() after reusing a previously freed page
* [MDEV-24275](https://jira.mariadb.org/browse/MDEV-24275) - [InnoDB persistent stats](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/innodb-persistent-statistics) analyze forces full scan forcing lock crash
* [MDEV-24449](https://jira.mariadb.org/browse/MDEV-24449) - Corruption of system tablespace or last recovered page

### Galera

* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera-cluster/README.md) updated to 25.3.32
* [MDEV-23328](https://jira.mariadb.org/browse/MDEV-23328) - Server hang due to Galera lock conflict resolution
* [MDEV-23851](https://jira.mariadb.org/browse/MDEV-23851) - BF-BF Conflict issue because of UK GAP locks
* [MDEV-20717](https://jira.mariadb.org/browse/MDEV-20717) - Plugin system variables and activation options can break [mysqld --wsrep\_recover](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_recover)
* [MDEV-25179](https://jira.mariadb.org/browse/MDEV-25179) - [wsrep\_provider](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_provider) and [wsrep\_notify\_cmd](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_notify_cmd) system variables are now read-only

### Replication

* [MDEV-8134](https://jira.mariadb.org/browse/MDEV-8134) - relay-log is corrected to rotate past 999999
* [MDEV-23033](https://jira.mariadb.org/browse/MDEV-23033) - fixed slave applier for row-based events with FK constraints on virtual columns
* [MDEV-4633](https://jira.mariadb.org/browse/MDEV-4633) - Relay\_Log\_Space of Show-Slave-Status is made thread-safe

### Misc

* [MDEV-24122](https://jira.mariadb.org/browse/MDEV-24122) - anomalies in mysql.user tables on previously 5.7 MySQL versions corrected
* [MDEV-23630](https://jira.mariadb.org/browse/MDEV-23630) - [mysqldump --system](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysqldump) option
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-27928](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-27928)

Upgrading from 10.2 versions earlier than 10.2.17 is **highly recommended**\
for all [**Galera**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability\
issues with earlier versions. See the bug issue page for more information.\
When upgrading from [MariaDB 10.2.16](mariadb-10216-release-notes.md) or earlier to [MariaDB 10.2.17](mariadb-10217-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in [MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.2.37](mariadb-10237-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10237-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.37](mariadb-10237-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-9-10-4-18-10-3-28-and-10-2-37-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.
