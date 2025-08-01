# MariaDB Java Client 1.1.3 Release Notes

{% include "../../../.gitbook/includes/latest-java.md" %}

[Download](https://downloads.mariadb.org/client-java/1.1.3/) | **Release Notes** | [Changelog](../changelogs/1.1/mariadb-java-client-113-changelog.md) |[Java Client Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-the-mariadb-java-client/README.md)

**Release date:** 01 July 2013

MariaDB Java Client 1.1.3 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_\
release. In general this means that there are no known serious bugs,\
except for those marked as feature requests, that no bugs were fixed\
since last release that caused a notable code changes, and that we\
believe the code is ready for general usage (based on bug inflow).

**For a description of the MariaDB Java Client see the**[**About the MariaDB Java Client**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-the-mariadb-java-client/README.md) **page.**

For a list of changes made in this release, with links to detailed\
information on each push, see the[changelog](../changelogs/1.1/mariadb-java-client-113-changelog.md).

## New functionality

* On Windows, it is now possible to use named pipes if server enables them. To connect to the server using named pipe, pass pipe=\<pipe\_name> URL parameter or property. The pipe filename name should be passed without the `\\pipe\<machine>` prefix. ([CONJ-36](https://jira.mariadb.org/browse/CONJ-36))
* It is now possible to do SSL validation for self signed certificates, using serverSslCert, (provide CA certificate for the server's certificate). It allows to avoid SSL handshake errors (untrusted CA) when working with self-signed certificates, and is more secure than the existing trustServerCertificate option. ([CONJ-48](https://jira.mariadb.org/browse/CONJ-48))

## Bugs fixed in this release

Some of the bugs fixed include the following:

* Change assertion in `PacketOutputStream.startPacket()` to be IOException, so it can be caught. "Last packet not finished" condition can happen , if underlying stream is broken (e.g write operation failed) ([CONJ-34](https://jira.mariadb.org/browse/CONJ-34))
* If custom `SocketFactory` creates an already connected socket, do not execute Socket.connect() ([CONJ-37](https://jira.mariadb.org/browse/CONJ-37))
* Ensure proper locking in `MySQLCallableStatement.execute()`, in scenarios that use single connection simultaneously from multiple threads. Hold the connection lock for the duration of 3 operations - setting parameters , executing statement, and reading off output parameters) ([CONJ-38](https://jira.mariadb.org/browse/CONJ-38))
* For multi-row inserts, `getGeneratedKeys()` will return ResultSet with multiple entries ([CONJ-39](https://jira.mariadb.org/browse/CONJ-39))
* `java.util.Date` can now be passed to PreparedStatement.setObject(). ([CONJ-40](https://jira.mariadb.org/browse/CONJ-40))
* Allow for missing space it temporal escapes, for better compatibility with ConnectorJ\
  ([CONJ-42](https://jira.mariadb.org/browse/CONJ-42))
* `PreparedStatement.getResultSetMetaData()` called before query execution threw exception, if query string contained at least once placeholder ([CONJ-43](https://jira.mariadb.org/browse/CONJ-43))
* `DatabaseMetaData.getPrimaryKeys()` returned incorrect value in KEY\_SEQ column ([CONJ-41](https://jira.mariadb.org/browse/CONJ-41))
* (Performance enhancement) Changed `DatabaseMetadata.getImportedKeys()` not to use information schema, but to parse the output of "show create table" instead. This considerably speeds up several scenarios involving Hibernate ([CONJ-35](https://jira.mariadb.org/browse/CONJ-35))
* Fixed `ResultSet.getDisplaySize()` for character columns - due to UTF-8 usage it was 3x more than expected (size in bytes, instead of size in chars)
* Fix bug in prepared statement parsing code (skipping next character after backslash '')([CONJ-44](https://jira.mariadb.org/browse/CONJ-44))
* Fix `Statement.executeBatch()` methods to throw `BatchUpdateException`, as in JDBC spec ([CONJ-47](https://jira.mariadb.org/browse/CONJ-47))

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
