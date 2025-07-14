# MariaDB 10.5.3 Release Notes

The most recent release of [MariaDB 10.5](what-is-mariadb-105.md) is:[**MariaDB 10.5.28**](mariadb-10-5-28-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.5.28/)

[Download](https://downloads.mariadb.org/mariadb/10.5.3)[Release Notes](mariadb-1053-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-1053-changelog.md)[Overview of 10.5](what-is-mariadb-105.md)

**Release date:** 12 May 2020

[MariaDB 10.5](what-is-mariadb-105.md) is the current _development_ series of MariaDB. It is an evolution\
of [MariaDB 10.4](../../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.5.3](mariadb-1053-release-notes.md) is a [_**Release Candidate**_](../../../mariadb-release-criteria.md) (RC) release.

**Do not use non-stable (non-GA) releases in production!**

**For an overview of** [**MariaDB 10.5**](what-is-mariadb-105.md) **see the**[**What is MariaDB 10.5?**](what-is-mariadb-105.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the second beta release in the [MariaDB 10.5](what-is-mariadb-105.md) series.

Notable changes of this release include:

### Syntax

* Application period tables: [WITHOUT OVERLAPS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/application-time-periods#without-overlaps) ([MDEV-16978](https://jira.mariadb.org/browse/MDEV-16978))
* Introduce a file format constraint to ALTER TABLE. See [innodb\_instant\_alter\_column\_allowed](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_instant_alter_column_allowed) ([MDEV-20590](https://jira.mariadb.org/browse/MDEV-20590))

### Large Pages

* Modernise Linux Large Page support (multiplesizes) ([MDEV-18851](https://jira.mariadb.org/browse/MDEV-18851))

### Storage Engines

* Partitioned [S3 tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/s3-storage-engine) are discoverable. This means that if you create a partitioned S3 table, both the partitioned table and its partitions can be directly used by another server that has access to the S3 storage. ([MDEV-22088](https://jira.mariadb.org/browse/MDEV-22088))

### Performance

* Optimizer flag rowid\_filter leads to long query ([MDEV-21794](https://jira.mariadb.org/browse/MDEV-21794))
* WSREP\_ON is unnecessarily expensive to evaluate ([MDEV-22203](https://jira.mariadb.org/browse/MDEV-22203)
* Misc wsrep performance optimization ([MDEV-7962](https://jira.mariadb.org/browse/MDEV-7962))

### Security

* Added system user for user view which allows to remove root ([MDEV-19650](https://jira.mariadb.org/browse/MDEV-19650))
* WolfSSL updated
* [ALTER USER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/alter-user) doesn't remove excess authentication plugins from [mysql.global\_priv](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-global_priv-table) ([MDEV-21928](https://jira.mariadb.org/browse/MDEV-21928))
* [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) creating empty [global\_priv table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/the-mysql-database-tables/mysql-global_priv-table) ([MDEV-21244](https://jira.mariadb.org/browse/MDEV-21244))

### Aria

* Updated [aria\_pack](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/aria-clients-and-utilities/aria_pack) to support transactional tables and added the `--datadir`, `--ignore-control-file` and `--require-control-file` options. More details [here](https://github.com/mariadb/server/commit/dbde95d91259a0658715dfb5f8c7e50716fc001b)

### ALTER TABLE

* Error on online ADD PRIMARY KEY after instant DROP/reorder ([MDEV-21658](https://jira.mariadb.org/browse/MDEV-21658))
* Assertion failure in file data0type.cc ([MDEV-20726](https://jira.mariadb.org/browse/MDEV-20726))
* Server aborts upon attempt to create foreign key on spatial field ([MDEV-21792](https://jira.mariadb.org/browse/MDEV-21792))
* DROP COLUMN, DROP INDEX is wrongly claimed to be ALGORITHM=INSTANT ([MDEV-22465](https://jira.mariadb.org/browse/MDEV-22465))
* Introduce a file format constraint ([MDEV-20590](https://jira.mariadb.org/browse/MDEV-20590))
* FORCE all partition to rebuild if any one of the partition does rebuild ([MDEV-21832](https://jira.mariadb.org/browse/MDEV-21832))
* InnoDB aborts while adding instant column for discarded tablespace ([MDEV-22446](https://jira.mariadb.org/browse/MDEV-22446))
* Misc ALTER TABLE assertion failure ([MDEV-22358](https://jira.mariadb.org/browse/MDEV-22358))

### Optimizer

* Optimizer, Wrong query results with `optimizer_switch="split_materialized=on"` ([MDEV-21614](https://jira.mariadb.org/browse/MDEV-21614))
* SHOW GRANTS does not quote role names properly ([MDEV-20076](https://jira.mariadb.org/browse/MDEV-20076))
* Paritioning INSERT chooses wrong partition for RANGE partitioning by DECIMAL column ([MDEV-21195](https://jira.mariadb.org/browse/MDEV-21195))

### mariadb-backup

* [mariadb-backup](../../mariadb-10-5-series/broken-reference/) does not honor ignore\_db\_dirs from server config ([MDEV-19347](https://jira.mariadb.org/browse/MDEV-19347))
* mariadb-backup `--ftwrl-wait-timeout` never times out on explicit lock ([MDEV-20230](https://jira.mariadb.org/browse/MDEV-20230))

### Crash Recovery

* Loop of Read redo log up to LSN ([MDEV-21826](https://jira.mariadb.org/browse/MDEV-21826))
* `buf_page_get_gen()` should apply buffered page initialized redo log during recovery ([MDEV-21572](https://jira.mariadb.org/browse/MDEV-21572))
* Running out of file descriptors and eventual crash ([MDEV-18027](https://jira.mariadb.org/browse/MDEV-18027))
* Efficient InnoDB redo log record format ([MDEV-12353](https://jira.mariadb.org/browse/MDEV-12353))
* Punch holes when pages are freed ([MDEV-15528](https://jira.mariadb.org/browse/MDEV-15528))

### Other

* Use MariaDB in error messages instead of MySQL ([MDEV-17812](https://jira.mariadb.org/browse/MDEV-17812))
* FULLTEXT INDEX, Assertion \`\`!table->fts->in\_queue`' failed in` fts\_optimize\_remove\_table\` ([MDEV-21550](https://jira.mariadb.org/browse/MDEV-21550))
* Wrong estimate of affected BLOB columns in update of PRIMARY KEY ([MDEV-22384](https://jira.mariadb.org/browse/MDEV-22384))
* Duplicate key value is silently truncated to 64 characters in `print_keydup_error` ([MDEV-20604](https://jira.mariadb.org/browse/MDEV-20604))
* Session tracking returns incorrectly long tracking data ([MDEV-22504](https://jira.mariadb.org/browse/MDEV-22504))
* Add `pam_user_map.so` file to binary tarball package ([MDEV-21913](https://jira.mariadb.org/browse/MDEV-21913))
* Misc fixes for Mac build (MENT-606)
* [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is made aware of the upstream slave tables to issue warnings when that takes place ([MDEV-10047](https://jira.mariadb.org/browse/MDEV-10047))
* InnoDB [ALTER TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table) fixes ([MDEV-21564](https://jira.mariadb.org/browse/MDEV-21564), [MDEV-19092](https://jira.mariadb.org/browse/MDEV-19092), [MDEV-21549](https://jira.mariadb.org/browse/MDEV-21549))
* InnoDB FULLTEXT INDEX fixes ([MDEV-21563](https://jira.mariadb.org/browse/MDEV-21563))
* Corruption for `SET GLOBAL innodb_` string variables ([MDEV-22393](https://jira.mariadb.org/browse/MDEV-22393))
* Test suite, Add JUnit support to MTR to generate XML test result ([MDEV-22176](https://jira.mariadb.org/browse/MDEV-22176))
* [mysqldump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysqldump) parameter, `--ignore-table-data`, added ([MDEV-22037](https://jira.mariadb.org/browse/MDEV-22037))
* Refactored `MYSQL_BIN_LOG::xid_count_per_binlog` to satisfy UBSAN enabled build ([MDEV-20923](https://jira.mariadb.org/browse/MDEV-20923))
* Unregister of slave threads disconnected before COM\_BINLOG\_DUMP (Bug#29915479)
* Server can fail while replicating conditional comments (Bug#28388217)
* Added the `xml-report` option to [mysql-test-run](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/testing-tools/mariadb-test/mariadb-test-run-pl-options) ([MDEV-22176](https://jira.mariadb.org/browse/MDEV-22176))
* Packages and [repositories](https://downloads.mariadb.org/mariadb/repositories/) for Ubuntu 20.04 "focal" added

## Changelog

For a complete list of changes made in [MariaDB 10.5.3](mariadb-1053-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-1053-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.5.3](mariadb-1053-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-3-release-candidate-now-available/).

**Do not use non-stable (non-GA) releases in production!**

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
