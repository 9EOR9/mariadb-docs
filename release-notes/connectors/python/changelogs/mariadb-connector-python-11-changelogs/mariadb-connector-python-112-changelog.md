# MariaDB Connector/Python 1.1.2 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/Python is:[**MariaDB Connector/Python 1.1.12**](../../mariadb-connector-python-1-1-release-notes/mariadb-connector-python-1-1-12-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-python-1-1-release-notes/mariadb-connector-python-1-1-2-release-notes.md)[Changelog](mariadb-connector-python-112-changelog.md)[Connector/Python Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb-connector-python/README.md)

**Release date:** 27 Jun 2022

For the highlights of this release, see the[release notes](../../mariadb-connector-python-1-1-release-notes/mariadb-connector-python-1-1-2-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-python/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #418dbf0](https://github.com/mariadb-corporation/mariadb-connector-python/commit/418dbf0)\
  2022-06-23 14:45:12 +0200
  * Set version number to 1.1.2:
* [Revision #64882fc](https://github.com/mariadb-corporation/mariadb-connector-python/commit/64882fc)\
  2022-06-23 14:43:36 +0200
  * Merge pull request #21 from vaerksted/1.1
* [Revision #d2f9780](https://github.com/mariadb-corporation/mariadb-connector-python/commit/d2f9780)\
  2022-06-22 16:22:27 -0500
  * typos
* [Revision #5420fe3](https://github.com/mariadb-corporation/mariadb-connector-python/commit/5420fe3)\
  2022-06-08 13:43:20 +0200
  * Various fixes:
* [Revision #ad4937d](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ad4937d)\
  2022-06-07 08:37:48 +0200
  * Changed error message for closed connection
* [Revision #a9fcc27](https://github.com/mariadb-corporation/mariadb-connector-python/commit/a9fcc27)\
  2022-05-30 09:16:23 +0200
  * Fixed version\_info for GA
* [Revision #fde6a22](https://github.com/mariadb-corporation/mariadb-connector-python/commit/fde6a22)\
  2022-05-30 07:33:24 +0200
  * Setup:
* [Revision #f23e4e9](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f23e4e9)\
  2022-05-25 18:54:11 +0200
  * [CONPY-205](https://jira.mariadb.org/browse/CONPY-205): Added error constants
* [Revision #30c8f33](https://github.com/mariadb-corporation/mariadb-connector-python/commit/30c8f33)\
  2022-05-25 18:47:03 +0200
  * [CONPY-205](https://jira.mariadb.org/browse/CONPY-205): Inconsistent exceptions
* [Revision #0a7f751](https://github.com/mariadb-corporation/mariadb-connector-python/commit/0a7f751)\
  2022-05-21 10:06:26 +0200
  * Test fixes
* [Revision #7394d84](https://github.com/mariadb-corporation/mariadb-connector-python/commit/7394d84)\
  2022-05-21 10:02:18 +0200
  * Don't clear rowcount after bulk
* [Revision #693442e](https://github.com/mariadb-corporation/mariadb-connector-python/commit/693442e)\
  2022-05-21 08:35:35 +0200
  * Fixed typo
* [Revision #f93370a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f93370a)\
  2022-05-21 07:59:18 +0200
  * Cursor: Set buffered to True if no args were specified
* [Revision #e3207bb](https://github.com/mariadb-corporation/mariadb-connector-python/commit/e3207bb)\
  2022-05-21 07:15:23 +0200
  * Merge branch '1.1' of [mariadb-connector-python](https://github.com/mariadb-corporation/mariadb-connector-python) into 1.1
* [Revision #107d737](https://github.com/mariadb-corporation/mariadb-connector-python/commit/107d737)\
  2022-05-20 17:42:45 +0200
  * \[misc] adding osx test
* [Revision #4f88242](https://github.com/mariadb-corporation/mariadb-connector-python/commit/4f88242)\
  2022-05-21 07:13:34 +0200
  * Added new connection method dump\_debug\_info()
* [Revision #ef57069](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ef57069)\
  2022-05-19 12:04:59 +0200
  * [CONPY-202](https://jira.mariadb.org/browse/CONPY-202): Fixed typo in installation
* [Revision #9b8a32d](https://github.com/mariadb-corporation/mariadb-connector-python/commit/9b8a32d)\
  2022-05-10 09:06:56 +0200
  * Build fixes:
* [Revision #1aa2bbe](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1aa2bbe)\
  2022-04-11 08:03:20 +0200
  *
    * Documentation
* [Revision #48aea2f](https://github.com/mariadb-corporation/mariadb-connector-python/commit/48aea2f)\
  2022-04-05 16:54:37 +0200
  * Docu fxes
* [Revision #9ae99cd](https://github.com/mariadb-corporation/mariadb-connector-python/commit/9ae99cd)\
  2022-04-03 18:38:48 +0200
  *
    * Documentation fixes - removed COMMAND constants
* [Revision #55ce15a](https://github.com/mariadb-corporation/mariadb-connector-python/commit/55ce15a)\
  2022-04-03 07:03:32 +0200
  * Minor documentation fixes
* [Revision #70ed9b4](https://github.com/mariadb-corporation/mariadb-connector-python/commit/70ed9b4)\
  2022-04-02 20:02:52 +0200
  * Added missing docstring for cursor.paramcount
* [Revision #f2fc6e8](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f2fc6e8)\
  2022-03-25 06:30:23 +0100
  * test for [CONPY-178](https://jira.mariadb.org/browse/CONPY-178)
* [Revision #2e81925](https://github.com/mariadb-corporation/mariadb-connector-python/commit/2e81925)\
  2022-02-20 14:34:51 +0100
  * Skip test if we are connected to MySQL server
* [Revision #ba1bce8](https://github.com/mariadb-corporation/mariadb-connector-python/commit/ba1bce8)\
  2022-02-20 08:56:21 +0100
  * Added test for REPLACE RETURNING
* [Revision #f844622](https://github.com/mariadb-corporation/mariadb-connector-python/commit/f844622)\
  2022-02-20 05:03:43 +0100
  * Added test for [CONPY-194](https://jira.mariadb.org/browse/CONPY-194)
* [Revision #1d74599](https://github.com/mariadb-corporation/mariadb-connector-python/commit/1d74599)\
  2022-02-20 04:42:28 +0100
  * Fix for [CONPY-194](https://jira.mariadb.org/browse/CONPY-194):
