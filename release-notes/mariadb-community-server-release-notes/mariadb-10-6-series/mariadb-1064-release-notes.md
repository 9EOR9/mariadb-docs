# MariaDB 10.6.4 Release Notes

The most recent release of [MariaDB 10.6](what-is-mariadb-106.md) is:[**MariaDB 10.6.21**](mariadb-10-6-21-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.6.21/)

[Download 10.6.4](https://downloads.mariadb.org/mariadb/10.6.4)[Release Notes](mariadb-1064-release-notes.md)[Changelog](../changelogs/changelogs-mariadb-106-series/mariadb-1064-changelog.md)[Overview of 10.6](what-is-mariadb-106.md)

**Release date:** 6 Aug 2021

Warning: This version can cause InnoDB file corruption on FreeBSD and on AIX. Stick to an earlier release, or upgrade to a more recent release, if you are running either of these environments. See [MDEV-26537](https://jira.mariadb.org/browse/MDEV-26537).

[MariaDB 10.6](what-is-mariadb-106.md) is the current stable series of MariaDB. It is an evolution\
of [MariaDB 10.5](../mariadb-10-5-series/what-is-mariadb-105.md) with several entirely new features.

[MariaDB 10.6.4](mariadb-1064-release-notes.md) is a [_**Stable (GA)**_](../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.6**](what-is-mariadb-106.md) **see the**[**What is MariaDB 10.6?**](what-is-mariadb-106.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### InnoDB

* InnoDB no longer acquires advisory file locks by default ([MDEV-24393](https://jira.mariadb.org/browse/MDEV-24393))
* Encryption: Automatically disable key rotation checks for file\_key\_management plugin ([MDEV-14180](https://jira.mariadb.org/browse/MDEV-14180))
* Some fixes from MySQL 5.7.35 ([MDEV-26205](https://jira.mariadb.org/browse/MDEV-26205))
* Fixed scrubbing on AIX ([MDEV-26110](https://jira.mariadb.org/browse/MDEV-26110))
* buf\_pool.flush\_list corrupted by buffer pool resizing or ROW\_FORMAT=COMPRESSED ([MDEV-26200](https://jira.mariadb.org/browse/MDEV-26200))

### Optimizer

* A query that uses ORDER BY .. LIMIT clause and "Range checked for\
  each record optimization" could produce incorrect results under some\
  circumstances ([MDEV-25858](https://jira.mariadb.org/browse/MDEV-25858))
* Queries that have more than 32 equality conditions\
  comparing columns of different tables ("tableX.colX=tableY.colY) could cause\
  a stack overrun in the query optimizer ([MDEV-17783](https://jira.mariadb.org/browse/MDEV-17783), [MDEV-23937](https://jira.mariadb.org/browse/MDEV-23937))
* "Condition pushdown into derived table" optimization cannot be\
  applied if the expression being pushed refers to a derived table column which\
  is computed from expression that has a stored function call, @session variable\
  reference, or other similar construct.\
  The fix for [MDEV-25969](https://jira.mariadb.org/browse/MDEV-25969) makes it so that only the problematic part of the\
  condition is not pushed. The rest of the condition is now pushed. ([MDEV-25969](https://jira.mariadb.org/browse/MDEV-25969))
* A query with window function on the left side of the subquery could\
  cause a crash. ([MDEV-25630](https://jira.mariadb.org/browse/MDEV-25630))
* Fixed the issue fixed in MySQL Bug #76803: DML or locking SELECT statements\
  that use outer joins could produce this warning in the error log: `[ERROR] InnoDB: Unlock row could not find a 3 mode lock on the record.` ([MDEV-26106](https://jira.mariadb.org/browse/MDEV-26106))

### Packaging & Misc

* As per the [MariaDB Deprecation Policy](../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.6](what-is-mariadb-106.md) for Ubuntu 20.10 Groovy
* Debian 11 Bullseye repositories added
* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera-cluster/README.md) updated to 26.4.9
* Linux on IBM Z (s390x) architecture added with releases on Ubuntu-20.04 Focal

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-2372](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2372)
  * [CVE-2021-2389](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2389)

## Changelog

For a complete list of changes and bugfixes made in [MariaDB 10.6.4](mariadb-1064-release-notes.md), with links to detailed\
information on each push, see the [changelog](../changelogs/changelogs-mariadb-106-series/mariadb-1064-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.6.4](mariadb-1064-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-6-4-10-5-12-10-4-21-10-3-31-and-10-2-40-now-available/).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
