# MariaDB 10.2.44 Release Notes

[Download](https://downloads.mariadb.org/mariadb/10.2.44/)[Release Notes](mariadb-10244-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10244-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 20 May 2022

[MariaDB 10.2](what-is-mariadb-102.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.44](mariadb-10244-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

* As per the [MariaDB Maintenance Policy](https://mariadb.org/about/#maintenance-policy), this will be the final release of [MariaDB 10.2](what-is-mariadb-102.md)

### Replication

* Automatically generated Gtid\_log\_list\_event is made to recognize within replication event group as a formal member ([MDEV-28550](https://jira.mariadb.org/browse/MDEV-28550))
* [Replication unsafe](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/unsafe-statements-for-statement-based-replication) [INSERT .. ON DUPLICATE KEY UPDATE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/inserting-loading-data/insert-on-duplicate-key-update) using two or more unique key values at a time with [MIXED format binlogging](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log/binary-log-formats#mixed-logging) is corrected ([MDEV-28310](https://jira.mariadb.org/browse/MDEV-28310))
* [Replication unsafe](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/unsafe-statements-for-statement-based-replication) [INSERT .. ON DUPLICATE KEY UPDATE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/data-manipulation/inserting-loading-data/insert-on-duplicate-key-update) stops issuing unnecessary "Unsafe statement" with [MIXED binlog format](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/server-monitoring-logs/binary-log/binary-log-formats#mixed-logging) ([MDEV-21810](https://jira.mariadb.org/browse/MDEV-21810))
* Incomplete replication event groups are detected to error out by the slave IO thread ([MDEV-27697](https://jira.mariadb.org/browse/MDEV-27697))
* [mysqlbinlog --stop-never --raw](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog/mariadb-binlog-options) now flushes the result file to disk after each processed event so the file can be listed with the actual bytes ([MDEV-14608](https://jira.mariadb.org/browse/MDEV-14608))

### Backup

* Incorrect binlogs after Galera SST using rsync and [mariadb-backup](https://mariadb.com/docs/server/server-usage/backup-and-restore/mariadb-backup) ([MDEV-27524](https://jira.mariadb.org/browse/MDEV-27524))
* [mariadb-backup](https://mariadb.com/docs/server/server-usage/backup-and-restore/mariadb-backup) does not detect multi-source replication slave ([MDEV-21037](https://jira.mariadb.org/browse/MDEV-21037))
* Useless warning "InnoDB: Allocated tablespace ID for , old maximum was 0" during backup stage ([MDEV-27343](https://jira.mariadb.org/browse/MDEV-27343))
* [mariadb-backup](https://mariadb.com/docs/server/server-usage/backup-and-restore/mariadb-backup) prepare fails for incrementals if a new schema is created after full backup is taken ([MDEV-28446](https://jira.mariadb.org/browse/MDEV-28446))

### Optimizer

* Subquery in an UPDATE query uses full scan instead of range ([MDEV-22377](https://jira.mariadb.org/browse/MDEV-22377))
* Assertion \`item1->type() == Item::FIELD\_ITEM ... ([MDEV-19398](https://jira.mariadb.org/browse/MDEV-19398))
* Server crashes in Expression\_cache\_tracker::fetch\_current\_stats ([MDEV-28268](https://jira.mariadb.org/browse/MDEV-28268))
* MariaDB server crash at Item\_subselect::init\_expr\_cache\_tracker ([MDEV-26164](https://jira.mariadb.org/browse/MDEV-26164), [MDEV-26047](https://jira.mariadb.org/browse/MDEV-26047))
* Crash with union of my\_decimal type in ORDER BY clause ([MDEV-25994](https://jira.mariadb.org/browse/MDEV-25994))
* SIGSEGV in st\_join\_table::cleanup ([MDEV-24560](https://jira.mariadb.org/browse/MDEV-24560))
* Assertion \`!eliminated' failed in Item\_subselect::exec ([MDEV-28437](https://jira.mariadb.org/browse/MDEV-28437))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-46669](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46669)
  * [CVE-2022-21427](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-21427)
  * [CVE-2022-27377](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27377)
  * [CVE-2022-27378](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27378)
  * [CVE-2022-27380](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27380)
  * [CVE-2022-27381](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27381)
  * [CVE-2022-27383](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27383)
  * [CVE-2022-27384](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27384)
  * [CVE-2022-27386](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27386)
  * [CVE-2022-27387](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27387)
  * [CVE-2022-27445](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-27445)
  * [CVE-2022-32083](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-32083)
  * [CVE-2022-32088](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-32088)

Upgrading from 10.2 versions earlier than 10.2.17 is **highly recommended**\
for all [**Galera**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability\
issues with earlier versions. See the bug issue page for more information.\
When upgrading from [MariaDB 10.2.16](mariadb-10216-release-notes.md) or earlier to [MariaDB 10.2.17](mariadb-10217-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in [MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.2.44](mariadb-10244-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-10244-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.44](mariadb-10244-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-9-1-10-8-3-10-7-4-10-6-8-10-5-16-10-4-25-10-3-35-and-10-2-44-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
