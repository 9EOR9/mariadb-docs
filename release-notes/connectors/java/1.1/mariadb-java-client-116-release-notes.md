# MariaDB Java Client 1.1.6 Release Notes

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of [MariaDB Connector/J](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-j/README.md) is:[**MariaDB Connector/J 3.5.3**](../3.5/mariadb-connector-j-3-5-3-release-notes.md)

[Download](https://downloads.mariadb.org/client-java/1.1.6/) |**Release Notes** |[Changelog](../changelogs/1.1/mariadb-java-client-116-changelog.md) |[Java Client Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-the-mariadb-java-client/README.md)

**Release date:** 18 Feb 2014

MariaDB Java Client 1.1.6 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_\
release. In general this means that there are no known serious bugs,\
except for those marked as feature requests, that no bugs were fixed\
since last release that caused notable code changes, and that we\
believe the code is ready for general usage (based on bug inflow).

**For a description of the MariaDB Java Client see the**[**About the MariaDB Java Client**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-the-mariadb-java-client/README.md) **page.**

For a list of all changes made in this release, with links to detailed\
information on each push, see the[changelog](../changelogs/1.1/mariadb-java-client-116-changelog.md).

## New functionality

New connection parameter serverTimezone:\
If set, timezone conversions will occur when storing temporal data with preparedStatement (setDate(), setTime(), setTimestamp()) and when reading data using ResultSet (getDate(),getTime(),getTimestamp())\
The effect is similar to setting the [time\_zone](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables#time_zone) session variable. The difference is better cross-platform compatibility (i.e timezone names like "Asia/Omsk" can also be used when the server is on Windows). Also, this option works for both [datetime](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/datetime) and [timestamp](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/date-and-time-data-types/timestamp) datatypes, while the server-side option has no effect on datetime. ([CONJ-65](https://jira.mariadb.org/browse/CONJ-65))

## Bugs fixed in this release

Some of the bugs fixed include:

* Index parts that are not not parts of primary keys may be returned by `DatabaseMetaData.getPrimaryKeys()` ([CONJ-66](https://jira.mariadb.org/browse/CONJ-66))
* Fixed UTF8 length calculation ([CONJ-73](https://jira.mariadb.org/browse/CONJ-73))
* Prevent batch execution if the batchlist for statements and prepared statements is null. ([CONJ-74](https://jira.mariadb.org/browse/CONJ-74))
* MySQLDatabaseMetaData fix: `GetColumns` now returns type.BIT instead of type.TINYINT if tinyInt1IsBit option is set ([CONJ-72](https://jira.mariadb.org/browse/CONJ-72))
* Autoselect database for SSL connections ([CONJ-71](https://jira.mariadb.org/browse/CONJ-71))
* Throw exception for unsupported JDBC 4.1 functions ([CONJ-67](https://jira.mariadb.org/browse/CONJ-67))
* All timeout parameters will be specified in mircoseconds (instead of seconds). ([CONJ-78](https://jira.mariadb.org/browse/CONJ-78))
* Fixed a leak in callable statements (Thanks to Andrew Gaul)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
