# MariaDB Connector/Node.js 3.4.1 Changelog

{% include "../../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/nodejs-connector) | [Release Notes](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-4-1-release-notes.md) | [Changelog](mariadb-connector-node-js-3-4-1-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide)

**Release date:** 2 Apr 2025

For the highlights of this release, see the [release notes](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-4-1-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-nodejs) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #a752a1e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a752a1e) bump 3.4.1 version
* [Revision #2e63f76](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2e63f76) \[misc] pool throwing first error of connection/reconnection loop, to avoid having minimal timeout of last try
* [Revision #01cd640](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/01cd640) \[[CONJS-306](https://jira.mariadb.org/browse/CONJS-306)] parsec hash correction for "zero configuration ssl"
* [Revision #02876ed](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/02876ed) \[misc] batch result correct behavior when not using bulk compare to using bulk
* [Revision #4e9d2f1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4e9d2f1) \[misc] test stability improvement when testing with mysql
* [Revision #cc996d0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cc996d0) \[misc] pool error ensuring to have cause when possible
* [Revision #3d39742](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/3d39742) \[misc] maxAllowedPacket test correction
* [Revision #52b3035](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/52b3035) \[misc] documenting batch `fullResult` option
* [Revision #6d3e94f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6d3e94f) \[misc] correcting default testing port value
* [Revision #70ecc93](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/70ecc93) \[misc] class small factorization and documentation
* [Revision #d5d4c02](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d5d4c02) \[misc] removing debug info logging in tests
* [Revision #9f06bc5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9f06bc5) \[misc] ensuring data type corresponds to expected type
* [Revision #8a2c47e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8a2c47e) \[misc] only set setKeepAlive with keepAliveInitialDelay when socket handle has already been set
* [Revision #627f1d2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/627f1d2) \[misc] documentation improvement (examples addition)
* [Revision #2bf5248](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2bf5248) \[misc] improve test proxy error detection
* [Revision #6657f2d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6657f2d) \[misc] correct max\_allowed\_packet test
* [Revision #c20bf8c](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c20bf8c) \[misc] ensuring socketTimeout / queryTimeout value
* [Revision #9934244](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9934244) \[misc] batch test correction
* [Revision #a898cf5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a898cf5) \[[CONJS-316](https://jira.mariadb.org/browse/CONJS-316)] avoid batch OOM when pipelining by processing items by batches of 1000.
* [Revision #5570307](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5570307) \[misc] pool testing correction
* [Revision #d21726e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d21726e) \[misc] refactoring to simplify classes
* [Revision #d8835d6](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d8835d6) \[misc] test addition: creating pool from connection string
* [Revision #d24394d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/d24394d) \[[CONJS-275](https://jira.mariadb.org/browse/CONJS-275)] ensure compatibility with server not supporting detailed
* [Revision #46b36df](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/46b36df) \[misc] ensure pool connection to be listed in active connection even during connection validation
* [Revision #f5c5f78](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f5c5f78) \[[CONJS-275](https://jira.mariadb.org/browse/CONJS-275)] ensure having error detail when test fails
* [Revision #e03c076](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e03c076) \[[CONJS-275](https://jira.mariadb.org/browse/CONJS-275)] permit returning all Bulk insert id's
* [Revision #64ef6f8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/64ef6f8) \[misc] documentation improvement
* [Revision #7a71296](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7a71296) \[[CONJS-314](https://jira.mariadb.org/browse/CONJS-314)] ensure respecting max\_allowed\_packet parameter
* [Revision #c168f5f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/c168f5f) \[[CONJS-306](https://jira.mariadb.org/browse/CONJS-306)] Support "zero configuration ssl" for parsec authentication
* [Revision #76a6a64](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/76a6a64) \[[CONJS-314](https://jira.mariadb.org/browse/CONJS-314)] Bulk might return unexpected error "Cannot read properties of undefined (reading '0')" #299
* [Revision #46b8c6a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/46b8c6a) \[[CONJS-312](https://jira.mariadb.org/browse/CONJS-312)] ensure pool health validation won't throw any error when pool has still not connection
* [Revision #253bc02](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/253bc02) \[[CONJS-315](https://jira.mariadb.org/browse/CONJS-315)] test addition
* [Revision #f550eba](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/f550eba) \[[CONJS-315](https://jira.mariadb.org/browse/CONJS-315)] wrong data for result-set row of exactly 16M of data
* [Revision #40a15c8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/40a15c8) \[misc] pool default create size corresponding to expected pool size
* [Revision #793400e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/793400e) \[[CONJS-305](https://jira.mariadb.org/browse/CONJS-305)] Connection close alias for end function not in typescript definition #300
* [Revision #8942a99](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8942a99) \[[CONJS-313](https://jira.mariadb.org/browse/CONJS-313)] permit using question mark along with
* [Revision #bc1b82f](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bc1b82f) \[misc] documentation improvement
* [Revision #ddec028](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ddec028) \[[CONJS-313](https://jira.mariadb.org/browse/CONJS-313)] permit using question mark parameters even when using namedPlaceholders option - mysql2 compatibility #306
* [Revision #0e3508a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0e3508a) \[[CONJS-312](https://jira.mariadb.org/browse/CONJS-312)] pool error message improvement when failing to create connection
* [Revision #9b4bfaa](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9b4bfaa) Merge branch 'master' into develop
* [Revision #ad99ea8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ad99ea8) Check MaxScale version
* [Revision #df29974](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/df29974) \[misc] removal of glibc-source in travis testing
* [Revision #cb87169](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cb87169) \[misc] removal of glibc-source in travis testing
* [Revision #38103eb](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/38103eb) \[misc] Skip ephemeral cert tests older MaxScale versions correction
* [Revision #b111946](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/b111946) Skip ephemeral cert tests older MaxScale versions
* [Revision #e2b42e0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e2b42e0) Update MaxScale versions
* [Revision #ca34b2d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ca34b2d) \[misc] Skip ephemeral cert tests older MaxScale versions correction
* [Revision #e237adf](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e237adf) Skip ephemeral cert tests older MaxScale versions
* [Revision #017837d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/017837d) Update MaxScale versions
* [Revision #5b4eae7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/5b4eae7) \[misc] bulk ending with "Got a packet bigger than 'max\_allowed\_packet' bytes" error #297
* [Revision #4f9be98](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4f9be98) \[misc] changing capability name EXTENDED\_TYPE\_INFO to EXTENDED\_METADATA, in order to correspond to server and other connectors

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
