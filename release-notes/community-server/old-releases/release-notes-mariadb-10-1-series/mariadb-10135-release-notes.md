# MariaDB 10.1.35 Release Notes

The most recent release of [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is:[**MariaDB 10.1.48**](mariadb-10148-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.1.48/)

[Download](https://downloads.mariadb.org/mariadb/10.1.35)[Release Notes](mariadb-10135-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10135-changelog.md)[Overview of 10.1](changes-improvements-in-mariadb-10-1.md)

**Release date:** 7 Aug 2018

[MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) is a previous stable series of MariaDB. It is an evolution\
of [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.1.35](mariadb-10135-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

**For an overview of** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **see the**[**What is MariaDB 10.1?**](changes-improvements-in-mariadb-10-1.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

* New variable, [core\_file](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#core_file) for specifying whether to write a core file on crash.
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
* Galera [MDEV-15822](https://jira.mariadb.org/browse/MDEV-15822): WSREP: BF lock wait long for trx

### Security Fixes

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2018-3064](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3064)
  * [CVE-2018-3063](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3063)
  * [CVE-2018-3058](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3058)
  * [CVE-2018-3066](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-3066)

## Changelog

For a complete list of changes made in [MariaDB 10.1.35](mariadb-10135-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-101-series/mariadb-10135-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.1.35](mariadb-10135-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-1-35-and-mariadb-galera-cluster-10-0-36-now-available/).

A file format compatibility bug that was introduced in [MariaDB 10.1.0](mariadb-10-1-0-release-notes.md) was fixed in [MariaDB 10.1.21](mariadb-10121-release-notes.md).\
Using [page\_compression](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-page-compression) or non-default [innodb\_page\_size](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/innodb/innodb-system-variables) created files that were incompatible with [MariaDB 10.0](../release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md) or MySQL 5.6. [MariaDB 10.1.21](mariadb-10121-release-notes.md) and higher will convert affected files from earlier [MariaDB 10.1](changes-improvements-in-mariadb-10-1.md) releases to a compatible format.**This prevents a downgrade to earlier** [**MariaDB 10.1**](changes-improvements-in-mariadb-10-1.md) **versions.**[See the commit for details.](https://github.com/MariaDB/server/commit/ab1e6fefd869242d962cb91a006f37bb9ad534a7)

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
