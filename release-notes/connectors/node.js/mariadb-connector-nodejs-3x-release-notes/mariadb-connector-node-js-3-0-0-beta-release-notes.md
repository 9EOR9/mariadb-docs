# MariaDB Connector/Node.js 3.0.0-beta Release Notes

{% include "../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://mariadb.com/downloads/#connectors) | [Release Notes](mariadb-connector-node-js-3-0-0-beta-release-notes.md) | [Changelog](../changelogs/mariadb-connector-nodejs-3x-changelogs/mariadb-connector-nodejs-300-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide)

**Release date:** 30 Jun 2021

MariaDB Connector/Node.js 3.0.0 is a [_**Beta**_](../../../mariadb-release-criteria.md) release.

**Do not use&#x20;**_**beta**_**&#x20;releases in production!**

{% hint style="success" %}
**For an overview of MariaDB Connector/Node.js see the** [**About MariaDB Connector/Node.js**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide) **page**
{% endhint %}

## Notable Changes

### Prepared statement implementation

Driver now permits using prepared statement.\
This methods are compatible with mysql2 with some differences:

* permit streaming parameters
* execute use by default a prepared cache that hasn't infinite length (option ‘prepareCacheLength’ with default to 256)
* Implement [mariadb 10.6](../../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md) new feature, skipping metadata when possible for better performance

New Connection methods:

* [connection.prepare(sql) → Promise](https://github.com/mariadb-corporation/mariadb-connector-nodejs/blob/maintenance/3.x/documentation/promise-api#connectionpreparesql--promise): Prepares a query.
* [connection.execute(sql\[, values\]) → Promise](https://github.com/mariadb-corporation/mariadb-connector-nodejs/blob/maintenance/3.x/documentation/promise-api#connectionexecutesql-values--promise): Prepare and Executes a query.

Example:

```js
const prepare = await conn.prepare('INSERT INTO mytable(id,val) VALUES (?,?)');
await prepare.execute([1, 'val1']);
prepare.close();
```

Or directly :

```js
await conn.execute('INSERT INTO mytable(id,val) VALUES (?,?)', [1, 'val1']);
```

If reusing query multiple time, this permits to perform better, specifically using [mariadb 10.6](../../../mariadb-community-server-release-notes/mariadb-10-6-series/what-is-mariadb-106.md). Performance comparison with mysql2 driver show up to 20% performance gain. More info will follow before GA release.

### Exact Number implementation

Default behaviour for decoding [BIGINT](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/numeric-data-types/bigint) / [DECIMAL](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/numeric-data-types/decimal) datatype for 2.x version and mysql/mysql2 drivers return a javascript [Number](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Number) object.\
BIGINT / DECIMAL values might not be in the safe range, resulting in approximate results.

Since 3.x version, driver has reliable default, returning:

* DECIMAL => javascript String
* BIGINT => javascript [BigInt](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/numeric-data-types/bigint) object

For compatibility with the previous versions or mysql/mysql driver, 3 options have been added to return BIGINT/DECIMAL as Number, like previous defaults.

| Option           | Description                                                                                                          | Type    | default |
| ---------------- | -------------------------------------------------------------------------------------------------------------------- | ------- | ------- |
| Option           | Description                                                                                                          | Type    | default |
| insertIdAsNumber | Whether the query should return last insert id from INSERT/UPDATE command as BigInt or Number. default return BigInt | boolean | false   |
| decimalAsNumber  | Whether the query should return decimal as Number. If enabled, this might return approximate values.                 | boolean | false   |
| bigIntAsNumber   | Whether the query should return BigInt data type as Number. If enabled, this might return approximate values.        | boolean | false   |

Previous options `supportBigNumbers` and `bigNumberStrings` still exist for compatibility, but are now deprecated.

### Custom logging API

Driver permit mapping the logs to an external logger. There is 3 caller functions:

* network(string): called for each network exchange.
* query(string): called for each commands
* error(Error): called for each error.

if setting one function, function will be used for all loggers. (ie. logger: console.log === logger: { network: console.log, query: console.log, error: console.log})

Example:

```js
const mariadb = require('mariadb');
const winston = require('winston');

const logger = winston.createLogger({
  level: 'info',
  transports: [
    // - Write all logs with level `error` and below to `error.log`
    // - Write all logs with level `info` and below to `combined.log`
    new winston.transports.Console({ filename: 'error.log', level: 'error' }),
    new winston.transports.Console({ filename: 'combined.log' })
  ]
});

const pool = mariadb.createPool({
  host: 'mydb.com',
  user:'myUser',
  password: 'myPwd',
  logger: {
    network: (msg) => logger.silly(msg),
    query: (msg) => logger.info(msg),
    error: (err) => logger.error(err),
  }
});
```

## Changelog

For a complete list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-nodejs-3x-changelogs/mariadb-connector-nodejs-300-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
