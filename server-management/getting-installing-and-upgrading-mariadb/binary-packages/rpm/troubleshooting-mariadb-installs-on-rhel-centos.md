# Troubleshooting MariaDB Installs on RHEL / CentOS

The following article is about different issues people have encountered when installing MariaDB on RHEL / CentOS.

It is highly recommended to [install with yum](yum.md) where possible.

In RHEL/ CentOS it is also possible to install a [RPM](http://downloads.askmonty.org/mariadb/) or a [tar ball](../installing-mariadb-binary-tarballs.md). The RPM is the preferred version, except if you want to install many versions of MariaDB or install MariaDB in a non standard location.

#

## Replacing MySQL

If you removed an MySQL RPM to install MariaDB, note that the MySQL RPM on uninstall renames /etc/my.cnf to /etc/my.cnf.rpmsave.

After installing MariaDB you should do the following to restore your configuration options:

```
mv /etc/my.cnf.rpmsave /etc/my.cnf
```

#

## Unsupported configuration options

If you are using any of the following options in your /etc/my.cnf or other my.cnf file you should remove them. This is also true for MySQL 5.1 or newer:

```
skip-bdb
```

#

# See also

* [Installing with yum (recommended)](yum.md)
* [Installing MariaDB RPM Files](/en/installing-mariadb-rpm-files/)
* [Checking MariaDB RPM Package Signatures](checking-mariadb-rpm-package-signatures.md)