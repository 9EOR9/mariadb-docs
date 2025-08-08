# MariaDB 10.3.26 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download 10.3.26](https://downloads.mariadb.org/mariadb/10.3.26/) | [Release Notes](mariadb-10326-release-notes.md) | [Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10326-changelog.md) | [Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 3 Nov 2020

[MariaDB 10.3](what-is-mariadb-103.md) is the previous stable series of MariaDB, and an evolution of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features\
not found anywhere else and with backported and reimplemented features from\
MySQL.

[MariaDB 10.3.26](mariadb-10326-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* Set the default value of [innodb\_log\_optimize\_ddl](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_log_optimize_ddl) to `OFF` by default ([MDEV-23720](https://jira.mariadb.org/browse/MDEV-23720))
* [BLACKHOLE Storage Engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/blackhole) maximum index size increased from 1000 to 3500 bytes ([MDEV-24017](https://jira.mariadb.org/browse/MDEV-24017))
* [Calculating (auto rounding)](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/variables-and-modes/server-system-variables#div_precision_increment) issue ([MDEV-23702](https://jira.mariadb.org/browse/MDEV-23702))
* Temporary tables can no longer overwrite existing files. Instead an error is returned should a conflict occur ([MDEV-23569](https://jira.mariadb.org/browse/MDEV-23569))
* Binlog checksum verification at recovery time ([MDEV-23832](https://jira.mariadb.org/browse/MDEV-23832))
* Verbose print-out of [Geometry types](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/geometry/geometry-types) by [mysqlbinlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog) ([MDEV-22330](https://jira.mariadb.org/browse/MDEV-22330))
* [SHOW BINLOG EVENTS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-binlog-events) from validates when binlog checksummed ([MDEV-21839](https://jira.mariadb.org/browse/MDEV-21839))
* Freeing memory of [replicate\_do\_table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#replicate_do_table) ([MDEV-23534](https://jira.mariadb.org/browse/MDEV-23534))
* Corrected verbose [mysqlbinlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog) output for multi-record Rows-log-event ([MDEV-16372](https://jira.mariadb.org/browse/MDEV-16372))
* [SET GLOBAL replicate\_do\_db = DEFAULT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#replicate_do_db) no longer causes crash ([MDEV-20744](https://jira.mariadb.org/browse/MDEV-20744))
* [User killed queries](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/kill) that were running an index condition pushdown in InnoDB will now return an error ([MDEV-23938](https://jira.mariadb.org/browse/MDEV-23938))
* Wrong direxec param data caused crash; Numerous fixes about Mac builds (by Dmitri Shulga) ([MDEV-19838](https://jira.mariadb.org/browse/MDEV-19838))
* [server\_audit plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/mariadb-audit-plugin) now logs proxy users ([MDEV-19443](https://jira.mariadb.org/browse/MDEV-19443))
* Crash on `SELECT` on a table with indexed virtual columns ([MDEV-18366](https://jira.mariadb.org/browse/MDEV-18366))
* [InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb) updated to 5.7.32 ([MDEV-23989](https://jira.mariadb.org/browse/MDEV-23989))
* Bug fixes related to adaptive hash index ([MDEV-23452](https://jira.mariadb.org/browse/MDEV-23452), [MDEV-23370](https://jira.mariadb.org/browse/MDEV-23370))
* Fixed a bug in the recovery of encrypted tables ([MDEV-23456](https://jira.mariadb.org/browse/MDEV-23456))
* Fixed a race condition in MVCC reads ([MDEV-22924](https://jira.mariadb.org/browse/MDEV-22924))
* `ALTER TABLE` fixes ([MDEV-22277](https://jira.mariadb.org/browse/MDEV-22277), [MDEV-22939](https://jira.mariadb.org/browse/MDEV-22939), [MDEV-23685](https://jira.mariadb.org/browse/MDEV-23685), [MDEV-23722](https://jira.mariadb.org/browse/MDEV-23722))
* Diskspace not reused for BLOB in data file ([MDEV-23072](https://jira.mariadb.org/browse/MDEV-23072))
* InnoDB: Failing assertion: `!space->referenced()` ([MDEV-23651](https://jira.mariadb.org/browse/MDEV-23651))
* `SIGSEGV` in `maria_create()` because of double free ([MDEV-23222](https://jira.mariadb.org/browse/MDEV-23222))
* `CREATE TEMPORARY TABLE .. LIKE` (system versioned table) returns error if unique index is defined in the table ([MDEV-23968](https://jira.mariadb.org/browse/MDEV-23968))
* Error upon querying the view, that selecting from versioned table with partitions ([MDEV-23779](https://jira.mariadb.org/browse/MDEV-23779))
* `CREATE .. SELECT` wrong result on join versioned table ([MDEV-23799](https://jira.mariadb.org/browse/MDEV-23799))
* Fixed a crash with the [NTH\_VALUE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/window-functions/nth_value) function ([MDEV-15180](https://jira.mariadb.org/browse/MDEV-15180))
* Computing certain [window functions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/window-functions) on a server started with [--encrypt-tmp\_files=ON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/variables-and-modes/server-system-variables#encrypt_tmp_files) could cause a wrong query result or crash ([MDEV-23867](https://jira.mariadb.org/browse/MDEV-23867))
* A query with a certain form of WHERE clause over a table with multiple indexes could pick a less efficient range plan ([MDEV-23811](https://jira.mariadb.org/browse/MDEV-23811))
* Fixed a memory leak for correlated subqueries with ROLLUP ([MDEV-17066](https://jira.mariadb.org/browse/MDEV-17066))

### Galera

* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) updated to 25.3.31
* Fixed galera got stuck after flush tables ([MDEV-22707](https://jira.mariadb.org/browse/MDEV-22707))
* Fixed data loss on rolling upgrade between 10.3 and 10.4 ([MDEV-22723](https://jira.mariadb.org/browse/MDEV-22723))
* IPv6 SST handling improved ([MDEV-21770](https://jira.mariadb.org/browse/MDEV-21770), [MDEV-23576](https://jira.mariadb.org/browse/MDEV-23576), [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580), [MDEV-23581](https://jira.mariadb.org/browse/MDEV-23581), [MDEV-23574](https://jira.mariadb.org/browse/MDEV-23574))
* Fixed SIGSEGV in lock\_rec\_unlock ([MDEV-23101](https://jira.mariadb.org/browse/MDEV-23101))
* Fixed replication of timezone if only 1 timezone is loaded ([MDEV-22626](https://jira.mariadb.org/browse/MDEV-22626))
* Fixed replication of [CREATE OR REPLACE TRIGGER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/triggers-events/triggers/create-trigger) ([MDEV-21578](https://jira.mariadb.org/browse/MDEV-21578))
* Fixed SST FLUSH TABLES WITH READ LOCK timeout ([MDEV-22543](https://jira.mariadb.org/browse/MDEV-22543))

### Notes

* As per the [MariaDB Deprecation Policy](../../about/platform-deprecation-policy.md), this will be the last release of [MariaDB 10.3](what-is-mariadb-103.md) for CentOS/RHEL 6 and Fedora 31
* Packages for [Ubuntu 20.10 "Groovy Gorilla"](https://downloads.mariadb.org/mariadb/repositories/#distro=Ubuntu\&distro_release=groovy--ubuntu_groovy) added
* Packages for [Debian 10 "buster"](https://downloads.mariadb.org/mariadb/repositories/#distro=Debian\&distro_release=buster--buster) arm64 and ppc64el added
* Packages for [Debian 9 "stretch"](https://downloads.mariadb.org/mariadb/repositories/#distro=Debian\&distro_release=stretch--stretch) arm64 added
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2020-14812](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14812)
  * [CVE-2020-14765](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14765)
  * [CVE-2020-14776](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14776)
  * [CVE-2020-14789](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14789)
  * [CVE-2020-28912](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-28912) ([MDEV-24040](https://jira.mariadb.org/browse/MDEV-24040))
  * [CVE-2021-2194](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2194) ([MDEV-18366](https://jira.mariadb.org/browse/MDEV-18366))

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.26](mariadb-10326-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10326-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.26](mariadb-10326-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-11-10-3-22-and-10-2-30-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
