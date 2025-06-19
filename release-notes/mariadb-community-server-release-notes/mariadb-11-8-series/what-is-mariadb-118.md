# Changes and Improvements in MariaDB 11.8

{% include "../../../.gitbook/includes/the-most-recent-release-of-... (4).md" %}

[MariaDB 11.8](what-is-mariadb-118.md) is a long-term release, maintained until June 2028.

This list includes all features since the previous long-term release, [MariaDB 11.4](../mariadb-11-4-series/what-is-mariadb-114.md) (those introduced in the [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md), [MariaDB 11.6](../old-releases/release-notes-mariadb-11-6-rolling-releases/what-is-mariadb-116.md) and [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md) rolling releases).

## Upgrading

* See [Upgrading Between Major MariaDB Versions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/upgrading/upgrading-between-major-mariadb-versions) and [Upgrading from MariaDB 10.11 to MariaDB 11.0](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/upgrading/upgrading-to-unmaintained-mariadb-releases/upgrading-from-mariadb-10-11-to-mariadb-11-0).

## New Features

### Vectors

* New function [VEC\_DISTANCE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/vectors/vector-functions/vector-functions-vec_distance) for calculating either a Euclidean or Cosine distance between two vectors, depending on the underlying index type ([MDEV-35450](https://jira.mariadb.org/browse/MDEV-35450))
* aarch64 SIMD instructions now supported ([MDEV-34699](https://jira.mariadb.org/browse/MDEV-34699))

### Character Sets

* The default [character set](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets) has been changed from `latin1` to `utf8mb4` ([MDEV-19123](https://jira.mariadb.org/browse/MDEV-19123), [MariaDB 11.6](../old-releases/release-notes-mariadb-11-6-rolling-releases/what-is-mariadb-116.md))
* Change [default Unicode collation](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets/supported-character-sets-and-collations) to uca1400\_ai\_ci, a modern Unicode collation with proper support for SMP characters (including emoji)([MDEV-25829](https://jira.mariadb.org/browse/MDEV-25829), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))

### Optimizer

* Optimizer can now take advantage of queries of the format [SUBSTR(col, 1, n) = const\_str](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/substring) ([MDEV-34911](https://jira.mariadb.org/browse/MDEV-34911))
* Add basic optimizer support for [virtual columns](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/generated-columns) - see [Virtual Column Support in the Optimizer](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/virtual-column-support-in-the-optimizer) ([MDEV-35616](https://jira.mariadb.org/browse/MDEV-35616))
* Improve selectivity computations for multi-part keys ([MDEV-33697](https://jira.mariadb.org/browse/MDEV-33697), [MariaDB 11.6](../old-releases/release-notes-mariadb-11-6-rolling-releases/what-is-mariadb-116.md))
* [Index condition pushdown](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/index-condition-pushdown) is now supported for partitioned tables ([MDEV-12404](https://jira.mariadb.org/browse/MDEV-12404), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* ANALYZE for statement should show selectivity of pushed index condition ([MDEV-18478](https://jira.mariadb.org/browse/MDEV-18478), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))

### Temporary files and tables

* [Limit size of created disk temporary files and tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/limiting-size-of-created-disk-temporary-files-and-tables/limiting-size-of-created-disk-temporary-files-and-tables-overview) ([MDEV-9101](https://jira.mariadb.org/browse/MDEV-9101), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* There are two system variables used for controlling this feature ([MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md)):
  * [max\_tmp\_session\_space\_usage](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/limiting-size-of-created-disk-temporary-files-and-tables/max_tmp_session_space_usage-system-variable): Limits the the temporary space allowance per user
  * [max\_tmp\_total\_space\_usage](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/limiting-size-of-created-disk-temporary-files-and-tables/max_tmp_total_space_usage-system-variable): Limits the temporary space allowance for all users.

### Data Types

* The [TIMESTAMP](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/timestamp) range of values was extended. The maximal allowed value for timestamps was '2038-01-19 03:14:07 UTC', and is now '2106-02-07 06:28:15 UTC'. This does not change the storage format, and new tables can be read by old MariaDB servers as long as timestamp values are within the old timestamp range. At the moment this is only supported on 64-bit platforms ([MDEV-32188](https://jira.mariadb.org/browse/MDEV-32188), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))

### Authentication

* [New authentication plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-parsec) ([MDEV-32618](https://jira.mariadb.org/browse/MDEV-32618), [MariaDB 11.6](../old-releases/release-notes-mariadb-11-6-rolling-releases/what-is-mariadb-116.md))
* Extend [Unix socket authentication](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/authentication-plugins/authentication-plugin-unix-socket) to support authentication\_string ([MDEV-33479](https://jira.mariadb.org/browse/MDEV-33479), [MariaDB 11.6](../old-releases/release-notes-mariadb-11-6-rolling-releases/what-is-mariadb-116.md))

### InnoDB

* Fix [innodb-adaptive-hash-index](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_adaptive_hash_index) scalability with multiple threads ([MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049))

### Backup and Restore

* Added the `--dir` option to [mariadb-import](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-import), allowing one to restore all tables from a backup directory created using [mariadb-dump --dir](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) ([MDEV-33627](https://jira.mariadb.org/browse/MDEV-33627), [MariaDB 11.6](../old-releases/release-notes-mariadb-11-6-rolling-releases/what-is-mariadb-116.md))
  * Added the related `--database`, `--ignore-database`, `--table` and `--ignore-table` options.
  * Refactor [mariadb-import](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-import) threading
* Automatic SST user account management ([MDEV-31809](https://jira.mariadb.org/browse/MDEV-31809), [MariaDB 11.6](../old-releases/release-notes-mariadb-11-6-rolling-releases/what-is-mariadb-116.md))
* The [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) `--no-autocommit` option is now set by default to allow faster data loading by InnoDB, writing only one undo log for the whole operation ([MDEV-32250](https://jira.mariadb.org/browse/MDEV-32250))
* [mariadb-import](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-import) has a new option, `--innodb-optimize-keys` to delay creation of secondary indexes until after data load, resulting in faster loads. On by default. ([MDEV-34740](https://jira.mariadb.org/browse/MDEV-34740))
* Parallel dump of multiple databases via [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) with the `--dir` option ([MDEV-33625](https://jira.mariadb.org/browse/MDEV-33625), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))

### Replication

* When [binlogging](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log) is enabled, committing a large transaction no longer freezes all other transactions until completed ([MDEV-32014](https://jira.mariadb.org/browse/MDEV-32014), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* [binlog\_optimize\_thread\_scheduling](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#binlog_optimize_thread_scheduling) has been deprecated ([MDEV-33756](https://jira.mariadb.org/browse/MDEV-33756), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* Async rollback prepared transactions during binlog crash recovery ([MDEV-33853](https://jira.mariadb.org/browse/MDEV-33853), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* New variable, [slave\_abort\_blocking\_timeout](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#slave_abort_blocking_timeout), for aborting long-running queries on a replica ([MDEV-34857](https://jira.mariadb.org/browse/MDEV-34857), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* New variable, [binlog\_large\_commit\_threshold](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#binlog_large_commit_threshold), for increasing transaction concurrency for large transactions ([MDEV-32014](https://jira.mariadb.org/browse/MDEV-32014), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* [binlog\_optimize\_thread\_scheduling](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#binlog_optimize_thread_scheduling) deprecated ([MDEV-33756](https://jira.mariadb.org/browse/MDEV-33756), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* New definition for Seconds\_Behind\_Master ([MDEV-33856](https://jira.mariadb.org/browse/MDEV-33856), [MariaDB 11.6](../old-releases/release-notes-mariadb-11-6-rolling-releases/what-is-mariadb-116.md))
  * Added three variables to [SHOW ALL REPLICAS STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-replica-status)
  * New [Information Schema SLAVE\_STATUS Table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-slave_status-table)

### UUID

* New function for generating version 4 UUIDs [UUID\_v4](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/miscellaneous-functions/uuid_v4) ([MDEV-11339](https://jira.mariadb.org/browse/MDEV-11339), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* New function for generating version 7 UUIDs [UUID\_v7](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/miscellaneous-functions/uuid_v7) ([MDEV-32637](https://jira.mariadb.org/browse/MDEV-32637), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))

### GIS

New GIS functions. These functions improve compatibility with MySQL 8.

* [ST\_Validate](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/miscellaneous-gis-functions/st_validate) ([MDEV-34137](https://jira.mariadb.org/browse/MDEV-34137))
* [MBRCoveredBy](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/mbr-minimum-bounding-rectangle/mbrcoveredby) ([MDEV-34138](https://jira.mariadb.org/browse/MDEV-34138))
* [ST\_Simplify](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/miscellaneous-gis-functions/st_simplify) ([MDEV-34141](https://jira.mariadb.org/browse/MDEV-34141))
* [ST\_GeoHash](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/miscellaneous-gis-functions/st_geohash) ([MDEV-34158](https://jira.mariadb.org/browse/MDEV-34158))
* [ST\_LatFromGeoHash](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/miscellaneous-gis-functions/st_latfromgeohash) ([MDEV-34159](https://jira.mariadb.org/browse/MDEV-34159))
* [ST\_LongFromGeoHash](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/miscellaneous-gis-functions/st_longfromgeohash) ([MDEV-34160](https://jira.mariadb.org/browse/MDEV-34160))
* [ST\_PointFromGeoHash](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/miscellaneous-gis-functions/st_pointfromgeohash) ([MDEV-34277](https://jira.mariadb.org/browse/MDEV-34277))
* [ST\_IsValid](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/miscellaneous-gis-functions/st_isvalid) ([MDEV-34276](https://jira.mariadb.org/browse/MDEV-34276))
* [ST\_Collect](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/miscellaneous-gis-functions/st_collect) ([MDEV-34278](https://jira.mariadb.org/browse/MDEV-34278))

### Other Functions

* New [FORMAT\_BYTES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/miscellaneous-functions/miscellaneous-functions-format_bytes) function. Given a byte count, returns a string consisting of a value and the units in a human-readable format ([MDEV-31736](https://jira.mariadb.org/browse/MDEV-31736))

### Referential Integrity

* [CHECK TABLE ... EXTENDED](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/check-table) now also checks for referential integrity ([MDEV-34309](https://jira.mariadb.org/browse/MDEV-34309))

### Protocol

* Permit bulk implementation to return ALL individual results ([MDEV-30366](https://jira.mariadb.org/browse/MDEV-30366), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* Send initial values of system variables in first OK packet ([MDEV-31609](https://jira.mariadb.org/browse/MDEV-31609), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))

### Observability

* New [USERS table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-users-table) in the Information Schema for storing information about users, [password expiry](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/user-account-management/user-password-expiry), and the limits set by [max\_password\_errors](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#max_password_errors) ([MDEV-23729](https://jira.mariadb.org/browse/MDEV-23729), [MDEV-32218](https://jira.mariadb.org/browse/MDEV-32218), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* Add more columns to Information Schema [TABLE\_STATISTICS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-table_statistics-table), [CLIENT\_STATISTICS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-client_statistics-table) and [USER STATISTICS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-user_statistics-table) tables ([MDEV-33151](https://jira.mariadb.org/browse/MDEV-33151), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* Add QUERIES column to Information Schema [INDEX\_STATISTICS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-index_statistics-table) table ([MDEV-33152](https://jira.mariadb.org/browse/MDEV-33152), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* Add [FLUSH GLOBAL STATUS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/flush-commands/flush#flush-status) ([MDEV-33145](https://jira.mariadb.org/browse/MDEV-33145), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* Provide InnoDB async IO statistics ([MDEV-32841](https://jira.mariadb.org/browse/MDEV-32841), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* Show variable deprecation for [mariadbd --help](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/starting-and-stopping-mariadb/mariadbd-options#-help) output ([MDEV-28671](https://jira.mariadb.org/browse/MDEV-28671), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* Extend [Query Response Time plugin](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/plugins/other-plugins/query-response-time-plugin) to be compatible with Percona server ([MDEV-33501](https://jira.mariadb.org/browse/MDEV-33501), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))

### [Sequences](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sequences)

* Additional features for Sequences ([MDEV-28152](https://jira.mariadb.org/browse/MDEV-28152), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
  * [CREATE SEQUENCE ... AS](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sequences/create-sequence) permits creating as any [INT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/numeric-data-types/int) type (including [BIGINT UNSIGNED](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/numeric-data-types/bigint)), extending the range
  * [Information Schema Sequences table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-sequences-table)
  * Parser accepts larger and smaller values for [MINVALUE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sequences/create-sequence#minvalue) and [MAXVALUE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sequences/create-sequence#maxvalue)
* [ANALYZE TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/analyze-table) on [sequences](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sequences) no longer attempts to collect statistics ([MDEV-33938](https://jira.mariadb.org/browse/MDEV-33938))

### System-Versioned Tables

* Allow a [system-versioned table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/temporal-tables/system-versioned-tables) to be converted from implicit to explicit row\_start/row\_end columns ([MDEV-27293](https://jira.mariadb.org/browse/MDEV-27293), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))

### Stored Routines

* ROW data type for stored function return values ([MDEV-12252](https://jira.mariadb.org/browse/MDEV-12252), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))

### Derived Tables

* Add optional correlation column list for [derived tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/joins-subqueries/subqueries/subqueries-in-a-from-clause-derived-tables) ([MDEV-31466](https://jira.mariadb.org/browse/MDEV-31466), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))

### \[SHOW] CREATE SERVER

* Implement [SHOW CREATE SERVER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-create-server) ([MDEV-15696](https://jira.mariadb.org/browse/MDEV-15696), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* Allow arbitrary options in [CREATE SERVER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/create-server) ([MDEV-34716](https://jira.mariadb.org/browse/MDEV-34716), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))

### Slow Query Log

* New variable, [log\_slow\_always\_query\_time](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/slow-query-log/log_slow_always_query_time-system-variable), for specifying that all queries longer than this time are logged to the [slow query log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/slow-query-log), regardless of [log\_slow\_min\_examined\_row\_limit](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#log_slow_min_examined_row_limit) and [log\_slow\_rate\_limit](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#log_slow_rate_limit) ([MDEV-33144](https://jira.mariadb.org/browse/MDEV-33144), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))

### Information Schema

* When querying the [information Schema](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema), [stored functions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/stored-routines/stored-functions) that have the same name as a native function no longer generate a warning ([MDEV-35437](https://jira.mariadb.org/browse/MDEV-35437))

### Spider

* The Spider variables [spider\_table\_crd\_thread\_count](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider/spider-system-variables#spider_table_crd_thread_count) and [spider\_table\_sts\_thread\_count](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider/spider-system-variables#spider_table_sts_thread_count) have been deprecated ([MDEV-28009](https://jira.mariadb.org/browse/MDEV-28009), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* Deprecate [spider\_casual\_read](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/spider/spider-system-variables#spider_casual_read) ([MDEV-31789](https://jira.mariadb.org/browse/MDEV-31789), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))

### General

* [SESSION\_USER()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/information-functions/session_user), which used to be an alias for [USER()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/information-functions/user) now shows the value of [CURRENT\_USER()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/information-functions/current_user) when the session was created ([MDEV-30908](https://jira.mariadb.org/browse/MDEV-30908), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* CURRENT\_TIMESTAMP should return a TIMESTAMP (WITH TIME ZONE?) ([MDEV-15751](https://jira.mariadb.org/browse/MDEV-15751), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* A warning has been added when [max\_sort\_length](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#max_sort_length) is exceeded. ([MDEV-27277](https://jira.mariadb.org/browse/MDEV-27277), [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md))
* Single-table [DELETEs](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/changing-deleting-data/delete) now support table aliases ([MDEV-33988](https://jira.mariadb.org/browse/MDEV-33988), [MariaDB 11.6](../old-releases/release-notes-mariadb-11-6-rolling-releases/what-is-mariadb-116.md))
* Set thread names for MariaDB Server threads ([MDEV-32537](https://jira.mariadb.org/browse/MDEV-32537), [MariaDB 11.6](../old-releases/release-notes-mariadb-11-6-rolling-releases/what-is-mariadb-116.md))
* [REPAIR TABLE ... FORCE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/repair-table) ([MDEV-33449](https://jira.mariadb.org/browse/MDEV-33449), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* Deprecate and ignore the [alter\_algorithm](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#alter_algorithm) system variable ([MDEV-33655](https://jira.mariadb.org/browse/MDEV-33655), [MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))

### Variables

* For a list of all new variables, see [System Variables Added in MariaDB 11.8](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/system-and-status-variables-added-by-major-release/system-variables-added-in-mariadb-11-8) and [Status Variables Added in MariaDB 11.8](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/system-and-status-variables-added-by-major-release/system-and-status-variables-added-by-major-unmaintained-release/system-variables-added-in-mariadb-11-5).

## Removed Features

The following deprecated features have been removed:

* ... COMPRESSED... ([MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
  * the correct syntax is COMPRESSED... ...
* [wsrep\_load\_data\_splitting](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_load_data_splitting) ([MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))
* [integer latches in OQGraph](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/oqgraph-storage-engine/oqgraph-overview) (and the related [oqgraph\_allow\_create\_integer\_latch](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/oqgraph-system-and-status-variables#oqgraph_allow_create_integer_latch) variable). ([MariaDB 11.5](../old-releases/release-notes-mariadb-11-5-rolling-releases/what-is-mariadb-115.md))

## Security Vulnerabilities Fixed in [MariaDB 11.8](what-is-mariadb-118.md)

For a complete list of security vulnerabilities (CVEs) fixed across all\
versions of MariaDB, see the [Security Vulnerabilities Fixed in MariaDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security)\
page.\
Add listcve macro here - removed for performance reasons

## List of All [MariaDB 11.8](what-is-mariadb-118.md) Releases

| Date        | Release                                           | Status | Release Notes                                    | Changelog                                                                                |
| ----------- | ------------------------------------------------- | ------ | ------------------------------------------------ | ---------------------------------------------------------------------------------------- |
| Date        | Release                                           | Status | Release Notes                                    | Changelog                                                                                |
| 13 Feb 2024 | [MariaDB 11.8.1](mariadb-11-8-1-release-notes.md) | RC     | [Release Notes](mariadb-11-8-1-release-notes.md) | [Changelog](../../changelogs/changelogs-mariadb-11-7-series/mariadb-11-7-1-changelog.md) |
| 18 Dec 2024 | [MariaDB 11.8.0](mariadb-11-8-0-release-notes.md) | Alpha  | [Release Notes](mariadb-11-8-0-release-notes.md) |                                                                                          |

{% @marketo/form formid="4316" formId="4316" %}
