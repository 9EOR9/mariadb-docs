# MariaDB 5.2.0 Release Notes

The most recent release in the [MariaDB 5.2 series](changes-improvements-in-mariadb-5-2.md) is:[**MariaDB 5.2.14**](mariadb-5214-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.2.0-beta) | **Release Notes** | [Changelog](../../changelogs/changelogs-mariadb-52-series/mariadb-520-changelog.md) |[Overview of 5.2](changes-improvements-in-mariadb-5-2.md)

**Release date:** 10 Apr 2010

### Release Notes

See the [MariaDB versus MySQL](https://mariadb.com/docs/release-notes/compatibility-and-differences/mariadb-vs-mysql-compatibility) page for a high-level overview of the differences between MariaDB and MySQL. For a description of this release see the [MariaDB 5.1 overview](../release-notes-mariadb-5-1-series/changes-improvements-in-mariadb-5-1.md).

This is a beta release of MariaDB. We believe it to be relatively bug-free, and want to get it out so everyone can try it. Development is ongoing, see [MariaDB 5.2 TODO](https://askmonty.org/wiki/MariaDB_5.2_TODO) for a list of features that are planned for future [MariaDB 5.2](changes-improvements-in-mariadb-5-2.md) releases.

New features and changes in this version include:

#### [userstatv2](https://www.percona.com/docs/wiki/patches:userstatv2) patch from Percona

* This patch enables the gathering of more detailed statistics in [MariaDB 5.2](changes-improvements-in-mariadb-5-2.md).\
  As part of this patch, several new [INFORMATION\_SCHEMA](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/information-schema)\
  tables (with corresponding new `FLUSH` and`SHOW` commands) have been added. See:[User Statistics](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/user-statistics) for details.

#### Virtual columns patch (Contribution)

* We've added `VIRTUAL` and `PERSISTENT` virtual\
  columns to [MariaDB 5.2](changes-improvements-in-mariadb-5-2.md). See: [Virtual columns](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/generated-columns) for details.

#### Add a mysqlbinlog option to change the used database. [MWL#36](https://askmonty.org/worklog/?tid=36)

* We've added a new `--rewrite-db=name` option to mysqlbinlog\
  for applying updates to a database with a different name than the original.\
  See: [mysqlbinlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog) for details.

#### Maria storage engine group commit

* Two new system variables have been added:`maria_group_commit` and`maria_group_commit_interval`. See[Server System Variables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables) for details.

#### Backport libservices [MWL#98](https://askmonty.org/worklog/?tid=98)

* We've backported the[MySQL 5.5 Services for Plugins](https://dev.mysql.com/doc/refman/5.5/en/plugin-services.html)\
  to [MariaDB 5.2](changes-improvements-in-mariadb-5-2.md).

#### Fix the packaging scripts [MWL#88](https://askmonty.org/worklog/?tid=88)

* We updated the packaging scripts in [MariaDB 5.2](changes-improvements-in-mariadb-5-2.md) to fix some errors.

#### Pluggable authentication.[MWL#101](https://askmonty.org/worklog/?tid=101)

* In [MariaDB 5.2](changes-improvements-in-mariadb-5-2.md) the authentication of users is delegated to plugins. See:[Pluggable authentication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/pluggable-authentication-overview) for details.

#### Additional information added to engine description, new MariaDB plugin declaration [MWL#61](https://askmonty.org/worklog/?tid=61)

* We've added two new columns to the[INFORMATION\_SCHEMA.PLUGINS table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/information-schema/information-schema-tables/plugins-table-information-schema).
* For plugin authors: As part of this change, the MariaDB plugin declaration\
  now differs slightly from the MySQL plugin declaration (the MySQL plugin\
  declaration is still supported for dynamically loaded plugins). See:[Writing Plugins](https://mariadb.com/docs/general-resources/development-articles/mariadb-internals/development-writing-plugins-for-mariadb) for details.

#### Segmented Key Cache for MyISAM [MWL#85](https://askmonty.org/worklog/?tid=85)

* [Segmented Key Cache](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/segmented-key-cache)

#### New engine-defined options in the CREATE TABLE [MWL#43](https://askmonty.org/worklog/?tid=43)

* Storage engines can now allow the user to specify additional attributes per\
  index, field, or table. The engine needs to declare what attributes it\
  introduces. See: [Extending CREATE TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/storage-engines-storage-engine-development/engine-defined-new-tablefieldindex-attributes) for more\
  information.

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
