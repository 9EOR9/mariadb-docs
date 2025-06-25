# MariaDB 10.11.0 Release Notes

The most recent release of [MariaDB 10.11](what-is-mariadb-1011.md) is:[**MariaDB 10.11.11**](mariadb-10-11-11-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.11.11/)

[Download](https://downloads.mariadb.org/mariadb/10.11.0)[Release Notes](mariadb-10-11-0-release-notes.md)[Overview of 10.11](what-is-mariadb-1011.md)

**Release date:** 26 Sep 2022

**Do not use&#x20;**_**alpha**_**&#x20;releases in production!**

[MariaDB 10.11](what-is-mariadb-1011.md) is a current development series of MariaDB. It is an evolution\
of [MariaDB 10.10](../old-releases/release-notes-mariadb-10-10-series/what-is-mariadb-1010.md) with several entirely new features.

Unlike recent new releases, [MariaDB 10.11.0](mariadb-10-11-0-release-notes.md) is a single preview release. Features are to be considered preview, and none are guaranteed to make it into [MariaDB 10.11](what-is-mariadb-1011.md).

The preview is available as a container **quay.io/mariadb-foundation/mariadb-devel:10.11-preview**.

**For an overview of** [**MariaDB 10.11**](what-is-mariadb-1011.md) **see the**[**What is MariaDB 10.11?**](what-is-mariadb-1011.md) **page.**

Thanks, and enjoy MariaDB!

### Authentication

* Windows - passwordless login for mariadb root user, for OS admin users, using the [gssapi authentication plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-gssapi) ([MDEV-26715](https://jira.mariadb.org/browse/MDEV-26715))
* [GRANT to PUBLIC](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#to-public) ([MDEV-5215](https://jira.mariadb.org/browse/MDEV-5215)) ([blog post](https://mariadb.org/grant-to-public-in-mariadb/))
* Separate [SUPER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#super) and [READ ONLY ADMIN](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/grant#read_only-admin) privileges ([MDEV-29596](https://jira.mariadb.org/browse/MDEV-29596))

### Optimizer

* Semi-join optimization for single-table update/delete statements ([MDEV-7487](https://jira.mariadb.org/browse/MDEV-7487))
* Allow pushdown of queries involving UNIONs in outer select to foreign engines ([MDEV-25080](https://jira.mariadb.org/browse/MDEV-25080))
* Make [ANALYZE FORMAT=JSON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/analyze-and-explain-statements/analyze-format-json) show time spent in the query optimizer ([MDEV-28926](https://jira.mariadb.org/browse/MDEV-28926))

### Information Schema

* Performance Issues reading the [Information Schema Parameters table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-parameters-table) ([MDEV-29104](https://jira.mariadb.org/browse/MDEV-29104))
* Full table scan in the [Information Schema Parameters](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-parameters-table) and [Information Schema Routines](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-routines-table) tables ([MDEV-20609](https://jira.mariadb.org/browse/MDEV-20609))

### System versioning

* [System versioning](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/system-versioned-tables) setting, [system\_versioning\_insert\_history](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/system-versioned-tables#system_versioning_insert_history), to allow history modification ([MDEV-16546](https://jira.mariadb.org/browse/MDEV-16546))
* [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysqldump): dump and restore historical data ([MDEV-16029](https://jira.mariadb.org/browse/MDEV-16029))

### InnoDB

* [innodb\_write\_io\_threads](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_write_io_threads) and [innodb\_read\_io\_threads](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_read_io_threads) are now dynamic, and their values can be changed without restarting the server ([MDEV-11026](https://jira.mariadb.org/browse/MDEV-11026))

### General

* Rename [slow queries](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/slow-query-log) variables ([MDEV-7567](https://jira.mariadb.org/browse/MDEV-7567))
  * [log\_slow\_min\_examined\_row\_limit](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#log_slow_min_examined_row_limit) (min\_examined\_row\_limit)
  * [log\_slow\_query](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#log_slow_query) (slow\_query\_log)
  * [log\_slow\_query\_file\_name](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#log_slow_query_file) (slow\_query\_log\_file) This will be renamed to [log\_slow\_query\_file](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#log_slow_query_file) in the next [MariaDB 10.11](what-is-mariadb-1011.md) release.
  * [log\_slow\_query\_time](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#log_slow_query_time) (long\_query\_time)
* [replicate\_rewrite\_db](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#replicate_rewrite_db) is now a system variable, no longer just an option ([MDEV-15530](https://jira.mariadb.org/browse/MDEV-15530))

**Do not use&#x20;**_**alpha**_**&#x20;releases on production systems!**\
For a complete list of changes made in [MariaDB 10.11.0](mariadb-10-11-0-release-notes.md), with links to detailed\
information on each push, see the [changelog](../changelogs/changelogs-mariadb-101-series/mariadb-10110-changelog.md).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
