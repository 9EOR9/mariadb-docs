# MariaDB 10.0.36 Release Notes

The most recent release in the [MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) series is:[**MariaDB 10.0.38**](mariadb-10038-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb/10.0.38)

[Download](https://downloads.mariadb.org/mariadb/10.0.36)[Release Notes](mariadb-10036-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-100-series/mariadb-10036-changelog.md)[Overview of 10.0](changes-improvements-in-mariadb-10-0.md)

**Release date:** 1 Aug 2018

[MariaDB 10.0](changes-improvements-in-mariadb-10-0.md) is a previous stable series of MariaDB. It is an evolution of [MariaDB 5.5](../release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md) with several entirely new features not found anywhere else and with\
backported and reimplemented features from MySQL 5.6.

This is a [_**Stable**_](../../../mariadb-release-criteria.md) (_GA_) release.

**For an overview of** [**MariaDB 10.0**](changes-improvements-in-mariadb-10-0.md) **see the**[**What is MariaDB 10.0?**](changes-improvements-in-mariadb-10-0.md) **page.**

Thanks, and enjoy MariaDB!

## Notable changes

* ALTER TABLE:
  * Bug #25928471: ONLINE ALTER AND CONCURRENT DELETE ON TABLE WITH MANY TEXT COLUMNS CAUSES CRASH
  * [MDEV-14693](https://jira.mariadb.org/browse/MDEV-14693) XA: Assertion \`!clust\_index->online\_log' failed in rollback\_inplace\_alter\_table
  * [MDEV-16119](https://jira.mariadb.org/browse/MDEV-16119) InnoDB lock->index refers to a freed object after failed ADD INDEX
  * [MDEV-16124](https://jira.mariadb.org/browse/MDEV-16124) fil\_rename\_tablespace() times out and crashes server during table-rebuilding ALTER TABLE
  * [MDEV-15953](https://jira.mariadb.org/browse/MDEV-15953) Alter InnoDB Partitioned Table Moves Files (which were originally not in the datadir) to the datadir
  * [MDEV-16851](https://jira.mariadb.org/browse/MDEV-16851) On schema mismatch in IMPORT TABLESPACE, display ROW\_FORMAT in clear text
* Fulltext search:
  * Bug #27041445 SERVER ABORTS IF FTS\_DOC\_ID EXCEEDS FTS\_DOC\_ID\_MAX\_STEP
  * Bug #26334149 - MYSQL CRASHES WHEN FULL TEXT INDEXES IBD FILES ARE ORPHANED DUE TO RENAME TABLE
  * Bug #27326796 - MYSQL CRASH WITH INNODB ASSERTION FAILURE IN FILE PARS0PARS.CC
  * [MDEV-16855](https://jira.mariadb.org/browse/MDEV-16855) Fix fts\_sync\_synchronization in InnoDB
* [MDEV-16267](https://jira.mariadb.org/browse/MDEV-16267) Wrong INFORMATION\_SCHEMA.INNODB\_BUFFER\_PAGE.TABLE\_NAME
* [MDEV-16456](https://jira.mariadb.org/browse/MDEV-16456) InnoDB error "returned OS error 71" complains about wrong path
* [MDEV-16596](https://jira.mariadb.org/browse/MDEV-16596) : Windows - redo log does not work on native 4K sector disks
* [MDEV-16515](https://jira.mariadb.org/browse/MDEV-16515) (also fixes some adaptive hash index corruption that can cause data corruption)
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-3064](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3064)
  * [CVE-2018-3063](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3063)
  * [CVE-2018-3058](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3058)
  * [CVE-2018-3066](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3066)

## Changelog

For a complete list of changes made in [MariaDB 10.0.36](mariadb-10036-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-100-series/mariadb-10036-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.0.36](mariadb-10036-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-0-36-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
