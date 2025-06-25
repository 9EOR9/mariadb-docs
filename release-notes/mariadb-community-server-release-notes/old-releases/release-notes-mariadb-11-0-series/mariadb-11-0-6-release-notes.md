# MariaDB 11.0.6 Release Notes

[Download](https://downloads.mariadb.org/mariadb/11.0.6/)[Release Notes](mariadb-11-0-6-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-11-0-series/mariadb-11-0-6-changelog.md)[Overview of 11.0](what-is-mariadb-110.md)

[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/11.0.6/)

**Release date:** 16 May 2024

[MariaDB 11.0](what-is-mariadb-110.md) is a current short-term stable series of MariaDB and will be [maintained until](https://mariadb.org/about/#maintenance-policy) June 2024. It is an evolution of [MariaDB 10.11](../../mariadb-10-11-series/what-is-mariadb-1011.md) with several entirely new features.

[MariaDB 11.0.6](mariadb-11-0-6-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

[MariaDB 11.0.6](mariadb-11-0-6-release-notes.md) is the last release of the [MariaDB 11.0](what-is-mariadb-110.md) release series.

**For an overview of** [**MariaDB 11.0**](what-is-mariadb-110.md) **see the**[**What is MariaDB 11.0?**](what-is-mariadb-110.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

From this version, the [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) tool adds a new [sandbox](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/mariadb-client/mariadb-command-line-client#-sandbox) command to the top of every dump file. This command cannot be interpreted by MariaDB command line client versions that do not have the sandbox command, or by MySQL command line clients, and an error will be generated in these clients. Other methods of importing the dump will work not have this issue.

### Storage Engines

#### InnoDB

* Introduce the [innodb\_log\_spin\_wait\_delay](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_log_spin_wait_delay) system variable to address excessive context switching caused by log\_sys.lsn\_lock (observed on write-intensive workloads on NUMA systems) ([MDEV-33515](https://jira.mariadb.org/browse/MDEV-33515))
* Fix InnoDB holding shared dict\_sys.latch while waiting for FOREIGN KEY child table lock on DDL ([MDEV-32899](https://jira.mariadb.org/browse/MDEV-32899))
* Fix adaptive hash index corruption after [ALTER TABLE…DISCARD TABLESPACE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table#discard-tablespace) ([MDEV-33400](https://jira.mariadb.org/browse/MDEV-33400))
* Server no longer aborts while altering an InnoDB statistics table ([MDEV-33462](https://jira.mariadb.org/browse/MDEV-33462))
* Fix LeakSanitizer errors in rec\_copy\_prefix\_to\_buf ([MDEV-33230](https://jira.mariadb.org/browse/MDEV-33230))
* Fix InnoDB fatal error: Clustered record field for column x not found ([MDEV-33558](https://jira.mariadb.org/browse/MDEV-33558))
* Fix InnoDB hang when temporarily running out of buffer pool ([MDEV-33613](https://jira.mariadb.org/browse/MDEV-33613))
* Fix alter operation hang when encryption thread works on the same tablespace ([MDEV-33770](https://jira.mariadb.org/browse/MDEV-33770))
* Fix MariaDB segfault on rowid filter query involving generated column ([MDEV-33795](https://jira.mariadb.org/browse/MDEV-33795))
* Fix discard/import tablespace, restart, index corruption ([MDEV-33512](https://jira.mariadb.org/browse/MDEV-33512))
* Fix server hang on DROP INDEX or RENAME INDEX ([MDEV-33993](https://jira.mariadb.org/browse/MDEV-33993))
* Fix mariadb-backup --backup hang ([MDEV-33669](https://jira.mariadb.org/browse/MDEV-33669))
* Fix server hang caused by InnoDB change buffer ([MDEV-33543](https://jira.mariadb.org/browse/MDEV-33543))
* Fix assertion failures upon adding a too long key to table with COMPRESSED row format ([MDEV-31161](https://jira.mariadb.org/browse/MDEV-31161))
* IMPORT TABLESPACE no longer fails with column count or index count mismatch ([MDEV-30655](https://jira.mariadb.org/browse/MDEV-30655))
* Fix alter table corruption while applying the modification log ([MDEV-19044](https://jira.mariadb.org/browse/MDEV-19044))
* Fix inconsistent behaviors of UPDATE under RU & RC isolation level ([MDEV-26643](https://jira.mariadb.org/browse/MDEV-26643))
* Fix weird SELECT view when a record is modified to the same value by two transactions ([MDEV-26642](https://jira.mariadb.org/browse/MDEV-26642))
* Fix inconsistent read and write, which use the same predicate (WHERE clause) ([MDEV-29565](https://jira.mariadb.org/browse/MDEV-29565))
* Fix inconsistent SELECT view when modifying a record added by another transaction ([MDEV-26671](https://jira.mariadb.org/browse/MDEV-26671))
* Fix weird read view after ROLLBACK of other transactions ([MDEV-33802](https://jira.mariadb.org/browse/MDEV-33802))
* Read only server no longer throws error when running a create temporary table as select statement ([MDEV-33889](https://jira.mariadb.org/browse/MDEV-33889))
* Change buffer index no longer fails to delete the records ([MDEV-32489](https://jira.mariadb.org/browse/MDEV-32489))
* Fix InnoDB include OS error information when failing to write to iblogfile0 ([MDEV-33397](https://jira.mariadb.org/browse/MDEV-33397))
* Fix phantom rows caused by UPDATE of PRIMARY KEY ([MDEV-32898](https://jira.mariadb.org/browse/MDEV-32898))
  * New system variable, [innodb\_snapshot\_isolation](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_snapshot_isolation)
* In-place migration from MySQL 5.7 no longer causes invalid AUTO\_INCREMENT values ([MDEV-33277](https://jira.mariadb.org/browse/MDEV-33277))
* Fix InnoDB log corruption before upgrading it on startup ([MDEV-32445](https://jira.mariadb.org/browse/MDEV-32445))
* Table no longer gets rebuilt with ALTER TABLE ADD COLUMN ([MDEV-33214](https://jira.mariadb.org/browse/MDEV-33214))

#### [Aria](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/aria)

* Fixed that internal temporary tables did not wait for freed disk space, and related issues ([MDEV-33813](https://jira.mariadb.org/browse/MDEV-33813))

#### [Federated](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/federatedx-storage-engine)

* Fix wrong result on 2nd execution of prepared statement for query with derived table ([MDEV-31361](https://jira.mariadb.org/browse/MDEV-31361))

#### [Spider](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider)

* Improve Spider performance by pushing down [TIMESTAMPDIFF](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/date-time-functions/timestampdiff) function ([MDEV-28992](https://jira.mariadb.org/browse/MDEV-28992)) and [CASE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/programmatic-compound-statements/case-statement) statement ([MDEV-28993](https://jira.mariadb.org/browse/MDEV-28993)) to data nodes
* Fix server crash when deleting partitions from a table with spider engine ([MDEV-33731](https://jira.mariadb.org/browse/MDEV-33731))
* SPIDER plugin initialization no longer fails at 'create table if not exists mysql.spider\_tables ... with 'Specified key was too long; max key length is 1000 bytes', Warning: Memory not freed: 10720 ([MDEV-33242](https://jira.mariadb.org/browse/MDEV-33242))
* Fix spider plugin init failure with no\_zero\_date sql\_mode ([MDEV-33494](https://jira.mariadb.org/browse/MDEV-33494))
* Fix sql plugin init failure with traditional sql\_mode ([MDEV-33584](https://jira.mariadb.org/browse/MDEV-33584))
* Fix parsing failure on valid left join select by translating the on expression to () ([MDEV-33679](https://jira.mariadb.org/browse/MDEV-33679))
* Fix Spider: ERROR 12710 (HY000): Invalid information from remote table when using [MariaDB 10.5](../../mariadb-10-5-series/what-is-mariadb-105.md) local and [MariaDB 10.6](../../mariadb-10-6-series/what-is-mariadb-106.md) remote ([MDEV-33777](https://jira.mariadb.org/browse/MDEV-33777))
* Fix bug where [Spider variables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider/spider-system-variables) were not available if Spider was loaded upon server startup ([MDEV-33441](https://jira.mariadb.org/browse/MDEV-33441))

### Backup

* Port backup features from Enterprise Server. This adds support for [BACKUP STAGE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/backup-commands/backup-stage) to [mariadb-backup](broken-reference), and obsoletes the [no-backup-locks](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-0-series/broken-reference/README.md) and [rysnc](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-11-0-series/broken-reference/README.md) options ([MDEV-32932](https://jira.mariadb.org/browse/MDEV-32932))
* [mariadb-backup](broken-reference) now preserves [innodb\_encrypt\_tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_encrypt_tables) ([MDEV-33334](https://jira.mariadb.org/browse/MDEV-33334))
* Fix [mariadb-backup](broken-reference) problem on older mariadb (opendir(NULL)) caused by [MDEV-30968](https://jira.mariadb.org/browse/MDEV-30968) ([MDEV-31251](https://jira.mariadb.org/browse/MDEV-31251))
* Fix [mariadb-backup --backup](broken-reference) FATAL ERROR: ... Can't open datafile cool\_down/t3 ([MDEV-33011](https://jira.mariadb.org/browse/MDEV-33011))
* [mariadb-backup --backup](broken-reference) now includes retry logic for undo tablespaces ([MDEV-33980](https://jira.mariadb.org/browse/MDEV-33980))
* Fix crash recovery in [mariadb-backup --prepare](broken-reference) due to insufficient [innodb\_log\_file\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_log_file_size) ([MDEV-33540](https://jira.mariadb.org/browse/MDEV-33540))
* Fix crash in [mariadb-backup --prepare --export](broken-reference) after `--prepare` ([MDEV-33023](https://jira.mariadb.org/browse/MDEV-33023))
* [mariadb-backup](broken-reference) now considers O/S user when `--user` option is omitted ([MDEV-32893](https://jira.mariadb.org/browse/MDEV-32893))

### [Character Sets](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets), [Data Types](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types)

* Fixed improper application of [ORDER BY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/order-by) COLLATE to non-character columns ([MDEV-33318](https://jira.mariadb.org/browse/MDEV-33318))
* Default charset now works with PHP MySQLi extension ([MDEV-32975](https://jira.mariadb.org/browse/MDEV-32975))
* Fixed Bad SEPARATOR value in [GROUP\_CONCAT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/aggregate-functions/group_concat) on character set conversion ([MDEV-33772](https://jira.mariadb.org/browse/MDEV-33772))
* Fixed out of range error in [AVG](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/aggregate-functions/avg)([YEAR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/date-time-functions/year)([datetime](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/datetime))) due to a wrong data type ([MDEV-33496](https://jira.mariadb.org/browse/MDEV-33496))
* Fixed [GREATEST()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/operators/comparison-operators/greatest) and [LEAST()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/operators/comparison-operators/least) problems with [NULLs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/null-values) ([MDEV-21034](https://jira.mariadb.org/browse/MDEV-21034))

#### JSON

* View created via [JSON\_ARRAYAGG](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_arrayagg) now returns correct json object ([MDEV-30646](https://jira.mariadb.org/browse/MDEV-30646))
* [JSON\_TYPE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_type) now detects the type of String Values and correctly returns Date/DateTime values ([MDEV-19487](https://jira.mariadb.org/browse/MDEV-19487))
* [JSON\_REMOVE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_remove) no longer returns NULL on valid arguments ([MDEV-22141](https://jira.mariadb.org/browse/MDEV-22141))
* [JSON\_EXTRACT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_extract) no longer returns multiple values for same path ([MDEV-32287](https://jira.mariadb.org/browse/MDEV-32287))

### Encryption, TLS, SSL

* WolfSSL's math is unnecessarily slow ([MDEV-33482](https://jira.mariadb.org/browse/MDEV-33482))

### Optimization & Tuning

* Server crashes in JOIN\_CACHE::write\_record\_data upon EXPLAIN with subqueries and constant tables ([MDEV-21102](https://jira.mariadb.org/browse/MDEV-21102))
* Wrong result with cross Join given join order ([MDEV-30975](https://jira.mariadb.org/browse/MDEV-30975))
* Wrong warnings on 2-nd execution of PS for query with GROUP\_CONCAT ([MDEV-31276](https://jira.mariadb.org/browse/MDEV-31276))
* Wrong result with semi-join and splittable derived table ([MDEV-23878](https://jira.mariadb.org/browse/MDEV-23878))
* Optimizer choosing incorrect index in 10.6, 10.5 but not in 10.4 ([MDEV-33306](https://jira.mariadb.org/browse/MDEV-33306))
* Aggregation functions fail to leverage uniqueness property ([MDEV-30660](https://jira.mariadb.org/browse/MDEV-30660))
* Partitioning is broken on big endian architectures ([MDEV-33623](https://jira.mariadb.org/browse/MDEV-33623))

### Plugins

* The [audit plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/mariadb-audit-plugin) now reports the user and host in all cases ([MDEV-33393](https://jira.mariadb.org/browse/MDEV-33393))

### Replication

* \--gtid-ignore-duplicate can double-apply event in case of parallel replication retry ([MDEV-33475](https://jira.mariadb.org/browse/MDEV-33475))
* Deadlock kill of XA PREPARE can break replication / rpl.rpl\_parallel\_multi\_domain\_xa sporadic failure ([MDEV-34042](https://jira.mariadb.org/browse/MDEV-34042))
* mysql\_manager\_submit Segfault at Startup Still Possible During Recovery ([MDEV-33799](https://jira.mariadb.org/browse/MDEV-33799))
* Server crash in Rows\_log\_event::update\_sequence upon replaying binary log ([MDEV-31779](https://jira.mariadb.org/browse/MDEV-31779))
* Slave crashed:reload\_acl\_and\_cache during shutdown ([MDEV-30260](https://jira.mariadb.org/browse/MDEV-30260))
* Rpl\_semi\_sync\_slave\_status is ON When Replication Is Not Configured ([MDEV-33546](https://jira.mariadb.org/browse/MDEV-33546))
* When binlog\_annotate\_row\_events on , event of binlog file is truncated ([MDEV-9179](https://jira.mariadb.org/browse/MDEV-9179))
* Add more warnings to be able to better diagnose network issues ([MDEV-33582](https://jira.mariadb.org/browse/MDEV-33582))
* Improve times and states in show processlist for replication ([MDEV-33620](https://jira.mariadb.org/browse/MDEV-33620))
* Adapt parallel slave's round-robin scheduling to XA events ([MDEV-33668](https://jira.mariadb.org/browse/MDEV-33668))
* release row locks for non-modified rows at XA PREPARE ([MDEV-33454](https://jira.mariadb.org/browse/MDEV-33454))
* Semi-sync Wait Point AFTER\_COMMIT Slow on Workloads with Heavy Concurrency ([MDEV-33551](https://jira.mariadb.org/browse/MDEV-33551))

#### Galera

* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera-cluster/README.md) updated to 26.4.18
  * NOTE: Includes increasing the GCS protocol version, which prevents downgrades of individual nodes in the cluster as soon as all nodes have been updated
* Disallow bulk insert operation during partition update statement ([MDEV-33979](https://jira.mariadb.org/browse/MDEV-33979))
* GCF-1060 test hangs when BF-abort logic mistreats transactions with explicit MDL locks ([MDEV-33136](https://jira.mariadb.org/browse/MDEV-33136))

### SQL, Data Definition, and Data Manipulation

* Transportable Tablespaces no longer leave [AUTO\_INCREMENT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/auto_increment) in a mismatched state ([MDEV-18288](https://jira.mariadb.org/browse/MDEV-18288))
* Fix wrong row targeted with "insert ... on duplicate" and "replace", leading to data corruption ([MDEV-30046](https://jira.mariadb.org/browse/MDEV-30046))
* Fix incorrect DEFAULT expression evaluated in [UPDATE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/update) ([MDEV-33790](https://jira.mariadb.org/browse/MDEV-33790))
* Fix server crash when UPDATE statement with duplicate key is run after setting a low thread\_stack ([MDEV-33622](https://jira.mariadb.org/browse/MDEV-33622))
* Fix incorrect handling of [UPDATE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/update) in PS mode when a table's column declared as NOT NULL ([MDEV-33549](https://jira.mariadb.org/browse/MDEV-33549))
* Fix crash in EXECUTE IMMEDIATE 'CREATE OR REPLACE TABLE t1 (a INT DEFAULT ?)' USING DEFAULT ([MDEV-15703](https://jira.mariadb.org/browse/MDEV-15703))
* Fix wrong result on 2nd execution of PS to select from view using derived ([MDEV-31277](https://jira.mariadb.org/browse/MDEV-31277))
* Fix wrong warnings on 2nd execution of PS for query with GROUP\_CONCAT ([MDEV-31276](https://jira.mariadb.org/browse/MDEV-31276))
* [TIMESTAMP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/timestamp) value of '1970-01-01 00:00:00' can no longer be indirectly inserted in [strict mode](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/variables-and-modes/sql-mode#strict-mode) ([MDEV-34088](https://jira.mariadb.org/browse/MDEV-34088))
* Fix out of range error in [AVG](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/aggregate-functions/avg)([YEAR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/date-time-functions/year)([datetime](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/datetime))) due to a wrong data type ([MDEV-33496](https://jira.mariadb.org/browse/MDEV-33496))
* Fix zero datetime reinterpreting as '1970-01-01 00:00:00' on field\_datetime=field\_timestamp ([MDEV-34069](https://jira.mariadb.org/browse/MDEV-34069))
* unix\_timestamp(coalesce(timestamp\_column)) no longer returns NULL on '1970-01-01 00:00:00.000001' ([MDEV-34061](https://jira.mariadb.org/browse/MDEV-34061))
* Fix crash using UDF in WHERE clause of VIEW ([MDEV-24507](https://jira.mariadb.org/browse/MDEV-24507))
* Fix update for portion changes autoincrement key in period table ([MDEV-25370](https://jira.mariadb.org/browse/MDEV-25370))
* Fix SIGABRT resulting from CREATE TABLE with generated column and RLIKE ([MDEV-21058](https://jira.mariadb.org/browse/MDEV-21058))

### Platforms & Packaging

* MariaDB-client community can't be installed in red hat ubi9 ([MDEV-32791](https://jira.mariadb.org/browse/MDEV-32791))

### General

#### Scripts & Clients

* It's now possible to disable system commands with the [mariadb --sandbox](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/mariadb-client/mariadb-command-line-client#-sandbox) option. ([MDEV-21778](https://jira.mariadb.org/browse/MDEV-21778))
* [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) now exports the data with sandbox mode enable, so that the mariadb client will not execute potentially dangerous cli commands.([MDEV-33727](https://jira.mariadb.org/browse/MDEV-33727))
* [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) commands such as `mariadb-dump --dump-slave=2 --master-data=2` now record both positions ([MDEV-4827](https://jira.mariadb.org/browse/MDEV-4827))
* Loading [time zones](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets/internationalization-and-localization/time-zones) now works with [alter\_algorithm](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#alter_algorithm) INPLACE ([MDEV-33044](https://jira.mariadb.org/browse/MDEV-33044))

#### Server

* Moving from [MariaDB 10.5](../../mariadb-10-5-series/what-is-mariadb-105.md) to 10.6 mysql\_upgrade is not updating some system tables ([MDEV-33726](https://jira.mariadb.org/browse/MDEV-33726))
* Original IP not shown in network related error messages when proxy\_protocol is in use ([MDEV-33506](https://jira.mariadb.org/browse/MDEV-33506))
* Server incorrectly describes known variables as UNKNOWN if invalid values are specified at startup ([MDEV-33469](https://jira.mariadb.org/browse/MDEV-33469))
* update case insensitive (large) unique key with insensitive change of value - duplicate key ([MDEV-29345](https://jira.mariadb.org/browse/MDEV-29345))
* MariaDB will abort server startup if it finds an invalid parameter, but won't check for other invalid params ([MDEV-26923](https://jira.mariadb.org/browse/MDEV-26923))
* Slowdown when running nested statement with many partitions ([MDEV-33502](https://jira.mariadb.org/browse/MDEV-33502))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2024-21096](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2024-21096)

## Changelog

For a complete list of changes made in [MariaDB 11.0.6](mariadb-11-0-6-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-11-0-series/mariadb-11-0-6-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 11.0.6](mariadb-11-0-6-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-11-2-4-11-1-5-11-0-6-10-11-8-10-6-18-10-5-25-10-4-34-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
