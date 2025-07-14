# MariaDB Connector/Node.js 3.1.0 Release Notes

{% include "../../../.gitbook/includes/latest-nodejs.md" %}

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/nodejs-connector) | [Release Notes](mariadb-connector-node-js-3-1-0-release-notes.md) | [Changelog](../changelogs/mariadb-connector-nodejs-3x-changelogs/mariadb-connector-node-js-3-1-0-changelog.md) | [Connector/Node.js Overview](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide)

**Release date:** 15 Feb 2023

MariaDB Connector/Node.js 3.1.0 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

{% hint style="success" %}
**For an overview of MariaDB Connector/Node.js see the** [**About MariaDB Connector/Node.js**](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-nodejs/mariadb-connector-node-js-guide) **page**
{% endhint %}

## Notable Changes

### Timezone handling

[CONJS-237](https://jira.mariadb.org/browse/CONJS-237)\
Connector now set session timezone, solving issue with [time function](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/reference/data-types/string-data-types/character-sets/internationalization-and-localization/time-zones#time-zone-effects-on-functions),\
removing needs of client side conversion.

This requires that when using timezone options, to have corresponding server TZ data filled.

### Performance

* [CONJS-230](https://jira.mariadb.org/browse/CONJS-230) better metadata parsing performance
* [CONJS-229](https://jira.mariadb.org/browse/CONJS-229) performance improvement when parsing lots of parameter
* [CONJS-238](https://jira.mariadb.org/browse/CONJS-238) faster execution for known length packet

see [here](https://github.com/mariadb-corporation/mariadb-connector-nodejs/blob/master/documentation/benchmarks) for updated result compared to other connectors

### Other changes

* [CONJS-225](https://jira.mariadb.org/browse/CONJS-225) Make result set's meta property non-enumerable
* [CONJS-235](https://jira.mariadb.org/browse/CONJS-235) Allow to pass TypeScript generic types without need of "as"

## Issues Fixed

* [CONJS-231](https://jira.mariadb.org/browse/CONJS-231) When executing batch with a parameter can be too long to fit in one mysql packet, parameter can have 4 byte missing
* [CONJS-236](https://jira.mariadb.org/browse/CONJS-236) datatype TIME wrong binary decoding when not having microseconds
* [CONJS-239](https://jira.mariadb.org/browse/CONJS-239) When using connection with callback, pre-commands (like `initSql`) might not always be executed first
* [CONJS-232](https://jira.mariadb.org/browse/CONJS-232) in case of a long query running, connection.destroy() will close connection, but might leave server still running query for some time
* [CONJS-240](https://jira.mariadb.org/browse/CONJS-240) adding a Prepare result wrapper to avoid multiple close issue with cache
* [CONJS-241](https://jira.mariadb.org/browse/CONJS-241) metaAsArray missing option in typescript description

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
