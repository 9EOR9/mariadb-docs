# MariaDB 10.4.13 Release Notes

The most recent release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download](https://downloads.mariadb.org/mariadb/10.4.13/)[Release Notes](mariadb-10413-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10413-changelog.md)[Overview of 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104)

**Release date:** 12 May 2020

[MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is the current _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.13](mariadb-10413-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) **see the**[**What is MariaDB 10.4?**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

### Events

* Fixed issue that, from [MariaDB 10.3.19](../release-notes-mariadb-10-3-series/mariadb-10319-release-notes.md), disabled all [events](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/triggers-events/event-scheduler/events) created by a server with a different `server_id`. Note that the fix does not re-enable affected events. ([MDEV-21758](https://jira.mariadb.org/browse/MDEV-21758))

### Privileges

* [SHOW PRIVILEGES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-privileges) now correctly lists the `Delete history` privilege, rather than displaying it as `Delete versioning rows`. ([MDEV-20382](https://jira.mariadb.org/browse/MDEV-20382))

### Performance

* Optimizer flag rowid\_filter leads to long query ([MDEV-21794](https://jira.mariadb.org/browse/MDEV-21794))
* WSREP\_ON is unnecessarily expensive to evaluate ([MDEV-22203](https://jira.mariadb.org/browse/MDEV-22203)
* Misc wsrep performance optimization ([MDEV-7962](https://jira.mariadb.org/browse/MDEV-7962))

### Security

* Added system user for user view which allows to remove root ([MDEV-19650](https://jira.mariadb.org/browse/MDEV-19650))
* WolfSSL updated
* ALTER USER doesn't remove excess authentication plugins from mysql.global\_priv ([MDEV-21928](https://jira.mariadb.org/browse/MDEV-21928))
* mysql\_upgrade creating empty global\_priv table ([MDEV-21244](https://jira.mariadb.org/browse/MDEV-21244))

### Aria

* Updated `aria_pack` to support transactional tables and added options: `--datadir`, `--ignore-control-file`, `--require-control-file`, more details [here](https://github.com/mariadb/server/commit/dbde95d91259a0658715dfb5f8c7e50716fc001b)

### ALTER TABLE

* Error on online ADD PRIMARY KEY after instant DROP/reorder ([MDEV-21658](https://jira.mariadb.org/browse/MDEV-21658))
* Assertion failure in file data0type.cc ([MDEV-20726](https://jira.mariadb.org/browse/MDEV-20726))
* Server aborts upon attempt to create foreign key on spatial field ([MDEV-21792](https://jira.mariadb.org/browse/MDEV-21792))
* DROP COLUMN, DROP INDEX is wrongly claimed to be ALGORITHM=INSTANT ([MDEV-22465](https://jira.mariadb.org/browse/MDEV-22465))
* Introduce a file format constraint to ALTER TABLE. See [innodb\_instant\_alter\_column\_allowed](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_instant_alter_column_allowed) ([MDEV-20590](https://jira.mariadb.org/browse/MDEV-20590))
* FORCE all partition to rebuild if any one of the partition does rebuild ([MDEV-21832](https://jira.mariadb.org/browse/MDEV-21832))
* InnoDB aborts while adding instant column for discarded tablespace ([MDEV-22446](https://jira.mariadb.org/browse/MDEV-22446))

### FULLTEXT INDEX

* Assertion \`\`!table->fts->in\_queue`' failed in` fts\_optimize\_remove\_table\` ([MDEV-21550](https://jira.mariadb.org/browse/MDEV-21550))
* FTS thread aborts during shutdown ([MDEV-21563](https://jira.mariadb.org/browse/MDEV-21563))

### Optimizer

* Optimizer, Wrong query results with `optimizer_switch="split_materialized=on"` ([MDEV-21614](https://jira.mariadb.org/browse/MDEV-21614))
* SHOW GRANTS does not quote role names properly ([MDEV-20076](https://jira.mariadb.org/browse/MDEV-20076))
* Paritioning INSERT chooses wrong partition for RANGE partitioning by DECIMAL column ([MDEV-21195](https://jira.mariadb.org/browse/MDEV-21195))

### mariadb-backup

* mariadb-backup does not honor ignore\_db\_dirs from server config ([MDEV-19347](https://jira.mariadb.org/browse/MDEV-19347))
* mariadb-backup `--ftwrl-wait-timeout` never times out on explicit lock ([MDEV-20230](https://jira.mariadb.org/browse/MDEV-20230))

### Crash Recovery

* Running out of file descriptors and eventual crash ([MDEV-18027](https://jira.mariadb.org/browse/MDEV-18027))

### Galera

* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) updated to 26.4.4
* Galera Cluster Node During IST gets stuck going from "Synced" to "Joining:..." ([MDEV-21002](https://jira.mariadb.org/browse/MDEV-21002))

### Other

* [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 11.0 ([MDEV-22032](https://jira.mariadb.org/browse/MDEV-22032))
* Wrong estimate of affected BLOB columns in update of PRIMARY KEY ([MDEV-22384](https://jira.mariadb.org/browse/MDEV-22384))
* Duplicate key value is silently truncated to 64 characters in `print_keydup_error` ([MDEV-20604](https://jira.mariadb.org/browse/MDEV-20604))
* Session tracking returns incorrectly long tracking data ([MDEV-22504](https://jira.mariadb.org/browse/MDEV-22504))
* Add `pam_user_map.so` file to binary tarball package ([MDEV-21913](https://jira.mariadb.org/browse/MDEV-21913))
* mysql\_upgrade is made aware of the upstream slave tables to issue warnings when that takes place ([MDEV-10047](https://jira.mariadb.org/browse/MDEV-10047))
* Corruption for `SET GLOBAL innodb_` string variables ([MDEV-22393](https://jira.mariadb.org/browse/MDEV-22393))
* [mysqldump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysqldump) parameter, `--ignore-table-data`, added ([MDEV-22037](https://jira.mariadb.org/browse/MDEV-22037))
* Server can fail while replicating conditional comments (Bug#28388217)
* Added the `xml-report` option to [mysql-test-run](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/testing-tools/mariadb-test/mariadb-test-run-pl-options) ([MDEV-22176](https://jira.mariadb.org/browse/MDEV-22176))
* Packages and [repositories](https://downloads.mariadb.org/mariadb/repositories/) for Ubuntu 20.04 "focal" added
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) for Debian 8 "Jessie"
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2020-2752](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2752)
  * [CVE-2020-2812](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2812)
  * [CVE-2020-2814](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2814)
  * [CVE-2020-2760](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2760)
  * [CVE-2020-13249](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-13249)

## Changelog

For a complete list of changes made in [MariaDB 10.4.13](mariadb-10413-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10413-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.13](mariadb-10413-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-13-10-3-23-10-2-32-10-1-45-and-5-5-68-now-available).\
Thanks, and enjoy MariaDB!

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
