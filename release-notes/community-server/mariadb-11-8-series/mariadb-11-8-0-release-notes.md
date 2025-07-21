# MariaDB 11.8.0 Release Notes

{% include "../../.gitbook/includes/latest-11-8.md" %}

<a href="https://downloads.mariadb.org/mariadb/11.8.0/" class="button primary">Download</a> <a href="mariadb-11-8-2-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-11-8-series/mariadb-11.8.2-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-118.md" class="button secondary">Overview of 11.8</a>

**Release date:** 18 Dec 2024

{% include "../../.gitbook/includes/non-stable.md" %}

[MariaDB 11.8](what-is-mariadb-118.md) is a long-term development series of MariaDB. It is an evolution of [MariaDB 11.7](../old-releases/mariadb-11-7-rolling-releases/what-is-mariadb-117.md) with several entirely new features.

[MariaDB 11.8.0](mariadb-11-8-0-release-notes.md) is a single preview release. Features are to be considered previews, and none are guaranteed to make it into [MariaDB 11.8](what-is-mariadb-118.md).

The preview is available as a container **quay.io/mariadb-foundation/mariadb-devel:11.8-preview**.

**For an overview of** [**MariaDB 11.8**](what-is-mariadb-118.md)**, see the** [**What is MariaDB 11.8?**](what-is-mariadb-118.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### Vectors

* New function [VEC\_DISTANCE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/vectors/vector-functions/vector-functions-vec_distance) for calculating either a Euclidean or Cosine distance between two vectors, depending on the underlying index type ([MDEV-35450](https://jira.mariadb.org/browse/MDEV-35450))
* aarch64 SIMD instructions now supported ([MDEV-34699](https://jira.mariadb.org/browse/MDEV-34699))

### Optimizer

* Expanded [Optimizer hints](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/optimizer-hints#expanded-optimizer-hints) ([MDEV-35504](https://jira.mariadb.org/browse/MDEV-35504))
  * Implement [subquery optimizer hints](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/optimizer-hints#subquery-hints) ([MDEV-34888](https://jira.mariadb.org/browse/MDEV-34888))
  * Implement [MAX\_EXECUTION\_TIME hint](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/selecting-data/optimizer-hints#max_execution_time) ([MDEV-34860](https://jira.mariadb.org/browse/MDEV-34860))
  * Optimizer hints did not make it into the final [MariaDB 11.8](what-is-mariadb-118.md) release.
* Optimizer can now take advantage of queries of the format [SUBSTR(col, 1, n) = const\_str](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/string-functions/substring) ([MDEV-34911](https://jira.mariadb.org/browse/MDEV-34911))
* Add basic optimizer support for [virtual columns](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/create/generated-columns) - see [Virtual Column Support in the Optimizer](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/query-optimizations/virtual-column-support-in-the-optimizer) ([MDEV-35616](https://jira.mariadb.org/browse/MDEV-35616))

### InnoDB

* Fix [innodb-adaptive-hash-index](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_adaptive_hash_index) scalability with multiple threads ([MDEV-35049](https://jira.mariadb.org/browse/MDEV-35049))

### Importing

* The [mariadb-dump](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-dump) `--no-autocommit` option is now set by default to allow faster data loading by InnoDB, writing only one undo log for the whole operation ([MDEV-32250](https://jira.mariadb.org/browse/MDEV-32250))
* [mariadb-import](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/backup-restore-and-import-clients/mariadb-import) has a new option `--innodb-optimize-keys` to delay creation of secondary indexes until after data load, resulting in faster loads. By default. ([MDEV-34740](https://jira.mariadb.org/browse/MDEV-34740))

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

### Functions

* New [FORMAT\_BYTES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/secondary-functions/miscellaneous-functions/miscellaneous-functions-format_bytes) function. Given a byte count, returns a string consisting of a value and the units in a human-readable format ([MDEV-31736](https://jira.mariadb.org/browse/MDEV-31736))

### Referential Integrity

* [CHECK TABLE ... EXTENDED](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/check-table) now also checks for referential integrity ([MDEV-34309](https://jira.mariadb.org/browse/MDEV-34309))

### Information Schema

* When querying the [information Schema](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/system-tables/information-schema), [stored functions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/stored-routines/stored-functions) that have the same name as a native function no longer generate a warning ([MDEV-35437](https://jira.mariadb.org/browse/MDEV-35437))

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
