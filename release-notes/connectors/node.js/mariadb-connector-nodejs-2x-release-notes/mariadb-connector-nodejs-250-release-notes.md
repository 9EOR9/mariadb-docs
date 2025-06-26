# MariaDB Connector/Node.js 2.5.0 Release Notes

The most recent [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release of [MariaDB Connector/Node.js](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-nodejs/README.md) is:[**MariaDB Connector/Node.js 3.4.2**](../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-4-2-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](mariadb-connector-nodejs-250-release-notes.md)[Changelog](../changelogs/mariadb-connector-nodejs-2x-changelogs/mariadb-connector-nodejs-250-changelog.md)[Connector/Node.js Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-nodejs/README.md)

**Release date:** 19 Oct 2020

MariaDB Connector/Node.js 2.5.0 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

**For an overview of MariaDB Connector/Node.js see the**[**About MariaDB Connector/Node.js**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connectornodejs/README.md) **page**

## Notable Changes

* [CONJS-148](https://jira.mariadb.org/browse/CONJS-148) - permit setting socket keep alive (option `keepAliveDelay`)
* [CONJS-143](https://jira.mariadb.org/browse/CONJS-143) - Array parameter escaping differ from mysql/mysql2
* [CONJS-133](https://jira.mariadb.org/browse/CONJS-133) - Support ES2020 BigInt object (option `supportBigInt`)
* [CONJS-77](https://jira.mariadb.org/browse/CONJS-77) - Support MySQL caching\_sha256\_password authentication
* [CONJS-76](https://jira.mariadb.org/browse/CONJS-76) - Support MySQL sha256\_password authentication

New Options

| option                  | description                                                                                                                                                                                                                                                                                                                                                                                                                                                 | type      | default |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------- |
| option                  | description                                                                                                                                                                                                                                                                                                                                                                                                                                                 | type      | default |
| arrayParenthesis        | Indicate if array are included in parenthesis. This option permit compatibility with version < 2.5                                                                                                                                                                                                                                                                                                                                                          | _boolean_ | false   |
| rsaPublicKey            | Indicate path/content to MySQL server RSA public key. use requires Node.js v11.6+                                                                                                                                                                                                                                                                                                                                                                           | _string_  |         |
| cachingRsaPublicKey     | Indicate path/content to MySQL server caching RSA public key. use requires Node.js v11.6+                                                                                                                                                                                                                                                                                                                                                                   | _string_  |         |
| allowPublicKeyRetrieval | Indicate that if `rsaPublicKey` or `cachingRsaPublicKey` public key are not provided, if client can ask server to send public key.                                                                                                                                                                                                                                                                                                                          | _boolean_ | false   |
| supportBigInt           | Whether resultset should return javascript ES2020 [BigInt](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt) for [BIGINT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/numeric-data-types/bigint) data type. This ensures having expected value even for value > 2^53 (see [safe](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/node-js-connection-options) range). | _boolean_ | false   |
| keepAliveDelay          | permit to enable socket keep alive, setting delay. 0 means not enabled. Keep in mind that this don't reset server [@@wait\_timeout](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/ha-and-performance/optimization-and-tuning/system-variables/server-system-variables) (use pool option idleTimeout for that). in ms                                                                                                                                       | _int_     |         |

[CONJS-143](https://jira.mariadb.org/browse/CONJS-143) is a breaking change. Queries that have a IN parameter with array parameters format change.\
previous format did not accept parenthesis :

```js
conn.query('SELECT * FROM arrayParam WHERE id = ? AND val IN ?', [1, ['b', 'c']]);
```

now, format is

```js
conn.query('SELECT * FROM arrayParam WHERE id = ? AND val IN (?)', [1, ['b', 'c']]);
```

same than mysql/mysql2 drivers.\
previous behaviour can be reverted setting option `arrayParenthesis` to true.

## Bugs Fixed

* [CONJS-145](https://jira.mariadb.org/browse/CONJS-145) - batch rewrite error when packet reach maxAllowedPacket
* [CONJS-146](https://jira.mariadb.org/browse/CONJS-146) - Using callback API, batch, avoid return error if connection not established
* [CONJS-144](https://jira.mariadb.org/browse/CONJS-144) - TypeScript type ssl wrong definitions

## Changelog

For a complete list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-nodejs-2x-changelogs/mariadb-connector-nodejs-250-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
