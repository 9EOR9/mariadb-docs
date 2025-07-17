# Connector/Node.js 2.0.2 Release Notes

{% include "../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://mariadb.com/downloads/?showall=1\&tab=connectors\&group=mariadbconnectors\&product=Node.js%20connector\&version=2.0.2) | [Release Notes](mariadb-connector-nodejs-202-release-notes.md) | [Changelog](../changelogs/mariadb-connector-nodejs-2x-changelogs/mariadb-connector-nodejs-202-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide.md)

**Release date:** 13 Dec 2018

MariaDB Connector/Node.js 2.0.2 is a [_**Release Candidate (RC)**_](../../../community-server/about/release-criteria.md) release.

{% hint style="success" %}
**For an overview of MariaDB Connector/Node.js see the** [**About MariaDB Connector/Node.js**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide) **page**
{% endhint %}

## Notable Updates

New options:

### correction

* using option connectAttributes value \_server\_host is correctly filled on Performance Schema.
* batch improvement
  * error is now thrown when no values
  * BULK better handling when socket fail during command
  * Object with toSqlString function parameter support
  * null value correction when using BULK
  * timezone correction when not using "local" default values
  * now support very long parameter (> 16M)
  * rewrite correctly parse double slash
  * timezone option parsing correction (correctly handle negative values)
* test coverage improvement
* minor performance improvement
* pool end() now correctly wait for all connections ending

## Changelog

For a complete list of changes made in this release, with links to detailed information\
on each push, see the [changelog](../changelogs/mariadb-connector-nodejs-2x-changelogs/mariadb-connector-nodejs-202-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
