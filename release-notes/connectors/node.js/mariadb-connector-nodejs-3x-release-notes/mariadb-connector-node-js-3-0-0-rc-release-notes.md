# MariaDB Connector/Node.js 3.0.0-rc Release Notes

{% include "../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://mariadb.com/downloads/#connectors) | [Release Notes](mariadb-connector-node-js-3-0-0-rc-release-notes.md) | [Changelog](../changelogs/mariadb-connector-nodejs-3x-changelogs/mariadb-connector-nodejs-300-rc-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide)

**Release date:** 20 Oct 2021

MariaDB Connector/Node.js 3.0.0-rc is an [_**RC**_](../../../mariadb-release-criteria.md) release.

**Do not use non-stable (non-GA) releases in production!**

{% hint style="success" %}
**For an overview of MariaDB Connector/Node.js see the** [**About MariaDB Connector/Node.js**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide) **page**
{% endhint %}

see [3.0.0-beta](mariadb-connector-node-js-3-0-0-beta-release-notes.md) for 3.0.0 content from previous version.

## Notable Changes

### Streaming resultset now respect backpressure

Before 3.0, implementation ensure connection state, at the cost of not handling backpressure well.

Streaming a resultset ensured the connection state before version 3.0, at the cost of not handling backpressure well.\
Since the goal of queryStream is to avoid the use of a large amount of memory, handling of backpressure has been optimized. If data handling takes some amount of time, the socket is paused to avoid the node socket buffer growing indefinitely.\
This has an impact on the use of function stream.pipeline as queryStream now needs to be closed explicitly to ensure that a connection is not in a wrong state ( unhandled rows in the socket buffer). Example

```js
const queryStream = connection.queryStream("SELECT * FROM mysql.user");
stream.pipeline(queryStream, transformStream, someWriterStream, (err) => { queryStream.close(); });
```

### Better options default setting

pool cluster option _removeNodeErrorCount_ now default to infinity. This avoids having pool removed from cluster when a server temporarily fails.

pool option _resetAfterUse_ now default to false. This permit avoids executing a command each time a connection is returned to pool.

### Optimized defaults

\[[CONJS-176](https://jira.mariadb.org/browse/CONJS-176)],\[[CONJS-179](https://jira.mariadb.org/browse/CONJS-179)]

* The pool cluster option removeNodeErrorCount now defaults to infinity. This avoids that some pool is removed from the cluster when a server temporarily fails.
* The pool option resetAfterUse now defaults to false. This avoids the execution of a COM\_RESET each time a connection is returned to the pool.

### New 'stream' option

| Option | Description                                                        | Type     | default |
| ------ | ------------------------------------------------------------------ | -------- | ------- |
| stream | permits to set a function with parameter to set stream (since 3.0) | function |         |

The option `stream` provides a way to execute a function with a callback parameter before each connection stream creation.

This can permit setting a SSH Tunnel for example:

```js
const mariadb = require('mariadb');
const tunnel = require('tunnel-ssh');
const fs = require('fs');

const conn = await mariadb.createConnection({
        user: 'dbuser',
        password: 'dbpwd',
        port: 27000,
        stream: (cb) => 
          tunnel(
            {
              // remote connection ssh info
              username: 'sshuser',
              host: '157.230.123.7',
              port: 22,
              privateKey: fs.readFileSync('./key.ppk'),
              // database (here on ssh server)
              dstHost: '127.0.0.1',
              dstPort: 3306,
              // local interface
              localHost: '127.0.0.1',
              localPort: 27000
            },
            cb
          )
      });
```

### Various corrections

* \[[CONJS-125](https://jira.mariadb.org/browse/CONJS-125)] Batch operations now support the returning clause (example command like `insert into XXX values (?,?,?) returning id`)
* \[[CONJS-125](https://jira.mariadb.org/browse/CONJS-125)] permit using batch with returning clause
* \[[CONJS-170](https://jira.mariadb.org/browse/CONJS-170)] Pool.query(undefined) never release connection
* \[[CONJS-173](https://jira.mariadb.org/browse/CONJS-173)] not permitting providing null as a value without an array
* \[[CONJS-178](https://jira.mariadb.org/browse/CONJS-178)] Update code to recent Ecma version
* \[[CONJS-172](https://jira.mariadb.org/browse/CONJS-172)] performance improvement for multi-line result-set

## Changelog

For a complete list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-nodejs-3x-changelogs/mariadb-connector-nodejs-300-rc-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
