# MariaDB Connector/Node.js 3.4.1 Release Notes

The most recent [_**Stable (GA)**_](../../../mariadb-release-criteria.md) release of [MariaDB Connector/Node.js](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-nodejs/README.md) is:[**MariaDB Connector/Node.js 3.4.2**](mariadb-connector-node-js-3-4-2-release-notes.md)

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/nodejs-connector)[Release Notes](mariadb-connector-node-js-3-4-1-release-notes.md)[Changelog](../changelogs/mariadb-connector-nodejs-3x-changelogs/mariadb-connector-node-js-3-4-1-changelog.md)[Connector/Node.js Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-nodejs/README.md)

**Release date:** 2 Apr 2025

MariaDB Connector/Node.js 3.4.1 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

**For an overview of MariaDB Connector/Node.js see the**[**About MariaDB Connector/Node.js**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connectornodejs/README.md) **page**

## Issues Fixed

* [CONJS-306](https://jira.mariadb.org/browse/CONJS-306): Support "zero configuration ssl" for parsec authentication
* [CONJS-315](https://jira.mariadb.org/browse/CONJS-315): Fixed issue with incorrect data for result-set rows of exactly 16M of data
* [CONJS-312](https://jira.mariadb.org/browse/CONJS-312): Improved pool error messages when failing to create connections
* [CONJS-313](https://jira.mariadb.org/browse/CONJS-313): Now allows using question mark parameters even when using namedPlaceholders option (mysql compatibility)
* [CONJS-305](https://jira.mariadb.org/browse/CONJS-305): Added Connection close alias for end function in TypeScript definition
* [CONJS-314](https://jira.mariadb.org/browse/CONJS-314): Fixed Bulk operations potentially returning unexpected error "Cannot read properties of undefined (reading '0')"
* [CONJS-275](https://jira.mariadb.org/browse/CONJS-275): Added capability to return all Bulk insert IDs for MariaDB server 11.5.1+
* [CONJS-304](https://jira.mariadb.org/browse/CONJS-304): Fixed bulk operations ending with "Got a packet bigger than 'max\_allowed\_packet' bytes" error
* [CONJS-316](https://jira.mariadb.org/browse/CONJS-316): Enhanced handling of non-bulk batched operations to avoid out-of-memory errors for batches not using bulk

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
