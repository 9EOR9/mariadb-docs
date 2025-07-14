# MariaDB 10.3.12 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.12/)[Release Notes](mariadb-10312-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10312-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 7 Jan 2019

[MariaDB 10.3](what-is-mariadb-103.md) is an evolution\
of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.3.12](mariadb-10312-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [MDEV-17589](https://jira.mariadb.org/browse/MDEV-17589) - Stack-buffer-overflow with indexed varchar (utf8) field
* [MDEV-16987](https://jira.mariadb.org/browse/MDEV-16987) - [ALTER DATABASE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-database) possible in read-only mode (forbid ALTER DATABASE in read\_only)
* [MDEV-17720](https://jira.mariadb.org/browse/MDEV-17720) - [slave\_ddl\_exec\_mode=IDEMPOTENT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#slave_ddl_exec_mode) does not handle [DROP DATABASE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/drop/drop-database)
* [MDEV-6453](https://jira.mariadb.org/browse/MDEV-6453) - Assertion \`inited==NONE || (inited==RND && scan)' failed in handler::ha\_rnd\_init(bool) with InnoDB, joins, AND/OR conditions
* [MDEV-18105](https://jira.mariadb.org/browse/MDEV-18105) - [MariaDB Backup](https://mariadb.com/docs/server/server-usage/backup-and-restore/mariadb-backup/) fails to copy encrypted InnoDB system tablespace if LSN>4G
* [MDEV-17470](https://jira.mariadb.org/browse/MDEV-17470) - Orphan temporary files after interrupted [ALTER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table) cause InnoDB: Operating system error number 17 and eventual fatal error 71
* [MDEV-17765](https://jira.mariadb.org/browse/MDEV-17765): Locking bug fix for SPATIAL INDEX
* ALTER TABLE Fixes for FULLTEXT INDEX: [MDEV-17923](https://jira.mariadb.org/browse/MDEV-17923), [MDEV-17904](https://jira.mariadb.org/browse/MDEV-17904), [MDEV-17938](https://jira.mariadb.org/browse/MDEV-17938)
* Other ALTER TABLE fixes: [MDEV-17470](https://jira.mariadb.org/browse/MDEV-17470), [MDEV-17833](https://jira.mariadb.org/browse/MDEV-17833), [MDEV-17815](https://jira.mariadb.org/browse/MDEV-17815), [MDEV-18039](https://jira.mariadb.org/browse/MDEV-18039), [MDEV-18041](https://jira.mariadb.org/browse/MDEV-18041)
* Fixes for regressions introduced in [MariaDB 10.3.10](mariadb-10310-release-notes.md) by the backup-safe TRUNCATE TABLE ([MDEV-13564](https://jira.mariadb.org/browse/MDEV-13564), innodb\_safe\_truncate=ON) and innodb\_undo\_log\_truncate:
  * [MDEV-17780](https://jira.mariadb.org/browse/MDEV-17780), [MDEV-17816](https://jira.mariadb.org/browse/MDEV-17816), [MDEV-17849](https://jira.mariadb.org/browse/MDEV-17849), [MDEV-17851](https://jira.mariadb.org/browse/MDEV-17851), [MDEV-17885](https://jira.mariadb.org/browse/MDEV-17885), [MDEV-17859](https://jira.mariadb.org/browse/MDEV-17859), [MDEV-17989](https://jira.mariadb.org/browse/MDEV-17989)
* Several improvements to MariaDB Server and backup for dealing with encrypted or page\_compressed pages:
  * [MDEV-17957](https://jira.mariadb.org/browse/MDEV-17957): Make [innodb\_checksum\_algorithm](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_checksum_algorithm) stricter for strict\_\* values
  * [MDEV-17958](https://jira.mariadb.org/browse/MDEV-17958): On little-endian systems, remove bug-compatible variant of [innodb\_checksum\_algorithm=crc32](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_checksum_algorithm)
  * [MDEV-12112](https://jira.mariadb.org/browse/MDEV-12112): corruption in encrypted table may be overlooked
  * [MDEV-18025](https://jira.mariadb.org/browse/MDEV-18025): [MariaDB Backup](https://mariadb.com/docs/server/server-usage/backup-and-restore/mariadb-backup/) fails to detect corrupted page\_compressed=1 tables
* Virtual columns: [MDEV-17199](https://jira.mariadb.org/browse/MDEV-17199) Assertion \`pos < table->n\_v\_def' failed after upgrade from before 10.2
* [MDEV-17881](https://jira.mariadb.org/browse/MDEV-17881): Assertion failure in cmp\_dtuple\_rec\_with\_match\_bytes after instant ADD COLUMN
* The [Galera library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) in the repositories has been updated to version 25.3.25
* Experimental packages for the RedHat 8 beta have been added in this release. See the [package repository tool](https://downloads.mariadb.org/mariadb/repositories/#distro=RedHat\&version=10.3\&distro_release=rhel8-amd64--rhel8) to configure the repository and for installation instructions.
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.12](mariadb-10312-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10312-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.12](mariadb-10312-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-3-12-and-mariadb-connector-c-3-0-8-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
