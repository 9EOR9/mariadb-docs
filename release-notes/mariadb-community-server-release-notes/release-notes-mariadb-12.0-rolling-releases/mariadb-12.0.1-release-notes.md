# MariaDB 12.0.1 Release Notes

<a href="https://mariadb.com/downloads" class="button primary">Download</a>  <a href="mariadb-12.0.1-release-notes.md" class="button secondary">Release Notes</a>  <a href="../changelogs/changelogs-mariadb-12.0-series/mariadb-12.0.1-changelog.md" class="button secondary">Changelog</a>  <a href="what-is-mariadb-120.md" class="button secondary">Overview of 12.0</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/12.0.1/)

**Release date:** 5 Jun 2025

{% include "../../.gitbook/includes/non-stable.md" %}

[MariaDB 12.0](what-is-mariadb-120.md) is a [rolling release](../../mariadb-release-model.md). It is an evolution of [MariaDB 11.8](../mariadb-11-8-series/what-is-mariadb-118.md) with several entirely new features.

MariaDB 12.0.1 is a [_**Release Candidate (RC)**_](../../mariadb-release-criteria.md) release.

{% hint style="success" %}
**For an overview of MariaDB 12.0 see the** [**Changes and Improvements in MariaDB 12.0**](what-is-mariadb-120.md) **page.**
{% endhint %}

Thanks, and enjoy MariaDB!

## Notable Items <a href="#notable-items" id="notable-items"></a>

### Security <a href="#security" id="security"></a>

* Support for passphrase protected keys ([MDEV-14091](https://jira.mariadb.org/browse/MDEV-14091))
* New SET SESSION AUTHORIZATION ([MDEV-20299](https://jira.mariadb.org/browse/MDEV-20299))
* Implement SHA2 support for file\_key\_management.so plugin (TDE) ([MDEV-34712](https://jira.mariadb.org/browse/MDEV-34712))

### Data types <a href="#data-types" id="data-types"></a>

* Comparison ROW(stored\_func(),1)=ROW(1,1) erroneously called stored\_func() twice per row. It led to a performance degradation, as well as to a double execution of the possible stored function side effects. ([MDEV-36322](https://jira.mariadb.org/browse/MDEV-36322))

### Stored Routines <a href="#stored-routines" id="stored-routines"></a>

* Add support for the pre-defined weak SYS\_REFCURSOR ([MDEV-20034](https://jira.mariadb.org/browse/MDEV-20034))

### Server <a href="#server" id="server"></a>

* TO\_CHAR FM format not recognized in SQL\_MODE=Oracle ([MDEV-36216](https://jira.mariadb.org/browse/MDEV-36216))
* Support mariadb-check and CHECK TABLE with SEQUENCE ([MDEV-22491](https://jira.mariadb.org/browse/MDEV-22491))

### Optimizer <a href="#optimizer" id="optimizer"></a>

* find\_order\_in\_list mismatch when order item needs fixing() ([MDEV-36607](https://jira.mariadb.org/browse/MDEV-36607))
* If the join\_condition is specified via USING (column\_list), the query plan depends on the sequence of tables in the query ([MDEV-36592](https://jira.mariadb.org/browse/MDEV-36592))
* Add support for optimizer hints ([MDEV-35504](https://jira.mariadb.org/browse/MDEV-35504))
  * QB\_NAME()
  * NO\_RANGE\_OPTIMIZATION()
  * NO\_ICP()
  * MRR(), NO\_MRR()
  * BKA(), NO\_BKA()
  * BNL(), NO\_BNL()
* Add support for subquery optimizer hints ([MDEV-34888](https://jira.mariadb.org/browse/MDEV-34888))
  * SEMIJOIN()
  * SUBQUERY()
* Add support for join order hints ([MDEV-34870](https://jira.mariadb.org/browse/MDEV-34870))
  * JOIN\_FIXED\_ORDER similar to existing STRAIGHT\_JOIN hint
  * JOIN\_ORDER to apply the specified table order
  * JOIN\_PREFIX to hint what tables should be first in the join
  * JOIN\_SUFFIX to hint what tables should be last in the join
* Add support for the MAX\_EXECUTION\_TIME hint ([MDEV-34860](https://jira.mariadb.org/browse/MDEV-34860))

### GIS <a href="#gis" id="gis"></a>

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

### Trigger <a href="#trigger" id="trigger"></a>

* Add support for TRIGGERS that fire on multiple events ([MDEV-10164](https://jira.mariadb.org/browse/MDEV-10164))

### Replication <a href="#replication" id="replication"></a>

* Server now displays if it was started with [skip-slave-start](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/starting-and-stopping-mariadb/mariadbd-options#skip-slave-start) option ([MDEV-27669](https://jira.mariadb.org/browse/MDEV-27669))

### Galera <a href="#galera" id="galera"></a>

* Skip FK checks in Galera during applying in IST ([MDEV-34822](https://jira.mariadb.org/browse/MDEV-34822))

### Audit Plugin <a href="#audit-plugin" id="audit-plugin"></a>

* Log HOST:PORT of incoming connection instead of just the host ([MDEV-1282](https://jira.mariadb.org/browse/MDEV-1282))
* Add tls\_version field for connection audit plugins ([MDEV-33834](https://jira.mariadb.org/browse/MDEV-33834))

### Configuration <a href="#configuration" id="configuration"></a>

* Get option group suffix from $MARIADB\_GROUP\_SUFFIX in addition to $MYSQL\_GROUP\_SUFFIX ([MDEV-21375](https://jira.mariadb.org/browse/MDEV-21375))

### Clients and Scripts <a href="#clients-and-scripts" id="clients-and-scripts"></a>

* Can set an alternative directory path for searching scripts invoked via the source command, with the `--script-dir` mariadb client option ([MDEV-23818](https://jira.mariadb.org/browse/MDEV-23818))

## Changelog <a href="#changelog" id="changelog"></a>

For a complete list of changes made in MariaDB 12.0.1, with links to detailed information on each push, see the [changelog](https://kb-archive.mariadb.net/en/mariadb-12-0-1-changelog/).

## Contributors <a href="#contributors" id="contributors"></a>

For a full list of contributors to MariaDB 12.0.1, see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-11-7-2-and-mariadb-11-8-1-now-available/).

***

{% include "../../.gitbook/includes/announce.md" %}

{% @marketo/form formid="4316" formId="4316" %}
