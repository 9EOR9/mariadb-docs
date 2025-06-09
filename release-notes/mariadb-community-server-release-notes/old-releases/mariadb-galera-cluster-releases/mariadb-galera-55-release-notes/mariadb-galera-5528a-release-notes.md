# MariaDB Galera 5.5.28a Release Notes

The most recent [MariaDB Galera Cluster 5.5](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) release is:[**MariaDB Galera Cluster 5.5.63**](mariadb-galera-cluster-5563-release-notes.md) [Download Now](https://downloads.mariadb.org/mariadb-galera/5.5.63)

[Download](https://downloads.mariadb.org/mariadb-galera/5.5.28a) |**Release Notes** |[Changelog](../mariadb-galera-55-changelogs/mariadb-galera-5528a-changelog.md) |[Overview of Galera](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/what-is-mariadb-galera-cluster/README.md)

**Release date:** 21 Dec 2012

[MariaDB Galera 5.5.28](https://mariadb.com/kb/en/mariadb-galera-cluster-5528-release-notes/)a is a [_**Release Candidate**_](../../../../mariadb-release-criteria.md) (RC) release. It is\
a merge of [MariaDB 5.5.28a](../../release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md) and Galera Cluster with some\
additional bug fixes.

Various articles about MariaDB Galera Cluster, including[known limitations](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/galera-management/mariadb-galera-cluster-known-limitations) and[how to get started](https://app.gitbook.com/s/3VYeeVGUV4AMqrA3zwy7/galera-management/getting-started-with-mariadb-galera-cluster) are\
available in the [**Galera**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/galera/README.md) section of the Knowledgebase.

For a list of changes made in [MariaDB Galera 5.5.28](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb-galera-cluster-5528-release-notes/README.md)a, with links to detailed\
information on each push, see the[MariaDB Galera 5.5.28a Changelog](../mariadb-galera-55-changelogs/mariadb-galera-5528a-changelog.md).

In most respects [MariaDB](https://mariadb.com/kb/en/mariadb/) will work exactly as MySQL: all commands,\
interfaces, libraries and APIs that exist in MySQL also exist in MariaDB.

## Includes [MariaDB 5.5.28](../../release-notes-mariadb-5-5-series/mariadb-5528-release-notes.md)a and Galera Cluster

[MariaDB Galera 5.5.28](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb-galera-cluster-5528-release-notes/README.md)a includes [MariaDB 5.5.28](../../release-notes-mariadb-5-5-series/mariadb-5528-release-notes.md)a and[Galera Cluster](https://codership.com/content/using-galera-cluster). See the[MariaDB 5.5.28](../../release-notes-mariadb-5-5-series/mariadb-5528-release-notes.md)a [Release Notes](../../release-notes-mariadb-5-5-series/mariadb-5528a-release-notes.md) and[Changelog](../../../../changelogs/changelogs-mariadb-55-series/mariadb-5528a-changelog.md) for more information on the changes in[MariaDB 5.5.28](../../release-notes-mariadb-5-5-series/mariadb-5528-release-notes.md)a.

## Packaging Fixes

Numerous packaging fixes have been incorporated into this release of MariaDB\
Galera Cluster. In addition to the previously available RedHat, CentOS, and\
Fedora packages, Ubuntu and Debian packages are now available.

## Combined Repositories

The repositories for MariaDB and MariaDB Galera Cluster are now combined. The\
old MariaDB Galera Cluster Repository is being updated for this release but\
will go away in the near future, so if you are using that repository, please\
visit the[MariaDB Repository Configuration Tool](https://downloads.mariadb.org/mariadb/repositories/)\
and update your repository configuration file. If you feel comfortable editing\
your existing repo config file the change is pretty easy, just replace\
'5.5-galera' with '5.5'.

When using the repositories to install MariaDB Galera Cluster, the only\
difference between it and installing MariaDB is to specify the MariaDB Galera\
Server package instead of the MariaDB Server package and to install the Galera\
package. For example, on Ubuntu, after updating the mariadb.list file the\
following command will install MariaDB Galera Server:

```bash
sudo apt-get update
sudo apt-get install mariadb-galera-server
```

If MariaDB is already installed on the server the package manager will\
uninstall the appropriate packages prior to installing the MariaDB Galera\
Cluster packages.

See the [MariaDB 5.5.28a Changelog](../../../../changelogs/changelogs-mariadb-55-series/mariadb-5528a-changelog.md) for full details\
of the many packaging and other fixes.

Thanks, and enjoy MariaDB Galera Cluster!

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
