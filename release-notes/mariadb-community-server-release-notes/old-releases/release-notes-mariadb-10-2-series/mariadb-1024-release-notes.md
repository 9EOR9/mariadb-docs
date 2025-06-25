# MariaDB 10.2.4 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.4)[Release Notes](mariadb-1024-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-1024-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 17 Feb 2017

[MariaDB 10.2](what-is-mariadb-102.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.4](mariadb-1024-release-notes.md) is a [_**Release Candidate**_](../../../mariadb-release-criteria.md) _**(RC)**_ release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the first release candidate (RC) release in the [MariaDB 10.2](what-is-mariadb-102.md) series.

* New [reserved word](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sql-language-structure/reserved-words): ROWS. This can no longer be used as an [identifier](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sql-language-structure/identifier-names) without being quoted.
* Default [binary log format](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables) changed to mixed ([MDEV-7635](https://jira.mariadb.org/browse/MDEV-7635)).
* Default values of [replicate\_annotate\_row\_events](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables) and [binlog\_annotate\_row\_events](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables) changed to `ON` ([MDEV-7635](https://jira.mariadb.org/browse/MDEV-7635))..
* Default value of [slave\_net\_timeout](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables) reduced to 60 seconds ([MDEV-7635](https://jira.mariadb.org/browse/MDEV-7635)).
* Default value of [group\_concat\_max\_len](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#group_concat_max_len) changed to 1M ([MDEV-7635](https://jira.mariadb.org/browse/MDEV-7635)).
* Default value of [innodb\_compression\_algorithm](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) changed to `zlib` - this does not mean pages are now compressed by default, see [compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression) ([MDEV-11838](https://jira.mariadb.org/browse/MDEV-11838)).
* Default value of [innodb\_log\_compressed\_pages](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) changed to `ON` ([MDEV-7635](https://jira.mariadb.org/browse/MDEV-7635)).
* Default value of [innodb\_use\_atomic\_writes](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) and [innodb\_use\_trim](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) changed to `ON`.
* The unused [innodb\_api\_\*](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) variables have been removed ([MDEV-12050](https://jira.mariadb.org/browse/MDEV-12050)).
* Numerous other system variable changes.
* DML\_only [flashback](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log/flashback) can rollback instances/databases/tables to an old snapshot ([MDEV-10570](https://jira.mariadb.org/browse/MDEV-10570)).
* Implement [ST\_AsGeoJSON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/geometry-constructors/geojson-st_asgeojson) and [ST\_GeomFromGeoJSON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/geometry-constructors/st_geomfromgeojson) functions so the spatial features can be imported/exported using GeoJSON format ([MDEV-11042](https://jira.mariadb.org/browse/MDEV-11042)).
* [Zipped File Tables](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect/connect-table-types/connect-zipped-file-tables) for the CONNECT storage engine ([MDEV-11295](https://jira.mariadb.org/browse/MDEV-11295)).
* Persistent [AUTO\_INCREMENT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/auto_increment) for InnoDB ([MDEV-6076](https://jira.mariadb.org/browse/MDEV-6076)).
* Default values of the [aria\_recover](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/aria/aria-system-variables#aria_recover) and [myisam\_recover\_options](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/myisam-storage-engine/myisam-system-variables#myisam_recover_options) system variables changed to `BACKUP,QUICK`.
* Support COM\_RESET\_CONNECTION ([MDEV-10340](https://jira.mariadb.org/browse/MDEV-10340)).
* [innodb\_log\_files\_in\_group](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) can now be set to `1` ([MDEV-12061](https://jira.mariadb.org/browse/MDEV-12061)).
* MariaDB now works when started with a MySQL 5.7.6+ data directory. ([MDEV-11170](https://jira.mariadb.org/browse/MDEV-11170))
* OpenSUSE 42 repositories have been added in this release.
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.2](what-is-mariadb-102.md) for Ubuntu 12.04 "precise", Fedora 23, and openSUSE 13

### New status variables

* [innodb\_have\_punch\_hole](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables)
* [innodb\_pages0read](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables)
* [innodb\_scrub\_log](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables)
* [innodb\_encryption\_num\_key\_requests](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/innodb-status-variables)
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Notes

For a complete list of changes made in [MariaDB 10.2.4](mariadb-1024-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-1024-changelog.md).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
