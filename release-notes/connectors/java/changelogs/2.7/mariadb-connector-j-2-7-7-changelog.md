# MariaDB Connector/J 2.7.7 Changelog

{% include "../../../../.gitbook/includes/latest-java.md" %}

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../2.7/mariadb-connector-j-2-7-7-release-notes.md)[Changelog](mariadb-connector-j-2-7-7-changelog.md)[Connector/J Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-j/README.md)

**Release date:** 08 Nov 2022

For the highlights of this release, see the[release notes](../../2.7/mariadb-connector-j-2-7-7-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-j) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #eadfa639](https://github.com/mariadb-corporation/mariadb-connector-j/commit/eadfa639) - \[[CONJ-1021](https://jira.mariadb.org/browse/CONJ-1021)] correcting windows GSSAPI test
* [Revision #16b80b54](https://github.com/mariadb-corporation/mariadb-connector-j/commit/16b80b54) - \[misc] mysql test correction
* [Revision #36892f08](https://github.com/mariadb-corporation/mariadb-connector-j/commit/36892f08) - \[misc] test suite stability improvement
* [Revision #bc680ceb](https://github.com/mariadb-corporation/mariadb-connector-j/commit/bc680ceb) - \[[CONJ-1021](https://jira.mariadb.org/browse/CONJ-1021)] add windows GSSAPI test
* [Revision #07e18447](https://github.com/mariadb-corporation/mariadb-connector-j/commit/07e18447) - \[[CONJ-1021](https://jira.mariadb.org/browse/CONJ-1021)] GSSAPI authentication might result in connection reset
* [Revision #60955838](https://github.com/mariadb-corporation/mariadb-connector-j/commit/60955838) - \[misc] ensure test suite reliability
* [Revision #66dcc307](https://github.com/mariadb-corporation/mariadb-connector-j/commit/66dcc307) - \[misc] skip test with `FLUSH PRIVILEGES` with MySQL server 8.0.31 that broke server public key retrieval afterwhile
* [Revision #b79ba565](https://github.com/mariadb-corporation/mariadb-connector-j/commit/b79ba565) - \[[CONJ-1019](https://jira.mariadb.org/browse/CONJ-1019)] DatabaseMetaData.getImportedKeys should return real value for PK\_NAME column
* [Revision #df715bd5](https://github.com/mariadb-corporation/mariadb-connector-j/commit/df715bd5) - \[misc] ensure test stability for galera
* [Revision #11d9a164](https://github.com/mariadb-corporation/mariadb-connector-j/commit/11d9a164) - \[[CONJ-1016](https://jira.mariadb.org/browse/CONJ-1016)] avoid splitting BULK command into multiple commands in case of prepareStatement.setNull() use
* [Revision #b6e80e20](https://github.com/mariadb-corporation/mariadb-connector-j/commit/b6e80e20) - \[[CONJ-1011](https://jira.mariadb.org/browse/CONJ-1011)] correcting possible NPE when using statement.cancel() that coincide with statement.close() in another thread
* [Revision #6cfdd7ed](https://github.com/mariadb-corporation/mariadb-connector-j/commit/6cfdd7ed) - \[misc] update jacoco to 0.8.8 to permit build with java 17
* [Revision #639a07e8](https://github.com/mariadb-corporation/mariadb-connector-j/commit/639a07e8) - \[misc] bump 2.7.7 snapshot version
* [Revision #8196fd8c](https://github.com/mariadb-corporation/mariadb-connector-j/commit/8196fd8c) - \[misc] corrected redondant check
* [Revision #0cb2fd12](https://github.com/mariadb-corporation/mariadb-connector-j/commit/0cb2fd12) - \[misc] update test suite to run on current supported server version
* [Revision #351546cb](https://github.com/mariadb-corporation/mariadb-connector-j/commit/351546cb) - \[[CONJ-1007](https://jira.mariadb.org/browse/CONJ-1007)] only fix socket descriptor issue for unix socket
* [Revision #872e9b1a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/872e9b1a) - \[misc] Leaking socket file descriptors when using unix domain sockets when path doesn't exist
* [Revision #e6b9e3e3](https://github.com/mariadb-corporation/mariadb-connector-j/commit/e6b9e3e3) - \[misc] adding [MariaDB 10.8](../../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-8-series/what-is-mariadb-108.md) to test suite. Build is now 10.9

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
