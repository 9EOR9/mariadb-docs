# MariaDB 10.3.30 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download 10.3.30](https://downloads.mariadb.org/mariadb/10.3.30/)[Release Notes](mariadb-10330-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10330-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 23 Jun 2021

[MariaDB 10.3](what-is-mariadb-103.md) is the previous stable series of MariaDB, and an evolution of[MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else and\
with backported and reimplemented features from MySQL.

[MariaDB 10.3.30](mariadb-10330-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

This version of MariaDB is being released now to fix the following two\
regressions:

* Table alias from previous statement interferes later commands ([MDEV-25672](https://jira.mariadb.org/browse/MDEV-25672))
* Join using derived with aggregation returns incorrect results ([MDEV-25714](https://jira.mariadb.org/browse/MDEV-25714))

In addition to the above, this release also contains the following fixes:

### InnoDB

* Change buffer entries are lost on InnoDB restart ([MDEV-25869](https://jira.mariadb.org/browse/MDEV-25869))
* InnoDB spatial indexes miss large geometry fields after [MDEV-25459](https://jira.mariadb.org/browse/MDEV-25459) ([MDEV-25758](https://jira.mariadb.org/browse/MDEV-25758))
* Double free of transaction during truncate operation ([MDEV-25663](https://jira.mariadb.org/browse/MDEV-25663))
* Double free of table when inplace alter FTS add index fails ([MDEV-25721](https://jira.mariadb.org/browse/MDEV-25721))
* Potential hang in purge for virtual columns ([MDEV-25664](https://jira.mariadb.org/browse/MDEV-25664))
* Change buffer entries for secondary indexes are lost on InnoDB restart\
  ([MDEV-25869](https://jira.mariadb.org/browse/MDEV-25869))

### Replication

* Do not replicate killed multi-table OPTIMIZE TABLE when the signal arrives\
  before any table has been processed ([MDEV-22530](https://jira.mariadb.org/browse/MDEV-22530))
* Fix optistic parallel applier to not deadlock on admin commands OPTIMIZE,\
  REPAIR, and ANALYZE ([MDEV-17515](https://jira.mariadb.org/browse/MDEV-17515))
* Backport [MDEV-20821](https://jira.mariadb.org/browse/MDEV-20821) parallel slave server shutdown hang ([MDEV-22370](https://jira.mariadb.org/browse/MDEV-22370))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-46666](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46666)
  * [CVE-2021-46657](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46657)

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).\
MongoDB protocol support files for the [CONNECT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) engine are missing in this release.\
If you want to use [CONNECT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) engine with MongoDB, you need to download[Mongo2.jar](https://github.com/MariaDB/server/raw/mariadb-10.2.38/storage/connect/mysql-test/connect/std_data/Mongo2.jar) or [Mongo3.jar](https://github.com/MariaDB/server/raw/mariadb-10.2.38/storage/connect/mysql-test/connect/std_data/Mongo3.jar) and put a path to this file into the `connect_class_path` in the `my.cnf`.

## Changelog

For a complete list of changes made in [MariaDB 10.3.30](mariadb-10330-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10330-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.30](mariadb-10330-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-11-10-4-20-10-3-30-and-10-2-39-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
