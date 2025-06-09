# MariaDB 10.2.19 Release Notes

The most recent release of [MariaDB 10.2](what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.19/)[Release Notes](mariadb-10219-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10219-changelog.md)[Overview of 10.2](what-is-mariadb-102.md)

**Release date:** 13 Nov 2018

[MariaDB 10.2](what-is-mariadb-102.md) is the previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.1](../release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.19](mariadb-10219-release-notes.md) will be a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.2**](what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](what-is-mariadb-102.md) **page.**

Upgrading from earlier 10.2.x versions is **highly recommended** for all **Galera** users due to bug [MDEV-12837](https://jira.mariadb.org/browse/MDEV-12837) which caused serious stability issues with earlier versions. See the bug issue page for more information.

Thanks, and enjoy MariaDB!

## Notable Changes

* [innodb\_safe\_truncate](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables)\
  system variable for a backup-safe TRUNCATE TABLE implementation that is based\
  on RENAME, CREATE, DROP ([MDEV-14717](https://jira.mariadb.org/browse/MDEV-14717), [MDEV-14585](https://jira.mariadb.org/browse/MDEV-14585), [MDEV-13564](https://jira.mariadb.org/browse/MDEV-13564))
  * Default value for this variable is `ON`
  * If you absolutely must use [XtraBackup](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/backing-up-and-restoring-databases-percona-xtrabackup/percona-xtrabackup-overview) instead of[Mariabackup](broken-reference), you can set it to `OFF` and restart\
    the server
* [MDEV-17289](https://jira.mariadb.org/browse/MDEV-17289): Multi-pass recovery fails to apply some redo log records
* [MDEV-17073](https://jira.mariadb.org/browse/MDEV-17073): INSERT…ON DUPLICATE KEY UPDATE became more deadlock-prone
* [MDEV-17491](https://jira.mariadb.org/browse/MDEV-17491): micro optimize page\_id\_t
* [MDEV-13671](https://jira.mariadb.org/browse/MDEV-13671): InnoDB should use case-insensitive column name comparisons like the rest of the server
* Fixes for indexed virtual columns: [MDEV-17215](https://jira.mariadb.org/browse/MDEV-17215), [MDEV-16980](https://jira.mariadb.org/browse/MDEV-16980)
* [MDEV-17433](https://jira.mariadb.org/browse/MDEV-17433): Allow InnoDB start up with empty ib\_logfile0 from `mariabackup --prepare`
* [MDEV-12547](https://jira.mariadb.org/browse/MDEV-12547): InnoDB FULLTEXT index has too strict innodb\_ft\_result\_cache\_limit max limit
* [MDEV-17541](https://jira.mariadb.org/browse/MDEV-17541): KILL QUERY during lock wait in FOREIGN KEY check causes hang
* [MDEV-17531](https://jira.mariadb.org/browse/MDEV-17531): Crash in RENAME TABLE with FOREIGN KEY and FULLTEXT INDEX
* [MDEV-17532](https://jira.mariadb.org/browse/MDEV-17532): Performance\_schema reports wrong directory for the temporary\
  files of `ALTER TABLE…ALGORITHM=INPLACE`
* [MDEV-17545](https://jira.mariadb.org/browse/MDEV-17545): Predicate lock for SPATIAL INDEX should lock non-matching record
* [MDEV-17546](https://jira.mariadb.org/browse/MDEV-17546): SPATIAL INDEX should not be allowed for FOREIGN KEY
* [MDEV-17548](https://jira.mariadb.org/browse/MDEV-17548): Incorrect access to off-page column for indexed virtual column
* [MDEV-12023](https://jira.mariadb.org/browse/MDEV-12023): Assertion failure `sym_node->table != NULL` on startup
* [MDEV-17230](https://jira.mariadb.org/browse/MDEV-17230): encryption\_key\_id from alter is ignored by encryption threads
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be\
  the last release of [MariaDB 10.2](what-is-mariadb-102.md) for Fedora 27
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-3282](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3282)
  * [CVE-2016-9843](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-9843)
  * [CVE-2018-3174](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3174)
  * [CVE-2018-3143](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3143)
  * [CVE-2018-3156](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3156)
  * [CVE-2018-3251](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3251)
  * [CVE-2018-3185](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3185)
  * [CVE-2018-3277](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3277)
  * [CVE-2018-3162](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3162)
  * [CVE-2018-3173](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3173)
  * [CVE-2018-3200](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3200)
  * [CVE-2018-3284](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3284)

When upgrading from [MariaDB 10.2.16](mariadb-10216-release-notes.md) or earlier to [MariaDB 10.2.17](mariadb-10217-release-notes.md) or higher,\
running `[mysql_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade)` is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).

## Changelog

For a complete list of changes made in [MariaDB 10.2.19](mariadb-10219-release-notes.md) with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-102-series/mariadb-10219-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.2.19](mariadb-10219-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-2-19-now-available).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
