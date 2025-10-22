# MariaDB 12.1.1 Release Notes

{% include "../../.gitbook/includes/latest-12-1.md" %}

<a href="https://downloads.mariadb.org/mariadb/12.1.1/" class="button primary">Download</a> <a href="mariadb-12.1.1-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-12.1-series/mariadb-12.1.1-changelog.md" class="button secondary">Changelog</a> <a href="changes-and-improvements-in-mariadb-12.1.md" class="button secondary">Overview of 12.1</a>

**Release date:** 7 Aug 2025

{% include "../../.gitbook/includes/non-stable.md" %}

[MariaDB 12.1](changes-and-improvements-in-mariadb-12.1.md) is a [rolling release](../about/release-model.md). It is an evolution of [MariaDB 12.0](../release-notes-mariadb-12.0-rolling-releases/what-is-mariadb-120.md) with several entirely new features.

MariaDB 12.1.1 is a [_**Release Candidate (RC)**_](../about/release-criteria.md) release.

{% hint style="success" %}
**For an overview of MariaDB 12.1 see the** [**MariaDB 12.1 Changes & Improvements**](changes-and-improvements-in-mariadb-12.1.md) **page.**
{% endhint %}

Thanks, and enjoy MariaDB!

## New Features

### Performance improvements <a href="#performance-improvements" id="performance-improvements"></a>

* Segmented key cache for [Aria storage engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/aria) ([MDEV-24](https://jira.mariadb.org/browse/MDEV-24))
  * [aria\_pagecache\_segments](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/aria/aria-system-variables#aria_pagecache_segments) system variable
* MDL scalability improvements ([MDEV-19749](https://jira.mariadb.org/browse/MDEV-19749))
* Parallel replication for [Galera](https://app.gitbook.com/o/diTpXxF5WsbHqTReoBsS/s/3VYeeVGUV4AMqrA3zwy7/) replicas ([MDEV-20065](https://jira.mariadb.org/browse/MDEV-20065))
* Buffered logging for [audit plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/mariadb-audit-plugin) ([MDEV-34680](https://jira.mariadb.org/browse/MDEV-34680))
* Faster [vector](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/vectors) distance calculations via extrapolation ([MDEV-36205](https://jira.mariadb.org/browse/MDEV-36205))

### Compatibility features <a href="#compatibility-features" id="compatibility-features"></a>

* caching\_sha2\_password plugin ([MDEV-9804](https://jira.mariadb.org/browse/MDEV-9804))
* ( + ) for outer join syntax ([MDEV-13817](https://jira.mariadb.org/browse/MDEV-13817))
* Add [semisynchronous replication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/semisynchronous-replication) variable, [rpl\_semi\_sync\_master\_wait\_for\_slave\_count](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/semisynchronous-replication#rpl_semi_sync_master_wait_for_slave_count) ([MDEV-18983](https://jira.mariadb.org/browse/MDEV-18983))
* Associative arrays: DECLARE TYPE .. TABLE OF .. INDEX BY ([MDEV-34319](https://jira.mariadb.org/browse/MDEV-34319))
* [DROP USER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/drop-user) will now by default issue a warning if the user has active sessions, or fail in [Oracle mode](../about/compatibility-and-differences/sql_modeoracle.md) ([MDEV-35617](https://jira.mariadb.org/browse/MDEV-35617))
* Optimizer hints: \[NO\_]JOIN\_INDEX, \[NO\_]GROUP\_INDEX, \[NO\_]ORDER\_INDEX, \[NO\_]INDEX ([MDEV-35856](https://jira.mariadb.org/browse/MDEV-35856))
* Optimizer hints: \[NO\_]SPLIT\_MATERIALIZED ([MDEV-36092](https://jira.mariadb.org/browse/MDEV-36092))
* Optimizer hints: \[NO\_]DERIVED\_CONDITION\_PUSHDOWN, \[NO\_]MERGE ([MDEV-36106](https://jira.mariadb.org/browse/MDEV-36106))

### Miscellaneous <a href="#miscellaneous" id="miscellaneous"></a>

* Add [analyze\_max\_length](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/variables-and-modes/server-system-variables#analyze_max_length) option to not collect statistics for long char/varchars ([MDEV-36536](https://jira.mariadb.org/browse/MDEV-36536))
* Retry applying of write sets on galera nodes ([MDEV-36077](https://jira.mariadb.org/browse/MDEV-36077))
* [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) now supports wildcards with the `-L` or `--wildcards` option ([MDEV-21376](https://jira.mariadb.org/browse/MDEV-21376))
* Per-table unique FOREIGN KEY constraint names ([MDEV-28933](https://jira.mariadb.org/browse/MDEV-28933))
* Support for functional indexes in GROUP/ORDER BY ([MDEV-36132](https://jira.mariadb.org/browse/MDEV-36132))
* Include definitions of tables and views in the optimizer trace ([MDEV-36483](https://jira.mariadb.org/browse/MDEV-36483))

## Changelog

For a complete list of changes made in MariaDB 12.1.1, with links to detailed information on each push, see the [changelog](../changelogs/changelogs-mariadb-12.1-series/mariadb-12.1.1-changelog.md).

***

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
