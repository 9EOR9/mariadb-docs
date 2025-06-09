# MariaDB 10.3.9 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download](https://downloads.mariadb.org/mariadb/10.3.9)[Release Notes](mariadb-1039-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-1039-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 15 Aug 2018

[MariaDB 10.3](what-is-mariadb-103.md) is an evolution\
of [MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.3.9](mariadb-1039-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the**[**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page or watch the webinar recording,** [**What's new in MariaDB TX 3.0**](https://go.mariadb.com/mariadbtx3.0_webinar_registration-LP.html?utm_source=kb\&utm_campaign=mariadbtx-ondemand-webinar_kb-release-notes)**.**

Thanks, and enjoy MariaDB!

## Notable Changes

Notable changes of this release include:

* New variable [innodb\_log\_optimize\_ddl](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) for avoiding delay due to page flushing and allowing concurrent backup.
* New variable, [core\_file](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#core_file) for specifying whether to write a core file on crash.
* InnoDB updated to 5.7.23
* ALTER TABLE fixes:
  * [MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637) - Fix hang due to DDL with FOREIGN KEY or persistent statistics
  * [MDEV-15953](https://jira.mariadb.org/browse/MDEV-15953) - Alter InnoDB Partitioned Table Moves Files (which were originally not in the datadir) to the datadir
  * [MDEV-16515](https://jira.mariadb.org/browse/MDEV-16515) - InnoDB: Failing assertion: ++retries < 10000 in file dict0dict.cc line 2737
  * [MDEV-16809](https://jira.mariadb.org/browse/MDEV-16809) - Allow full redo logging for ALTER TABLE
  * [MDEV-16131](https://jira.mariadb.org/browse/MDEV-16131) - Assertion \`is\_instant() || id == DICT\_INDEXES\_ID' failed in dict\_index\_t::instant\_field\_value
  * [MDEV-16830](https://jira.mariadb.org/browse/MDEV-16830) - ALTER TABLE DROP FOREIGN KEY - unexpected end of stream error
* Temporary tables: [MDEV-16713](https://jira.mariadb.org/browse/MDEV-16713) - InnoDB hang with repeating log entry
* [MDEV-16596](https://jira.mariadb.org/browse/MDEV-16596) - Windows - redo log does not work on native 4K sector disks
* indexed virtual columns: [MDEV-15855](https://jira.mariadb.org/browse/MDEV-15855) - Deadlock between purge thread and DDL statement
* locking: [MDEV-16664](https://jira.mariadb.org/browse/MDEV-16664) - Change the default to innodb\_lock\_schedule\_algorithm=fcfs
* Galera: [MDEV-15822](https://jira.mariadb.org/browse/MDEV-15822) - WSREP: BF lock wait long for trx
* [MDEV-16675](https://jira.mariadb.org/browse/MDEV-16675) - Unnecessary explicit lock acquisition during UPDATE or DELETE
* Packages and a repository for openSUSE 15 have been added with this release, visit the [Repository Configuration Tool](https://downloads.mariadb.org/mariadb/repositories/) for instructions on adding the repository
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-3060](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3060)
  * [CVE-2018-3064](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3064)
  * [CVE-2018-3063](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3063)
  * [CVE-2018-3058](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3058)
  * [CVE-2018-3066](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3066)

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running `[mysql_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade)` is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.3.9](mariadb-1039-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-10-3-series/mariadb-1039-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.9](mariadb-1039-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-3-9-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
