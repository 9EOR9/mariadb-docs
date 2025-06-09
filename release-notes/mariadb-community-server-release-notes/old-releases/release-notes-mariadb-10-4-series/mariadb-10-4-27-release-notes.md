# MariaDB 10.4.27 Release Notes

The most recent release of [MariaDB 10.4](what-is-mariadb-104.md) is:[**MariaDB 10.4.34**](mariadb-10-4-34-release-notes.md) Stable (GA) [Download Now](https://downloads.mariadb.org/mariadb/10.4.34/)

[Download 10.4.27](https://downloads.mariadb.org/mariadb/10.4.27/)[Release Notes](mariadb-10-4-27-release-notes.md)[Changelog](../../../changelogs/changelogs-mariadb-10-4-series/mariadb-10-4-27-changelog.md)[Overview of 10.4](what-is-mariadb-104.md)

**Release date:** 7 Nov 2022

[MariaDB 10.4](what-is-mariadb-104.md) is a previous _stable_ series of MariaDB, maintained until June 2024. It is an evolution\
of [MariaDB 10.3](../release-notes-mariadb-10-3-series/what-is-mariadb-103.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.4.27](mariadb-10-4-27-release-notes.md) is a [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.4**](what-is-mariadb-104.md) **see the**[**What is MariaDB 10.4?**](what-is-mariadb-104.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### SSL

* The server no longer tolerates incorrectly configured SSL ([MDEV-29811](https://jira.mariadb.org/browse/MDEV-29811)). If you have enabled SSL in `my.cnf` but have not configured it properly (for example, a certificate file is missing), MariaDB used to silently disable SSL, leaving you under impression that everything was fine and connections were secure. Since this release, MariaDB will fail to start if SSL is enabled, but cannot be switched on.

### Backup

* [mariabackup --compress](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/backing-up-and-restoring-databases/mariabackup/mariabackup-options#-compress) hangs ([MDEV-29043](https://jira.mariadb.org/browse/MDEV-29043))
* Assertion on info.page\_size failed in xb\_delta\_open\_matching\_space ([MDEV-18589](https://jira.mariadb.org/browse/MDEV-18589))

### InnoDB

* InnoDB unnecessarily extends data files ([MDEV-13013](https://jira.mariadb.org/browse/MDEV-13013))
* Adaptive hash index [MDEV-27700](https://jira.mariadb.org/browse/MDEV-27700), [MDEV-29384](https://jira.mariadb.org/browse/MDEV-29384)
* MVCC and locking [MDEV-29666](https://jira.mariadb.org/browse/MDEV-29666), [MDEV-27927](https://jira.mariadb.org/browse/MDEV-27927)
* Virtual columns [MDEV-29299](https://jira.mariadb.org/browse/MDEV-29299), [MDEV-29753](https://jira.mariadb.org/browse/MDEV-29753)

### Galera

* [Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera-cluster/README.md) updated to 26.4.13
* Galera server crashes after 10.3 > 10.4 upgrade ([MDEV-29375](https://jira.mariadb.org/browse/MDEV-29375))
* [wsrep\_incoming\_addresses](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-status-variables#wsrep_incoming_addresses) status variable prints 0 as port number if the port is not mentioned in [wsrep\_node\_incoming\_address](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/reference/galera-cluster-system-variables#wsrep_node_incoming_address) system variable ([MDEV-28868](https://jira.mariadb.org/browse/MDEV-28868))

### JSON

* [JSON\_VALUE()](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-functions/special-functions/json-functions/json_value) does not parse NULL properties properly ([MDEV-27151](https://jira.mariadb.org/browse/MDEV-27151))

### Replication

* minor correction in unsafe warning message ([MDEV-28827](https://jira.mariadb.org/browse/MDEV-28827))
* False replication error-stop of [REVOKE PRIVILEGES](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/revoke) from a non-existing user on primary ([MDEV-28530](https://jira.mariadb.org/browse/MDEV-28530)) in combination with a filtering replica is corrected
* [SET DEFAULT ROLE](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/sql-statements/account-management-sql-statements/set-default-role) replication is mended on a replica that filters system tables ([MDEV-28294](https://jira.mariadb.org/browse/MDEV-28294))

### Repositories

* Beginning with the next release (Q1 2023), our Yum, DNF, and Zypper repositories for Red Hat, Fedora, and SUSE will be migrated to being signed with a new [GPG key](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/gpg). The key we are migrating to is the same one we already use for our Debian and Ubuntu Repositories.
  * The short Key ID is: `0xC74CD1D8`
  * The long Key ID is: `0xF1656F24C74CD1D8`
  * The full fingerprint of the key is: `177F 4010 FE56 CA33 3630 0305 F165 6F24 C74C D1D8`
  * The key can be imported now in preparation for this change using the following command:

```bash
sudo rpm --import https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY
```

### Docker Official Image

The following changes have been made to the `docker.io/library/mariadb` container image.

* The number of gpg packages packages has been removed, leaving enough to `apt-get update`, but `dirmngr` that would fetch keys has been removed. (inspired by [issue #469](https://github.com/MariaDB/mariadb-docker/issues/469))
* The environment variable `LANG=C.UTF-8` has been added for those that exec into containers and copy paste UTF8 characters (fixes [issue #468](https://github.com/MariaDB/mariadb-docker/issues/468)).
* Adds OCI labels to image (fixes [issue 436](https://github.com/MariaDB/mariadb-docker/issues/436) and [users need for version](https://github.com/MariaDB/mariadb-docker/commit/942cd5347b86c84cc4d493147b17c3e3b93fbee3))
* MariaDB config: skip-host-cache and skip-name-resolve moved to `/etc/mysql/mariadb.conf.d/05-skipcache.cnf`

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):\
  <\</style

## Changelog

For a complete list of changes made in [MariaDB 10.4.27](mariadb-10-4-27-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../../changelogs/changelogs-mariadb-10-4-series/mariadb-10-4-27-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.4.27](mariadb-10-4-27-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-9-4-10-8-6-10-7-7-10-6-11-10-5-18-10-4-27-and-10-3-37-now-available/).

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.
