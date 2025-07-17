# MariaDB 10.5.7 Release Notes

The most recent release of [MariaDB 10.5](what-is-mariadb-105.md) is:[**MariaDB 10.5.28**](mariadb-10-5-28-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.5.28/)

[Download 10.5.7](https://downloads.mariadb.org/mariadb/10.5.7/)[Release Notes](mariadb-1057-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-1057-changelog.md)[Overview of 10.5](what-is-mariadb-105.md)

**Release date:** 3 Nov 2020

[MariaDB 10.5](what-is-mariadb-105.md) is the current _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.4](../../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.5.7](mariadb-1057-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of** [**MariaDB 10.5**](what-is-mariadb-105.md) **see the**[**What is MariaDB 10.5?**](what-is-mariadb-105.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This release introduced an InnoDB data corruption bug ([MDEV-24096](https://jira.mariadb.org/browse/MDEV-24096)). If any InnoDB tables contain indexed virtual columns or unique indexes on BLOB or TEXT columns, any InnoDB tables or tablespaces may become irreparably corrupted.

* Improved write performance ([MDEV-23399](https://jira.mariadb.org/browse/MDEV-23399), [MDEV-23855](https://jira.mariadb.org/browse/MDEV-23855), [MDEV-24037](https://jira.mariadb.org/browse/MDEV-24037))
* [MDEV-18323](https://jira.mariadb.org/browse/MDEV-18323) It is now possible to upgrade from MySQL 5.7 Tables containing JSON, by loading the MYSQL\_JSON datatype plugin first. See [Making MariaDB understand MySQL JSON](https://mariadb.org/making-mariadb-understand-mysql-json/).
* Update [S3 engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/s3-storage-engine) to maturity Gamma
* [mariadbd --temp-pool](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/starting-and-stopping-mariadb/mariadbd-options) option deprecated and defaulted to zero ([MDEV-22278](https://jira.mariadb.org/browse/MDEV-22278))
* [BLACKHOLE Storage Engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/blackhole) maximum index size increased from 1000 to 3500 bytes ([MDEV-24017](https://jira.mariadb.org/browse/MDEV-24017))
* [Calculating (auto rounding)](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#div_precision_increment) issue ([MDEV-23702](https://jira.mariadb.org/browse/MDEV-23702))
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
* [ALTER TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table) fixes ([MDEV-22277](https://jira.mariadb.org/browse/MDEV-22277), [MDEV-22939](https://jira.mariadb.org/browse/MDEV-22939), [MDEV-23199](https://jira.mariadb.org/browse/MDEV-23199), [MDEV-23356](https://jira.mariadb.org/browse/MDEV-23356), [MDEV-23499](https://jira.mariadb.org/browse/MDEV-23499), [MDEV-23672](https://jira.mariadb.org/browse/MDEV-23672), [MDEV-23685](https://jira.mariadb.org/browse/MDEV-23685), [MDEV-23722](https://jira.mariadb.org/browse/MDEV-23722))
* Diskspace not reused for BLOB in data file ([MDEV-23072](https://jira.mariadb.org/browse/MDEV-23072))
* InnoDB: Failing assertion: `!space->referenced()` ([MDEV-23651](https://jira.mariadb.org/browse/MDEV-23651))
* `SIGSEGV` in `maria_create()` because of double free ([MDEV-23222](https://jira.mariadb.org/browse/MDEV-23222))
* `CREATE TEMPORARY TABLE .. LIKE` (system versioned table) returns error if unique index is defined in the table ([MDEV-23968](https://jira.mariadb.org/browse/MDEV-23968))
* Error upon querying the view, that selecting from versioned table with partitions ([MDEV-23779](https://jira.mariadb.org/browse/MDEV-23779))
* `CREATE .. SELECT` wrong result on join versioned table ([MDEV-23799](https://jira.mariadb.org/browse/MDEV-23799))
* `SIGSEGV` in `check_fields` on `UPDATE` ([MDEV-22805](https://jira.mariadb.org/browse/MDEV-22805))
* Parser fix ([MDEV-23094](https://jira.mariadb.org/browse/MDEV-23094))
* Add CRC-32 code to `mysys`, giving notable speedup in checksum calculation on x64 ([MDEV-19935](https://jira.mariadb.org/browse/MDEV-19935))
* Faster CRC-32C checksum calculations ([MDEV-23495](https://jira.mariadb.org/browse/MDEV-23495), [MDEV-22749](https://jira.mariadb.org/browse/MDEV-22749))
* Fixes to potential corruption bugs ([MDEV-23973](https://jira.mariadb.org/browse/MDEV-23973), [MDEV-24054](https://jira.mariadb.org/browse/MDEV-24054))
* Fixed delayed replication with S3 storage engine slave ([MDEV-23691](https://jira.mariadb.org/browse/MDEV-23691))
* Deadlock between `BACKUP STAGE BLOCK_COMMIT` and parallel replication ([MDEV-23586](https://jira.mariadb.org/browse/MDEV-23586))
* `CREATE` fails after `DROP` without `.frm` ([MDEV-23549](https://jira.mariadb.org/browse/MDEV-23549))

### S3 Storage Engine

* Update [S3 engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/s3-storage-engine) to maturity Gamma
* Add the [s3\_use\_http](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/s3-storage-engine/s3-storage-engine-system-variables#s3_use_http) and [s3\_port](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/s3-storage-engine/s3-storage-engine-system-variables#s3_port) system variables

### Galera

* [Galera wsrep library](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/readme/mariadb-galera-cluster-guide) updated to 26.4.6
* Fixed assertion failure on before\_commit ([MDEV-22681](https://jira.mariadb.org/browse/MDEV-22681))
* Fixed assertion after ROLLBACK AND CHAIN ([MDEV-22055](https://jira.mariadb.org/browse/MDEV-22055))
* Fixed replication of DROP TRIGGER ([MDEV-23638](https://jira.mariadb.org/browse/MDEV-23638))
* IPv6 SST handling improved ([MDEV-21770](https://jira.mariadb.org/browse/MDEV-21770), [MDEV-23576](https://jira.mariadb.org/browse/MDEV-23576), [MDEV-23580](https://jira.mariadb.org/browse/MDEV-23580), [MDEV-23581](https://jira.mariadb.org/browse/MDEV-23581), [MDEV-23574](https://jira.mariadb.org/browse/MDEV-23574))
* Fixed SIGSEGV in lock\_rec\_unlock ([MDEV-23101](https://jira.mariadb.org/browse/MDEV-23101))
* Fixed replication of timezone if only 1 timezone is loaded ([MDEV-22626](https://jira.mariadb.org/browse/MDEV-22626))
* Fixed replication of CREATE OR REPLACE TRIGGER ([MDEV-21578](https://jira.mariadb.org/browse/MDEV-21578))
* Fixed SST FLUSH TABLES WITH READ LOCK timeout ([MDEV-22543](https://jira.mariadb.org/browse/MDEV-22543))

### Notes

* As per the [MariaDB Deprecation Policy](../../about/platform-deprecation-policy.md), this will be the last release of [MariaDB 10.5](what-is-mariadb-105.md) for CentOS/RHEL 6 and Fedora 31
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
  * [CVE-2022-21427](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-21427)

## Changelog

For a complete list of changes made in [MariaDB 10.5.7](mariadb-1057-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-1057-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.5.7](mariadb-1057-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/first-mariadb-10-5-alpha-release/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
