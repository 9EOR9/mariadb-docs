# MariaDB 10.5.11 Release Notes

The most recent release of [MariaDB 10.5](what-is-mariadb-105.md) is:[**MariaDB 10.5.28**](mariadb-10-5-28-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.5.28/)

[Download 10.5.11](https://downloads.mariadb.org/mariadb/10.5.11/)[Release Notes](mariadb-10511-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-10511-changelog.md)[Overview of 10.5](what-is-mariadb-105.md)

**Release date:** 23 Jun 2021

[MariaDB 10.5](what-is-mariadb-105.md) is the current _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.4](../../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.5.11](mariadb-10511-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of** [**MariaDB 10.5**](what-is-mariadb-105.md) **see the**[**What is MariaDB 10.5?**](what-is-mariadb-105.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

This version of MariaDB is being released now to fix the following two\
regressions:

* Table alias from previous statement interferes later commands ([MDEV-25672](https://jira.mariadb.org/browse/MDEV-25672))
* Join using derived with aggregation returns incorrect results ([MDEV-25714](https://jira.mariadb.org/browse/MDEV-25714))

In addition to the above, this release also contains the following fixes:

### InnoDB

* InnoDB spatial indexes miss large geometry fields after [MDEV-25459](https://jira.mariadb.org/browse/MDEV-25459) ([MDEV-25758](https://jira.mariadb.org/browse/MDEV-25758))
* Double free of transaction during truncate operation ([MDEV-25663](https://jira.mariadb.org/browse/MDEV-25663))
* Double free of table when inplace alter FTS add index fails ([MDEV-25721](https://jira.mariadb.org/browse/MDEV-25721))
* Potential hang in purge for virtual columns ([MDEV-25664](https://jira.mariadb.org/browse/MDEV-25664))
* Change buffer records are lost under heavy load ([MDEV-25783](https://jira.mariadb.org/browse/MDEV-25783))
* Not applying INSERT\_REUSE\_REDUNDANT ([MDEV-25745](https://jira.mariadb.org/browse/MDEV-25745))
* InnoDB recovery fails with `[ERROR] InnoDB: Not applying INSERT_REUSE_REDUNDANT due to corruption` ([MDEV-25745](https://jira.mariadb.org/browse/MDEV-25745))
* [CHECK TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/check-table) harvests InnoDB: Index 'abdcef' contains 10001 entries, should be\
  10000 ([MDEV-25783](https://jira.mariadb.org/browse/MDEV-25783))

### Replication

* Do not replicate killed multi-table [OPTIMIZE TABLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimizing-tables/optimize-table) when the signal arrives\
  before any table has been processed ([MDEV-22530](https://jira.mariadb.org/browse/MDEV-22530))
* Fix optimistic parallel applier to not deadlock on admin commands [OPTIMIZE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/optimizing-tables/optimize-table),[REPAIR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/repair-table), and [ANALYZE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/table-statements/analyze-table) ([MDEV-17515](https://jira.mariadb.org/browse/MDEV-17515))
* Backport [MDEV-20821](https://jira.mariadb.org/browse/MDEV-20821) parallel slave server shutdown hang ([MDEV-22370](https://jira.mariadb.org/browse/MDEV-22370))
* Removed deprecated `--base64-output` to correct BINLOG clause in[mysqlbinlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog) output ([MDEV-25222](https://jira.mariadb.org/browse/MDEV-25222))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-46666](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46666)
  * [CVE-2021-46657](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46657)

## Changelog

For a complete list of changes made in [MariaDB 10.5.11](mariadb-10511-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-10511-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.5.11](mariadb-10511-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-5-11-10-4-20-10-3-30-and-10-2-39-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
