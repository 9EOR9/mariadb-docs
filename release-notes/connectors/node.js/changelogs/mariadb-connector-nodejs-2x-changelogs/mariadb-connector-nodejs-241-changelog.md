# Connector/Node.js 2.4.1 Changelog

{% include "../../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://mariadb.com/downloads/#connectors) | [Release Notes](../../mariadb-connector-nodejs-2x-release-notes/mariadb-connector-nodejs-241-release-notes.md) | [Changelog](mariadb-connector-nodejs-241-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide)

**Release date:** 2 Jul 2020

For the highlights of this release, see the [release notes](../../mariadb-connector-nodejs-2x-release-notes/mariadb-connector-nodejs-241-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-nodejs) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #38c49b1](https://github.com/mariadb-corporation/mariadb-connector-j/commit/38c49b1) Merge branch 'release/2.4.1'
* [Revision #f4e8ed5](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f4e8ed5) \[misc] set skysql test as allowed failure
* [Revision #f7a95b9](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f7a95b9) Bump 2.4.1
* [Revision #783f792](https://github.com/mariadb-corporation/mariadb-connector-j/commit/783f792) \[misc] test improvement for slow VM
* [Revision #6e569f8](https://github.com/mariadb-corporation/mariadb-connector-j/commit/6e569f8) \[misc] update appveyor testing latest release. removing deprecated 5.5 version
* [Revision #b2d7e2a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/b2d7e2a) Merge branch 'pull/118' into develop
* [Revision #4df6a96](https://github.com/mariadb-corporation/mariadb-connector-j/commit/4df6a96) \[misc] improve test reliability
* [Revision #5ac2db6](https://github.com/mariadb-corporation/mariadb-connector-j/commit/5ac2db6) \[[CONJS-139](https://jira.mariadb.org/browse/CONJS-139)] createConnection(string)\` does not support URL-encoded credentials #115
* [Revision #27f2070](https://github.com/mariadb-corporation/mariadb-connector-j/commit/27f2070) \[misc] test reliability improvement Docker use focal for [MariaDB 10.3](../../../../community-server/old-releases/release-notes-mariadb-10-3-series/what-is-mariadb-103.md) and 10.4, and default to support TLS1.2 minimum version. TLSv1 and TLSv1.1 test are changed to take c\
  ase of those changes.
* [Revision #1a08e78](https://github.com/mariadb-corporation/mariadb-connector-j/commit/1a08e78) \[misc] correcting test for server that don't support TLSv1.1 anymore
* [Revision #5f1341e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/5f1341e) \[[CONJS-138](https://jira.mariadb.org/browse/CONJS-138)] pool.getConnection() might not timeout even with acquireTimeout set #116 Pool option `acquireTimeout` ensure that pool.getConnection() throw an error if there\
  is no available connection after this timeout is reached.
* [Revision #8f32c88](https://github.com/mariadb-corporation/mariadb-connector-j/commit/8f32c88) \[misc] correcting ssl test for TLSv1 and [mariadb 10.3](../../../../community-server/old-releases/release-notes-mariadb-10-3-series/what-is-mariadb-103.md)+
* [Revision #e78a5ad](https://github.com/mariadb-corporation/mariadb-connector-j/commit/e78a5ad) \[misc] correcting SSL test
* [Revision #b23caeb](https://github.com/mariadb-corporation/mariadb-connector-j/commit/b23caeb) \[[CONJS-141](https://jira.mariadb.org/browse/CONJS-141)] set default value of option `restoreNodeTimeout` to 1000.
* [Revision #7629e49](https://github.com/mariadb-corporation/mariadb-connector-j/commit/7629e49) \[[CONJS-140](https://jira.mariadb.org/browse/CONJS-140)] eslint correction
* [Revision #0c70e88](https://github.com/mariadb-corporation/mariadb-connector-j/commit/0c70e88) Support passing null values in array when doing queries
* [Revision #7291295](https://github.com/mariadb-corporation/mariadb-connector-j/commit/7291295) \[[CONJS-137](https://jira.mariadb.org/browse/CONJS-137)] fix unstable resultset state when having 'duplicate field name' error #113
* [Revision #cda6634](https://github.com/mariadb-corporation/mariadb-connector-j/commit/cda6634) \[misc] node.js 14 test skipping not compatible node-gyp
* [Revision #ae75e2c](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ae75e2c) \[misc] node.js 14 test addition
* [Revision #fdc486d](https://github.com/mariadb-corporation/mariadb-connector-j/commit/fdc486d) \[misc] changelog update
* [Revision #e4faf11](https://github.com/mariadb-corporation/mariadb-connector-j/commit/e4faf11) Merge tag '2.4.0' into develop

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
