# MariaDB Connector/J 1.4.0 Changelog

{% include "../../../../.gitbook/includes/latest-java.md" %}

[Download](https://downloads.mariadb.org/connector-java/1.4.0/)[Release Notes](../../1.4/mariadb-connector-j-140-release-notes.md)[Changelog](mariadb-connector-j-140-changelog.md)[Connector/J Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-j/README.md)

**Release date:** 1 Apr 2016

For the highlights of this release, see the[release notes](../../1.4/mariadb-connector-j-140-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-j) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #851578a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/851578a)
  * Temporary test openjdk7 deletion on travis due to [5227](https://github.com/travis-ci/travis-ci/issues/5227)
* [Revision #2651df1](https://github.com/mariadb-corporation/mariadb-connector-j/commit/2651df1)
  * Kerberos merge correction
* [Revision #cd11a81](https://github.com/mariadb-corporation/mariadb-connector-j/commit/cd11a81)
  * \[[CONJ-217](https://jira.mariadb.org/browse/CONJ-217)] merge correction
* [Revision #adf5d45](https://github.com/mariadb-corporation/mariadb-connector-j/commit/adf5d45)
  * \[[CONJ-138](https://jira.mariadb.org/browse/CONJ-138)] correction of isBeforeFirst() result
* [Revision #cbe5a5c](https://github.com/mariadb-corporation/mariadb-connector-j/commit/cbe5a5c)
  * Printstacktrace deletion
* [Revision #b14d9c4](https://github.com/mariadb-corporation/mariadb-connector-j/commit/b14d9c4)
  * Merge pull request #79 from MariaDB/1.4.0-merge
* [Revision #71c2d54](https://github.com/mariadb-corporation/mariadb-connector-j/commit/71c2d54)
  * Checkstyle correction + documentation GSSAPI
* [Revision #85fa733](https://github.com/mariadb-corporation/mariadb-connector-j/commit/85fa733)
  * Merge pull request #78 from MariaDB/1.4.0-merge
* [Revision #44fb011](https://github.com/mariadb-corporation/mariadb-connector-j/commit/44fb011)
  * Merge branch 'master' into 1.4.0-merge
* [Revision #54e1a97](https://github.com/mariadb-corporation/mariadb-connector-j/commit/54e1a97)
  * Merge pull request #77 from fullcontact/poolImprovements
* [Revision #318ca24](https://github.com/mariadb-corporation/mariadb-connector-j/commit/318ca24)
  * \[[CONJ-271](https://jira.mariadb.org/browse/CONJ-271)] correction of resultset return value of first/last when resultset has no result.
* [Revision #f9a06a3](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f9a06a3)
  * Add PAM and kerberos authentication
* [Revision #49e3e35](https://github.com/mariadb-corporation/mariadb-connector-j/commit/49e3e35)
  * Correction for mysql 5.6, 5.7 (moreResult missing flag)
* [Revision #c050427](https://github.com/mariadb-corporation/mariadb-connector-j/commit/c050427)
  * Failover query relaunched correction
* [Revision #ac5dd67](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ac5dd67)
  * Error message improvement for batch parameter
* [Revision #cbddaca](https://github.com/mariadb-corporation/mariadb-connector-j/commit/cbddaca)
  * Improve buffer reading for resultset
* [Revision #9dec404](https://github.com/mariadb-corporation/mariadb-connector-j/commit/9dec404)
  * Change javadoc to use inheritDoc
* [Revision #fc44edf](https://github.com/mariadb-corporation/mariadb-connector-j/commit/fc44edf)
  * Merging 1.4.0 with 1.3.7
* [Revision #7bc83db](https://github.com/mariadb-corporation/mariadb-connector-j/commit/7bc83db)
  * Code normalization
* [Revision #52c9964](https://github.com/mariadb-corporation/mariadb-connector-j/commit/52c9964)
  * Tag 1.4.0-beta-1
* [Revision #e3b7ed3](https://github.com/mariadb-corporation/mariadb-connector-j/commit/e3b7ed3)
  * Add noAccessToProcedureBodies test
* [Revision #a3dbf61](https://github.com/mariadb-corporation/mariadb-connector-j/commit/a3dbf61)
  * Correction for better integration tests
* [Revision #d019529](https://github.com/mariadb-corporation/mariadb-connector-j/commit/d019529)
  * Correction for test due to server error [MDEV-8984](https://jira.mariadb.org/browse/MDEV-8984) on [mariadb 10.1.11](../../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-1-series/mariadb-10111-release-notes.md)
* [Revision #1689a86](https://github.com/mariadb-corporation/mariadb-connector-j/commit/1689a86)
  * New CallableStatement implementation
* [Revision #28b1811](https://github.com/mariadb-corporation/mariadb-connector-j/commit/28b1811)
  * Failover correction for fetching implementation
* [Revision #9e2fccd](https://github.com/mariadb-corporation/mariadb-connector-j/commit/9e2fccd)
  * ATOI implementation for better performance when reading number result
* [Revision #692c477](https://github.com/mariadb-corporation/mariadb-connector-j/commit/692c477)
  * UseReadAheadInput implementation
* [Revision #627dc09](https://github.com/mariadb-corporation/mariadb-connector-j/commit/627dc09)
  * Fetch size implementation
* [Revision #dca1012](https://github.com/mariadb-corporation/mariadb-connector-j/commit/dca1012)
  * Keep buffer for a time to avoid reinitialisation
* [Revision #f566ca8](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f566ca8)
  * \[[CONJ-269](https://jira.mariadb.org/browse/CONJ-269)] handle server configuration autocommit=0
* [Revision #efc6405](https://github.com/mariadb-corporation/mariadb-connector-j/commit/efc6405)
  * Clean setQueryTimeout functionnality
* [Revision #46c4166](https://github.com/mariadb-corporation/mariadb-connector-j/commit/46c4166)
  * \[[CONJ-250](https://jira.mariadb.org/browse/CONJ-250)] Switch internal pools to use daemon threads to solve
* [Revision #959dcd1](https://github.com/mariadb-corporation/mariadb-connector-j/commit/959dcd1)
  * Test correction on Date '0000-00-00' incompatible with mysql 5.7

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
