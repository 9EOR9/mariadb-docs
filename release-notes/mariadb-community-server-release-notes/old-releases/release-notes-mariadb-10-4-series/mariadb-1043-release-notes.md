# MariaDB 10.4.3 Release Notes

The most recent release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download](https://downloads.mariadb.org/mariadb/10.4.3)[Release Notes](mariadb-1043-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-1043-changelog.md)[Overview of 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104)

**Release date:** 25 Feb 2019

[MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is the current _development_ series of MariaDB. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.3](mariadb-1043-release-notes.md) is a [_**Release Candidate**_](../../../mariadb-release-criteria.md) release.

**Do not use non-stable (non-GA) releases in production!**

**For an overview of** [**MariaDB 10.4**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) **see the**[**What is MariaDB 10.4?**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

Notable changes of this release include:

* [MDEV-12484](https://jira.mariadb.org/browse/MDEV-12484): The [unix\_socket authentication plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-unix-socket) is now default on Unix-like systems, which is a major change to authentication in MariaDB
* [MDEV-11340](https://jira.mariadb.org/browse/MDEV-11340): Allow multiple alternative authentication methods for the same user
* [MDEV-7597](https://jira.mariadb.org/browse/MDEV-7597): [User password expiry](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/user-account-management/user-password-expiry)
* [MDEV-6111](https://jira.mariadb.org/browse/MDEV-6111): Implementation of the [optimizer trace](https://mariadb.com/docs/general-resources/development-articles/mariadb-internals/mariadb-internals-documentation-query-optimizer/mariadb-internals-documentation-optimizer-trace), one can enable the optimizer trace by enabling the system variable [optimizer\_trace](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#optimizer_trace)
* [Temporal tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables) extended with support for [application-time periods](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/application-time-periods) ([MDEV-16973](https://jira.mariadb.org/browse/MDEV-16973), [MDEV-16974](https://jira.mariadb.org/browse/MDEV-16974), [MDEV-16975](https://jira.mariadb.org/browse/MDEV-16975), [MDEV-17082](https://jira.mariadb.org/browse/MDEV-17082))
* [MDEV-18551](https://jira.mariadb.org/browse/MDEV-18551): The default for [eq\_range\_index\_dive\_limit](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#eq_range_index_dive_limit) is now `200` (previously `0`)
* [MDEV-17903](https://jira.mariadb.org/browse/MDEV-17903): The [optimizer switch](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/optimizer-switch) flag `optimize_join_buffer_size` now defaults to `on`
* New [optimizer switch](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/optimizer-switch) flags `rowid_filter` and `condition_pushdown_from_having`
* [MDEV-18439](https://jira.mariadb.org/browse/MDEV-18439): [core\_file](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#core_file) on Windows now defaults to `ON`
* [MDEV-18608](https://jira.mariadb.org/browse/MDEV-18608): [Histograms](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/histogram-based-statistics) are now used (but not collected) by default.
* [MDEV-13916](https://jira.mariadb.org/browse/MDEV-13916): The [JSON\_VALID](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_valid) function is automatically used as a [CHECK constraint](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/constraint#check-constraints) for the [JSON data type alias](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/json) in order to ensure that a valid json document is inserted
* [Spider](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider) updated to 3.3.14
* Unique indexes can be created on [BLOB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/blob) or [TEXT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/text) fields ([MDEV-371](https://jira.mariadb.org/browse/MDEV-371))
* [MDEV-18564](https://jira.mariadb.org/browse/MDEV-18564): [wsrep\_load\_data\_splitting](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_load_data_splitting) is deprecated and now set to `OFF` by default
* [analyze\_sample\_percentage](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#analyze_sample_percentage) system variable
* InnoDB ALTER TABLE fixes: [MDEV-18222](https://jira.mariadb.org/browse/MDEV-18222), [MDEV-18256](https://jira.mariadb.org/browse/MDEV-18256), [MDEV-18016](https://jira.mariadb.org/browse/MDEV-18016), [MDEV-18295](https://jira.mariadb.org/browse/MDEV-18295), [MDEV-16849](https://jira.mariadb.org/browse/MDEV-16849), [MDEV-18219](https://jira.mariadb.org/browse/MDEV-18219)
* mariadb-backup fixes: [MDEV-18194](https://jira.mariadb.org/browse/MDEV-18194), [MDEV-18415](https://jira.mariadb.org/browse/MDEV-18415), [MDEV-18611](https://jira.mariadb.org/browse/MDEV-18611)
* New InnoDB features:
  * [MDEV-12026](https://jira.mariadb.org/browse/MDEV-12026): Implement [innodb\_checksum\_algorithm=full\_crc32](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_checksum_algorithm)
  * [MDEV-15563](https://jira.mariadb.org/browse/MDEV-15563): More Instant VARCHAR extension
  * [MDEV-15564](https://jira.mariadb.org/browse/MDEV-15564): Instant collation or charset changes for non-indexed columns
  * [MDEV-16188](https://jira.mariadb.org/browse/MDEV-16188): Use in-memory PK filters built from range index scans
* Debian has stopped supporting the ppc64el architecture for Debian 8\
  Jessie and so this is the last release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) on Jessie for that\
  architecture
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 10.4.3](mariadb-1043-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-1043-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.3](mariadb-1043-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-3-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
