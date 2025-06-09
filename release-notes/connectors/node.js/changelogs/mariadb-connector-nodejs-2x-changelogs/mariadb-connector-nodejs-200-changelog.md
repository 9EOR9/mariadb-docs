# MariaDB Connector/Node.js 2.0.0 Changelog

The most recent [_**Stable (GA)**_](../../../../mariadb-release-criteria.md) release of [MariaDB Connector/Node.js](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-nodejs/README.md) is:[**MariaDB Connector/Node.js 3.4.2**](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-4-2-release-notes.md)

[Download](https://downloads.mariadb.org/connector-nodejs/2.0.0/)[Release Notes](../../mariadb-connector-nodejs-2x-release-notes/mariadb-connector-nodejs-200-release-notes.md)[Changelog](mariadb-connector-nodejs-200-changelog.md)[Connector/Node.js Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-nodejs/README.md)

**Release date:** 25 Sep 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-nodejs-2x-release-notes/mariadb-connector-nodejs-200-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-nodejs) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #1513511](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1513511) - \[misc] tag version as 2.0.0-alpha ¶
* [Revision #4c70c51](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4c70c51) - \[misc] changing test streaming file to internal mariadb server to avoid any socket closed from server end. ¶
* [Revision #cd6d938](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/cd6d938) - \[[CONJS-39](https://jira.mariadb.org/browse/CONJS-39)] correcting geometry test for MySQL 5.5 that doesn't have ST\_LineFromText / ST\_PointFromText / ST\_PolygonFromText functions - part 2 ¶
* [Revision #4b7b4e1](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/4b7b4e1) - \[[CONJS-39](https://jira.mariadb.org/browse/CONJS-39)] correcting geometry test for MySQL 5.5 that doesn't have ST\_LineFromText / ST\_PointFromText / ST\_PolygonFromText functions ¶
* [Revision #dbdbd4a](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/dbdbd4a) - \[[CONJS-39](https://jira.mariadb.org/browse/CONJS-39)] correcting MySQL geometry test ( ST\_\* commands not existing before 5.7) ¶
* [Revision #7c2bdcb](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/7c2bdcb) - \[[CONJS-39](https://jira.mariadb.org/browse/CONJS-39)] support geometry type : correction for MariaDB < 10.1.4 and MySQL < 8.0.0 geometry support report information isMariaDB() / hasMinVersion() to information level to permit use on internal functions ¶
* [Revision #20ff129](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/20ff129) - \[misc] simplify use of connection information. ¶
* [Revision #bc7174d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/bc7174d) - \[misc] set Promise API documentation to a dedicated page. ¶
* [Revision #6df9209](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/6df9209) - \[misc] connection.end() immediate resolution on socket QUIT packet send. ¶
* [Revision #1c65cc7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/1c65cc7) - \[[CONJS-39](https://jira.mariadb.org/browse/CONJS-39)] support geometric GeoJSON structure format ¶
* [Revision #a4ac4c9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a4ac4c9) - \[[CONJS-24](https://jira.mariadb.org/browse/CONJS-24)] new option "sessionVariables" to permit setting session variable at connection ¶
* [Revision #ea105f8](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/ea105f8) - \[misc] adding test coverage (compression multi-packet + buffer skipping numeric) ¶
* [Revision #0221c53](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0221c53) - \[misc] avoiding mysql error message if ending and sequence command has not ended ¶
* [Revision #64ce336](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/64ce336) - \[misc] avoid validating all pool connection on benchmark end ¶
* [Revision #0869c96](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0869c96) - \[[CONJS-42](https://jira.mariadb.org/browse/CONJS-42)] check other connections in pool when an unexpected connection error occur ¶
* [Revision #2c88755](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/2c88755) - \[[CONJS-39](https://jira.mariadb.org/browse/CONJS-39)] adapt geometry test to mysql that for version < 8 doesn't permit empty GeometryCollection ¶
* [Revision #944a93b](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/944a93b) - \[[CONJS-39](https://jira.mariadb.org/browse/CONJS-39)] support geometry type ¶
* [Revision #852ca61](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/852ca61) - \[[CONJS-44](https://jira.mariadb.org/browse/CONJS-44)] Create option to permit setting Object to one prepareStatement parameter ¶
* [Revision #50b338d](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/50b338d) - \[[CONJS-43](https://jira.mariadb.org/browse/CONJS-43)] Callback API is missing ¶
* [Revision #a8d1298](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a8d1298) - \[misc] report community documentation change ¶
* [Revision #a3828a0](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a3828a0) - \[misc] report community documentation change ¶
* [Revision #090ce29](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/090ce29) - \[misc] report community documentation change ¶
* [Revision #73f0ca7](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/73f0ca7) - \[misc] README : changing pipelining image ¶
* [Revision #223e6a4](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/223e6a4) - \[misc] README : changing pipelining image ¶
* [Revision #a4ee4d9](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/a4ee4d9) - \[misc] correcting image url ¶
* [Revision #9dd6766](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/9dd6766) - \[misc] README : adding pipelining image ¶
* [Revision #096d2df](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/096d2df) - \[misc] correcting README links ¶
* [Revision #417d0c5](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/417d0c5) - \[misc] benchmark pool, use max connection number to 4 ¶
* [Revision #0f2fe47](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/0f2fe47) - \[misc] removing zip benchmark on travis, since doesn't really have meaning, mysql comparison doesn't have compress option ¶
* [Revision #924f958](https://github.com/mariadb-corporation/mariadb-connector-nodejs/commit/924f958) - \[misc] change pool implementation to permit node 6 compatibility (removal of async await)

Be notified of new MariaDB Server releases automatically by [subscribing](https://lists.mariadb.org/postorius/lists/announce.lists.mariadb.org/) to the MariaDB Foundation community announce 'at' lists.mariadb.org announcement list (this is a low traffic, announce-only list). MariaDB plc customers will be notified for all new releases, security issues and critical bug fixes for all MariaDB plc products thanks to the Notification Services.

MariaDB may already be included in your favorite OS distribution. More\
information can be found on the[Distributions which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/readme-1)\
page.
