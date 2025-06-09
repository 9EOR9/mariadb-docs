# MariaDB Connector/J 1.6.2 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of [MariaDB Connector/J](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-j/README.md) is:[**MariaDB Connector/J 3.5.3**](../../mariadb-connector-j-3-5-release-notes/mariadb-connector-j-3-5-3-release-notes.md)

[Download](https://downloads.mariadb.org/connector-java/1.6.2/)[Release Notes](../../mariadb-connectorj-16-release-notes/mariadb-connector-j-162-release-notes.md)[Changelog](mariadb-connector-j-162-changelog.md)[Connector/J Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-j/README.md)

**Release date:** 27 Jun 2017

For the highlights of this release, see the[release notes](../../mariadb-connectorj-16-release-notes/mariadb-connector-j-162-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-j) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #774a5ae](https://github.com/mariadb-corporation/mariadb-connector-j/commit/774a5ae) - bump 1.6.2 version
* [Revision #842207cd](https://github.com/mariadb-corporation/mariadb-connector-j/commit/842207cd) - \[misc] remove meaningless test
* [Revision #e7e5cea4](https://github.com/mariadb-corporation/mariadb-connector-j/commit/e7e5cea4) - \[[CONJ-498](https://jira.mariadb.org/browse/CONJ-498)] ensure race condition when enablePacketDebug is not set
* [Revision #ddbb34a9](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ddbb34a9) - \[[CONJ-498](https://jira.mariadb.org/browse/CONJ-498)] java 6 compatibility support - adding travis environment
* [Revision #82d13da5](https://github.com/mariadb-corporation/mariadb-connector-j/commit/82d13da5) - \[[CONJ-498](https://jira.mariadb.org/browse/CONJ-498)] java 6 compatibility support
* [Revision #161b17d9](https://github.com/mariadb-corporation/mariadb-connector-j/commit/161b17d9) - Merge remote-tracking branch 'origin/develop' into develop-jre6
* [Revision #39d3a82e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/39d3a82e) - \[[CONJ-422](https://jira.mariadb.org/browse/CONJ-422)] change test
* [Revision #52d489dc](https://github.com/mariadb-corporation/mariadb-connector-j/commit/52d489dc) - \[test] Maxscale issue when creating a database, need a few ms before connecting
* [Revision #1bbb16b3](https://github.com/mariadb-corporation/mariadb-connector-j/commit/1bbb16b3) - \[test] disabling travis jdk9 temporary due to [7944](https://github.com/travis-ci/travis-ci/issues/7944)
* [Revision #1f0bc801](https://github.com/mariadb-corporation/mariadb-connector-j/commit/1f0bc801) - \[[CONJ-497](https://jira.mariadb.org/browse/CONJ-497)] escape string correction for big query > 8M - test correction
* [Revision #abea4db8](https://github.com/mariadb-corporation/mariadb-connector-j/commit/abea4db8) - \[[CONJ-497](https://jira.mariadb.org/browse/CONJ-497)] escape string correction for big query > 8M
* [Revision #0aaa9b04](https://github.com/mariadb-corporation/mariadb-connector-j/commit/0aaa9b04) - Proposed fix for [CONJ-497](https://jira.mariadb.org/browse/CONJ-497)
* [Revision #457aea48](https://github.com/mariadb-corporation/mariadb-connector-j/commit/457aea48) - \[misc] add debug trace to EOF error
* [Revision #0732f4e9](https://github.com/mariadb-corporation/mariadb-connector-j/commit/0732f4e9) - \[misc] add parsing to option "sessionVariable"
* [Revision #95ee9c7a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/95ee9c7a) - \[[CONJ-473](https://jira.mariadb.org/browse/CONJ-473)] when useServerPrepStmts is not set, the PREPARE statement must not be cached.
* [Revision #f85aacb0](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f85aacb0) - \[misc] correcting cloning CallableProcedureStatement
* [Revision #7869842e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/7869842e) - \[misc] default intellij config update
* [Revision #818fa38a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/818fa38a) - Merge branches 'develop' and 'master' of [mariadb-connector-j](https://github.com/MariaDB/mariadb-connector-j) into develop
* [Revision #11897e66](https://github.com/mariadb-corporation/mariadb-connector-j/commit/11897e66) - \[[CONJ-494](https://jira.mariadb.org/browse/CONJ-494)] Handle PrepareStatement.getParameterMetaData() if query cannot be PREPAREd
* [Revision #c60cb780](https://github.com/mariadb-corporation/mariadb-connector-j/commit/c60cb780) - \[misc] corrected documentation
* [Revision #044c1b5b](https://github.com/mariadb-corporation/mariadb-connector-j/commit/044c1b5b) - \[misc] ensure stability if option "enablePacketDebug" is set and IOException occur in when establishing socket
* [Revision #496da260](https://github.com/mariadb-corporation/mariadb-connector-j/commit/496da260) - \[misc] ensure stability if option "enablePacketDebug" is set and IOException occur in when establishing socket
* [Revision #50737577](https://github.com/mariadb-corporation/mariadb-connector-j/commit/50737577) - \[misc] permit having debug trace when option "enablePacketDebug" for for authentication packet IOException
* [Revision #64ca2365](https://github.com/mariadb-corporation/mariadb-connector-j/commit/64ca2365) - \[misc] permit having debug trace when option "enablePacketDebug" for for authentication packet IOException
* [Revision #95bfc8c1](https://github.com/mariadb-corporation/mariadb-connector-j/commit/95bfc8c1) - \[misc] improve tests if connection failed to have the initial error code
* [Revision #0302e1c0](https://github.com/mariadb-corporation/mariadb-connector-j/commit/0302e1c0) - \[misc] improve testing
* [Revision #c85626b9](https://github.com/mariadb-corporation/mariadb-connector-j/commit/c85626b9) - \[misc] checkstyle correction
* [Revision #db9e5199](https://github.com/mariadb-corporation/mariadb-connector-j/commit/db9e5199) - \[misc] compatibility to JRE 6

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.

{% @marketo/form formid="4316" formId="4316" %}
