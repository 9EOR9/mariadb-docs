# MariaDB Connector/Node.js 0.7.0 Changelog

{% include "../../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://downloads.mariadb.org/connector-nodejs/0.7.0/) | [Release Notes](../../mariadb-connector-nodejs-0x-release-notes/mariadb-connector-nodejs-070-release-notes.md) | [Changelog](mariadb-connector-nodejs-070-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide)

**Release date:** 19 Jul 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-nodejs-0x-release-notes/mariadb-connector-nodejs-070-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-nodejs) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #924f958](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/924f958) - \[misc] change pool implementation to permit node 6 compatibility (removal of async await)
* [Revision #92cb4be](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/92cb4be) - \[misc] set version to 0.7.0
* [Revision #2caaf03](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2caaf03) - \[misc] appveyor badge display master branch result
* [Revision #8bb5a7b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8bb5a7b) - \[[CONJ-17](https://jira.mariadb.org/browse/CONJ-17)] pool option testing minDelayValidation
* [Revision #2cb388c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2cb388c) - \[[CONJ-17](https://jira.mariadb.org/browse/CONJ-17)] adding pool documentation changing default pool option : - connectionLimit to 10 - minDelayValidation to 500ms
* [Revision #f8fa83b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f8fa83b) - \[misc] correcting pool timeout test
* [Revision #03330b6](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/03330b6) - \[misc] enable coveralls script when not benchmarking
* [Revision #2970495](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2970495) - \[misc] enable coveralls script
* [Revision #2925ec0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2925ec0) - \[[CONJS-17](https://jira.mariadb.org/browse/CONJS-17)] pool testing stability correction
* [Revision #52616f0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/52616f0) - \[[CONJS-17](https://jira.mariadb.org/browse/CONJS-17)] adding callback pool implementation
* [Revision #8521f0a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8521f0a) - \[misc] project transferred to official MariaDB repository
* [Revision #62f1fca](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/62f1fca) - \[misc] changing stream event "columns" to "fields" for mysql compatibility
* [Revision #1635181](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1635181) - \[misc] changing benchmark with pool to random number
* [Revision #0928c58](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0928c58) - \[misc] travis test coverals removal for bench
* [Revision #87cfc35](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/87cfc35) - \[misc] searching to identify travis error not reproducing on local environment
* [Revision #4a40707](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4a40707) - \[misc] correct test for auth-pam that wasn't reliable
* [Revision #1ae9b5f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1ae9b5f) - \[misc] correcting connection last use time in pool
* [Revision #93f4d25](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/93f4d25) - \[misc] changing appveyor test to use last MariaDB released version
* [Revision #0cba8ed](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0cba8ed) - \[misc] destroy connection failover on end if connection creation fail. Test correction for ssl error message changed in node 10 version
* [Revision #fd360c4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fd360c4) - \[misc] ensuring pool test stability
* [Revision #1f40093](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1f40093) - \[misc] appveyor testing : removing node 6 adding pool benchmark
* [Revision #b1ee447](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b1ee447) - \[misc] ensuring test stability using "FLUSH PRIVILEGES" after creating test user
* [Revision #6b4e3d9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6b4e3d9) - \[misc] adding coverage in development guide
* [Revision #df8ae23](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/df8ae23) - \[misc] documentation format correction, and correcting error in example
* [Revision #3b1a783](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/3b1a783) - \[misc] pool timeout with multiple task in queue correction
* [Revision #e510fe3](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e510fe3) - \[misc] pool test stability improvement
* [Revision #b32ee2e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b32ee2e) - Revises Pipelining
* [Revision #9c1770e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9c1770e) - Revises the Developers Guide
* [Revision #dda2c96](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/dda2c96) - pool reviewed
* [Revision #fc4b9aa](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fc4b9aa) - Updates to connection options documentation
* [Revision #f8d190c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f8d190c) - Revises the Callback API docs
* [Revision #1abfbea](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1abfbea) - Revises benchmarks.md
* [Revision #2828c7f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2828c7f) - pool first draft implementation
* [Revision #979ba3b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/979ba3b) - Finishes updating README
* [Revision #254cc5e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/254cc5e) - Updates to query() section of README
* [Revision #a13db05](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a13db05) - Updates to READEME on query
* [Revision #9a4af55](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9a4af55) - Updates text for connections
* [Revision #f83fac0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f83fac0) - Updated the Quick Start section of README
* [Revision #55a4d73](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/55a4d73) - Cleans up Benchmarks section of README
* [Revision #445747f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/445747f) - Cleans up and expands text on Why a New Client section
* [Revision #c631437](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c631437) - Corrected ES2017 example in README
* [Revision #b625751](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b625751) - ensuring debug log test length
* [Revision #3af811f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/3af811f) - contribution guide reviewed
* [Revision #3133174](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/3133174) - Actual benchmark tests
* [Revision #0fc6382](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0fc6382) - adding benchmark tests
* [Revision #d7e4cdd](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d7e4cdd) - adding benchmark tests
* [Revision #06c3794](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/06c3794) - benchmark documentation
* [Revision #61a6e43](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/61a6e43) - main readme correction
* [Revision #c40ed9b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c40ed9b) - test correction
* [Revision #e7b4a70](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e7b4a70) - metadata change for performance
* [Revision #61db40b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/61db40b) - correcting benchmark display
* [Revision #6f2c4b6](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6f2c4b6) - correcting benchmark display
* [Revision #a73bb1d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a73bb1d) - Improving documentation
* [Revision #506953f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/506953f) - Improving documentation
* [Revision #b721f82](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b721f82) - \[misc] changing stream function to queryStream to follow promise-mysql API remove not accessible code adding test coverage for failing socket using callback
* [Revision #ee1b58f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ee1b58f) - \[misc] adding the option "metaAsArray" for mysql2 and existing mysql promise package implementation compatibility
* [Revision #d406d4b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d406d4b) - \[misc] appveyor correction for [mariadb 5.5](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/connectors/node.js/changelogs/mariadb-connector-nodejs-0x-changelogs/broken-reference/README.md) (with less memory use)
* [Revision #4c09946](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4c09946) - \[misc] test appveyor correction for [mariadb 5.5](https://github.com/mariadb-corporation/docs-server/blob/test/release-notes/connectors/node.js/changelogs/mariadb-connector-nodejs-0x-changelogs/broken-reference/README.md)
* [Revision #b9a3f22](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b9a3f22) - \[misc] test correction debug log when compression
* [Revision #2eccb16](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2eccb16) - \[misc] streaming when using callback implementation
* [Revision #b191638](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b191638) - \[misc] correcting debug range since default connectAttributes now default to false
* [Revision #4b6af81](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4b6af81) - \[misc] correcting debug range since default connectAttributes now default to false
* [Revision #5f53e53](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5f53e53) - \[misc] correcting debug range since default connectAttributes now default to false
* [Revision #ab91e48](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ab91e48) - \[misc] connectAttributes option description, and adding boolean possibility to permit not sending it or sending default/additional information
* [Revision #2828ce0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2828ce0) - \[misc] small buffer writing optimization
* [Revision #1fa092a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1fa092a) - ensuring benchmarks connection stay alive with ping between all tests
* [Revision #da9d047](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/da9d047) - benchmark promise AND callback implementation correction appveyor default configuration
* [Revision #521ab80](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/521ab80) - adding test error logging, and connection correction
* [Revision #d4b736d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d4b736d) - alter user password using mysql\_native\_password for mysql 8
* [Revision #6d93f1f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6d93f1f) - changing appveyor innodb\_log\_file\_size to correspond to max-allowed-packet value
* [Revision #4dcb3f9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4dcb3f9) - connection attributes size test verification
* [Revision #d77da68](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d77da68) - correct compress debug size fro travis that have huge computer name
* [Revision #0d5fc77](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0d5fc77) - appveyor max\_allowed\_packet increased to 21mb
* [Revision #498f872](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/498f872) - correcting ssl test for mysql 8 that doesn't permit using PASSWORD()
* [Revision #b18be9e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b18be9e) - adding compression test (debug log, command canceled client side)
* [Revision #4ccac53](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4ccac53) - correcting ssl test with password
* [Revision #19af44e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/19af44e) - appveyor max-allowed-packet increasing to correct test
* [Revision #f09f76c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f09f76c) - correcting mysql\_native\_password plugin that was encrypting with the seed null data
* [Revision #b5e7225](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b5e7225) - connection attributes really used on connection
* [Revision #6128920](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6128920) - test separation for compression
* [Revision #eb48627](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/eb48627) - completing connection API testing
* [Revision #11412ee](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/11412ee) - completing connection API testing
* [Revision #dae670a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/dae670a) - replacing assert.isTrue/isFalse by assert() to simplify code
* [Revision #731cea7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/731cea7) - test connection metadata correction for appveyor/travis
* [Revision #ad3b37a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ad3b37a) - test correction for debug output
* [Revision #f714061](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f714061) - parsing handling command client error
* [Revision #6248558](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6248558) - removing useless assignation
* [Revision #a8443cc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a8443cc) - ensuring connection timeout doesn't interfere
* [Revision #9592b6b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9592b6b) - debug log test limit corrected for mysql 5.5 that doesn't support connection attributes
* [Revision #769c27a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/769c27a) - adding collation unit test adding query 4 bytes utf8 parameter encoding testing
* [Revision #74ff8ce](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/74ff8ce) - adding query option test adding query error message log test
* [Revision #1f7a9fc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1f7a9fc) - remove inaccessible code, correct database change code for server that doesn't support metadata change
* [Revision #d1b8713](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d1b8713) - adding tests : - changing database ok meta - nestTable string separator - rows as array
* [Revision #7d4d38c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7d4d38c) - correcting expected debug text length for all kind of server
* [Revision #d14be86](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d14be86) - correcting expected debug text length for all kind of server
* [Revision #5822c4a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5822c4a) - adding test coverage
* [Revision #ed865aa](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ed865aa) - adding test coverage
* [Revision #5261f9a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5261f9a) - error message maximum length correction test correction for server < 10.2
* [Revision #268c74a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/268c74a) - handle utf8 wrong surrogate
* [Revision #9635c4c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9635c4c) - adding tests query parsing
* [Revision #b24b321](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b24b321) - adding tests connection meta
* [Revision #0052ecd](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0052ecd) - adding new tests
* [Revision #5179933](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5179933) - adding coverall
* [Revision #cca157b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cca157b) - benchmarks based on mysql connector
* [Revision #8c9d735](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8c9d735) - test correction for node 6 compatibility
* [Revision #5154e8a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5154e8a) - faster test, avoiding assert error 2s time limit error
* [Revision #55c407c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/55c407c) - removing "error" event on command implementation, to ensure not throwing error
* [Revision #d872b84](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d872b84) - result-set streaming implementation
* [Revision #1a3fa11](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1a3fa11) - correcting beginTransaction success result when using callback
* [Revision #9a00895](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9a00895) - correcting commit / rollback success result when using callback
* [Revision #86b8571](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/86b8571) - skipping node-memwatch leak test for node 6
* [Revision #86169ad](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/86169ad) - skipping node-memwatch leak test for node 6
* [Revision #fc42e48](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fc42e48) - skipping node-memwatch leak test for node 6
* [Revision #959ab2b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/959ab2b) - skipping node-memwatch leak test for node 6
* [Revision #bc28e63](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bc28e63) - changing to node-memwatch to support node 10
* [Revision #f1aa9c8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f1aa9c8) - test correction, wrong mysql.user case
* [Revision #d25d326](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d25d326) - removing memwatch-next dev-dependency
* [Revision #262b324](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/262b324) - adding memory leak test detection
* [Revision #8384d95](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8384d95) - testing : updating server waiter script with promise implementation
* [Revision #439f3a1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/439f3a1) - testing : npm installation before checking docker server is up
* [Revision #a3f9842](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a3f9842) - removing npm update since not compatible with node.js 7
* [Revision #06470bc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/06470bc) - Separation of callback connection versus promise implementation
* [Revision #0fc8138](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0fc8138) - benchmarks use blachole engine only if available. benchmarks doesn't use mariasql by default. jslint code format
* [Revision #bf1929f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bf1929f) - \[misc] revert benchmark results presentation
* [Revision #1fe604d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1fe604d) - \[misc] error message correction - avoiding double connection header when using the "trace" option
* [Revision #308aaff](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/308aaff) - \[misc] test ed25519 authentication plugin only if server has been build with plugin
* [Revision #2344013](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2344013) - \[misc] test correction
* [Revision #ce2da19](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ce2da19) - \[misc] using query promise
* [Revision #2a1361a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2a1361a) - \[misc] always using promise. Callback can still be used for compatibility when option 'useCallback' is set
* [Revision #95f403b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/95f403b) - \[misc] test correction
* [Revision #edbc58b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/edbc58b) - \[misc] correction on promise connection.changeUser() to avoid relaunching authentication succeed
* [Revision #93dd4eb](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/93dd4eb) - \[misc] adding connection.changeUser() promise implementation
* [Revision #eb97fc7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/eb97fc7) - \[misc] adding full stacktrace when connecting error + ensuring having any error on socket end
* [Revision #caddb3f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/caddb3f) - \[misc] Promise implementation for connect() and end() methods
* [Revision #aaa9326](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/aaa9326) - \[misc] discard packet cache when closing
* [Revision #395dbe1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/395dbe1) - \[misc] detailled connection status and handshake events
* [Revision #f9efb89](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f9efb89) - \[misc] tag version 0.7.0
* [Revision #2c996ff](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2c996ff) - \[misc] correct server current build test script
* [Revision #be411a3](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/be411a3) - \[misc] removing packet sequence number checking
* [Revision #7101b9b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7101b9b) - \[misc] perf improvement : immediately send command when pipelining
* [Revision #b0b1498](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b0b1498) - \[misc] method renaming to avoid confusion (quote)
* [Revision #12bb9d1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/12bb9d1) - \[misc] small performance improvement, avoiding checking remaining buffer size before copying quote mainly
* [Revision #05e2269](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/05e2269) - \[misc] removing passing connection event object
* [Revision #efe3451](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/efe3451) - \[misc] removing unused code
* [Revision #31a3462](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/31a3462) - \[misc] correcting test to skip mysql change user
* [Revision #15ea477](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/15ea477) - \[misc] status change after changing user
* [Revision #f5eac9e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f5eac9e) - \[misc] adding method isValid() to quickly know connection state
* [Revision #e6ede2a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e6ede2a) - \[misc] changing folder "src" to "lib"
* [Revision #45015f8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/45015f8) - \[misc] adding option "trace" to permit retrieving query creation stacktrace
* [Revision #cb6b8e2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cb6b8e2) - \[misc] appveyor using last mariadb release
* [Revision #7c79d7b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7c79d7b) - \[misc] travis fix certificate request error on OpenSSL 1.1.0h
* [Revision #35a2a12](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/35a2a12) - adding session attributes informations (\_server\_host, \_os, \_client\_host)
* [Revision #62ead6e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/62ead6e) - adding current server build to testing, allowed to failed to ensure no regression are added in current server build
* [Revision #e131268](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e131268) - memory correction when using compression
* [Revision #9f1b370](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9f1b370) - changing appveyor download link
* [Revision #a7a1438](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a7a1438) - adding cache to travis
* [Revision #520817d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/520817d) - packet reader header read size test
* [Revision #afaa30a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/afaa30a) - packet reader header read size test
* [Revision #d9f71ae](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d9f71ae) - test public method correction
* [Revision #c54f430](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c54f430) - code small perf improvement adding test public method to permit testing
* [Revision #7825c54](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7825c54) - revert commit on using compression by default
* [Revision #0936b37](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0936b37) - Addition of code documentation for each connection method correcting destroy() implementation
* [Revision #590b019](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/590b019) - using revealing constructor pattern to list only public methods for accessible objects
* [Revision #6053c42](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6053c42) - ensuring test reliability on CI
* [Revision #47fde4d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/47fde4d) - setting connectTimeout to refer to socket initialization and adding new option socketTimeout to handle timeout when socket has connected
* [Revision #68a8264](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/68a8264) - correcting not using IF NOT EXISTS for old server compatibility
* [Revision #fa50ebf](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fa50ebf) - improving SSL test setting USE SSL/X509 on user when version permit it
* [Revision #cbfafce](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cbfafce) - adding mysql 8.0 to test suite
* [Revision #c334bf7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c334bf7) - README text correction
* [Revision #9a863ea](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9a863ea) - remove documentation link duplicate in README
* [Revision #c309a79](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c309a79) - improve presentation of benchmark results
* [Revision #04411d9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/04411d9) - Update README.md
* [Revision #5864334](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5864334) - Update README.md
* [Revision #ff6b154](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ff6b154) - Update README.md
* [Revision #3e420b0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/3e420b0) - Update README.md
* [Revision #5f311bf](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5f311bf) - implement benchmark part in README
* [Revision #36faa15](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/36faa15) - removing compress as default testing options
* [Revision #0aafaa2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0aafaa2) - removing deprecated Buffer() allocation
* [Revision #a419ad1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a419ad1) - socket bind compress correction
* [Revision #ae30888](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ae30888) - appveyor test name pipe correction
* [Revision #54c2f92](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/54c2f92) - code simplification
* [Revision #b55ca49](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b55ca49) - adding roadmap to README
* [Revision #846dd3e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/846dd3e) - separate generation from test
* [Revision #9c89b6f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9c89b6f) - Adding Error.code to follow Node.js direction and compatibility
* [Revision #6e90636](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6e90636) - Error handling standardization
* [Revision #a4c3f6e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a4c3f6e) - test using server current pipe name, not default value
* [Revision #cb577dc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cb577dc) - travis test correction for PAM configuration
* [Revision #79b6e4f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/79b6e4f) - increasing timeout, so unix PAM has time to verify authentication when using PAM authentication plugin
* [Revision #ea25804](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ea25804) - PAM need restart to take in account new configuration
* [Revision #a77b76c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a77b76c) - remove support for node 4/5
* [Revision #c3b3a00](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c3b3a00) - travis upgrading npm version to last one
* [Revision #923d96e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/923d96e) - correcting displaying docker logs
* [Revision #80f38e2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/80f38e2) - adding docker logs
* [Revision #fb7a510](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fb7a510) - trying to change docker running environment to permit dialog test
* [Revision #75b1c56](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/75b1c56) - adding dialog authentication test plugin. removing unused dialog parsing with encoding that can be unknown
* [Revision #1d312d9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1d312d9) - correcting ed25519 test for 10.3
* [Revision #c7b3153](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c7b3153) - avoid ed25529 test if plugin not present
* [Revision #e39240a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e39240a) - ed25529 test improvement
* [Revision #ffe6bf5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ffe6bf5) - test stability improvement
* [Revision #d7edb18](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d7edb18) - adding name pipe and socket authentication test
* [Revision #5c88956](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5c88956) - correcting authentication plugin implementation
* [Revision #c0ddf72](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c0ddf72) - permit benchmark working when connection are set before reading benchmarks files
* [Revision #30a2410](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/30a2410) - improving change user tests
* [Revision #bee6003](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bee6003) - small simplification to avoid one line in stacktrace
* [Revision #d1c38c0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d1c38c0) - disable change user method for mysql due to bug 83472
* [Revision #a3a55fe](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a3a55fe) - change user implementation, plugins correction
* [Revision #e83c591](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e83c591) - change user implementation
* [Revision #8245c47](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8245c47) - avoid reusing buffer even if flushed
* [Revision #8a31139](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8a31139) - adding TODO
* [Revision #111d5db](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/111d5db) - disable nagle algorithm
* [Revision #82ae254](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/82ae254) - trying to detect racecondition issue appveyor - part 2
* [Revision #bf4223d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bf4223d) - trying to detect racecondition issue appveyor
* [Revision #2cee453](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2cee453) - improve pipelining image 2
* [Revision #a832663](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a832663) - improve pipelining image
* [Revision #3bb46c2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/3bb46c2) - correcting image link
* [Revision #8a3a376](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8a3a376) - adding pipelining explaination in readme
* [Revision #54bbb44](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/54bbb44) - correcting debug size check
* [Revision #cca6c89](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cca6c89) - avoiding allocating output buffer if not needed
* [Revision #7f24c4a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7f24c4a) - permit benchmark with mariadb driver only resetting buffer with size according to remaining data to write
* [Revision #467023b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/467023b) - improving error message when socket failed to established
* [Revision #b51e109](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b51e109) - code simplification to fullfill eslint
* [Revision #d2b71d6](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d2b71d6) - avoid race condition sending data reusing the same buffer: next query does change the buffer that may be use directly by socket, resulting in corrupted send data.
* [Revision #4087e9e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4087e9e) - documentation correction
* [Revision #162e1a9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/162e1a9) - removing mysql/mysql2 dev dependencies
* [Revision #7918f9f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7918f9f) - benchmark more logs, adding mariasql to benchlist. 100% relate to fastest driver
* [Revision #cf886d7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cf886d7) - improving TLS documentation
* [Revision #b7d2cdf](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b7d2cdf) - improving TLS documentation
* [Revision #db3805a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/db3805a) - correcting travis client keystore generation for testing
* [Revision #a4317c1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a4317c1) - improving SSL documentation
* [Revision #89393cc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/89393cc) - adding SSL documentation
* [Revision #cd9b379](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cd9b379) - trying to reproduced appveyor issue with log
* [Revision #cdf2781](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cdf2781) - deleting yarn use
* [Revision #d4631c7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d4631c7) - correcting debug output
* [Revision #9b11bda](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9b11bda) - SSL configuration ensure TLS servername value for SNI cannot be overwritten by configuration
* [Revision #413402a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/413402a) - display len on appveyor testing
* [Revision #965b55f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/965b55f) - display benchmark error
* [Revision #d51ac6f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d51ac6f) - adding debug length option using yarn cache for CIs
* [Revision #9980627](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9980627) - updating appveyor server version adding debug to identify packet out of order error on appveyor
* [Revision #50dbbe0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/50dbbe0) - compression implementation correction add compression unit test
* [Revision #1915c88](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1915c88) - reusing chunk buffer to improve performance
* [Revision #ad212c0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ad212c0) - not throwing error after connection end, but command "error" event if no callback is set
* [Revision #192d8cd](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/192d8cd) - CI : giving root external access to permit testing TLS certificates
* [Revision #93d0409](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/93d0409) - CI : giving root external access to test ssl
* [Revision #829d481](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/829d481) - CI : giving root external access to test ssl
* [Revision #4c5c237](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4c5c237) - CI : testing correction part 4
* [Revision #4604148](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4604148) - CI : testing correction part 3
* [Revision #734be14](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/734be14) - CI : testing correction part 2
* [Revision #a1d6924](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a1d6924) - CI : testing correction
* [Revision #0d40ea6](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0d40ea6) - CI : logging default configuration - better logging
* [Revision #2348e82](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2348e82) - CI : logging default configuration
* [Revision #bdb34a5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bdb34a5) - ensuring altname verification en IPs
* [Revision #48c7c64](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/48c7c64) - appveyor using mariadb.example.com alias for hostname to permit SSL name verification
* [Revision #befa51f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/befa51f) - ensuring use of tlsSocket.getProtocol() only if node.version >= 5.7
* [Revision #7895aea](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7895aea) - correcting travis SSL tests - part 3
* [Revision #637dedd](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/637dedd) - correcting travis SSL tests - part 2
* [Revision #2e4ab7b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2e4ab7b) - correcting travis SSL tests
* [Revision #253d609](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/253d609) - improving socket error handling adding SSL tests
* [Revision #da394d6](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/da394d6) - ensure that packet buffer doesn't rely on socket chunk to avoid race operation
* [Revision #267d878](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/267d878) - TLs implementation
* [Revision #330176d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/330176d) - ensuring no race condition when reading IO packet
* [Revision #c9b45e9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c9b45e9) - small code correction
* [Revision #859e082](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/859e082) - deleting one buffer when reading packet
* [Revision #77219eb](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/77219eb) - benchmark removing pre-warmup compression correction
* [Revision #4afea73](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4afea73) - packet compression implementation packet sequence verification packet parsing correction skipping value connection options copying avoiding changing debug to all pool but by connection
* [Revision #b8c6f5b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b8c6f5b) - packet compression implementation packet sequence verification packet parsing correction skipping value connection options copying avoiding changing debug to all pool but by connection
* [Revision #e95a47f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e95a47f) - MySQL test detection correction
* [Revision #44771c5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/44771c5) - multi-packet result-set streaming correction
* [Revision #f5551ff](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f5551ff) - improving test error message
* [Revision #126cb3f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/126cb3f) - enable/disable option "debug" at runtime
* [Revision #1738762](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1738762) - better test error message
* [Revision #9862a9f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9862a9f) - adding benchmark test
* [Revision #4dae792](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4dae792) - changing timeout to ensure travis always finish big test
* [Revision #dd756c7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/dd756c7) - file reading compatibility for node.js < 6.3 avoid throwing error
* [Revision #9ea8fa0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9ea8fa0) - Local infile implementation
* [Revision #9ed0953](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9ed0953) - add error log message in case of erronous packet
* [Revision #c0559b2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c0559b2) - connection event handling improvement
* [Revision #355d027](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/355d027) - test improvement
* [Revision #71ad1a0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/71ad1a0) - improving readme
* [Revision #e970bfa](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e970bfa) - changing npm name to mariadb README status first
* [Revision #c534cd3](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c534cd3) - adding typecast documentation removing typecast boolean test that made no sense. If a typecast function is set, will cast type with function. if not a function, will use automatic casting to javascript type.
* [Revision #c604244](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c604244) - adding typecast option
* [Revision #c097399](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c097399) - adding placeholder documentation
* [Revision #e60291d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e60291d) - adding placeholder implementation
* [Revision #71a82f7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/71a82f7) - correction : doesn't throw error to command that are already finished
* [Revision #ad14637](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ad14637) - adding tests
* [Revision #bff0285](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bff0285) - adding tests connect callback run on next cycle
* [Revision #67f2c16](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/67f2c16) - adding tests
* [Revision #fdc2db9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fdc2db9) - permit using pipelining option at query level pipelining documentation
* [Revision #02967cf](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/02967cf) - not using process.nextTick but setImmediate to ensure that connector will give ticks to I/O before sending new commands better streaming test stability
* [Revision #178de52](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/178de52) - add streaming tests
* [Revision #aa3eb77](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/aa3eb77) - Add pipelining implementation
* [Revision #2a4cce3](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2a4cce3) - add tests for stored procedures
* [Revision #012feff](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/012feff) - add named pipe configuration for appveyor
* [Revision #4b9127a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4b9127a) - appveyor benchmarks default using named pipe on windows
* [Revision #1c954ac](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1c954ac) - removing appveyor comments
* [Revision #e908f25](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e908f25) - adding multi results test
* [Revision #92382ad](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/92382ad) - adding metadata test
* [Revision #e12fa99](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e12fa99) - correct missing import
* [Revision #3e7aa33](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/3e7aa33) - remove useless bitwise comparison
* [Revision #6a043ed](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6a043ed) - Benchmark improvement : - mariasql part of benchmark if available - benchmarks runs on appveyor Performance improvement : - suppress useless "if" - writer optimization method for utf8 parameter escaping - add connection.threadId compatibility to mysql
* gitrevn:/mysql2 correction - better number > 2^53 implementation
* [Revision #e67723d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e67723d) - benchmark: changing mariasql name results
* [Revision #74e4faa](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/74e4faa) - benchmark appveyor/travis using mariasql (informational only)
* [Revision #222fcf2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/222fcf2) - benchmark correction
* [Revision #db1b43f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/db1b43f) - Connection.ping() implementation
* [Revision #0cf3896](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0cf3896) - eslint code standardization travis bench use mariasql documentation correction
* [Revision #dda1ed3](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/dda1ed3) - remove unused conenction option. add connection option documentation. add few tests
* [Revision #fd1d66a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fd1d66a) - API compatibility: Connection.escape(value),Connection.escapeId(value), Connection.format(sql, values) still in Connection class, but throwing a better error message
* [Revision #9244d4f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9244d4f) - Avoid checking for current collation every time when writing String to socket. This is usually very rarely changed
* [Revision #f77d74a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f77d74a) - clarify connection private/public method and properties
* [Revision #27c57e4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/27c57e4) - Connection.commit/rollback implementation refactor
* [Revision #6d87a63](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6d87a63) - adding option when using localhost but docker to avoid testing named pipe / unix socket
* [Revision #087483a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/087483a) - handle Connection.connect() multiple call
* [Revision #cc56e3f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cc56e3f) - correcting benchmark to permit using named pipe and warming driver to have more accurate results. connection ending correction for named pipe + test
* [Revision #bebf8dc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bebf8dc) - correcting travis benchmark
* [Revision #989513e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/989513e) - improving README
* [Revision #a241550](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a241550) - improving README
* [Revision #2ee3b8e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2ee3b8e) - improving documentation
* [Revision #83bafc1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/83bafc1) - correct test
* [Revision #ba9fe17](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ba9fe17) - permit mocha skip
* [Revision #1a9910d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1a9910d) - adding new tests and associated correction
* [Revision #d6babac](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d6babac) - updating documentation - second part
* [Revision #0c4b5f4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0c4b5f4) - updating documentation - second part
* [Revision #c496fd2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c496fd2) - updating documentation
* [Revision #167dd03](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/167dd03) - changing documentation
* [Revision #aa6b855](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/aa6b855) - add new tests
* [Revision #89addc4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/89addc4) - correct appveyor testing
* [Revision #8a9c601](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8a9c601) - date test correction to ensure compatibility with MySQL 5.5 (doesn't permit datetime(6)) and MySQL 5.7 (no zero date)
* [Revision #8853ff4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8853ff4) - test correction to be compatible with 10.3
* [Revision #8480f35](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8480f35) - add supportBigNumbers / bigNumberStrings test
* [Revision #9994cee](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9994cee) - eslint file format correction
* [Revision #8c962b4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8c962b4) - add connection API implementation \* `beginTransaction(options, callback)`: begin transaction \* `commit(options, callback)`: commit current transaction \* `rollback(options, callback)`: rollback current transaction
* [Revision #1d283f4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1d283f4) - timeout test correction
* [Revision #4cceab5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4cceab5) - correcting CI links
* [Revision #abd30b4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/abd30b4) - add date/datetime test
* [Revision #ac346bc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ac346bc) - removing API Connection.escape, escapeId and format, not wanting client escaping
* [Revision #85fefe0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/85fefe0) - small column definition enhancement
* [Revision #4569aa0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4569aa0) - add Query API documentation
* [Revision #ba41b14](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ba41b14) - beginning documentation
* [Revision #15ccf84](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/15ccf84) - Removed hash.reset refernces from the code. Removed v8-profiler from dependencies. Un-checked package-lock.js file
* [Revision #7422984](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7422984) - first commit

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
