# MariaDB 10.2.0 Release Notes

The most recent release of [MariaDB 10.2](release-notes-mariadb-10-2-series/what-is-mariadb-102.md) is:[**MariaDB 10.2.44**](release-notes-mariadb-10-2-series/mariadb-10244-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.2.44/)

[Download](https://downloads.mariadb.org/mariadb/10.2.0)[Release Notes](mariadb-1020-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-1020-changelog.md)[Overview of 10.2](release-notes-mariadb-10-2-series/what-is-mariadb-102.md)

**Release date:** 18 Apr 2016

[MariaDB 10.2](release-notes-mariadb-10-2-series/what-is-mariadb-102.md) is the current development series of MariaDB. It is an evolution\
of [MariaDB 10.1](release-notes-mariadb-10-1-series/changes-improvements-in-mariadb-10-1.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL 5.6 and 5.7.

[MariaDB 10.2.0](mariadb-1020-release-notes.md) is an [_**Alpha**_](../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**alpha**_**&#x20;releases on production systems!**

**For an overview of** [**MariaDB 10.2**](release-notes-mariadb-10-2-series/what-is-mariadb-102.md) **see the**[**What is MariaDB 10.2?**](release-notes-mariadb-10-2-series/what-is-mariadb-102.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

This is the first alpha release in the [MariaDB 10.2](release-notes-mariadb-10-2-series/what-is-mariadb-102.md) series.

Notable changes of this release include:

Syntax:

* [Window functions](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/window-functions) have been introduced. This release adds support for a limited set of functions, and the basic execution algorithm. Development continues to expand the set of supported functions and optimize the execution.
* The [SHOW CREATE USER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/show/show-create-user) statement was introduced.
* New [CREATE USER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/create-user) options for limiting resource usage and tls/ssl.
* New [ALTER USER](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/alter-user) statement.
* New [reserved-words](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sql-language-structure/reserved-words): OVER and RECURSIVE. These can no longer be used as [identifier-names](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-structure/sql-language-structure/identifier-names) without being quoted.

Scripts:

* Continuous binary log backup has been added to [mysqlbinlog](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/logging-tools/mariadb-binlog) - [MDEV-8713](https://jira.mariadb.org/browse/MDEV-8713).
* [mysql\_zap](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/clients-and-utilities/legacy-clients-and-utilities/mysql_zap) and mysqlbug have been removed - [MDEV-7376](https://jira.mariadb.org/browse/MDEV-7376), [MDEV-8654](https://jira.mariadb.org/browse/MDEV-8654).

Information Schema:

* Added an information schema plugin to report all user variables, which creates the [Information Schema USER\_VARIABLES Table](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/system-tables/information-schema/information-schema-tables/information-schema-user_variables-table) - [MDEV-7331](https://jira.mariadb.org/browse/MDEV-7331).

Variables:

* [aria\_recover](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/aria/aria-system-variables#aria_recover) has been renamed to [aria\_recover\_options](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/aria/aria-system-variables#aria_recover_options) - [MDEV-8542](https://jira.mariadb.org/browse/MDEV-8542).
* The server version can now be faked to work around dated applications that require a particular version string - [MDEV-7780](https://jira.mariadb.org/browse/MDEV-7780)
* [slave\_parallel\_workers](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables) is now an alias for slave\_parallel\_threads.
* New status variables [com\_alter\_user](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-status-variables#com_alter_user), [com\_multi](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-status-variables#com_multi) and [com\_show\_create\_user](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-status-variables#com_show_create_user).

EXPLAIN:

* [EXPLAIN FORMAT=JSON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/analyze-and-explain-statements/explain-format-json) now shows `outer_ref_condition` field which contains the condition that the(?) SELECT checks on each re-execution - [MDEV-9652](https://jira.mariadb.org/browse/MDEV-9652).
* [EXPLAN FORMAT=JSON](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/administrative-sql-statements/analyze-and-explain-statements/explain-format-json) now shows `sort_key` field which shows the sort criteria used by `filesort` operation. ([commit 2078392](https://github.com/MariaDB/server/commit/2078392cc9bb49720ca3949731078af113ae4f43))
* EXPLAIN used to show incorrect information about how the optimizer resolved `ORDER BY` clause or `Distinct`. This is a long-standing problem coming from MySQL. Now, after [MDEV-8646](https://jira.mariadb.org/browse/MDEV-8646) and related fixes, the problem doesn't exist anymore. (For testcases, see [MDEV-7982](https://jira.mariadb.org/browse/MDEV-7982), [MDEV-8857](https://jira.mariadb.org/browse/MDEV-8857), [MDEV-7885](https://jira.mariadb.org/browse/MDEV-7885))

Optimizations:

* Connection setup was made faster by moving creation of THD to new thread ([MDEV-6150](https://jira.mariadb.org/browse/MDEV-6150))

Code:

* "fast mutexes" have been removed. These aren't faster than normal mutexes, and have been disabled by default for years - [MDEV-8111](https://jira.mariadb.org/browse/MDEV-8111).

## Notes

**Do not use&#x20;**_**alpha**_**&#x20;releases on production systems!**

* Repositories exist for 10.2, but because 10.2 is still alpha, it is not\
  visible in the[repository configuration tool](https://downloads.mariadb.org/mariadb/repositories/).\
  To configure a 10.2 apt, yum, or zypper repository using the tool, simply\
  select 10.1 and then when executing the instructions, change all occurrences of\
  '10.1' to '10.2'.
* [MDEV-9781](https://jira.mariadb.org/browse/MDEV-9781) - APT 1.2.7 (and later) prefers SHA2 GPG keys and now prints warnings when a repository is signed using a SHA1 key. We have created a new SHA2 key for use with our Debian "sid" repository. When we add an Ubuntu 16.04 "xenial" repository, it will also use this new key.
  * The Key ID is: `C74CD1D8`
  * The full fingerprint of the new key is: `177F 4010 FE56 CA33 3630 0305 F165 6F24 C74C D1D8`
  * The key can be added using the following command:

```bash
sudo apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8
```

## Changelog

For a complete list of changes made in [MariaDB 10.2.0](mariadb-1020-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-102-series/mariadb-1020-changelog.md).

{% include "https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/~/reusable/vX1KAy0t1XuYJaGsK28T/" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
