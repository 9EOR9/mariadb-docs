# MariaDB Connector/Node.js 3.3.0 Changelog

The most recent [_**Stable (GA)**_](../../../../mariadb-release-criteria.md) release of [MariaDB Connector/Node.js](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-nodejs/README.md) is:[**MariaDB Connector/Node.js 3.4.2**](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-4-2-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-3-0-release-notes.md)[Changelog](mariadb-connector-node-js-3-3-0-changelog.md)[Connector/Node.js Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-nodejs/README.md)

**Release date:** 21 Mar 2024

For the highlights of this release, see the[release notes](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-3-0-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-nodejs) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #b65aca1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b65aca1) - \[misc] changelog update
* [Revision #7ec5d09](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7ec5d09) - Merge branch 'master' into develop
* [Revision #8f88f9d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8f88f9d) - \[[CONJS-285](https://jira.mariadb.org/browse/CONJS-285)] DECIMAL field wrong decoding with deprecated option 'supportBigNumbers' set
* [Revision #0b8da71](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0b8da71) - \[misc] improving test for better stability
* [Revision #f1c0e1f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f1c0e1f) - \[misc] updating CHANGELOG missing correction
* [Revision #f4452f7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f4452f7) - \[misc] avoid possible redirection loop
* [Revision #deca8e1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/deca8e1) - \[misc] add contribution list
* [Revision #df973cd](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/df973cd) - \[misc] pool test correction
* [Revision #c8292b4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c8292b4) - \[misc] pool initializationTimeout default to acquireTimeout in order to have connector error cause to be logged
* [Revision #49f69f5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/49f69f5) - \[misc] updating node.js minimum version to 14, since lru-cache dependencies required node.js 14
* [Revision #343244c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/343244c) - \[[CONJS-284](https://jira.mariadb.org/browse/CONJS-284)] pipelining PREPARE EXECUTE correction
* [Revision #5e73d82](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5e73d82) - \[misc] update README
* [Revision #c0c1301](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c0c1301) - Merge branch 'develop'
* [Revision #11f502f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/11f502f) - \[misc] function correct naming
* [Revision #ddd55b4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ddd55b4) - \[misc] stack trace not always return complete stack when using `trace` option
* [Revision #90b5cf3](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/90b5cf3) - \[misc] test suite stability improvement
* [Revision #7569425](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7569425) - \[misc] various small corrections
* [Revision #623a9ab](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/623a9ab) - \[misc] adding coverage test - PAM plugin with ssl
* [Revision #73986cb](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/73986cb) - \[misc] test correction
* [Revision #9e7b53f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9e7b53f) - \[[CONJS-282](https://jira.mariadb.org/browse/CONJS-282)] ensure testing PAM with clear\_password\_auth
* [Revision #50e843c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/50e843c) - \[[CONJS-284](https://jira.mariadb.org/browse/CONJS-284)] pipeline PREPARE and EXECUTE
* [Revision #92e5c8e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/92e5c8e) - \[misc] using static parameter encoder
* [Revision #ec2cbf4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ec2cbf4) - \[misc] redirection test correction
* [Revision #e7a7e28](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e7a7e28) - \[[CONJS-283](https://jira.mariadb.org/browse/CONJS-283)] adding test case for wrong decoding of binary unsigned MEDIUMINT
* [Revision #5bba4a7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5bba4a7) - Merge branch 'patch-1' into develop
* [Revision #73ce9e8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/73ce9e8) - Fix decoding unsigned MEDIUMINT in binary decoder
* [Revision #6928a0e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6928a0e) - Merge branch 'master' into develop
* [Revision #6133c28](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6133c28) - Merge pull request #276
* [Revision #adeacf2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/adeacf2) - \[[CONJS-281](https://jira.mariadb.org/browse/CONJS-281)] cannot connect to 11.3+ server with character-set-collations = utf8mb4=uca1400\_ai\_ci
* [Revision #21f6d99](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/21f6d99) - Fix issue with mysql\_clear\_password
* [Revision #3335d7b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/3335d7b) - \[[CONJS-279](https://jira.mariadb.org/browse/CONJS-279)] faster datetime text encoding
* [Revision #fd7e6e6](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fd7e6e6) - \[[CONJS-279](https://jira.mariadb.org/browse/CONJS-279)] method parser faster search
* [Revision #c300740](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c300740) - \[misc] ensure test stability
* [Revision #a587a35](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a587a35) - \[misc] redirection test correction
* [Revision #fd1bbed](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fd1bbed) - \[misc] parsing performance improvement - part 2
* [Revision #9e8134f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9e8134f) - \[misc] parsing performance improvement
* [Revision #fa1a067](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fa1a067) - \[misc] ssl test correction
* [Revision #bab0283](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bab0283) - \[misc] correct ssl test
* [Revision #722b73b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/722b73b) - bump dependencies
* [Revision #7a77b16](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7a77b16) - \[misc] update copyright
* [Revision #c03fc52](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c03fc52) - \[[CONJS-278](https://jira.mariadb.org/browse/CONJS-278)] buffer overwrite correction
* [Revision #9b3346c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9b3346c) - \[[CONJS-278](https://jira.mariadb.org/browse/CONJS-278)] multiple part query (query bigger than 16M) wrongly reuse send buffer #274
* [Revision #df707b3](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/df707b3) - \[misc] code style correction
* [Revision #c236940](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c236940) - Merge branch 'master' into develop
* [Revision #2cbef9a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2cbef9a) - \[[CONJS-264](https://jira.mariadb.org/browse/CONJS-264)] TLS ephemeral certificate automatic implementation
* [Revision #977bd57](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/977bd57) - prepare for 3.3.0
* [Revision #289aff7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/289aff7) - \[misc] improving test stability
* [Revision #0e8e8ad](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0e8e8ad) - \[misc] correcting test for maxscale
* [Revision #714f302](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/714f302) - Merge branch 'develop'
* [Revision #01fabc6](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/01fabc6) - \[misc] adding maxscale redirection test
* [Revision #e8348cc](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e8348cc) - \[misc] corrected test with hardcoded database
* [Revision #9bbd12e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9bbd12e) - \[[CONJS-277](https://jira.mariadb.org/browse/CONJS-277)] using connection.importFile when connection is not connected to database result in error #266

{% @marketo/form formid="4316" formId="4316" %}
