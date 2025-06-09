# MariaDB Connector/Node.js 2.1.1 Changelog

The most recent [_**Stable (GA)**_](../../../../mariadb-release-criteria.md) release of [MariaDB Connector/Node.js](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-nodejs/README.md) is:[**MariaDB Connector/Node.js 3.4.2**](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-4-2-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-nodejs-2x-release-notes/mariadb-connector-nodejs-211-release-notes.md)[Changelog](mariadb-connector-nodejs-211-changelog.md)[Connector/Node.js Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-nodejs/README.md)

**Release date:** 06 Sept. 2019

For the highlights of this release, see the[release notes](../../mariadb-connector-nodejs-2x-release-notes/mariadb-connector-nodejs-211-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-nodejs) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #24bc77b](https://github.com/mariadb-corporation/mariadb-connector-j/commit/24bc77b) - \[misc] adding changelog for 2.1.1
* [Revision #0c0df1a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/0c0df1a) - \[misc] test TLS minimum version change in order to test old mysql server with Node.js 12
* [Revision #0f542cc](https://github.com/mariadb-corporation/mariadb-connector-j/commit/0f542cc) - \[misc] small performance improvement to avoid testing debug each packet
* [Revision #74ceab5](https://github.com/mariadb-corporation/mariadb-connector-j/commit/74ceab5) - \[misc] force test TLSv1.1 compatibility if Node.js 12 and MySQL before version 8.0
* [Revision #a9e11b1](https://github.com/mariadb-corporation/mariadb-connector-j/commit/a9e11b1) - \[misc] correcting SSL test that now can use TLSv1.3 protocol for [MariaDB 10.4](broken-reference)
* [Revision #fbe82aa](https://github.com/mariadb-corporation/mariadb-connector-j/commit/fbe82aa) - \[misc] removing memory leak detection for node.js 12 until mem-watch compatibility
* [Revision #6ae18cc](https://github.com/mariadb-corporation/mariadb-connector-j/commit/6ae18cc) - \[misc] removing node.js 6 from CI, ESLint 6 requiring 8 or newer
* [Revision #4da0e5a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/4da0e5a) - \[misc] CI testing replacing node.js v11 by supported LTS v12
* [Revision #aa25af9](https://github.com/mariadb-corporation/mariadb-connector-j/commit/aa25af9) - \[misc] update dependencies to latest version
* [Revision #f697e95](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f697e95) - \[misc] code style correction
* [Revision #1400b1f](https://github.com/mariadb-corporation/mariadb-connector-j/commit/1400b1f) - \[misc] type script correction for triple slash importation
* [Revision #a888b1d](https://github.com/mariadb-corporation/mariadb-connector-j/commit/a888b1d) - \[misc] Node.js v12 require TLSv1.2 by default Correcting SSL test to permit TLSv1 and TLSv1.1 in case of windows server
* [Revision #6b9402d](https://github.com/mariadb-corporation/mariadb-connector-j/commit/6b9402d) - Merge branch 'pull/73' into develop
* [Revision #848ebc0](https://github.com/mariadb-corporation/mariadb-connector-j/commit/848ebc0) - Merge branch 'master' into develop
* [Revision #5058c83](https://github.com/mariadb-corporation/mariadb-connector-j/commit/5058c83) - \[misc] benchmark init function using promise or callback implementation depending on benchmark
* [Revision #7f3e8ae](https://github.com/mariadb-corporation/mariadb-connector-j/commit/7f3e8ae) - Update package.json
* [Revision #46fbc65](https://github.com/mariadb-corporation/mariadb-connector-j/commit/46fbc65) - bump dependencies
* [Revision #a268e71](https://github.com/mariadb-corporation/mariadb-connector-j/commit/a268e71) - \[misc] eslint code style correction
* [Revision #3f77b33](https://github.com/mariadb-corporation/mariadb-connector-j/commit/3f77b33) - Merge pull request #71 from kkx/fix/cluster-pool-ordered-selector
* [Revision #993003b](https://github.com/mariadb-corporation/mariadb-connector-j/commit/993003b) - \[misc] documentation improvement for connection.reset(). Error now indicate that minimum version server is required.
* [Revision #04452fc](https://github.com/mariadb-corporation/mariadb-connector-j/commit/04452fc) - fix missing parameter for ordered selector
* [Revision #066a478](https://github.com/mariadb-corporation/mariadb-connector-j/commit/066a478) - Merge remote-tracking branch 'origin/master' into develop
* [Revision #940bdbc](https://github.com/mariadb-corporation/mariadb-connector-j/commit/940bdbc) - \[misc] test correction for recent MySQL 8 that add a new error when plugin is unknown by client
* [Revision #d068ce5](https://github.com/mariadb-corporation/mariadb-connector-j/commit/d068ce5) - \[misc] updating test for 10.4 possible default cipher and mysql non availability of TLSv1.2
* [Revision #01a9d9e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/01a9d9e) - \[misc] correcting indentation to follow lint rules.
* [Revision #a2aa58b](https://github.com/mariadb-corporation/mariadb-connector-j/commit/a2aa58b) - \[misc] correcting test for mysql community before 8.0 version that doesn't support TLSv1.2
* [Revision #9dd5ef3](https://github.com/mariadb-corporation/mariadb-connector-j/commit/9dd5ef3) - \[misc] adding 10.4 TLSv1.2 testing on windows
* [Revision #72a9e21](https://github.com/mariadb-corporation/mariadb-connector-j/commit/72a9e21) - \[MENT-29] azure CI install ubuntu from tar
* [Revision #9a6a0f0](https://github.com/mariadb-corporation/mariadb-connector-j/commit/9a6a0f0) - \[misc] benchmark result charset correction
* [Revision #9ffe95d](https://github.com/mariadb-corporation/mariadb-connector-j/commit/9ffe95d) - \[misc] correction callback documentation links and correct connection.batch return description
* [Revision #a915ff3](https://github.com/mariadb-corporation/mariadb-connector-j/commit/a915ff3) - \[misc] documentation link correction

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.
