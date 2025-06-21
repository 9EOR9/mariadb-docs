# MariaDB 10.4.2 Release Notes

The most recent release of [MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download](https://downloads.mariadb.org/mariadb/10.4.2/)[Release Notes](mariadb-1042-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-10-4-series/mariadb-1042-changelog.md)[Overview of 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md)

**Release date:** 29 Jan 2019

[MariaDB 10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) is the current _development_ series of MariaDB. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.2](mariadb-1042-release-notes.md) is a [_**Beta**_](../../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

**For an overview of** [**MariaDB 10.4**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) **see the**[**What is MariaDB 10.4?**](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Changes

Notable changes of this release include:

* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/galera-cluster/README.md) 4 version 26.4.0 has been added in this release, see the Galera 4 Notes section for details
* [Account Locking](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/user-account-management/account-locking) ([MDEV-13095](https://jira.mariadb.org/browse/MDEV-13095))
* a number of bugs related to [MDEV-15562](https://jira.mariadb.org/browse/MDEV-15562) Instant DROP COLUMN have been fixed
* New variable, [max\_password\_errors](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#max_password_errors) for limiting the number of failed connection attempts by a user.
* [MDEV-17475](https://jira.mariadb.org/browse/MDEV-17475): Maximum value of [table\_definition\_cache](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#table_definition_cache) is now `2097152`.

## Galera 4 Notes

### Upgrading to Galera 4 version 26.4.0

Rolling upgrades from earlier 10.3 (or older) MariaDB releases are not supported\
in this release. For upgrading a 10.3-based cluster, any applications accessing\
the cluster should be stopped and the cluster shut down. Then for each cluster\
node the following procedure should be carried out:

* Install [MariaDB 10.4.2](mariadb-1042-release-notes.md) and Galera 4 version 26.4.0
* Start MariaDB server, but make sure it is not trying to connect to the\
  cluster by configuring `wsrep_provider=none`
* While MariaDB server is running, run `mysql_upgrade` for the server
* Stop MariaDB server

After that, you can bootstrap the cluster. If there was ongoing application\
load on the cluster during the initial cluster shutdown phase, you should make\
sure to bootstrap the cluster with the node which was shutdown last.

We are working on rolling upgrade support for the final GA version of [MariaDB\
10.4](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-4-series/broken-reference/README.md). With a rolling upgrade, a live cluster can be upgraded node by node, and\
the cluster is able to process application load when having a hybrid setup of\
10.3 and 10.4 nodes.

### New Features in Galera 26.4.0

The ‘mysql’ schema contains new Galera replication related tables:

* `wsrep_cluster`
* `wsrep_cluster_members`
* `wsrep_streaming_log`

End users may read but not modify these tables.

The new streaming replication feature allows replicating transactions of\
unlimited size. With streaming replication, a cluster is replicating a\
transaction in small fragments during transaction execution. This transaction\
fragmenting is controlled by two new configuration variables:

* [wsrep_trx_fragment_unit](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_trx_fragment_unit) (bytes, rows, statements) defines the metrics for\
  how to measure transaction size limit for fragmenting. Possible values are:
  * `bytes`: transaction’s binlog events buffer size in bytes
  * `rows`: number of rows affected by the transaction
  * `statements`: number of SQL statements executed in the multi-statement\
    transaction
* [wsrep_trx_fragment_size](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_trx_fragment_size) defines the limit for fragmenting. When a\
  transaction’s size, in terms of the configured fragment unit, has grown over\
  this limit, a new fragment will be replicated.

Transactions replicated through galera replication will now process the commit\
phase using MariaDB's group commit logic. This will affect transaction\
throughput, especially when binary logging is enabled in the cluster.

### Limitations in Galera 26.4.0

* Upgrading from 10.3 version 25.3.25 to 10.4.2 version 26.4.0 must happen on a\
  stopped cluster. Only after all nodes have been upgraded to [MariaDB 10.4.2](mariadb-1042-release-notes.md)\
  and Galera 26.4.0 can the cluster be started up
* Splitting transactions of `LOAD DATA` execution will conflict with\
  streaming replication, and should not be used if streaming replication is\
  configured
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 10.4.2](mariadb-1042-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-10-4-series/mariadb-1042-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.2](mariadb-1042-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-4-2-now-available/).

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
