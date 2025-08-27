# MariaDB 10.1.3 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.3) | [Release Notes](mariadb-10-1-3-release-notes.md) | [Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-3-changelog.md) | [Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 2 Mar 2015

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.3](mariadb-10-1-3-release-notes.md) is a [_**Beta**_](../../about/release-criteria.md) release. One should not expect any notable new features or incompatible interface changes in 10.1 after this release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

This is the first beta release in the [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) series. One should not expect any notable new features or incompatible interface changes in 10.1 after this release.

## Major new features

* [Table and Tablespace Encryption](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/encryption/data-at-rest-encryption/data-at-rest-encryption-overview).
* [Optimistic mode of in-order parallel replication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/parallel-replication#optimistic-mode-of-in-order-parallel-replication) ([MDEV-6676](https://jira.mariadb.org/browse/MDEV-6676)) and two new associated system variables:
  * [slave\_parallel\_mode](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables)
  * [skip\_parallel\_replication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables)
* Enhanced semisync replication ([MDEV-162](https://jira.mariadb.org/browse/MDEV-162))

## Other notable changes

* Consistent support for `IF EXISTS`, `IF NOT EXISTS`, and `OR REPLACE` clauses:
  * These statements now also support `IF NOT EXISTS` and `OR REPLACE`:
    * [CREATE DATABASE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-database) ([MDEV-7280](https://jira.mariadb.org/browse/MDEV-7280))
    * [CREATE FUNCTION UDF](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/user-defined-functions/create-function-udf) ([MDEV-7283](https://jira.mariadb.org/browse/MDEV-7283))
    * [CREATE ROLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/create-role) ([MDEV-7288](https://jira.mariadb.org/browse/MDEV-7288))
    * [CREATE SERVER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-server) ([MDEV-7285](https://jira.mariadb.org/browse/MDEV-7285))
    * [CREATE USER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/create-user) ([MDEV-7288](https://jira.mariadb.org/browse/MDEV-7288))
    * [CREATE VIEW](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/views/create-view) ([MDEV-7283](https://jira.mariadb.org/browse/MDEV-7283))
  * These statements now support `IF EXISTS`:
    * [DROP ROLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/drop-role) ([MDEV-7288](https://jira.mariadb.org/browse/MDEV-7288))
    * [DROP USER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/drop-user) ([MDEV-7288](https://jira.mariadb.org/browse/MDEV-7288))
* [InnoDB/XtraDB Page compression now supports snappy compression method](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression)
* Dump Thread Enhancements from Google ([MDEV-7257](https://jira.mariadb.org/browse/MDEV-7257))
* The [wsrep\_dirty\_reads](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_dirty_reads) system variable for permitting dirty [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) reads.
* new read-only server variable [version\_ssl\_library](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/encryption/data-in-transit-encryption/ssltls-system-variables) that shows the version of currently used SSL library.
* new command-line option [--getopt-prefix-matching](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/getting-installing-and-upgrading-mariadb/starting-and-stopping-mariadb/mariadbd-options) that makes it possible to disable historical "unambiguous prefix" matching in the command-line option parsing.
* [INFORMATION\_SCHEMA.APPLICABLE\_ROLES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/information-schema/information-schema-tables/information-schema-applicable_roles-table) table has a new `IS_DEFAULT` column ([MDEV-6918](https://jira.mariadb.org/browse/MDEV-6918)). See [SET DEFAULT ROLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/set-default-role).
* [INFORMATION\_SCHEMA.VIEWS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/views/information-schema-views-table) table has a new `ALGORITHM` column ([MDEV-6731](https://jira.mariadb.org/browse/MDEV-6731)).
* Improved concurrency: table definition cache now has lock-free implementation completely avoiding any global locks.
* [EXPLAIN FORMAT=JSON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/analyze-and-explain-statements/explain-format-json) now supports and prints more optimizations (range+MRR, "range checked for each record", full scan on NULL key, expensive constants, etc)

**Do not use&#x20;**_**beta**_**&#x20;releases on production systems!**

Repositories exist for 10.1, but because 10.1 is still Beta, they are not visible in the [repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/). To configure a 10.1 apt, yum, or zypper repository using the tool, simply select 10.0 and then when executing the instructions, manually change all occurrences of '10.0' to '10.1'.

For a complete list of changes made in [MariaDB 10.1.3](mariadb-10-1-3-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10-1-3-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
