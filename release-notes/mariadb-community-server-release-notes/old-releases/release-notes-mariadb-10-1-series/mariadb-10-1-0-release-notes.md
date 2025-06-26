# MariaDB 10.1.0 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.0)[Release Notes](mariadb-10-1-0-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-0-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 30 Jun 2014

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.0](mariadb-10-1-0-release-notes.md) is an [_**Alpha**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the first alpha release in the [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) series.

Notable changes of this release include:

* InnoDB/XtraDB
  * [MDEV-6075](https://jira.mariadb.org/browse/MDEV-6075), Allow > 16K pages on InnoDB - InnoDB now allows [page size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) to be configured as 16K, 32K and 64K. Note that single row size must be < 16K. This feature will allow especially more blob columns to be created.
  * [MDEV-5335](https://jira.mariadb.org/browse/MDEV-5335), Force PK option - Added a new dynamic configuration variable [innodb\_force\_primary\_key](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) default off. If option is true, create table without primary key or unique key where all keyparts are NOT NULL is not accepted. Instead an error message is printed. Variable value can be changed with set global innodb\_force\_primary\_key = .
* Security
  * [MDEV-5730](https://jira.mariadb.org/browse/MDEV-5730), enhance security using special compilation options - MariaDB is now compiled with security hardening options by default. It\
    is an additional protection layer that makes new, yet unknown, security\
    vulnerabilities more difficult to exploit.
* Storage Engine functionality
  * [MDEV-6107](https://jira.mariadb.org/browse/MDEV-6107), merge default\_tmp\_storage\_engine - Added [default\_tmp\_storage\_engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#default_tmp_storage_engine) server variable and the command line\
    option.
  * [MDEV-4260](https://jira.mariadb.org/browse/MDEV-4260), Don't create frm files for temporary tables - Temporary tables no longer create frm files on disk. Which means that if the temporary table is created in the [MEMORY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/memory-storage-engine) engine, it will not touch the disk at all.
  * The [ARCHIVE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/archive) storage engine is no longer enabled by default, and the plugin needs to be specifically enabled.
  * The [BLACKHOLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/blackhole) storage engine is no longer enabled by default, and the plugin needs to be specifically enabled.
* Optimizer
  * [MDEV-406](https://jira.mariadb.org/browse/MDEV-406), [ANALYZE $stmt](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/analyze-and-explain-statements/analyze-statement) - Check how close the optimizer's estimates about the query plan are to the reality.
* Administration
  * [MDEV-6248](https://jira.mariadb.org/browse/MDEV-6248), GUI-friendly cmake options to enable/disable plugins - MariaDB now uses PLUGIN\_xxx cmake options to enable or disable plugins, not a combination of WITH\_xxx, WITHOUT\_xxx, WITH\_PLUGINX\_xxx, WITHOUT\_PLUGIN\_xxx, WITH\_xxx\_STORAGE\_ENGINE, WITHOUT\_xxx\_STORAGE\_ENGINE. See [Specifying What Plugins to Build](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/compiling-mariadb-from-source/compiling-mariadb-with-extra-modulesoptions/specifying-which-plugins-to-build).
* Improvements from WebScaleSQL
  * Fix errors detected by [ASan](https://www.chromium.org/developers/testing/addresssanitizer) at compile time - Not merged but ASan was run against MariaDB. It generated the following:
    * [MDEV-6314](https://jira.mariadb.org/browse/MDEV-6314) - Compile/run MariaDB with ASan (fixed in 10.0.13)
    * [MDEV-6315](https://jira.mariadb.org/browse/MDEV-6315) - TokuDB: ERROR: AddressSanitizer: attempting to call malloc\_usable\_size() for pointer which is not owned: 0x601200008f80 (not fixed)
    * [MDEV-6323](https://jira.mariadb.org/browse/MDEV-6323) - ‘explain\_node’ may be used uninitialized in this function (not fixed)
    * [MDEV-6325](https://jira.mariadb.org/browse/MDEV-6325) - TokuDB: hatoku\_hton.cc:1021:5: warning: ‘do\_commit’ may be used uninitialized in this function (not fixed)
  * [MDEV-6329](https://jira.mariadb.org/browse/MDEV-6329), Fix errors detected by ASan at runtime. Merged to 5.5.39.
  * Use single quotes for perl paths, in case of special symbols. Merged to 10.0.13.
  * Stop spawning dummy threads on client library initialization. Merged to 10.0.13.
* Performance
  * [MDEV-6249](https://jira.mariadb.org/browse/MDEV-6249), Disable [Performance Schema](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/performance-schema) by default
  * [MDEV-6246](https://jira.mariadb.org/browse/MDEV-6246), Merge 10.0.10-FusionIO to 10.1 - [Atomic writes](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/configuring-mariadb/mariadb-performance-advanced-configurations/atomic-write-support), [multi-threaded flushing and page compression](https://blog.mariadb.org/significant-performance-boost-with-new-mariadb-page-compression-on-fusionio/) are available for Fusion-IO devices in 10.1.0

**Do not use&#x20;**_**alpha**_**&#x20;releases on production systems!**

For a complete list of changes made in [MariaDB 10.1.0](mariadb-10-1-0-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-0-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
