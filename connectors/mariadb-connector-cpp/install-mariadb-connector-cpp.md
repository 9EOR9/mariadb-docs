# Install MariaDB Connector/C++

{% include "https://app.gitbook.com/s/GxVnu02ec8KJuFSxmB93/~/reusable/97ObD80oLdZu6qT33Vhb/" %}

## Requirement

MariaDB Connector/C++ has dependencies. You must install MariaDB Connector/C to use it.

| MariaDB Connector/C++ | MariaDB Connector/C |
| --------------------- | ------------------- |
| 1.1                   | 3.3.3 or later      |
| 1.0                   | 3.1.1 or later      |

For additional information, see "[MariaDB Connector/C++ Release Notes](../mariadb-connector-c/list-of-mariadb-connector-c-releases.md)".

## Linux Installation (Binary Tarball)

To install MariaDB Connector/C++ on Linux:

1. [Install MariaDB Connector/C](broken-reference).
2. Go to the [MariaDB Connector C++ download page](https://mariadb.com/downloads/connectors/connectors-data-access/cpp-connector)
3. Ensure the "Product" dropdown reads "C++ connector."
4. In the "Version" dropdown, select the version you want to download.
5. In the "OS" dropdown, select the Linux distribution you want to use.
6. Click the "Download" button to download the binary tarball.
7.  Extract the tarball:

    ```bash
    $ tar -xvzf mariadb-connector-cpp-*.tar.gz
    ```
8.  Change into the relevant directory:

    ```bash
    $ cd mariadb-connector-cpp-*/
    ```
9.  Install the directories for the header files:

    ```bash
    $ sudo install -d /usr/include/mariadb/conncpp
    $ sudo install -d /usr/include/mariadb/conncpp/compat
    ```
10. Install the header files:

    ```bash
    $ sudo install include/mariadb/* /usr/include/mariadb/
    $ sudo install include/mariadb/conncpp/* /usr/include/mariadb/conncpp
    $ sudo install include/mariadb/conncpp/compat/* /usr/include/mariadb/conncpp/compat
    ```
11. Install the directories for the shared libraries:

*   On CentOS, RHEL, Rocky Linux:

    ```bash
    $ sudo install -d /usr/lib64/mariadb
    $ sudo install -d /usr/lib64/mariadb/plugin
    ```
*   On Debian, Ubuntu:

    ```bash
    $ sudo install -d /usr/lib/mariadb
    $ sudo install -d /usr/lib/mariadb/plugin
    ```

1. Install the shared libraries:

*   On CentOS, RHEL, Rocky Linux:

    ```bash
    $ sudo install lib/mariadb/libmariadbcpp.so /usr/lib64
    $ sudo install lib/mariadb/plugin/* /usr/lib64/mariadb/plugin
    ```
*   On Debian, Ubuntu:

    ```bash
    $ sudo install lib/mariadb/libmariadbcpp.so /usr/lib
    $ sudo install lib/mariadb/plugin/* /usr/lib/mariadb/plugin
    ```

## Windows Installation (MSI)

To install MariaDB Connector/C++ on Windows:

1. MariaDB Connector/C dependency will be installed when Connector/C++ is installed.
2. Go to the [MariaDB Connector C++ download page](https://mariadb.com/downloads/connectors/connectors-data-access/cpp-connector)
3. Ensure the "Product" dropdown reads "C++ connector."
4. In the "Version" dropdown, select the version you want to download.
5. In the "OS" dropdown, select either "MS Windows (64-bit)" or "MS Windows (32-bit)", depending on whether you need a 64-bit or 32-bit connector.
6. Click the "Download" button to download the MSI package.
7. Run the MSI package and click "Next" to start the Setup Wizard.
8. On the second screen, click the license agreement checkbox, then click "Next."
9. On the third screen, click "Typical."
10. On the fourth screen, click "Install."
11. Click "Finish."
12. Add the directory path that contains the `mariadbcpp LIB` file (example `"C:\Program Files\MariaDB\MariaDB C++ Connector 64-bit"`) to `PATH` environment variable.

<sub>_This page is: Copyright © 2025 MariaDB. All rights reserved._</sub>

{% @marketo/form formId="4316" %}
