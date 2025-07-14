# MariaDB 10.3.23 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.23/)[Release Notes](mariadb-10323-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10323-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 12 May 2020

[MariaDB 10.3](what-is-mariadb-103.md) is the previous stable series of MariaDB, and an evolution of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features\
not found anywhere else and with backported and reimplemented features from\
MySQL.

[MariaDB 10.3.23](mariadb-10323-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

### Events

* Fixed issue that, from [MariaDB 10.3.19](mariadb-10319-release-notes.md), disabled all [events](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/triggers-events/event-scheduler/events) created by a server with a different `server_id`. Note that the fix does not re-enable affected events. ([MDEV-21758](https://jira.mariadb.org/browse/MDEV-21758))

### Privileges

* [SHOW PRIVILEGES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-privileges) now correctly lists the `Delete history` privilege, rather than displaying it as `Delete versioning rows`. ([MDEV-20382](https://jira.mariadb.org/browse/MDEV-20382))

### Other

* [HeidiSQL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/graphical-and-enhanced-clients/heidisql) updated to 11.0 ([MDEV-22032](https://jira.mariadb.org/browse/MDEV-22032))
* Introduce a file format constraint to ALTER TABLE. See [innodb\_instant\_alter\_column\_allowed](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_instant_alter_column_allowed) ([MDEV-20590](https://jira.mariadb.org/browse/MDEV-20590))
* ALTER TABLE, FORCE all partition to rebuild if any one of the partition does rebuild ([MDEV-21832](https://jira.mariadb.org/browse/MDEV-21832))
* ALTER TABLE, InnoDB aborts while adding instant column for discarded tablespace ([MDEV-22446](https://jira.mariadb.org/browse/MDEV-22446))
* Optimizer, Wrong query results with `optimizer_switch="split_materialized=on"` ([MDEV-21614](https://jira.mariadb.org/browse/MDEV-21614))
* SHOW GRANTS does not quote role names properly ([MDEV-20076](https://jira.mariadb.org/browse/MDEV-20076))
* Paritioning INSERT chooses wrong partition for RANGE partitioning by DECIMAL column ([MDEV-21195](https://jira.mariadb.org/browse/MDEV-21195))
* mariadb-backup does not honor ignore\_db\_dirs from server config ([MDEV-19347](https://jira.mariadb.org/browse/MDEV-19347))
* mariadb-backup `--ftwrl-wait-timeout` never times out on explicit lock ([MDEV-20230](https://jira.mariadb.org/browse/MDEV-20230))
* FULLTEXT INDEX, Assertion \`\`!table->fts->in\_queue`' failed in` fts\_optimize\_remove\_table\` ([MDEV-21550](https://jira.mariadb.org/browse/MDEV-21550))
* Wrong estimate of affected BLOB columns in update of PRIMARY KEY ([MDEV-22384](https://jira.mariadb.org/browse/MDEV-22384))
* Duplicate key value is silently truncated to 64 characters in `print_keydup_error` ([MDEV-20604](https://jira.mariadb.org/browse/MDEV-20604))
* Session tracking returns incorrectly long tracking data ([MDEV-22504](https://jira.mariadb.org/browse/MDEV-22504))
* Add `pam_user_map.so` file to binary tarball package ([MDEV-21913](https://jira.mariadb.org/browse/MDEV-21913))
* Running out of file descriptors and eventual crash ([MDEV-18027](https://jira.mariadb.org/browse/MDEV-18027))
* mysql\_upgrade is made aware of the upstream slave tables to issue warnings when that takes place ([MDEV-10047](https://jira.mariadb.org/browse/MDEV-10047))
* Corruption for `SET GLOBAL innodb_` string variables ([MDEV-22393](https://jira.mariadb.org/browse/MDEV-22393))
* wsrep performance optimization ([MDEV-7962](https://jira.mariadb.org/browse/MDEV-7962))
* [mysqldump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysqldump) parameter, `--ignore-table-data`, added ([MDEV-22037](https://jira.mariadb.org/browse/MDEV-22037))
* Server can fail while replicating conditional comments (Bug#28388217)
* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) updated to 25.3.29
* Added the `xml-report` option to [mysql-test-run](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/testing-tools/mariadb-test/mariadb-test-run-pl-options) ([MDEV-22176](https://jira.mariadb.org/browse/MDEV-22176))
* Packages and [repositories](https://downloads.mariadb.org/mariadb/repositories/) for Ubuntu 20.04 "focal" added
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.3](what-is-mariadb-103.md) for Debian 8 "Jessie"
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2020-2752](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2752)
  * [CVE-2020-2812](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2812)
  * [CVE-2020-2814](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2814)
  * [CVE-2020-2760](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-2760)
  * [CVE-2020-13249](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-13249)

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.23](mariadb-10323-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10323-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.23](mariadb-10323-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-13-10-3-23-10-2-32-10-1-45-and-5-5-68-now-available).\
Thanks, and enjoy MariaDB!>

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
