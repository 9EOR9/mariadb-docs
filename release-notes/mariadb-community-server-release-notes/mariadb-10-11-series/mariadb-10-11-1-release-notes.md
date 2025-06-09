# MariaDB 10.11.1 Release Notes

The most recent release of [MariaDB 10.11](what-is-mariadb-1011.md) is:[**MariaDB 10.11.11**](mariadb-10-11-11-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/10.11.11/)

[Download 10.11.1](https://downloads.mariadb.org/mariadb/10.11.1/)[Release Notes](mariadb-10-11-1-release-notes.md)[Changelog](../../changelogs/changelogs-mariadb-10-11-series/mariadb-10-11-1-changelog.md)[Overview of 10.11](what-is-mariadb-1011.md)

**Release date:** 17 Nov 2022

**Do not use non-stable (non-GA) releases in production!**

[MariaDB 10.11](what-is-mariadb-1011.md) is a current development series of MariaDB. It is an evolution of [MariaDB 10.10](../old-releases/release-notes-mariadb-10-10-series/what-is-mariadb-1010.md) with several entirely new features.

[MariaDB 10.11.1](mariadb-10-11-1-release-notes.md) is a [_**Release Candidate (RC)**_](../../mariadb-release-criteria.md) release.

**For an overview of** [**MariaDB 10.11**](what-is-mariadb-1011.md) **see the**[**What is MariaDB 10.11?**](what-is-mariadb-1011.md) **page.**

Thanks, and enjoy MariaDB!

## Notable Items

### Authentication

* [bind\_address](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#bind_address) now accepts a comma-separated list of addresses to bind to ([MDEV-24377](https://jira.mariadb.org/browse/MDEV-24377))

### InnoDB

* Allow [innodb\_undo\_tablespaces](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/storage-engines/innodb/innodb-system-variables#innodb_undo_tablespaces) to be changed after database creation ([MDEV-19229](https://jira.mariadb.org/browse/MDEV-19229))

### Replication

* Formerly only a server option, [replicate\_rewrite\_db](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/standard-replication/replication-and-binary-log-system-variables#replicate_rewrite_db) is now a global system variable ([MDEV-15530](https://jira.mariadb.org/browse/MDEV-15530))

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

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * CVE-\`-\`\`\`

## Changelog

For a complete list of changes made in [MariaDB 10.11.1](mariadb-10-11-1-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-10-11-series/mariadb-10-11-1-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.11.1](mariadb-10-11-1-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-7-1-rc-and-mariadb-10-6-5-10-5-13-10-4-22-10-3-32-and-10-2-41-now-available/).

**Do not use non-stable (non-GA) releases in production!**

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.
