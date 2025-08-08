# Step 2: Install MariaDB Enterprise Server

## Overview

This page details step 2 of the 4-step procedure "[Deploy HTAP Topology](./)".

This step installs MariaDB Enterprise Server MariaDB Enterprise ColumnStore 23.10, and dependencies.

Interactive commands are detailed. Alternatively, the described operations can be performed using automation.

## Retrieve Download Token

MariaDB Corporation provides package repositories for CentOS / RHEL (YUM) and Debian / Ubuntu (APT). A download token is required to access the MariaDB Enterprise Repository.

Customer Download Tokens are customer-specific and are available through the MariaDB Customer Portal.

To retrieve the token for your account:

1. Navigate to [https://customers.mariadb.com/downloads/token/](https://customers.mariadb.com/downloads/token/)
2. Log in.
3. Copy the Customer Download Token.

Substitute your token for `CUSTOMER_DOWNLOAD_TOKEN` when configuring the package repositories.

## Set Up Repository

1. On each Enterprise ColumnStore node, install the prerequisites for downloading the software from the Web.\
   Install on CentOS / RHEL (YUM):

```bash
$ sudo yum install curl
```

Install on Debian / Ubuntu (APT):

```bash
$ sudo apt install curl apt-transport-https
```

2. On each Enterprise ColumnStore node, configure package repositories and specify Enterprise Server:

```bash
$ curl -LsSO https://dlm.mariadb.com/enterprise-release-helpers/mariadb_es_repo_setup
```

```bash
$ echo "${checksum}  mariadb_es_repo_setup" \
       | sha256sum -c -
```

```bash
$ chmod +x mariadb_es_repo_setup
```

```bash
$ sudo ./mariadb_es_repo_setup --token="CUSTOMER_DOWNLOAD_TOKEN" --apply \
      --skip-maxscale \
      --skip-tools \
      --mariadb-server-version="11.4"
```

_Checksums of the various releases of the `mariadb_es_repo_setup` script can be found in the_ [_Versions_](../../../server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/mariadb-package-repository-setup-and-usage.md#versions) _section at the bottom of the_ [_MariaDB Package Repository Setup and Usage_](../../../server-management/install-and-upgrade-mariadb/installing-mariadb/binary-packages/mariadb-package-repository-setup-and-usage.md) _page. Substitute `${checksum}` in the example above with the latest checksum._

## Install Enterprise Server and Enterprise ColumnStore

1. **On each Enterprise ColumnStore node**, install additional dependencies:\
   Install on CentOS / RHEL (YUM)

```bash
$ sudo yum install epel-release

$ sudo yum install jemalloc
```

Install of Debian 10 and Ubuntu 20.04 (APT):

```bash
$ sudo apt install libjemalloc2
```

Install on Debian 9 and Ubuntu 18.04 (APT):

```bash
$ sudo apt install libjemalloc1
```

2. **On the Enterprise ColumnStore node**, install MariaDB Enterprise Server and MariaDB Enterprise ColumnStore:

Install on CentOS / RHEL (YUM):

```bash
$ sudo yum install MariaDB-server \
      MariaDB-backup \
      MariaDB-shared \
      MariaDB-client \
      MariaDB-columnstore-engine
```

Install on Debian / Ubuntu (APT):

```bash
$ sudo apt install mariadb-server \
      mariadb-backup \
      libmariadb3 \
      mariadb-client \
      mariadb-plugin-columnstore
```

## Next Step

Navigation in the procedure "Deploy HTAP Topology".

This page was step 2 of 4.

Next: Step 3: Start and Configure MariaDB Enterprise Server.

{% include "../../../.gitbook/includes/license-copyright-mariadb.md" %}

{% @marketo/form formId="4316" %}
