# MariaDB Connector/Node.js 2.0.2 Changelog

The most recent [_**Stable (GA)**_](../../../../mariadb-release-criteria.md) release of [MariaDB Connector/Node.js](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-nodejs/README.md) is:[**MariaDB Connector/Node.js 3.4.2**](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-4-2-release-notes.md)

[Download](https://mariadb.com/downloads/?showall=1\&tab=connectors\&group=mariadbconnectors\&product=Node.js%20connector\&version=2.0.2)[Release Notes](../../mariadb-connector-nodejs-2x-release-notes/mariadb-connector-nodejs-202-release-notes.md)[Changelog](mariadb-connector-nodejs-202-changelog.md)[Connector/Node.js Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-nodejs/README.md)

**Release date:** 13 Dec 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-nodejs-2x-release-notes/mariadb-connector-nodejs-202-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-nodejs) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #fe3837e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/fe3837e) - bump 2.0.2-rc tag
* [Revision #2a66c70](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2a66c70) - \[misc] add pool noControlAfterUse callback implementation
* [Revision #baf2f76](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/baf2f76) - \[misc] new pool noControlAfterUse to permit having no connection validation when giving back connection to pool.
* [Revision #11f0a5b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/11f0a5b) - \[misc] bulk callback test implementation minor corrections : - doesn't send COM\_STMT\_CLOSE if socket has been interrupted - pool end wait for complete close
* [Revision #dee8739](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/dee8739) - \[misc] using travis npm rebuild
* [Revision #e612d84](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/e612d84) - \[misc] correcting test cases when logPackets is enable
* [Revision #47e48d9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/47e48d9) - \[misc] removing npm dependency
* [Revision #de2a082](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/de2a082) - \[misc] correcting batch callback to use MariaDB bulk when possible
* [Revision #1a4dad2](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1a4dad2) - \[misc] correcting batch timezone option handling
* [Revision #8b91915](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8b91915) - \[misc] adding connection options tests
* [Revision #09e2900](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/09e2900) - \[misc] use logPackets only when enable
* [Revision #8c655b5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/8c655b5) - bump denque
* [Revision #9ad1e9d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9ad1e9d) - update benchmark.js
* [Revision #851281e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/851281e) - \[misc] double escape character in string parsing correction
* [Revision #a32fa24](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a32fa24) - \[misc] issues correction: - "\_server\_host" address connection attributes - rewrite batch error handling correction (too many parameters / or undefined) - bulk batch correction when using object with "toSqlString" function - bulk batch correcting null
* gitrevn:parameter value handling - removed "mysql\_clear\_password" as default connection plugin, since deprecated - adding test coverage
* [Revision #2fdefcb](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2fdefcb) - \[misc] batch rewrite error correction when having no parameter
* [Revision #86b9ed3](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/86b9ed3) - \[misc] correcting batch error handling for filtered pool cluster. adding test coverage for batch error.
* [Revision #4257efa](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4257efa) - \[misc] Cluster better error message when not retrieving Connection from cluster. filtered cluster test addition + query error better handling
* [Revision #73aa059](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/73aa059) - \[misc] correcting warning test for mysql 8
* [Revision #4bf32b7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4bf32b7) - \[misc] adding unit test, bulk code cleaning
* [Revision #bdbd20b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bdbd20b) - \[misc] test correction for better reliability
* [Revision #2827f78](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2827f78) - \[misc] correcting timezone option parsing bulk date fractional part correction adding test for batch adding reset transaction test
* [Revision #0da1b0e](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0da1b0e) - \[misc] correcting timezone option parsing bulk date fractional part correction adding test for batch

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/distributions-including-mariadb)\
page.

{% @marketo/form formid="4316" formId="4316" %}
