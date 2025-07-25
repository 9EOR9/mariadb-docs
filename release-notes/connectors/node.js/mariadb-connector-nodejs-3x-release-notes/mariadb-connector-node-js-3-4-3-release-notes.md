# Connector/Node.js 3.4.3 Release Notes

{% include "../../../.gitbook/includes/latest-nodejs.md" %}

{% hint style="warning" %}
An issue was discovered in the Connector/Node.js 3.4.3 release shortly after release and it has been replaced by Connector/Node.js 3.4.4. See the 3.4.4 [release notes](mariadb-connector-node-js-3-4-4-release-notes.md) for more details.
{% endhint %}

<a href="https://mariadb.com/downloads/connectors/connectors-data-access/nodejs-connector" class="button primary">Download</a> <a href="mariadb-connector-node-js-3-4-3-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/mariadb-connector-nodejs-3x-changelogs/mariadb-connector-node-js-3-4-3-changelog.md" class="button secondary">Changelog</a> <a href="https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide" class="button secondary">Connector/Node.js Overview</a>

**Release date:** 2 Jul 2025

MariaDB Connector/Node.js 3.4.3 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

{% hint style="success" %}
**For an overview of MariaDB Connector/Node.js see the** [**About MariaDB Connector/Node.js**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide) **page**
{% endhint %}

## Notable changes

* [CONJS-309](https://jira.mariadb.org/browse/CONJS-309): Enhanced TypeScript support by adding mariadb/callback type definitions

## Issues Fixed

* [CONJS-319](https://jira.mariadb.org/browse/CONJS-319): Resolved SSL identity verification issue where servername parameter wasn't being properly validated
* [CONJS-320](https://jira.mariadb.org/browse/CONJS-320): Fixed cluster filtering problems in query/execute operations when using the callback API
* [CONJS-321](https://jira.mariadb.org/browse/CONJS-321): Moved @types/geojson and @types/node packages to development dependencies for cleaner production builds

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
