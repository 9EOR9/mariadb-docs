# MariaDB 10.2.13 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.13)[Release Notes](mariadb-10213-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10213-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 13 Feb 2018

[MariaDB 10.2](what-is-mariadb-102.md) is the current stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.13](mariadb-10213-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Upgrading from earlier 10.2.x versions is **highly recommended** for all **Galera** users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability issues with earlier versions. See the bug issue page for more information.

Thanks, and enjoy MariaDB!

## Notable Changes

* [InnoDB](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-versions) updated to 5.7.21
* The [MyRocks](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/myrocks) storage engine is now Beta.
* [Galera wsrep library](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md) updated to 25.3.23
* [MDEV-14611](https://jira.mariadb.org/browse/MDEV-14611) - ALTER TABLE EXCHANGE PARTITION does not work properly when used with DATA DIRECTORY
* [MDEV-15249](https://jira.mariadb.org/browse/MDEV-15249) - Crash in MVCC read after IMPORT TABLESPACE
* Foreign key bugs:
  * [MDEV-15199](https://jira.mariadb.org/browse/MDEV-15199) - Referential integrity broken in ON DELETE CASCADE / [MDEV-14222](https://jira.mariadb.org/browse/MDEV-14222) Unnecessary 'cascade' memory allocation for every updated row
  * [MDEV-15219](https://jira.mariadb.org/browse/MDEV-15219) - FOREIGN KEY CASCADE or SET NULL operations will not resume after lock wait
  * [MDEV-15042](https://jira.mariadb.org/browse/MDEV-15042) - INSERT ON DUPLICATE KEY UPDATE produces error 1032 (Can't find record)
  * [MDEV-13205](https://jira.mariadb.org/browse/MDEV-13205) - InnoDB: Failing assertion: !dict\_index\_is\_online\_ddl(index) upon ALTER TABLE
* [MDEV-14958](https://jira.mariadb.org/browse/MDEV-14958) - Merge new release of InnoDB MySQL 5.7.21 to 10.2
* [MDEV-15165](https://jira.mariadb.org/browse/MDEV-15165) - InnoDB purge for index on virtual column is trying to access an incomplete record
* [MDEV-15143](https://jira.mariadb.org/browse/MDEV-15143) - InnoDB: Rollback of trx with id 0 completed
* [MDEV-11415](https://jira.mariadb.org/browse/MDEV-11415) - Remove excessive undo logging during [ALTER TABLE…ALGORITHM=COPY](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-definition/alter/alter-table#algorithm)
* [MDEV-15016](https://jira.mariadb.org/browse/MDEV-15016) - multiple page cleaner threads use a lot of CPU
* [MDEV-14941](https://jira.mariadb.org/browse/MDEV-14941) - Timeouts on persistent statistics tables caused by [MDEV-14511](https://jira.mariadb.org/browse/MDEV-14511)
* [MDEV-14985](https://jira.mariadb.org/browse/MDEV-14985) - innodb\_undo\_log\_truncate may be blocked if transactions were recovered at startup
* [MDEV-14441](https://jira.mariadb.org/browse/MDEV-14441) - InnoDB hangs when setting innodb\_adaptive\_hash\_index=OFF during UPDATE
* [MDEV-14887](https://jira.mariadb.org/browse/MDEV-14887) - On a 32-bit system, [MariaDB 10.2](what-is-mariadb-102.md) mishandles data file sizes exceeding 4GiB
* Fedora 27 packages added
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.2](what-is-mariadb-102.md) for Fedora 25

### Security Fixes

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-2562](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2562)
  * [CVE-2018-2622](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2622)
  * [CVE-2018-2640](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2640)
  * [CVE-2018-2665](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2665)
  * [CVE-2018-2668](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2668)
  * [CVE-2018-2612](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-2612)

## Notes

For a complete list of changes made in [MariaDB 10.2.13](mariadb-10213-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10213-changelog.md).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
