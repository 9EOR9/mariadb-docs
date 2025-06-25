# MariaDB 10.4.11 Release Notes

The most recent release of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

Note that this version contains an issue that disabled all events created by a server with a different server\_id. See [MDEV-21758](https://jira.mariadb.org/browse/MDEV-21758) for details.

[Download](https://downloads.mariadb.org/mariadb/10.4.11/)[Release Notes](mariadb-10411-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10411-changelog.md)[Overview of 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md)

**Release date:** 11 Dec 2019

[MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) is the current _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.11](mariadb-10411-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) **see the**[**What is MariaDB 10.4?**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

### General

* [MDEV-13492](https://jira.mariadb.org/browse/MDEV-13492): SEC\_E\_INVALID\_TOKEN when server sends large message during SSL handshake

### mariadb-backup

* [MDEV-18310](https://jira.mariadb.org/browse/MDEV-18310): Aria engine: Undo phase failed from incremental backup

### InnoDB

* [MDEV-20949](https://jira.mariadb.org/browse/MDEV-20949): Stop issuing '`row size`' error on DML
* [MDEV-20832](https://jira.mariadb.org/browse/MDEV-20832): Don't print "`row size too large`" warnings in error log if `innodb_strict_mode=OFF` and `log_warnings<=2`
* [MDEV-21024](https://jira.mariadb.org/browse/MDEV-21024): Remove redundant writes to the redo log
* [MDEV-21069](https://jira.mariadb.org/browse/MDEV-21069): Crash on `DROP TABLE` if the data file is corrupted
* some cleanup of AIO code, to better report errors
* [MDEV-20611](https://jira.mariadb.org/browse/MDEV-20611): MRR scan over partitioned InnoDB table produces "`Out of memory`" error
* [MDEV-21088](https://jira.mariadb.org/browse/MDEV-21088): Table cannot be loaded after instant `ADD/DROP COLUMN`
* [MDEV-21045](https://jira.mariadb.org/browse/MDEV-21045): heap-use-after-poison in `ADD PRIMARY KEY` after instant `ADD COLUMN`
* [MDEV-21172](https://jira.mariadb.org/browse/MDEV-21172): Memory leak after failed `ADD PRIMARY KEY`
* [MDEV-21158](https://jira.mariadb.org/browse/MDEV-21158): `trx_undo_seg_free()` is never redo-logged
* [MDEV-20190](https://jira.mariadb.org/browse/MDEV-20190): Instant operation fails when add column and collation change on non-indexed column

### Optimizer

* [MDEV-21044](https://jira.mariadb.org/browse/MDEV-21044): Wrong result when using a smaller size for sort buffer
* [MDEV-20611](https://jira.mariadb.org/browse/MDEV-20611): MRR scan over partitioned InnoDB table produces "Out of memory" error
* [MDEV-20407](https://jira.mariadb.org/browse/MDEV-20407): mysqld got `signal 11`; `rowid_filter`

### Replication

* [MDEV-19376](https://jira.mariadb.org/browse/MDEV-19376): `Repl_semi_sync_master::commit_trx` assertion failure
* [MDEV-20707](https://jira.mariadb.org/browse/MDEV-20707): Missing memory barrier in parallel replication error handler in `wait_for_prior_commit()`

### Versioning

* [MDEV-18929](https://jira.mariadb.org/browse/MDEV-18929): 2nd execution of SP does not detect `ER_VERS_NOT_VERSIONED`
* [MDEV-21011](https://jira.mariadb.org/browse/MDEV-21011): Table corruption reported for versioned partitioned table after `DELETE`

### Misc

* Packages for Fedora 31 have been added in this release
* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) for Fedora 29
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 10.4.11](mariadb-10411-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-4-series/mariadb-10411-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.11](mariadb-10411-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-11-10-3-21-and-10-2-30-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
