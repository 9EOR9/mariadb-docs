# MariaDB Connector/Node.js 3.3.1 Changelog

{% include "../../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://mariadb.com/downloads/#connectors) | [Release Notes](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-3-1-release-notes.md) | [Changelog](mariadb-connector-node-js-3-3-1-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide)

**Release date:** 5 Jun 2024

For the highlights of this release, see the[release notes](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-3-1-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-nodejs) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #26e1521](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/26e1521) \[misc] code style correction
* [Revision #007bfe0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/007bfe0) bump 3.3.1
* [Revision #e799888](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e799888) \[[CONJS-293](https://jira.mariadb.org/browse/CONJS-293)] batch with javascript date parameter not in TIMESTAMP range are saved as null #287
* [Revision #f6b9a18](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f6b9a18) \[misc] avoid useless variables
* [Revision #a63d795](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a63d795) \[misc] sending text parameter fast path, avoiding testing typeof value each time
* [Revision #39841b7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/39841b7) \[misc] replace math.floor by \~ when possible for better performance
* [Revision #40eec18](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/40eec18) \[misc] avoid static use
* [Revision #9aa3e13](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9aa3e13) \[misc] JSON parameter correction
* [Revision #35ce2dc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/35ce2dc) \[misc] command function now use JSON parameter
* [Revision #8d558c9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8d558c9) \[[CONJS-292](https://jira.mariadb.org/browse/CONJS-292)] ensure String object parameter
* [Revision #b2f592b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b2f592b) \[misc] avoid unnecessary condition verification
* [Revision #b66a383](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b66a383) \[misc] ensure possible future multi-catalog use
* [Revision #15198b9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/15198b9) \[misc] execute performance improvement when lots of parameters And some micro improvement: Object.prototype.toString '\[object Date]' for testing Date in place of costly instanceof
* [Revision #5de51bf](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5de51bf) \[misc] micro perf change on number to string
* [Revision #11868e2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/11868e2) \[misc] minor perf change
* [Revision #c09e77f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c09e77f) \[[CONJS-291](https://jira.mariadb.org/browse/CONJS-291)] performance reading column definition packet improvement
* [Revision #15d6676](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/15d6676) \[misc] binary number type faster check
* [Revision #a40a94b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a40a94b) \[misc] test correction for supporting MySQL 8.4
* [Revision #50aa5e3](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/50aa5e3) \[misc] ensure redirect empty value
* [Revision #9d3e35e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9d3e35e) \[misc] add node.js 22 to test suite
* [Revision #343c469](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/343c469) \[misc] adding pool toString() function
* [Revision #0167c18](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0167c18) \[[CONJS-290](https://jira.mariadb.org/browse/CONJS-290)] possible ECONRESET when executing batch #281
* [Revision #cef85db](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cef85db) \[[CONJS-289](https://jira.mariadb.org/browse/CONJS-289)] connection possibly staying in hanging state after batch execution #281
* [Revision #7eba249](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7eba249) \[misc] cleaning up test code, removing xpand and skysql code
* [Revision #5be0f20](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5be0f20) \[misc] ensure test stability
* [Revision #0f50b62](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0f50b62) \[misc] test addition
* [Revision #75d97f9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/75d97f9) \[[CONJS-288](https://jira.mariadb.org/browse/CONJS-288)] ensure pool timeout error give details #268
* [Revision #2cbeb34](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2cbeb34) \[misc] avoid double-negative variable use correction
* [Revision #a2ce0fb](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a2ce0fb) Merge branch 'master' into develop
* [Revision #d0913b4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d0913b4) Add missing QueryOptions type to prepare function
* [Revision #3e589c7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/3e589c7) \[misc] avoid double-negative variable use
* [Revision #78dfc92](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/78dfc92) \[misc] fix closing of prepared statements
* [Revision #2442249](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2442249) \[misc] check prepare cache is enabled before resetting it
* [Revision #b65aca1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b65aca1) \[misc] changelog update

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
