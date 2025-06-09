# MariaDB Connector/Node.js 3.1.0 Changelog

The most recent [_**Stable (GA)**_](../../../../mariadb-release-criteria.md) release of [MariaDB Connector/Node.js](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-nodejs/README.md) is:[**MariaDB Connector/Node.js 3.4.2**](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-4-2-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-1-0-release-notes.md)[Changelog](mariadb-connector-node-js-3-1-0-changelog.md)[Connector/Node.js Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-nodejs/README.md)

**Release date:** 15 Feb 2023

For the highlights of this release, see the[release notes](../../mariadb-connector-nodejs-3x-release-notes/mariadb-connector-node-js-3-1-0-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-nodejs) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #3d3cdc6](https://github.com/mariadb-corporation/mariadb-connector-j/commit/3d3cdc6) Merge branch 'release/3.1.0'
* [Revision #982a6a1](https://github.com/mariadb-corporation/mariadb-connector-j/commit/982a6a1) \[misc] changelog update
* [Revision #65327c7](https://github.com/mariadb-corporation/mariadb-connector-j/commit/65327c7) \[[CONJS-240](https://jira.mariadb.org/browse/CONJS-240)] ensuring PREPARE state when caching
* [Revision #ba70356](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ba70356) \[[CONJS-241](https://jira.mariadb.org/browse/CONJS-241)] metaAsArray missing option in typescript description
* [Revision #695bc10](https://github.com/mariadb-corporation/mariadb-connector-j/commit/695bc10) \[misc] benchmark initialization correction
* [Revision #f6861e5](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f6861e5) \[misc] update benchmark result for 3.1.0
* [Revision #5500df2](https://github.com/mariadb-corporation/mariadb-connector-j/commit/5500df2) \[misc] bench label correction
* [Revision #7b9001f](https://github.com/mariadb-corporation/mariadb-connector-j/commit/7b9001f) \[misc] test correction for windows
* [Revision #a71072d](https://github.com/mariadb-corporation/mariadb-connector-j/commit/a71072d) Merge tag '3.1.0' into develop
* [Revision #21d7547](https://github.com/mariadb-corporation/mariadb-connector-j/commit/21d7547) Merge branch 'release/3.1.0'
* [Revision #367ae7e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/367ae7e) bump 3.1.0 version
* [Revision #1683402](https://github.com/mariadb-corporation/mariadb-connector-j/commit/1683402) \[misc] benchmark update with recent version \* benchmark charset option change \* label correction
* [Revision #8ab9166](https://github.com/mariadb-corporation/mariadb-connector-j/commit/8ab9166) \[misc] test correction
* [Revision #987f5cd](https://github.com/mariadb-corporation/mariadb-connector-j/commit/987f5cd) \[misc] ensure pools ending active connections after a maximum of 10s after pool ends
* [Revision #9d64f84](https://github.com/mariadb-corporation/mariadb-connector-j/commit/9d64f84) \[[CONJS-239](https://jira.mariadb.org/browse/CONJS-239)] ensure when using callback connection that pre-commands are executed first
* [Revision #85f8baf](https://github.com/mariadb-corporation/mariadb-connector-j/commit/85f8baf) \[misc] test improvement
* [Revision #868a469](https://github.com/mariadb-corporation/mariadb-connector-j/commit/868a469) \[[CONJS-238](https://jira.mariadb.org/browse/CONJS-238)] faster execution for known length packet
* [Revision #f180049](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f180049) \[misc] correcting place of prepare parser
* [Revision #b32064a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/b32064a) \[misc] ensuring disabling nagle algorithm setting option
* [Revision #13d7595](https://github.com/mariadb-corporation/mariadb-connector-j/commit/13d7595) \[misc] faster Text Date encoder
* [Revision #e21952f](https://github.com/mariadb-corporation/mariadb-connector-j/commit/e21952f) \[misc] avoid unnecessary array creation for multiple result-set with metaAsArray enabled
* [Revision #32b49cd](https://github.com/mariadb-corporation/mariadb-connector-j/commit/32b49cd) \[msic] avoid unnecessary try catch when parsing OK\_Packet + fast path for single result
* [Revision #b253e2b](https://github.com/mariadb-corporation/mariadb-connector-j/commit/b253e2b) \[msic] avoid connection.addCommand returning unnecessary command object
* [Revision #3d501b6](https://github.com/mariadb-corporation/mariadb-connector-j/commit/3d501b6) \[msic] avoid unnecessary binding wrapper
* [Revision #f537713](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f537713) \[[CONJS-230](https://jira.mariadb.org/browse/CONJS-230)] correct encoding lost and avoid buffer copying
* [Revision #ae1fede](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ae1fede) \[misc] test stability improvement
* [Revision #9a01c46](https://github.com/mariadb-corporation/mariadb-connector-j/commit/9a01c46) \[[CONJS-237](https://jira.mariadb.org/browse/CONJS-237)] test stability improvement, when server doesn't have timezone entries filled
* [Revision #130b437](https://github.com/mariadb-corporation/mariadb-connector-j/commit/130b437) \[[CONJS-230](https://jira.mariadb.org/browse/CONJS-230)] improve metadata parsing
* [Revision #1d632d1](https://github.com/mariadb-corporation/mariadb-connector-j/commit/1d632d1) \[misc] remove deprecated use of Buffer.slice
* [Revision #81aa79c](https://github.com/mariadb-corporation/mariadb-connector-j/commit/81aa79c) \[[CONJS-237](https://jira.mariadb.org/browse/CONJS-237)] Timezone option improvement
* [Revision #e628a70](https://github.com/mariadb-corporation/mariadb-connector-j/commit/e628a70) \[misc] code correction: \* correct documented method parameters \* remove unused requirement \* remove unused parameters
* [Revision #5097be7](https://github.com/mariadb-corporation/mariadb-connector-j/commit/5097be7) \[misc] set testing limit to max\_allowed\_packet to 50M, to avoid suite running for hours
* [Revision #13a3d75](https://github.com/mariadb-corporation/mariadb-connector-j/commit/13a3d75) \[misc] test correction
* [Revision #8cbec0b](https://github.com/mariadb-corporation/mariadb-connector-j/commit/8cbec0b) \[misc] improve contribution guide
* [Revision #76f3f3d](https://github.com/mariadb-corporation/mariadb-connector-j/commit/76f3f3d) \[misc] improve test reliability
* [Revision #6d9f115](https://github.com/mariadb-corporation/mariadb-connector-j/commit/6d9f115) Merge branch 'master' into develop
* [Revision #f250817](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f250817) \[misc] correcting cast documentation
* [Revision #be84cc4](https://github.com/mariadb-corporation/mariadb-connector-j/commit/be84cc4) \[[CONJS-236](https://jira.mariadb.org/browse/CONJS-236)] binary TIME wrong decoding
* [Revision #58f4f2e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/58f4f2e) \[[CONJS-235](https://jira.mariadb.org/browse/CONJS-235)] allow to pass TypeScript generic type
* [Revision #27b293e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/27b293e) Merge branch 'p-kuen\_patch-1' into develop
* [Revision #d3cf0a6](https://github.com/mariadb-corporation/mariadb-connector-j/commit/d3cf0a6) Merge branch 'master' into develop
* [Revision #ebef145](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ebef145) docs: update new default value of connectTimeout since v2.5.6
* [Revision #f11b23c](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f11b23c) Merge branch 'master' into develop
* [Revision #f3bd6fb](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f3bd6fb) Merge branch 'fix/modify-entries-method' into develop
* [Revision #914fab4](https://github.com/mariadb-corporation/mariadb-connector-j/commit/914fab4) \[misc] small markdown correction
* [Revision #60f80be](https://github.com/mariadb-corporation/mariadb-connector-j/commit/60f80be) \[misc] test correction for mysql that doesn't support sha256\_password anymore
* [Revision #ab708e2](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ab708e2) Allow to pass type to query function
* [Revision #2f12c96](https://github.com/mariadb-corporation/mariadb-connector-j/commit/2f12c96) \[misc] test correction for mysql that doesn't support sha256\_password anymore
* [Revision #77b6150](https://github.com/mariadb-corporation/mariadb-connector-j/commit/77b6150) Merge pull request #223
* [Revision #cf7d862](https://github.com/mariadb-corporation/mariadb-connector-j/commit/cf7d862) \[misc] test correction for mysql that doesn't support sha256\_password anymore
* [Revision #b15e543](https://github.com/mariadb-corporation/mariadb-connector-j/commit/b15e543) docs: reformat documentation of pool options
* [Revision #0fcf207](https://github.com/mariadb-corporation/mariadb-connector-j/commit/0fcf207) docs: reformat documentation of pool options
* [Revision #04bc04d](https://github.com/mariadb-corporation/mariadb-connector-j/commit/04bc04d) \[misc] test correction
* [Revision #5c1cf30](https://github.com/mariadb-corporation/mariadb-connector-j/commit/5c1cf30) \[misc] code style correction
* [Revision #fae38f2](https://github.com/mariadb-corporation/mariadb-connector-j/commit/fae38f2) \[[CONJS-232](https://jira.mariadb.org/browse/CONJS-232)] killing connection when query are running fails
* [Revision #5daaa03](https://github.com/mariadb-corporation/mariadb-connector-j/commit/5daaa03) \[[CONJS-231](https://jira.mariadb.org/browse/CONJS-231)] BULK command when reaching maximum packet size might be wrongly split
* [Revision #c8122eb](https://github.com/mariadb-corporation/mariadb-connector-j/commit/c8122eb) \[misc] removing request SHA certificate since failing 5.7.40 / 8.0.31 without any reason
* [Revision #86f1212](https://github.com/mariadb-corporation/mariadb-connector-j/commit/86f1212) Modify unneeded `Object.entries()`
* [Revision #1ddb432](https://github.com/mariadb-corporation/mariadb-connector-j/commit/1ddb432) \[misc] binary number read parsing small improvement
* [Revision #d2e626e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/d2e626e) \[misc] ensure prepare cache use counter
* [Revision #cb26d24](https://github.com/mariadb-corporation/mariadb-connector-j/commit/cb26d24) \[misc] prepare parameter count correction
* [Revision #4d24aaf](https://github.com/mariadb-corporation/mariadb-connector-j/commit/4d24aaf) \[misc] Date parameter identification using `instanceof Date` that is more performant than `Object.prototype.toString.call(val) === '[object Date]'`
* [Revision #82b9a50](https://github.com/mariadb-corporation/mariadb-connector-j/commit/82b9a50) \[misc] avoid filling intermediary buffer when not required
* [Revision #119592e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/119592e) \[[CONJS-230](https://jira.mariadb.org/browse/CONJS-230)] avoid parsing PREPARE parameters meta. keeping only parameter number
* [Revision #52ef79e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/52ef79e) \[misc] avoid unnecessary parameters
* [Revision #ce506a3](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ce506a3) \[misc] adding test
* [Revision #f78cd09](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f78cd09) \[misc] fast path when TCP-IP packet contains multiple MySQL Packets
* [Revision #ee137c5](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ee137c5) \[[CONJS-230](https://jira.mariadb.org/browse/CONJS-230)] performance improvement, Column information name information being saved in a fit Buffer and avoid creating subpacket when not needed
* [Revision #364c582](https://github.com/mariadb-corporation/mariadb-connector-j/commit/364c582) \[misc] BigInt literal
* [Revision #697250e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/697250e) \[misc] performance improvement for bigIntAsNumber option
* [Revision #f1c3763](https://github.com/mariadb-corporation/mariadb-connector-j/commit/f1c3763) \[misc] add maxscale error lof when failing
* [Revision #393d49c](https://github.com/mariadb-corporation/mariadb-connector-j/commit/393d49c) \[misc] benchmark name correction
* [Revision #d0baac6](https://github.com/mariadb-corporation/mariadb-connector-j/commit/d0baac6) \[misc] result-set rows improvement, since at least one value
* [Revision #7bb676a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/7bb676a) \[[CONJS-229](https://jira.mariadb.org/browse/CONJS-229)] code style correction
* [Revision #9205259](https://github.com/mariadb-corporation/mariadb-connector-j/commit/9205259) \[[CONJS-229](https://jira.mariadb.org/browse/CONJS-229)] performance issue when parsing lots of parameter
* [Revision #8b51eb7](https://github.com/mariadb-corporation/mariadb-connector-j/commit/8b51eb7) \[misc] code style correction
* [Revision #67e2ed9](https://github.com/mariadb-corporation/mariadb-connector-j/commit/67e2ed9) Merge branch 'master' into develop
* [Revision #7e8696f](https://github.com/mariadb-corporation/mariadb-connector-j/commit/7e8696f) \[misc] code coverage correction
* [Revision #104c400](https://github.com/mariadb-corporation/mariadb-connector-j/commit/104c400) merge 3.0.2 version
* [Revision #6c7946c](https://github.com/mariadb-corporation/mariadb-connector-j/commit/6c7946c) \[[CONJS-226](https://jira.mariadb.org/browse/CONJS-226)] add missing metaAsArray documentation and typescript option
* [Revision #9c4562a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/9c4562a) \[[CONJS-225](https://jira.mariadb.org/browse/CONJS-225)] Make result set's meta property non-enumerable

{% @marketo/form formid="4316" formId="4316" %}
