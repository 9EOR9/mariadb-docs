# MariaDB Java Client 1.1.8 Release notes

{% include "../../../.gitbook/includes/latest-java.md" %}

[Download](https://downloads.mariadb.org/client-java/1.1.8)[Release Notes](mariadb-java-client-118-release-notes.md)[Changelog](../changelogs/1.1/mariadb-java-client-118-changelog.md)[Java Client Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-the-mariadb-java-client/README.md)

**Release date:** 16 Jan 2015

MariaDB Java Client 1.1.8 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_\
release. In general this means that there are no known serious bugs,\
except for those marked as feature requests, that no bugs were fixed\
since last release that caused notable code changes, and that we\
believe the code is ready for general usage (based on bug inflow).

**For a description of the MariaDB Java Client see the**[**About the MariaDB Java Client**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-the-mariadb-java-client/README.md) **page.**

For a list of all changes made in this release, with links to detailed\
information on each push, see the[changelog](../changelogs/1.1/mariadb-java-client-118-changelog.md).

## Bugs fixed in this release

Some of the bugs fixed include:

* Minimize connection overhead: remove check for NO\_BACKSLASH\_ESCAPES (this can be determined by checking server flag) and don't set autocommit if server flag already indicates autocommit mode ([CONJ-101](https://jira.mariadb.org/browse/CONJ-101))
* MySQLResultSet.getTimestamp(int, Calendar) throws NullPointerException if column is NULL ([CONJ-89](https://jira.mariadb.org/browse/CONJ-89))
* Insert of emoji in a column with collation utf8mb4 doesn't work ([CONJ-92](https://jira.mariadb.org/browse/CONJ-92))
* Connection fails if there are special chars (like '-') in the url. The bug fix also removes extra call for setting the default database, instead default database will be selected during handshake. ([CONJ-93](https://jira.mariadb.org/browse/CONJ-93))
* Connection fails if database name contains spaces ([CONJ-97](https://jira.mariadb.org/browse/CONJ-97))
* Don't throw an exception in case COM\_QUIT message to server fails
* ResultSet not closed on new execution of Statement ([CONJ-90](https://jira.mariadb.org/browse/CONJ-90))
* IndexOutOfBounds exception thrown by java.sql.Connection.isValid() ([CONJ-91](https://jira.mariadb.org/browse/CONJ-91))
* Better structure of database URL for connect in JUnit test cases ([CONJ-112](https://jira.mariadb.org/browse/CONJ-112))
* Change the BatchUpdateException constructor call to include the vendor code ([CONJ-113](https://jira.mariadb.org/browse/CONJ-113))
* Method getBinaryStream() on Blob's throws Out of range (position > stream size) ([CONJ-117](https://jira.mariadb.org/browse/CONJ-117))
* MySQLResultSet.getTimestamp(int, Calendar) throws NullPointerException if column is NULL ([CONJ-88](https://jira.mariadb.org/browse/CONJ-88))
* MySQLDataSource ignores calls to setPort/setDatabaseName/setServerName after calling getConnection ([CONJ-80](https://jira.mariadb.org/browse/CONJ-80))
* MySQLDataSource implementation discards properties ([CONJ-81](https://jira.mariadb.org/browse/CONJ-81))
* getGeneratedKeys() does not return generated keys in case of a batch SQL INSERT ([CONJ-83](https://jira.mariadb.org/browse/CONJ-83))
* Error calling stored procedure with DECIMAL parameter ([CONJ-103](https://jira.mariadb.org/browse/CONJ-103))
* Support for batch statements rewrite ([CONJ-99](https://jira.mariadb.org/browse/CONJ-99))
* setTimestamp truncates milliseconds ([CONJ-107](https://jira.mariadb.org/browse/CONJ-107))
* ConcurrentModificationException on calling close() on MySQLPooledConnections ([CONJ-76](https://jira.mariadb.org/browse/CONJ-76))
* Connection.createStatement should throw an Exception if the connection is closed ([CONJ-69](https://jira.mariadb.org/browse/CONJ-69))
* Implement useful jdbc4 abort(Executor arg) method on MySQLConnection ([CONJ-75](https://jira.mariadb.org/browse/CONJ-75))
* Accept escape sequence OJ in any case the server accepts ([CONJ-106](https://jira.mariadb.org/browse/CONJ-106))
* Statement.getGeneratedKeys() returns a non-empty ResultSet if AUTO\_INCREMENT was unaffected ([CONJ-108](https://jira.mariadb.org/browse/CONJ-108))
* Big (> 512 MiB) LOAD DATA LOCAL INFILE cannot be sent to server ([CONJ-115](https://jira.mariadb.org/browse/CONJ-115))
* Use utf8mb4 if the server charset is utf8mb4 ([CONJ-118](https://jira.mariadb.org/browse/CONJ-118))
* JDBC & MySQL incompatibilities for the ResultSet class ([CONJ-119](https://jira.mariadb.org/browse/CONJ-119))
* Fixed Connection.isValid(int) behavior ([CONJ-120](https://jira.mariadb.org/browse/CONJ-120))
* BIT(1) fields are represented as 0 or 1 with ResultSet.getString() ([CONJ-102](https://jira.mariadb.org/browse/CONJ-102))
* ResultSet.wasNull() should return true for zero timestamps ([CONJ-100](https://jira.mariadb.org/browse/CONJ-100))
* MySQLDataSource.setProperties fixed ([CONJ-123](https://jira.mariadb.org/browse/CONJ-123))
* BigInteger not supported when setObject is used on PreparedStatements ([CONJ-124](https://jira.mariadb.org/browse/CONJ-124))
* implement Connection.getNetworkTimeout and Connection.setNetworkTimeout (CON-121)
* invalid arguments were given for the XA operation ([CONJ-122](https://jira.mariadb.org/browse/CONJ-122))
* Data type LONGVARCHAR not supported in setObject() ([CONJ-82](https://jira.mariadb.org/browse/CONJ-82))
* MySQLType.GEOMETRY not handled in MySQLValueObject.getObject() ([CONJ-85](https://jira.mariadb.org/browse/CONJ-85))
* ResultSet from previos query after "Read timed out" socket exception ([CONJ-79](https://jira.mariadb.org/browse/CONJ-79))
* Make SQLException prettier when too large packet is sent to the server ([CONJ-116](https://jira.mariadb.org/browse/CONJ-116))
* PreparedStatement.setObject() returns IllegalParameterException: No '?' on that position ([CONJ-126](https://jira.mariadb.org/browse/CONJ-126))
* Username and password ignored in url for DataSource ([CONJ-127](https://jira.mariadb.org/browse/CONJ-127))

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
