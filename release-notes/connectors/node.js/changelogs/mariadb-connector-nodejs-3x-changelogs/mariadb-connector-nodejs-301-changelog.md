# MariaDB Connector/Node.js 3.0.1 Changelog

The most recent [_**Stable (GA)**_](../../../../mariadb-release-criteria.md) release of [MariaDB Connector/Node.js](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-nodejs/README.md) is:[**MariaDB Connector/Node.js 3.4.2**](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-4-2-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-0-1-release-notes.md)[Changelog](mariadb-connector-nodejs-301-changelog.md)[Connector/Node.js Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-nodejs/README.md)

**Release date:** 26 Jul 2022

For the highlights of this release, see the[release notes](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-0-1-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-nodejs) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #59da962](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/59da962) - \[misc] improving changelog for 3.0.1 release
* [Revision #66dc988](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/66dc988) - \[misc] updating changelog for 3.0.1 release
* [Revision #74240e8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/74240e8) - \[misc] test suite correction for CS build version
* [Revision #ebb3fef](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ebb3fef) - \[[CONJS-199](https://jira.mariadb.org/browse/CONJS-199)] return type for batch() is wrong on typescript
* [Revision #048fd65](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/048fd65) - \[misc] adding initial SQL command 'SET NAMES UTF8' for xpand until [XPT-266](https://jira.mariadb.org/browse/XPT-266) correction
* [Revision #5035639](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5035639) - \[misc] travis test adding suite
* [Revision #bb0ad25](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bb0ad25) - \[misc] adding MariaDB enterprise 10.4/10.5 to travis test suite
* [Revision #7710871](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7710871) - \[misc] correct travis benchmark run
* [Revision #74fc5ea](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/74fc5ea) - \[[CONJS-210](https://jira.mariadb.org/browse/CONJS-210)] benchmark result update with recent driver version
* [Revision #5b52edc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5b52edc) - \[misc] readme update
* [Revision #2d80d1c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2d80d1c) - \[[CONJS-210](https://jira.mariadb.org/browse/CONJS-210)] benchmarks simplification
* [Revision #e49ed58](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e49ed58) - \[misc] test improvement
* [Revision #de792a0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/de792a0) - \[misc] test correction after commit 4232e617b325d23b0cd571434ee9987a398aeb82
* [Revision #f6c0ace](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f6c0ace) - \[[CONJS-210](https://jira.mariadb.org/browse/CONJS-210)] metadata parsing improvement
* [Revision #3b8551b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/3b8551b) - \[[CONJS-210](https://jira.mariadb.org/browse/CONJS-210)] initializing smaller buffer streaming sending buffer, in order to maximize use of node buffer pool
* [Revision #4232e61](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4232e61) - \[[CONJS-210](https://jira.mariadb.org/browse/CONJS-210)] avoiding buffer copy when receiving data when packet is contained in socket data
* [Revision #f7982dc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f7982dc) - \[[CONJS-210](https://jira.mariadb.org/browse/CONJS-210)] multi-rows result-set performance improvement
* [Revision #a386038](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a386038) - \[misc] benchmark improvement - real pipelining test
* [Revision #a55ce22](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a55ce22) - \[misc] benchmark improvement
* [Revision #86c29ec](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/86c29ec) - \[[CONJS-210](https://jira.mariadb.org/browse/CONJS-210)] small performance improvement
* [Revision #723fe8e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/723fe8e) - \[misc] connection correction after #a862d8dbf7d9727d34fe4bb4f75f0846102d6ea3
* [Revision #ec3924c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ec3924c) - \[[CONJS-196](https://jira.mariadb.org/browse/CONJS-196)] 3.0 regression on release connection #195
* [Revision #709da77](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/709da77) - \[[CONJS-209](https://jira.mariadb.org/browse/CONJS-209)] permitting Batch with trace when BULK is not supported
* [Revision #a862d8d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a862d8d) - \[[CONJS-209](https://jira.mariadb.org/browse/CONJS-209)] trace option complete implementation
* [Revision #cfba137](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cfba137) - \[misc] correct README image links
* [Revision #f5c156f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f5c156f) - \[misc] test proxy suspending remote correction
* [Revision #e6a1a00](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e6a1a00) - \[misc] test proxy correction
* [Revision #c83cda5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c83cda5) - \[misc] test proxy improvement
* [Revision #f0e000d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f0e000d) - \[misc] adding 10.8 and 10.9 build testing
* [Revision #c147401](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c147401) - \[misc] pool ending, ensuring connection creation are ended correctly
* [Revision #a484ccf](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a484ccf) - \[misc] various micro enhancement \* pool: connection validation check isValid, correcting cases when a connection wasn't valid returning no response. \* cluster: ensure that when option `canRetry` is enable to not loop eternally if pool doesn't have connection anymore cluster end promise really returns Promise when pools are closed \* add test for cluster with one node only / or one node working only
* [Revision #2e53eaf](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2e53eaf) - \[[CONJS-208](https://jira.mariadb.org/browse/CONJS-208)] better pool error identification when leakDetectionTimeout is set
* [Revision #16e8bb8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/16e8bb8) - \[[CONJS-208](https://jira.mariadb.org/browse/CONJS-208)] better pool error identification
* [Revision #b484d42](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b484d42) - \[misc] ensure pool connection is released only once
* [Revision #dcb02e0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/dcb02e0) - \[misc] code coverage addition
* [Revision #89f0af4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/89f0af4) - \[misc] code coverage addition
* [Revision #ea7c195](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ea7c195) - \[[CONJS-206](https://jira.mariadb.org/browse/CONJS-206)] possible race condition on connection destroy when no other connection can be created
* [Revision #deece07](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/deece07) - \[misc] test addition to ensure SSL when required will throw an error if server does not support SSL
* [Revision #8b165b3](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8b165b3) - \[misc] test addition to ensure SSL when required will throw an error if server does not support SSL
* [Revision #d06f1f4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d06f1f4) - \[misc] remove forcing error on connection creation, server will throw error when expected.
* [Revision #b87af1a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b87af1a) - \[misc] code coverage addition
* [Revision #2b1b2e5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2b1b2e5) - \[[CONJS-205](https://jira.mariadb.org/browse/CONJS-205)] query hanging when using batch with option timeout in place of error thrown
* [Revision #72d2681](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/72d2681) - \[[CONJS-204](https://jira.mariadb.org/browse/CONJS-204)] handle password array with server pam\_use\_cleartext\_plugin
* [Revision #8cc784f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8cc784f) - \[[CONJS-203](https://jira.mariadb.org/browse/CONJS-203)] encoding error when using changeUser with connection attributes
* [Revision #8d3c0e9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8d3c0e9) - \[misc] adding test coverage
* [Revision #aef9a70](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/aef9a70) - \[[CONJS-202](https://jira.mariadb.org/browse/CONJS-202)] better support for pre-4.1 error message format
* [Revision #2eb3cfb](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2eb3cfb) - \[misc] test correction
* [Revision #7feb8c5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7feb8c5) - \[[CONJS-201](https://jira.mariadb.org/browse/CONJS-201)] typecast geometry parsing error
* [Revision #e11b1d6](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e11b1d6) - \[misc] add test coverage
* [Revision #59090b6](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/59090b6) - \[misc] removing 10.2 EOL from travis
* [Revision #2294360](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2294360) - \[misc] travis testing correction for node.js 18
* [Revision #6f0aa6f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6f0aa6f) - \[misc] changing travis test for node.js 18 to focal
* [Revision #6a4e879](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6a4e879) - \[[CONJS-198](https://jira.mariadb.org/browse/CONJS-198)] new option addition `checkNumberRange` to works with insertIdAsNumber/decimalAsNumber/bigIntAsNumber #201
* [Revision #268111d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/268111d) - \[[CONJS-200](https://jira.mariadb.org/browse/CONJS-200)] Improve pool connection error messaging
* [Revision #6117b64](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6117b64) - Merge branch 'master' into develop
* [Revision #94be5e8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/94be5e8) - \[misc] small performance enhancement to handle active connection counter
* [Revision #fe9b2a8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fe9b2a8) - \[[CONJS-197](https://jira.mariadb.org/browse/CONJS-197)] node.js 18 testing
* [Revision #c95657e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c95657e) - misc code style correction
* [Revision #4a9138c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4a9138c) - reporting leak message change #190
* [Revision #23041b8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/23041b8) - Merge branch 'maintenance/2.x' into develop
* [Revision #5ea70aa](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5ea70aa) - \[[CONJS-195](https://jira.mariadb.org/browse/CONJS-195)] add test case to avoid regression #196
* [Revision #49b91f9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/49b91f9) - fix "cannot mix BigInt and other types" error
* [Revision #787a0f9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/787a0f9) - \[[CONJS-194](https://jira.mariadb.org/browse/CONJS-194)] Charset change using parameterized query fails with "Uncaught TypeError: opts.emit is not a function"
* [Revision #7281586](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7281586) - bump 3.0.1 version
* [Revision #5121d6c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5121d6c) - \[[CONJS-193](https://jira.mariadb.org/browse/CONJS-193)] wrong error returned "Cannot read properties of undefined (reading 'charset')" when wrong handshake
* [Revision #e20e08b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e20e08b) - correct documentation link
* [Revision #2ae57a9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2ae57a9) - \[[CONJS-192](https://jira.mariadb.org/browse/CONJS-192)] support xpand \* handle TIMESTAMP type for xpand \* support binary xpand 0000-00-00 00:00:00 values \* Timestamp microsecond handling when using binary protocol
* [Revision #f204d9b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f204d9b) - docs: apply new default connectione timeout
* [Revision #64ca753](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/64ca753) - \[misc] improving test reliability
* [Revision #e11fa90](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e11fa90) - Merge branch 'master' into develop
* [Revision #a2db33c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a2db33c) - \[misc] remove old node.js compatibility
* [Revision #4ae8c0d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4ae8c0d) - Merge tag '3.0.0-main' into develop
* [Revision #b9d008a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b9d008a) - Merge branch 'release/3.0.0-main'
* [Revision #42cafe5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/42cafe5) - Update pool-base.js
* [Revision #6e78dde](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6e78dde) - Update pool-base.js

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
