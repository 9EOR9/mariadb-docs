# MariaDB Galera Cluster 5.5.57 Release Notes

The most recent [MariaDB Galera Cluster 5.5](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) release is:[**MariaDB Galera Cluster 5.5.63**](mariadb-galera-cluster-5563-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb-galera/5.5.63)

[Download](https://downloads.mariadb.org/mariadb-galera/5.5.57)[Release Notes](mariadb-galera-cluster-5557-release-notes.md)[Changelog](../mariadb-galera-55-changelogs/mariadb-galera-cluster-5557-changelog.md)[Overview of MariaDB Galera Cluster](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md)

**Release date:** 26 Jul 2017

MariaDB Galera Cluster 5.5.57 is a [_**Stable**_](../../../../mariadb-release-criteria.md) (GA)\
release. It is a merge of [MariaDB 5.5.57](../../release-notes-mariadb-5-5-series/mariadb-5557-release-notes.md) and[Galera Cluster](https://codership.com/content/using-galera-cluster) with\
additional bug fixes.

Various articles about MariaDB Galera Cluster, including[known limitations](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/galera-management/mariadb-galera-cluster-known-limitations) and[how to get started](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/galera-management/getting-started-with-mariadb-galera-cluster) are\
available in the [**Galera**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) section of the documentation.

## Updates and fixes in this version

* This release is a bug-fix release.
* Codership changes:[github.com/codership/mysql-wsrep/tree/5.5](https://github.com/codership/mysql-wsrep/tree/5.5)\
  (till commit `9949137`)
* The [Galera library](https://codership.com/content/using-galera-cluster) used\
  by MariaDB Galera Cluster and included in the MariaDB repositories is\
  currently at version 25.3.20.
* Fixes for the following [security vulnerabilities](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/security/securing-mariadb/security):
  * [CVE-2017-3636](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-3636)
  * [CVE-2017-3641](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-3641)
  * [CVE-2017-3653](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-3653)

See the [MariaDB 5.5.57 Release Notes](../../release-notes-mariadb-5-5-series/mariadb-5557-release-notes.md) for more\
information on fixes in this version.

## Changelog

A full list of all changes is in the[MariaDB Galera Cluster 5.5.57 Changelog](../mariadb-galera-55-changelogs/mariadb-galera-cluster-5557-changelog.md)\
and the [MariaDB 5.5.57 Changelog](../../../changelogs/changelogs-mariadb-55-series/mariadb-5557-changelog.md).

## Notes

* Running MariaDB Galera Cluster 5.5 and 10.0 nodes in a cluster is not\
  supported ([MDEV-6257](https://jira.mariadb.org/browse/MDEV-6257))
* This version of MariaDB Galera Cluster supports `wsrep` API v25 which means\
  MariaDB Galera Cluster can be used with either a 25.2.x or 25.3.x

{% include "../../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
