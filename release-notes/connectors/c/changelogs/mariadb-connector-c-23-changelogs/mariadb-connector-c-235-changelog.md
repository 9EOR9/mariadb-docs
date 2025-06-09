# MariaDB Connector/C 2.3.5 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/2.3.5)[Release Notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-235-release-notes.md)[Changelog](mariadb-connector-c-235-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 18 Jan 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-235-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #72a04d3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/72a04d3)\
  2018-01-17 08:01:21 +0100
  * Changed/fixed Wix installer images
* [Revision #bf3bcb3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bf3bcb3)\
  2017-11-08 04:56:04 +0100
  * [CONC-292](https://jira.mariadb.org/browse/CONC-292): Fxed malloc result check in dynamic columns
* [Revision #d137de7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d137de7)\
  2018-01-16 19:05:02 +0100
  * cosmetic fix in install.cmake (rpm installation layout)
* [Revision #117451e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/117451e)\
  2018-01-16 16:01:51 +0100
  * installation layout: fixed typos in plugin\_install\_dir
* [Revision #1512448](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1512448)\
  2018-01-16 15:21:56 +0100
  * Fix for [MDEV-10361](https://jira.mariadb.org/browse/MDEV-10361): Don't try to reconnect twice: if mysql->options.reconnect is set, ma\_simple\_command already tries to reconnect, so there is no need to reconnect in mysql\_ping again
* [Revision #6ad7e50](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6ad7e50)\
  2018-01-16 15:18:49 +0100
  * Revert "Fix for [MDEV-10361](https://jira.mariadb.org/browse/MDEV-10361): Don't try to reconnect twice: if mysql->options.reconnect is set,"
* [Revision #739bdc8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/739bdc8)\
  2018-01-16 15:05:00 +0100
  * Fix for [MDEV-10361](https://jira.mariadb.org/browse/MDEV-10361): Don't try to reconnect twice: if mysql->options.reconnect is set, ma\_simple\_command already tries to reconnect, so there is no need to reconnect in mysql\_ping again.
* [Revision #775be2e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/775be2e)\
  2018-01-16 14:35:45 +0100
  * Added install layout for debian packages
* [Revision #630f36c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/630f36c)\
  2017-12-25 16:10:20 +0100
  * [CONC-299](https://jira.mariadb.org/browse/CONC-299): Add support for missing collation and character sets
* [Revision #129e013](https://github.com/mariadb-corporation/mariadb-connector-c/commit/129e013)\
  2017-12-22 09:39:28 +0100
  * Merge pull request #24 from nalinaly/connector\_c\_2.3
* [Revision #040cfbd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/040cfbd)\
  2017-02-26 21:08:26 +0800
  * Fix for statement memory alloc:need reset block\_num
* [Revision #36c989b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/36c989b)\
  2017-12-22 08:49:35 +0100
  * Fix for [CONC-301](https://jira.mariadb.org/browse/CONC-301):
