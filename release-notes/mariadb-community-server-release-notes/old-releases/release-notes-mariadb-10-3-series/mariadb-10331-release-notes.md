# MariaDB 10.3.31 Release Notes

The most recent release of [MariaDB 10.3](what-is-mariadb-103.md) is:[**MariaDB 10.3.39**](mariadb-10-3-39-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.3.39/)

[Download 10.3.31](https://downloads.mariadb.org/mariadb/10.3.31/)[Release Notes](mariadb-10331-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10331-changelog.md)[Overview of 10.3](what-is-mariadb-103.md)

**Release date:** 6 Aug 2021

Warning: This version can cause InnoDB file corruption on FreeBSD and on AIX. If you are using AIX, please, stick to an earlier release, or upgrade to a more recent release. If you are using FreeBSD, upgrade to the bugfix release (the version ends with \_1) of the mariadb-server from the Ports Collection. See [MDEV-26537](https://jira.mariadb.org/browse/MDEV-26537).

[MariaDB 10.3](what-is-mariadb-103.md) is the previous stable series of MariaDB, and an evolution of[MariaDB 10.2](../release-notes-mariadb-10-2-series/what-is-mariadb-102.md) with several entirely new features not found anywhere else and\
with backported and reimplemented features from MySQL.

[MariaDB 10.3.31](mariadb-10331-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of MariaDB Server 10.3 see the** [**What is MariaDB 10.3?**](what-is-mariadb-103.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### InnoDB

* InnoDB no longer acquires advisory file locks by default ([MDEV-24393](https://jira.mariadb.org/browse/MDEV-24393))
* Encryption: Automatically disable key rotation checks for file\_key\_management plugin ([MDEV-14180](https://jira.mariadb.org/browse/MDEV-14180))
* Some fixes from MySQL 5.7.35 ([MDEV-26205](https://jira.mariadb.org/browse/MDEV-26205))

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
* Wrong result selecting from simple view with LIMIT and ORDER BY\
  Queries with views/derived table/CTEs that have this form: "(SELECT ... LIMIT )\
  ORDER BY ...>" could produce wrong results ([MDEV-25679](https://jira.mariadb.org/browse/MDEV-25679))

### Packaging & Misc

* As per the [MariaDB Deprecation Policy](../../../mariadb-platform-deprecation-policy.md), this will be the last release of [MariaDB 10.3](what-is-mariadb-103.md) for Ubuntu 20.10 Groovy
* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera-cluster/README.md) updated to 25.3.34

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2021-2372](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2372)
  * [CVE-2021-2389](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-2389)
  * [CVE-2021-46658](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46658)

When upgrading from [MariaDB 10.3.8](mariadb-1038-release-notes.md) or earlier to [MariaDB 10.3.9](mariadb-1039-release-notes.md) or higher,\
running [mysql\_upgrade](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_upgrade) is **required** due to changes introduced in[MDEV-14637](https://jira.mariadb.org/browse/MDEV-14637).\
MongoDB protocol support files for the [CONNECT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) engine are missing in this release.\
If you want to use [CONNECT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/connect) engine with MongoDB, you need to download[Mongo2.jar](https://github.com/MariaDB/server/raw/mariadb-10.2.38/storage/connect/mysql-test/connect/std_data/Mongo2.jar) or [Mongo3.jar](https://github.com/MariaDB/server/raw/mariadb-10.2.38/storage/connect/mysql-test/connect/std_data/Mongo3.jar) and put a path to this file into the `connect_class_path` in the `my.cnf`.

## Changelog

For a complete list of changes made in [MariaDB 10.3.31](mariadb-10331-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-3-series/mariadb-10331-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.3.31](mariadb-10331-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-6-4-10-5-12-10-4-21-10-3-31-and-10-2-40-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
