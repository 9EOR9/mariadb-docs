# MariaDB 5.1.39 Release Notes

The most recent release in the [MariaDB 5.1 series](changes-improvements-in-mariadb-5-1.md) is:[**MariaDB 5.1.67**](mariadb-5167-release-notes.md)

[Download](https://askmonty.org/wiki/MariaDB:Download:MariaDB_5.1.39) | **Release Notes** | [Changelog](../../changelogs/changelogs-mariadb-51-series/mariadb-5139-changelog.md) |[Overview of 5.1](changes-improvements-in-mariadb-5-1.md)

**Release date:** 15 Nov 2009

See the [MariaDB versus MySQL](https://mariadb.com/docs/release-notes/compatibility-and-differences/mariadb-vs-mysql-compatibility) page for a high-level\
overview of the differences between MariaDB and MySQL.

[MariaDB](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb/README.md) 5.1.39 Beta is based on [MySQL](https://mysql.com) 5.1.39\
and [XtraDB](https://www.percona.com/docs/wiki/percona-xtradb:start) 1.0.3-8.

MariaDB is kept up to date with the latest MySQL release from the same branch.

In most respects MariaDB will work exactly as MySQL; all commands, interfaces,\
libraries and APIs that exist in MySQL also exist in MariaDB.

In addition to the differences noted in the[MariaDB 5.1.38 Release Notes](mariadb-5138-release-notes.md), the main\
differences between MariaDB and MySQL are:

### Includes MySQL 5.1.39

For [MariaDB 5.1.39](mariadb-5139-release-notes.md) we have merged in all of the upstream changes from MySQL\
5.1.39. The[MySQL 5.1.39 release notes](https://dev.mysql.com/doc/refman/5.1/en/news-5-1-39.html)\
have details of what changes were made upstream by MySQL since 5.1.38.

### Includes XtraDB 1.0.3-8

We have included XtraDB 1.0.3-8 in this version of MariaDB. The[XtraDB 1.0.3-8 release notes](https://www.percona.com/docs/wiki/percona-xtradb:info:xtradb_changelog#release_1.0.3-8)\
have details of the changes made to XtraDB since version 1.0.3-6 (the version\
included with [MariaDB 5.1.38](mariadb-5138-release-notes.md)).

### FederatedX storage engine is included

The FederatedX storage engine replaces the old, not maintained, Federated storage engine.

See also: [FederatedX storage engine](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-usage/storage-engines/federatedx-storage-engine)

### Fewer warnings and bugs

Various changes were made in [MariaDB 5.1.39](mariadb-5139-release-notes.md) in our desire to fix warnings and\
eliminate bugs. These included removing invalid tests, removing unused\
declarations, cleaning up the codebase where appropriate, and so on.

### Test Suite improvements

For [MariaDB 5.1.39](mariadb-5139-release-notes.md) we have continued our work on improving the test suite. One\
thing we did was remove unnecessary and confusing 'skipped' messages from\
mysql-test-run.pl. In mysql-test-run.pl, we auto-generate combinations of\
replication tests. But this sometimes generates combinations that are\
meaningless, like running a test that requires row-based replication with\
statement-based. These superfluous combinations should not be reported as\
skipped, they should just be deleted. We do keep skip messages resulting from\
running mysql-test-run.pl in special ways, eg.\
\--mysqld=--binlog-format=statement.

Another thing we did was to remove the ndb suites from the list of default test\
suites, as we do not support NDB in MariaDB.

We have also done some work on speeding up the test suite. One way we've done\
this is to insert\
"`--disable_query_log ; begin ; ... commit; --enable_query_log`"\
around all while loops that do inserts.

We've also fixed a race condition in the test system by forcing a restart\
before maria\_showlog\_error to get rid of the status from previous connections.

### Binary tarballs now built on Ubuntu 8.04

For [MariaDB 5.1.39](mariadb-5139-release-notes.md) we switched from using Ubuntu 9.04 and glibc 2.9 for our\
builds to using Ubuntu 8.04.and glibc 2.7. This should make the binaries more\
compatible with various Linux systems.

### RPMs for CentOS 5

One benefit of our change to using Ubuntu 8.04 and glibc 2.7 for our builds is\
that we are now able to create CentOS 5 RPM packages. The[download](https://downloads.askmonty.org/) page has links to both the\
individual files and to a CentOS 5 YUM repository.

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
