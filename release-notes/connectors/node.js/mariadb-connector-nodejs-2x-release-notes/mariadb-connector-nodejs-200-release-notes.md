# MariaDB Connector/Node.js 2.0.0 Release Notes

{% include "../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://mariadb.com/downloads/connector) | [Release Notes](mariadb-connector-nodejs-200-release-notes.md) | [Changelog](../changelogs/mariadb-connector-nodejs-2x-changelogs/mariadb-connector-nodejs-200-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide)

**Release date:** 25 Sep 2018

MariaDB Connector/Node.js 2.0.0 is an [_**Alpha**_](../../../mariadb-release-criteria.md)\
release.

{% hint style="success" %}
**For an overview of MariaDB Connector/Node.js see the** [**About MariaDB Connector/Node.js**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide) **page**
{% endhint %}

## Features

* [CONJS-42](https://jira.mariadb.org/browse/CONJS-42) : check other connections in pool when an unexpected connection error occur
* [CONJS-44](https://jira.mariadb.org/browse/CONJS-44) : Create option to permit setting Object to one prepareStatement parameter
* [CONJS-43](https://jira.mariadb.org/browse/CONJS-43) : Callback API is missing
* [CONJS-39](https://jira.mariadb.org/browse/CONJS-39) : support geometric GeoJSON structure format
* [CONJS-24](https://jira.mariadb.org/browse/CONJS-24) : new option "sessionVariables" to permit setting session variable at connection
* connection.end() immediate resolution on socket QUIT packet send.
* improve documentation and set Promise API documentation to a dedicated page.
* change pool implementation to permit node 6 compatibility (removal of async await)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
