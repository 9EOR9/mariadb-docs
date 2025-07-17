# Connector/Node.js 3.3.1 Release Notes

{% include "../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/nodejs-connector) | [Release Notes](mariadb-connector-node-js-3-3-1-release-notes.md) | [Changelog](../changelogs/mariadb-connector-nodejs-3x-changelogs/mariadb-connector-node-js-3-3-1-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide)

**Release date:** 5 Jun 2024

MariaDB Connector/Node.js 3.3.1 is a [_**Stable**_](../../../community-server/about/release-criteria.md) _**(GA)**_ release.

{% hint style="success" %}
**For an overview of MariaDB Connector/Node.js see the** [**About MariaDB Connector/Node.js**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide) **page**
{% endhint %}

## Notable Changes

* [CONJS-288](https://jira.mariadb.org/browse/CONJS-288) A pool timeout error now returns connection timeout details

## Issues Fixed

* [CONJS-289](https://jira.mariadb.org/browse/CONJS-289) Connection can possibly stay in hang state after batch execution
  * [CONJS-290](https://jira.mariadb.org/browse/CONJS-290) When using batch with big values, a connection might be in a wrong state, which can result in Server error: `'(Got an error reading communication packets)'`
  * Client TCP error `ECONRESET`
* [CONJS-292](https://jira.mariadb.org/browse/CONJS-292) Connector does not permit passing a String object (≠ native string) parameter
  * `const objVal = new String('myValue');`
* [CONJS-286](https://jira.mariadb.org/browse/CONJS-286) When using a prepared statement and explicitly disabling prepare cache using prepareCacheLength=0, the connector might not retrieve results anymore
* [CONJS-287](https://jira.mariadb.org/browse/CONJS-287) Typescript is missing `'QueryOption'` for the `'prepare'` command
* [CONJS-293](https://jira.mariadb.org/browse/CONJS-293) When using batch, javascript Date values that are not in the range `1970-01-01 00:00:01 - 2038-01-19 03:14:07` are saved as null

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
