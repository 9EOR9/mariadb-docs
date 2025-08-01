# MariaDB Connector/J 1.3.3 Release Notes

{% include "../../../.gitbook/includes/latest-java.md" %}

[Download](https://downloads.mariadb.org/connector-java/1.3.3/)[Release Notes](mariadb-connector-j-133-release-notes.md)[Changelog](../changelogs/1.3/mariadb-connector-j-133-changelog.md)[Connector/J Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-j/README.md)

**Release date:** 8 Dec 2015

MariaDB Connector/J 1.3.3 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_\
release.

**For a description of MariaDB Connector/J see the**[**About MariaDB Connector/J**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-j/README.md) **page**

For a list of all changes made in this release, with links to detailed\
information on each push, see the [changelog](../changelogs/1.3/mariadb-connector-j-133-changelog.md).

This version is a bugfix release

## Notable changes and additions

### Major

* [CONJ-225](https://jira.mariadb.org/browse/CONJ-225) : ResultSet.getString correction for prepareStatement
* [CONJ-226](https://jira.mariadb.org/browse/CONJ-226) : PreparedStatement return NULL When TIME column value=00:00:00
* [CONJ-227](https://jira.mariadb.org/browse/CONJ-227) : Mariadb alias in url connection string wasn't working in HA mode
* [CONJ-228](https://jira.mariadb.org/browse/CONJ-228) : Handle unsigned numeric data
* [CONJ-179](https://jira.mariadb.org/browse/CONJ-179) : Statement.getMoreResults() returns wrong value

### Minor

* [CONJ-224](https://jira.mariadb.org/browse/CONJ-224) : Metadata driver version
* [CONJ-229](https://jira.mariadb.org/browse/CONJ-229) : Host is not mandatory for named pipe connection

## Behavior change

With the [CONJ-228](https://jira.mariadb.org/browse/CONJ-228) evolution, some behavior has changed : Exceptions are always thrown if any read data truncation happens.

### Example

SmallInt data type signed range is `-32768` to `32767`. The unsigned range is `0` to `65535`.\
Signed range is similar to the Java short primitive type.

A ResultSet.getShort() on a unsigned smallint value of `40000` will now throw an\
SQLException. (the previous version was returning the `32767` value).\
This value will be available by using a resultset.getInt().

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
