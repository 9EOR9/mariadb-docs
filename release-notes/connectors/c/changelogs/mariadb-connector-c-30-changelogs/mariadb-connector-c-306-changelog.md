# MariaDB Connector/C 3.0.6 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.6)[Release Notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-306-release-notes.md)[Changelog](mariadb-connector-c-306-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-c/README.md)

**Release date:** 2 Aug 2018

For the highlights of this release, see the[release notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-306-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #a0fd36c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a0fd36c)\
  2018-07-31 09:44:20 +0200
  * Revert "Bumped version number to 3.0.7"
* [Revision #f1fd014](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f1fd014)\
  2018-07-31 09:39:03 +0200
  * Fixed leak in ma\_tls\_read/write
* [Revision #f69eaf0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f69eaf0)\
  2018-07-31 06:44:13 +0200
  * Bumped version number to 3.0.7
* [Revision #5cb4d8d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5cb4d8d)\
  2018-07-27 07:46:05 +0200
  * Fixed typo which broke windows build
* [Revision #d76de10](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d76de10)\
  2018-07-27 07:35:36 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #499c8ab](https://github.com/mariadb-corporation/mariadb-connector-c/commit/499c8ab)\
  2018-07-27 07:23:16 +0200
  * Merge pull request #66 from grooverdan/[CONC-329](https://jira.mariadb.org/browse/CONC-329)-signed-char\_2
* [Revision #b19f6a4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b19f6a4)\
  2018-07-18 09:28:05 +1000
  * [CONC-329](https://jira.mariadb.org/browse/CONC-329): change pvio\_\*\_blocking to return int to accomidate SOCKET\_ERROR(-1)
* [Revision #d2ee129](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d2ee129)\
  2018-07-27 07:32:08 +0200
  * [CONC-297](https://jira.mariadb.org/browse/CONC-297): Fixed regression bug (which happend due to a bad merge)
* [Revision #1788e00](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1788e00)\
  2018-07-27 07:17:27 +0200
  * Fix for [CONC-332](https://jira.mariadb.org/browse/CONC-332): mysql\_change\_user doesn't reset server status
* [Revision #eb64582](https://github.com/mariadb-corporation/mariadb-connector-c/commit/eb64582)\
  2018-07-25 09:33:53 +0200
  * Debian layout changes/fixes
* [Revision #d3e06bc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d3e06bc)\
  2018-07-13 14:48:42 +0200
  * Added test for nested dynamic column
* [Revision #c95f86e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c95f86e)\
  2018-07-13 12:30:13 +0200
  * More coverity fixes
* [Revision #77fc17b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/77fc17b)\
  2018-07-06 17:39:07 +0200
  * remove coverity-scan, we do that in a separate branch coverity\_scan
* [Revision #3169da3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3169da3)\
  2018-07-06 12:36:41 +0200
  * .travis.yml fixes
* [Revision #23ec0ca](https://github.com/mariadb-corporation/mariadb-connector-c/commit/23ec0ca)\
  2018-07-06 09:29:26 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #c14a06f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c14a06f)\
  2018-07-04 17:50:32 +0200
  * Fix required for [ODBC-154](https://jira.mariadb.org/browse/ODBC-154)
* [Revision #b0f2e4e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b0f2e4e)\
  2018-07-06 09:28:24 +0200
  * Coverity fixes and travis integration
* [Revision #ffd9084](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ffd9084)\
  2018-07-04 07:56:17 +0200
  * Fixed comment for MY\_CHARSET\_INFO: csname is the name of the character set, while name is the name of the collation
* [Revision #41cc847](https://github.com/mariadb-corporation/mariadb-connector-c/commit/41cc847)\
  2018-07-04 07:37:03 +0200
  * Fix for [CONC-346](https://jira.mariadb.org/browse/CONC-346): Removed all OLD cmake policies - Symlink macro now uses cmake generator expression $\<TARGET\_FILE\_NAME:\*> - Since all plugins are built in the same directory, the location detection was removed for windows packaging - Installation of the windows \*.pdb for libmariadb now also uses a static path.
* [Revision #eda04fe](https://github.com/mariadb-corporation/mariadb-connector-c/commit/eda04fe)\
  2018-07-04 07:25:24 +0200
  * Fixed warning
* [Revision #6658605](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6658605)\
  2018-07-03 12:45:55 +0200
  * Skip test for [MDEV-16593](https://jira.mariadb.org/browse/MDEV-16593) (not fixed yet)
* [Revision #dc50976](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dc50976)\
  2018-07-03 11:22:31 +0200
  * Fix for travis tests: Older server versions don't support CREATE or REPLACE syntax.
* [Revision #a0d4b42](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a0d4b42)\
  2018-07-03 11:17:46 +0200
  * Fix for [CONC-345](https://jira.mariadb.org/browse/CONC-345): heap-use-after free in client\_mpvio\_read\_packet We need to check if pkt\_len is > 0 before the buffer content will be checked.
* [Revision #9e1fef0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9e1fef0)\
  2018-06-28 17:22:08 +0200
  * Fix for [CONC-344](https://jira.mariadb.org/browse/CONC-344): reset internal row counter before executing prepared statement
* [Revision #dd54e6f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dd54e6f)\
  2018-06-20 16:34:03 +0200
  * Typo in CMakeLists.txt WITH\_UNITTEST instead of
* [Revision #b937b75](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b937b75)\
  2018-06-14 06:51:50 +0200
  * Fix IS\_NUM macro ([MDEV-15263](https://jira.mariadb.org/browse/MDEV-15263))
* [Revision #5b01cd6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5b01cd6)\
  2018-06-13 17:28:50 +0200
  * Fix crash in mysql\_select\_db if db is null
* [Revision #3224654](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3224654)\
  2018-06-06 08:10:25 +0200
  * Bumped version number
* [Revision #82222e4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/82222e4)\
  2018-06-05 14:09:29 +0200
  * Merge pull request #63 from rasmushoj/master
* [Revision #ff5aac5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ff5aac5)\
  2018-05-28 11:17:28 +0000
  * [CONC-335](https://jira.mariadb.org/browse/CONC-335) Test latest Connector/C code as libmariadb in the latest versions of the server for 10.3 and 10.4 Added MTR testing with 10.3 and 10.4 branch

{% @marketo/form formid="4316" formId="4316" %}
