# Deploy with Package Tarballs

MariaDB Corporation provides package tarballs for some MariaDB database products.

Package tarballs provide multiple benefits:

* Package tarballs are compressed tar archives that contain software packages.
* Software packages can be installed using the operating system's package manager without relying on a remote repository.
* RPM (.rpm) files are distributed for CentOS, Red Hat Enterprise Linux (RHEL), and SUSE Linux Enterprise Server (SLES).
* DEB (.deb) files are distributed for Debian and Ubuntu.

If you want to deploy MariaDB database products without using a package tarball, [alternative deployment methods](../../deployment-general-installing-and-upgrading-instructions/deployment-methods.md) are available. Available deployment methods are component-specific.

## Use Cases

MariaDB database products can be deployed with package tarballs to support use cases, such as:

* Transfer the package tarball to an air-gapped network for installation without an internet connection
* Install software using a package manager without configuring a package repository
* Automatically install missing dependencies using a package manager

## Compatibility

The following MariaDB database products can be deployed using package tarballs:

* MariaDB Community Server 10.5
* MariaDB Community Server 10.6
* MariaDB Enterprise Server 10.5
* MariaDB Enterprise Server 10.6
* MariaDB Enterprise Server 11.4
* MariaDB MaxScale 22.08

## Download a Package Tarball

MariaDB Corporation provides package tarballs (.debs.tar, .rpms.tar) to support customers who leverage in-house package repositories to distribute software to their servers. Secure any such repository to prevent outside access.

MariaDB Corporation provides multiple interfaces to download package tarballs.

### Download a Package Tarball with a Web Browser

Steps to download a package tarball:

1. Go to the MariaDB Downloads page at [dles](https://mariadb.com/dles)
2. Complete customer login
3. Select the desired version and operating system, then click the Download button

### Download a Package Tarball with Command-Line or Automation

Package tarballs can be downloaded using command-line tools or automation from the MariaDB Download interface with the [Customer Download Token](../../deployment-general-installing-and-upgrading-instructions/token.md).

For additional information, see ["Download Binary Files"](../../deployment-general-installing-and-upgrading-instructions/token.md#download-binary-files).

## Installation from Package Tarball

Once downloaded and extracted, you can:

* Install .rpm packages (RHEL, CentOS, and SLES) using rpm -i
* Install .deb packages (Debian, Ubuntu) using dpkg -i
* Install from the simple package repositories included in the tarball. Missing dependencies will be resolved when using the apt, yum, or zypper package manager. See the README file enclosed in the package tarball for more information.
* Test packages before placement in an internal package repository for distribution to your servers. Secure this repository from outside access.

Installation loads software to the system. This software requires configuration before the database server is ready for use.

<sub>_This page is: Copyright © 2025 MariaDB. All rights reserved._</sub>

{% @marketo/form formId="4316" %}
