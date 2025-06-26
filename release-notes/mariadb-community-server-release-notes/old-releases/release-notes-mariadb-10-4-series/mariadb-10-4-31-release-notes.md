# MariaDB 10.4.31 Release Notes

[Download](https://mariadb.com/downloads/)[Release Notes](mariadb-10-4-31-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10-4-31-changelog.md)[Overview of 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.4.31/)

**Release date:** 14 Aug 2023

[MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) is a previous _stable_ series of MariaDB, [maintained until](https://mariadb.org/about/#maintenance-policy) June 2024. It is an evolution of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else and with backported and reimplemented features from MySQL.

[MariaDB 10.4.31](mariadb-10-4-31-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) **see the**[**What is MariaDB 10.4?**](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/what-is-mariadb-104) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### General

* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.4](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series) for Ubuntu 18.04 LTS "Bionic"
* [mysqldump --force](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) doesn't ignore error as it should ([MDEV-31092](https://jira.mariadb.org/browse/MDEV-31092))
* [ROW](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/row) variables do not get assigned from subselects ([MDEV-31250](https://jira.mariadb.org/browse/MDEV-31250))
* Crash after setting global session\_track\_system\_variables to an invalid value ([MDEV-25237](https://jira.mariadb.org/browse/MDEV-25237))
* ODKU of non-versioning column inserts history row ([MDEV-23100](https://jira.mariadb.org/browse/MDEV-23100))
* UPDATE not working properly on transaction precise system versioned table ([MDEV-25644](https://jira.mariadb.org/browse/MDEV-25644))
* Assertion \`\`const\_item\_cache == true'`failed in`Item\_func::fix\_fields\` ([MDEV-31319](https://jira.mariadb.org/browse/MDEV-31319))
* ANALYZE doesn't work with pushed derived tables ([MDEV-29284](https://jira.mariadb.org/browse/MDEV-29284))
* `get_partition_set` is never executed in `ha_partition::multi_range_key_create_key` due to bitwise & with 0 constant ([MDEV-24712](https://jira.mariadb.org/browse/MDEV-24712))
* Client can crash the server with a `mysql_list_fields("view")` call ([MDEV-30159](https://jira.mariadb.org/browse/MDEV-30159))
* `I_S.parameters` not immediatly changed updated after procedure change ([MDEV-31064](https://jira.mariadb.org/browse/MDEV-31064))

### Character Sets, Data Types

* UBSAN: null pointer passed as argument 1, which is declared to never be null in `my_strnncoll_binary` on `SELECT ... COUNT` or `GROUP_CONCAT` ([MDEV-28384](https://jira.mariadb.org/browse/MDEV-28384))
* Possibly wrong result or Assertion `0' failed in` Item\_func\_round::native\_op\` ([MDEV-23838](https://jira.mariadb.org/browse/MDEV-23838))
* Assertion \`\`(length % 4) == 0'`failed in`my\_lengthsp\_utf32`on`SELECT\` ([MDEV-29019](https://jira.mariadb.org/browse/MDEV-29019))
* UBSAN: negation of -X cannot be represented in type `'long long int'`; cast to an unsigned type to negate this value to itself in `Item_func_mul::int_op` and `Item_func_round::int_op` ([MDEV-30932](https://jira.mariadb.org/browse/MDEV-30932))
* Assorted assertion failures in json\_find\_path with certain collations ([MDEV-23187](https://jira.mariadb.org/browse/MDEV-23187))

### InnoDB

* innochecksum dies with Floating point exception ([MDEV-31641](https://jira.mariadb.org/browse/MDEV-31641))
* Deadlock with 3 concurrent [DELETEs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/delete) by [unique key](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/mariadb-quickstart-guides/mariadb-indexes-guide#unique-index) ([MDEV-10962](https://jira.mariadb.org/browse/MDEV-10962))
* Assertion \`\`!strcmp(index->table->name.m\_name, "SYS\_FOREIGN") || !strcmp(index->table->name.m\_name, "SYS\_FOREIGN\_COLS")'`failed in`btr\_node\_ptr\_max\_size\` ([MDEV-19216](https://jira.mariadb.org/browse/MDEV-19216))
* `MODIFY COLUMN` can break FK constraints, and lead to unrestorable dumps ([MDEV-31086](https://jira.mariadb.org/browse/MDEV-31086))

### Aria

* Various crashes upon INSERT/UPDATE after changing Aria settings ([MDEV-28054](https://jira.mariadb.org/browse/MDEV-28054))
* Various crashes/asserts/corruptions when Aria encryption is enabled/used, but the encryption plugin is not loaded ([MDEV-26258](https://jira.mariadb.org/browse/MDEV-26258))

### Spider

* SIGSEGV in `spider_db_open_item_field` and SIGSEGV in `spider_db_print_item_type`, on SELECT ([MDEV-29447](https://jira.mariadb.org/browse/MDEV-29447))
* [Spider variables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider/spider-system-variables) that double as table params overriding mechanism is buggy ([MDEV-31524](https://jira.mariadb.org/browse/MDEV-31524))

### Optimizer

* Assertion \`\`last\_key\_entry >= end\_pos'`failed in virtual bool`JOIN\_CACHE\_HASHED::put\_record()\` ([MDEV-31348](https://jira.mariadb.org/browse/MDEV-31348))
* Problem with open ranges on prefix blobs keys ([MDEV-31800](https://jira.mariadb.org/browse/MDEV-31800))
* Equal on two [RANK](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/window-functions/rank) [window functions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/window-functions) create wrong result ([MDEV-20010](https://jira.mariadb.org/browse/MDEV-20010))
* Recursive CTE execution is interrupted without errors or warnings ([MDEV-31214](https://jira.mariadb.org/browse/MDEV-31214))
* `MAX_SEL_ARG` memory exhaustion is not visible in the optimizer trace ([MDEV-30964](https://jira.mariadb.org/browse/MDEV-30964))
* [SHOW TABLES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-tables) not working properly with `lower_case_table_names=2` ([MDEV-30765](https://jira.mariadb.org/browse/MDEV-30765))
* Segfault on select query using index for group-by and filesort ([MDEV-30143](https://jira.mariadb.org/browse/MDEV-30143))

### Replication

* Parallel Slave SQL Thread Can Update Seconds\_Behind\_Master with Active Workers ([MDEV-30619](https://jira.mariadb.org/browse/MDEV-30619))
* [ALTER SEQUENCE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sequences/alter-sequence) ends up in optimistic parallel slave binlog out-of-order ([MDEV-31503](https://jira.mariadb.org/browse/MDEV-31503))
* [STOP SLAVE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/replication-statements/stop-replica) takes very long time on a busy system ([MDEV-13915](https://jira.mariadb.org/browse/MDEV-13915))
* rpl.rpl\_manual\_change\_index\_file occasionally fails in BB with Result length mismatch ([MDEV-30214](https://jira.mariadb.org/browse/MDEV-30214))

### Galera

* Node has been dropped from the cluster on Startup / Shutdown with async replica ([MDEV-31413](https://jira.mariadb.org/browse/MDEV-31413))
* MariaDB stuck on starting commit state (waiting on commit order critical section) ([MDEV-29293](https://jira.mariadb.org/browse/MDEV-29293))
* Assertion `state() == s_aborting || state() == s_must_replay` failed in int wsrep::transaction::after\_rollback() ([MDEV-30013](https://jira.mariadb.org/browse/MDEV-30013))
* Assertion `!wsrep_has_changes(thd) || (thd->lex->sql_command == SQLCOM_CREATE_TABLE && !thd->is_current_stmt_binlog_format_row()) || thd->wsrep_cs().transaction().state() == wsrep::transaction::s_aborted` failed ([MDEV-30388](https://jira.mariadb.org/browse/MDEV-30388))
* Server crashes when wsrep\_sst\_donor and wsrep\_cluster\_address set to NULL ([MDEV-28433](https://jira.mariadb.org/browse/MDEV-28433))
* Create temporary sequence can cause inconsistency ([MDEV-31335](https://jira.mariadb.org/browse/MDEV-31335))
* Galera 4 unable to query cluster state if not primary component ([MDEV-21479](https://jira.mariadb.org/browse/MDEV-21479))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-`-``#`

## Changelog

For a complete list of changes made in [MariaDB 10.4.31](mariadb-10-4-31-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10-4-31-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.31](mariadb-10-4-31-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-11-0-3-10-11-5-10-10-6-10-9-8-10-6-15-10-5-22-10-4-31-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
