# MariaDB 10.1.2 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.2)[Release Notes](mariadb-10-1-2-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-2-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 7 Dec 2014

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

This is an [_**Alpha**_](../../about/release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the third alpha release in the [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) series.

Notable changes of this release include:

* [--mysql56-temporal-format](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#mysql56_temporal_format)\
  option to use the MySQL-5.6 low level formats to store [TIME](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/time), [DATETIME](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/datetime) and [TIMESTAMP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/timestamp) types. ([MDEV-5528](https://jira.mariadb.org/browse/MDEV-5528))
* Support for Spatial Reference systems for the GIS data ([MDEV-60](https://jira.mariadb.org/browse/MDEV-60)), new `REF_SYSTEM_ID` column attribute can be used to specify Spatial Reference System ID for columns of spatial data types:

```sql
CREATE TABLE t1(g GEOMETRY(9,4) REF_SYSTEM_ID=101);
```

It can be queried via the [INFORMATION\_SCHEMA.GEOMETRY\_COLUMNS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/information-schema/information-schema-tables/information-schema-geometry_columns-table) table.

* [INFORMATION\_SCHEMA.SPATIAL\_REF\_SYS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/information-schema/information-schema-tables/information-schema-spatial_ref_sys-table) table.
* More functions from the [OGC](https://www.opengeospatial.org/) standard added ([MDEV-4045](https://jira.mariadb.org/browse/MDEV-4045)):
  * [ST\_Boundary](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/geometry-properties/st_boundary)
  * [ST\_ConvexHull](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/geometry-constructors/st_convexhull)
  * [ST\_IsRing](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/geometry-properties/st_isring)
  * [ST\_PointOnSurface](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/geometry-constructors/st_pointonsurface)
  * [ST\_Relate](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/geometry-properties/st_relate)
* Per-query variables - see [SET STATEMENT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/set-commands/set-statement) ([MDEV-5231](https://jira.mariadb.org/browse/MDEV-5231))
* [EXPLAIN FORMAT=JSON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/analyze-and-explain-statements/explain-format-json) ([MDEV-6109](https://jira.mariadb.org/browse/MDEV-6109))
* Scalability fixes ([MDEV-7004](https://jira.mariadb.org/browse/MDEV-7004)). Up to 60% higher throughput in sysbench benchmarks on Power8.
* [Password validation plugin API](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/mariadb-internals/password-validation) ([MDEV-6431](https://jira.mariadb.org/browse/MDEV-6431)).
* [simple\_password\_check](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/password-validation-plugins/simple-password-check-plugin) password validation plugin. It can enforce a minimum password length and guarantee that a password contains at least a specified number of uppercase and lowercase letters, digits, and punctuation characters.
* Assisted discovery in the [OQGRAPH Storage Engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/oqgraph-storage-engine) ([MDEV-5871](https://jira.mariadb.org/browse/MDEV-5871))
* [cracklib\_password\_check](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/password-validation-plugins/cracklib-password-check-plugin) password validation plugin. It only allows passwords that are strong enough to pass [CrackLib](https://sourceforge.net/projects/cracklib/) test. This is the same test that `pam_cracklib.so` does, installed by default on many Linux distributions.
* The number of rows affected by a slow UPDATE or DELETE is now recorded in the [slow query log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/slow-query-log) - see also [mysql.slow\_log Table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/the-mysql-database-tables/mysql-slow_log-table). ([MDEV-4412](https://jira.mariadb.org/browse/MDEV-4412))
* [GET\_LOCK()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/miscellaneous-functions/get_lock) now supports microseconds in the timeout, no longer rounding fractions to the nearest integer ([MDEV-4018](https://jira.mariadb.org/browse/MDEV-4018))
* domain\_id based replication filters - see [CHANGE MASTER TO](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/replication-statements/change-master-to) ([MDEV-6593](https://jira.mariadb.org/browse/MDEV-6593))
* Two new Information Schema tables for examining wsrep information, [WSREP\_MEMBERSHIP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/information-schema/information-schema-tables/information-schema-wsrep_membership-table) and [WSREP\_STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/information-schema/information-schema-tables/information-schema-wsrep_status-table) ([MDEV-7053](https://jira.mariadb.org/browse/MDEV-7053))
* [innodb\_log\_compressed\_pages](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables) is now set to `OFF` by default.
* The Facebook Prefix Index Queries Optimization ([MDEV-6929](https://jira.mariadb.org/browse/MDEV-6929)), enabled with [innodb\_prefix\_index\_cluster\_optimization](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables) and two new status variables, [Innodb\_secondary\_index\_triggered\_cluster\_reads](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables) and [Innodb\_secondary\_index\_triggered\_cluster\_reads\_avoided](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables) to track its effectiveness.
* Default size of [query\_alloc\_block\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#query_alloc_block_size) changed from `8192` to `16384` and [query\_prealloc\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#query_prealloc_size) from `8192` to `24576` to avoid the need for simple queries with one join to call `my_malloc`.
* Other Webscale patches ([MDEV-6039](https://jira.mariadb.org/browse/MDEV-6039))
* [Out parameters in PREPARE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/prepared-statements/out-parameters-in-prepare) were removed, as it was decided to rather implement the feature in a standard way.

**Do not use&#x20;**_**alpha**_**&#x20;releases on production systems!**

Repositories exist for 10.1, but because 10.1 is still Alpha, they are not visible in the [repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/). To configure a 10.1 apt, yum, or zypper repository using the tool, simply select 10.0 and then when executing the instructions, manually change all occurrences of '10.0' to '10.1'.

For a complete list of changes made in [MariaDB 10.1.2](mariadb-10-1-2-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-2-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
