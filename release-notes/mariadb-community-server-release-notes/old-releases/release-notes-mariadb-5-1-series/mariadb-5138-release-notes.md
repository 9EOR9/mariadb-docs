# MariaDB 5.1.38 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.1.38) | **Release Notes** | [Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5138-changelog.md) |[Overview of 5.1](changes-improvements-in-mariadb-5-1.md)

**Release date:** 29 Oct 2009

See the [MariaDB versus MySQL](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/broken-reference/README.md) page for a high-level\
overview of the differences between MariaDB and MySQL.

[MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) 5.1.38 Beta is based on [MySQL](https://mysql.com) 5.1.38\
and XtraDB 1.0.3-6.

MariaDB will be kept up to date with the latest MySQL release from the same\
branch.

In most respects MariaDB will work exactly as MySQL; all commands, interfaces,\
libraries and APIs that exist in MySQL also exist in MariaDB.

For 5.1.38, the main differences between MariaDB and MySQL are:

### Maria storage engine is included

The [Maria](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/aria) storage engine version 1.5 (the crash-safe version) is\
included in the source and binaries by default.

If you use the source, you can of course easily disable the Maria storage\
engine when configuring [MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md).

The new Maria storage engine specific options can be found here:[Maria storage engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/aria).

### XtraDB storage engine is included

[Percona XtraDB](https://www.percona.com/docs/wiki/percona-xtradb:start)\
replaces InnoDB in the [MariaDB 5.1](changes-improvements-in-mariadb-5-1.md) tree.

XtraDB is a drop in replacement of InnoDB (same table formats, no need to\
convert any data).

XtraDB gives you similar performance improvements for multi-cpu systems in[MariaDB 5.1](changes-improvements-in-mariadb-5-1.md) that you can expect from using InnoDB in MySQL 5.4.

See also [XtraDB storage engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb)

### PBXT storage engine is included

The [PBXT](https://www.primebase.org) storage engine version 1.0.08d is\
included in the source and binaries by default.

See also: [PBXT storage engine](https://github.com/mariadb-corporation/docs-release-notes/blob/test/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-1-series/pbxt-storage-engine/README.md)

### Faster complex queries

Our use of the Maria storage engine enables faster complex queries (queries\
which normally use disk-based temporary tables).

The [Maria](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/aria) storage engine is used for internal temporary tables, which\
should give you a speedup when doing complex selects. Maria is usually faster\
for temporary tables when compared to MyISAM because Maria caches row data in\
memory and normally doesn't have to write the temporary rows to disk.

### Pool of Threads

Limited sets of threads handling all queries.

See: [Pool of Threads](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/buffers-caches-and-threads/thread-pool/thread-pool-in-mariadb-51-53)

### Fewer warnings and bugs

* Fewer warnings when compiling. We believe that compiler warnings can\
  indicate bugs, and strive toward reduction to 0.
* Fewer bugs. If we see a bug while fixing a warning or cleaning up code,\
  we'll fix it when possible.

### Speed improvements

* There are some improvements to DBUG code to make its execution faster when\
  debug is compiled in but not used.
* `CHECKSUM TABLE` now ignores values in`NULL` fields. This makes `CHECKSUM TABLE`\
  faster and fixes some cases where the same table definition could give\
  different checksum values depending on row format. The disadvantage is the\
  value is now different compared to other MySQL installations. The new\
  checksum calculation is fixed for all table engines which use the default way\
  to calculate and MyISAM which does the calculation internally. Note: Old\
  MyISAM tables with internal checksum will return the same checksum as before.\
  To fix them to calculate according to new rules you have to do an`ALTER TABLE`. You can use the old ways to calculate\
  checksums by using the option `--old` to mysqld or set the\
  system variable '`@@old`' to 1 when you do`CHECKSUM TABLE ... EXTENDED;`
* We have eliminated/improved some not needed character set conversions.\
  Overall speed improvements is 1-5 % (according to sql-bench) but can be\
  higher for big results sets with all characters between 0x00-0x7f.

### Extensions

* MariaDB can handle up to 32 key segments per key (up from 16)
* Added a new handler function: prepare\_index\_scan() that is called before a\
  key scan is done.
* Added --abort-source-on-error to the mysql client.

### Better testing of features

* Wrong mutex usage detector. This helps us find and fix deadlocks when taking\
  mutex in inconsistent orders. In MariaDB we have removed several deadlocks\
  which exist in the normal MySQL code.

### Table elimination

Implementation of [MWL#17](https://askmonty.org/worklog/?tid=17): Table elimination

See [Table\_Elimination](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/table-elimination) for details.

### Slow Query Log Extended Statistics

This is based on the[microslow](https://www.percona.com/mysql/5.1.26/patches/microslow.patch) patch\
from [Percona](https://www.percona.com/).

See [Slow Query Log Extended Statistics](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/statistics-for-optimizing-queries/slow-query-log-extended-statistics)\
for details.

### Microsecond Precision in Processlist

This is based on the[microsec\_process](https://www.percona.com/mysql/5.0.77-b13/patches/microsec_process.patch)\
patch from [Percona](https://www.percona.com/).

See [TIME\_MS column in INFORMATION\_SCHEMA.PROCESSLIST](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/time_ms-column-in-information_schemaprocesslist) for details.

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formid="4316" formId="4316" %}
