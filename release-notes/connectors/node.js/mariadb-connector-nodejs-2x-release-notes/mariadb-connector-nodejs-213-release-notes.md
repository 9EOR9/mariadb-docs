# MariaDB Connector/Node.js 2.1.3 Release Notes

{% include "../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://mariadb.com/downloads/#connectors) | [Release Notes](mariadb-connector-nodejs-213-release-notes.md) | [Changelog](../changelogs/mariadb-connector-nodejs-2x-changelogs/mariadb-connector-nodejs-213-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide)

**Release date:** 19 Nov 2019

MariaDB Connector/Node.js 2.1.3 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

{% hint style="success" %}
**For an overview of MariaDB Connector/Node.js see the** [**About MariaDB Connector/Node.js**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide) **page**
{% endhint %}

## Notable Changes

* [CONJS-109](https://jira.mariadb.org/browse/CONJS-109) Missing mysql only collation definition
* [CONJS-108](https://jira.mariadb.org/browse/CONJS-108) typescript escape/escapeId definition
* [CONJS-107](https://jira.mariadb.org/browse/CONJS-107) Change user callback function not called when no option is set and changing collation only if collation option is correct
* [CONJS-106](https://jira.mariadb.org/browse/CONJS-106) properly escape boolean parameter false
* [CONJS-105](https://jira.mariadb.org/browse/CONJS-105) Typecast provided date function erroneous parsing
* [CONJS-104](https://jira.mariadb.org/browse/CONJS-104) Pam authentication must permit to provide multiple passwords

PAM authentication with multiple steps can be achieved using password as array:

```js
const mariadb = require('mariadb');

  mariadb.createConnection({host: 'mydb.com', user: 'myUser', password: ['myPwd', 'myAuthToken']})
    .then(conn => {
       ...
    })
    .catch(err => {
      ...
    });
```

## Misc

* better cluster error when pool is full
* adding test coverage

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
