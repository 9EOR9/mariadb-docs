# MariaDB 10.5.10 Release Notes

The most recent release of [MariaDB 10.5](what-is-mariadb-105.md) is:[**MariaDB 10.5.28**](mariadb-10-5-28-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.5.28/)

[Download 10.5.10](https://downloads.mariadb.org/mariadb/10.5.10/)[Release Notes](mariadb-10510-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-10510-changelog.md)[Overview of 10.5](what-is-mariadb-105.md)

**Release date:** 7 May 2021

[MariaDB 10.5](what-is-mariadb-105.md) is the current _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.4](../../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.5.10](mariadb-10510-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.5**](what-is-mariadb-105.md) **see the**[**What is MariaDB 10.5?**](what-is-mariadb-105.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* [ST\_DISTANCE\_SPHERE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/geometry-constructors/geometry-relations/st_distance_sphere) for calculating the spherical distance between two geometries (point or multipoint) on a sphere ([MDEV-13467](https://jira.mariadb.org/browse/MDEV-13467))
* Crash with invalid multi-table update of view in 2nd execution of SP ([MDEV-24823](https://jira.mariadb.org/browse/MDEV-24823))
* Incorrect name resolution for subqueries in ON expressions ([MDEV-25362](https://jira.mariadb.org/browse/MDEV-25362))
* Complex query in Store procedure corrupts results ([MDEV-25182](https://jira.mariadb.org/browse/MDEV-25182))
* `DELETE HISTORY` may delete current data on system-versioned table ([MDEV-25468](https://jira.mariadb.org/browse/MDEV-25468))
* Crashes with nested table value constructors ([MDEV-22786](https://jira.mariadb.org/browse/MDEV-22786))
* Server crashes in `thd_clear_errors()` ([MDEV-23542](https://jira.mariadb.org/browse/MDEV-23542))
* The statement set `password=password('')` executed in PS mode fails in case it is run by a user with expired password ([MDEV-25197](https://jira.mariadb.org/browse/MDEV-25197))

### mariadb-backup

* RENAME TABLE causes "Ignoring data file" messages ([MDEV-25568](https://jira.mariadb.org/browse/MDEV-25568))

### InnoDB

* Deprecated the `*innodb` and `*none` options in [innodb\_checksum\_algorithm](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables#innodb_checksum_algorithm) ([MDEV-25106](https://jira.mariadb.org/browse/MDEV-25106))
* MVCC read from index on CHAR or VARCHAR wrongly omits rows ([MDEV-25459](https://jira.mariadb.org/browse/MDEV-25459))
* Race conditions in persistent statistics ([MDEV-10682](https://jira.mariadb.org/browse/MDEV-10682), [MDEV-18802](https://jira.mariadb.org/browse/MDEV-18802), [MDEV-25051](https://jira.mariadb.org/browse/MDEV-25051))
* Sequence created by one connection remains invisible to another ([MDEV-24545](https://jira.mariadb.org/browse/MDEV-24545))
* innodb\_flush\_method=O\_DIRECT fails on compressed tables ([MDEV-25121](https://jira.mariadb.org/browse/MDEV-25121))
* RESET MASTER hangs ([MDEV-24302](https://jira.mariadb.org/browse/MDEV-24302))
* InnoDB crash recovery fixes ([MDEV-25031](https://jira.mariadb.org/browse/MDEV-25031), [MDEV-25110](https://jira.mariadb.org/browse/MDEV-25110))

### Replication

* Replication Heartbeat event was uncapable to cary 4GB+ offsets ([MDEV-16146](https://jira.mariadb.org/browse/MDEV-16146))
* FLUSH LOGS race against Binlog checkpoint event creation ([MDEV-24526](https://jira.mariadb.org/browse/MDEV-24526))￼
* slave\_compressed\_protocol did not work correctly with semi-sync ([MDEV-24773](https://jira.mariadb.org/browse/MDEV-24773))
* DROP TABLE should not cause "Query caused different errors on master and slave" on slave when it failed on master ([MDEV-25530](https://jira.mariadb.org/browse/MDEV-25530))
* Killing server during RESET MASTER may lose MyRocks transaction ([MDEV-25305](https://jira.mariadb.org/browse/MDEV-25305))

### Galera

* [Galera](https://app.gitbook.com/o/diTpXxF5WsbHqTReoBsS/s/3VYeeVGUV4AMqrA3zwy7/) updated to 26.4.8
* SET PASSWORD command fail with wsrep api ([MDEV-25258](https://jira.mariadb.org/browse/MDEV-25258))
* Long BF log wait turns on InnoDB Monitor output without telling, never turns it off ([MDEV-25319](https://jira.mariadb.org/browse/MDEV-25319))
* Assertion \`\`state\_ == s\_exec'`failed in`wsrep::client\_state::start\_transaction\` ([MDEV-22227](https://jira.mariadb.org/browse/MDEV-22227))
* Frequently Crashing Mariadb Cluster 10.4.18 ([MDEV-24980](https://jira.mariadb.org/browse/MDEV-24980))
* Signal 11 on `TABLE_LIST::placeholder()` ([MDEV-24878](https://jira.mariadb.org/browse/MDEV-24878))
* `ALTER TABLE` not replicated with Galera in [MariaDB 10.5.9](mariadb-1059-release-notes.md) ([MDEV-24956](https://jira.mariadb.org/browse/MDEV-24956))
* "Flush SSL" command doesn't reload wsrep cert ([MDEV-22668](https://jira.mariadb.org/browse/MDEV-22668))
* Avoid unnecessary rollbacks with SR ([MDEV-25553](https://jira.mariadb.org/browse/MDEV-25553))

### Packaging & Misc

* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.5](what-is-mariadb-105.md) for Ubuntu 16.04 Xenial and Fedora 32
* Ubuntu 21.04 Hirsute and Fedora 34 repositories added

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-2166](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2166)
  * [CVE-2021-2154](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2154)
  * [CVE-2022-21451](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-21451)

MongoDB protocol support files for the [CONNECT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) engine are missing in this release.\
If you want to use [CONNECT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) engine with MongoDB, you need to download [Mongo2.jar](https://github.com/MariaDB/server/raw/mariadb-10.2.38/storage/connect/mysql-test/connect/std_data/Mongo2.jar) or [Mongo3.jar](https://github.com/MariaDB/server/raw/mariadb-10.2.38/storage/connect/mysql-test/connect/std_data/Mongo3.jar) and put a path to this file into the `connect_class_path` in the `my.cnf`.

## Changelog

For a complete list of changes made in [MariaDB 10.5.10](mariadb-10510-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-10510-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.5.10](mariadb-10510-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-10-10-4-19-10-3-29-and-10-2-38-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
