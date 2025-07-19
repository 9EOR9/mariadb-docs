# MariaDB 10.5.14 Release Notes

{% include "../../../.gitbook/includes/latest-10-5.md" %}

&#x20;<a href="mariadb-10514-release-notes.md" class="button secondary">Release Notes</a> <a href="../../changelogs/changelogs-mariadb-105-series/mariadb-10514-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-105.md" class="button secondary">Overview of 10.5</a>

**Release date:** 9 Feb 2022

This release is no longer available for download after a problem was noticed when manually running mariadb-upgrade. See [MDEV-27789](https://jira.mariadb.org/browse/MDEV-27789) for more details. **Please use a later release.**

[MariaDB 10.5](what-is-mariadb-105.md) is a previous _stable_ series of MariaDB. It is an evolution\
of [MariaDB 10.4](../release-notes-mariadb-10-4-series/what-is-mariadb-104.md) with several entirely new features not found anywhere else\
and with backported and reimplemented features from MySQL.

[MariaDB 10.5.14](mariadb-10514-release-notes.md) is a [_**Stable (GA)**_](../../about/release-criteria.md) release.

Thanks, and enjoy MariaDB!

## Notable Items

### InnoDB

* [--skip-symbolic-links](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/starting-and-stopping-mariadb/mariadbd-options) does not disallow `.isl` file creation ([MDEV-26870](https://jira.mariadb.org/browse/MDEV-26870))
* Indexed [CHAR](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/char) columns are broken with NO\_PAD [collations](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets) ([MDEV-25440](https://jira.mariadb.org/browse/MDEV-25440))
* insert-intention lock conflicts with waiting ORDINARY lock ([MDEV-27025](https://jira.mariadb.org/browse/MDEV-27025))
* Crash recovery improvements ([MDEV-26784](https://jira.mariadb.org/browse/MDEV-26784), [MDEV-27022](https://jira.mariadb.org/browse/MDEV-27022), [MDEV-27183](https://jira.mariadb.org/browse/MDEV-27183), [MDEV-27610](https://jira.mariadb.org/browse/MDEV-27610))

### Galera

* [Galera](https://app.gitbook.com/o/diTpXxF5WsbHqTReoBsS/s/3VYeeVGUV4AMqrA3zwy7/) updated to 26.4.11
* Galera SST scripts should use ssl\_capath (not ssl\_ca) for CA directory ([MDEV-27181](https://jira.mariadb.org/browse/MDEV-27181))
* Alter Sequence do not replicate to another nodes with in Galera Cluster ([MDEV-19353](https://jira.mariadb.org/browse/MDEV-19353))
* Galera crash - Assertion. Possible parallel writeset problem ([MDEV-26803](https://jira.mariadb.org/browse/MDEV-26803))
* CREATE TABLE with FOREIGN KEY constraint fails to apply in parallel ([MDEV-27276](https://jira.mariadb.org/browse/MDEV-27276))
* Galera cluster node consider old server\_id value even after modification of server\_id `[wsrep_gtid_mode=ON]` ([MDEV-26223](https://jira.mariadb.org/browse/MDEV-26223))

### Replication

* Seconds behind master corrected from artificial spikes at relay-log rotation ([MDEV-16091](https://jira.mariadb.org/browse/MDEV-16091))
* Statement rollback in binlog when transaction creates or drop temporary table is set right ([MDEV-26833](https://jira.mariadb.org/browse/MDEV-26833))
* CREATE-or-REPLACE SEQUENCE is made to binlog with the DDL flag to stabilize its parallel execution on slave ([MDEV-27365](https://jira.mariadb.org/browse/MDEV-27365))

### Packaging & Misc

* prohibition running two upgrades in parallel ([MDEV-27068](https://jira.mariadb.org/browse/MDEV-27068), [MDEV-27107](https://jira.mariadb.org/browse/MDEV-27107), [MDEV-27279](https://jira.mariadb.org/browse/MDEV-27279))
* As per the [MariaDB Deprecation Policy](../../about/platform-deprecation-policy.md), this will be the last release of [MariaDB 10.5](what-is-mariadb-105.md) for Ubuntu 21.04 Hirsute, CentOS 8, and Fedora 33
* [mariadb\_repo\_setup](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/mariadb-package-repository-setup-and-usage) script updated to version 2022-02-08, with the following fixes and enhancements:
  * Default location of the script has been moved to: [mariadb\_repo\_setup](https://r.mariadb.com/downloads/mariadb_repo_setup) (old location is deprecated, but still works)
  * The GPG keyring file, used with Debian and Ubuntu repositories, has moved to: [mariadb-keyring-2019.gpg](https://supplychain.mariadb.com/mariadb-keyring-2019.gpg) and the checksum for the file can be found at: [mariadb-keyring-2019.gpg.sha256](https://supplychain.mariadb.com/mariadb-keyring-2019.gpg.sha256)
  * Support for RHEL and SLES aarch64 repositories added
  * New function added to verify that the MariaDB Server version, if specified on the command line, follows the correct naming and that a corresponding repository actually exists.
  * Fixed repository pinning for Ubuntu and Debian repositories
  * MariaDB Server 10.7 is now the default server version

### Docker Library

* Faster initialization by disabling binary logging during initialization ([MDEV-27074](https://jira.mariadb.org/browse/MDEV-27074))
* mysql\_upgrade can be run if needed using the environment variable MARIADB\_AUTO\_UPGRADE=1 ([MDEV-25670](https://jira.mariadb.org/browse/MDEV-25670))
* A healthcheck script /usr/local/bin/healthcheck.sh is installed in the container with various checking options ([MDEV-25434](https://jira.mariadb.org/browse/MDEV-25434))
* mysql@localhost user is created with the environment variable MARIADB\_MYSQL\_LOCALHOST\_USER=1 and additional grants (beyond USAGE) with MARIADB\_MYSQL\_LOCALHOST\_GRANTS={global grant list} ([MDEV-27732](https://jira.mariadb.org/browse/MDEV-27732))
* skip innodb buffer pool loads/dumps on temporary startup/shutdown for faster startup/initialization, and accurate "healthcheck.sh --innodb\_buffer\_pool\_loaded"
* change group ownership on datadir/socket dir ([issue #401](https://github.com/MariaDB/mariadb-docker/issues/401))
* log note about note on Securing system users, mysql\_secure\_installation not required ([reddit suggestion](https://www.reddit.com/r/docker/comments/rhwf28/mysql_secure_installation_on_mariadb_with_docker/))
* speed up Docker Library initialization of timezones ([MDEV-27608](https://jira.mariadb.org/browse/MDEV-27608), [MDEV-23326](https://jira.mariadb.org/browse/MDEV-23326))

### Security

* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2022-24052](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-24052)
  * [CVE-2022-24051](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-24051)
  * [CVE-2022-24050](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-24050)
  * [CVE-2022-24048](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-24048)
  * [CVE-2021-46659](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46659)
  * [CVE-2022-0778](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-0778)
  * [CVE-2022-21595](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-21595)

## Changelog

For a complete list of changes made in [MariaDB 10.5.14](mariadb-10514-release-notes.md), with links to detailed\
information on each push, see the [changelog](../../changelogs/changelogs-mariadb-105-series/mariadb-10514-changelog.md).

## Contributors

For a full list of contributors to [MariaDB 10.5.14](mariadb-10514-release-notes.md), see the [MariaDB Foundation release announcement](https://mariadb.org/mariadb-10-8-1-rc-and-mariadb-10-7-2-10-6-6-10-5-14-10-4-23-10-3-33-and-10-2-42-now-available/).

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
