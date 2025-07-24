# Connector/C 3.1.0 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.1.0/)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-310-release-notes.md)[Changelog](mariadb-connector-c-310-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-c/README.md)

**Release date:** 8 Apr 2019

For the highlights of this release, see the [release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-310-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #1285dc7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1285dc7)\
  2019-03-11 18:03:44 +0100
  * Fix compiler warning when using GnuTLS
* [Revision #2d5021d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2d5021d)\
  2019-03-09 19:44:47 +0100
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 3.1
* [Revision #4ac8030](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4ac8030)\
  2019-03-05 00:28:28 +0100
  * fix memory leaks to keep LeakSanitizer happy
* [Revision #9043f91](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9043f91)\
  2019-03-09 19:44:07 +0100
  * Merge remote-tracking branch 'origin/3.0' into 3.1
* [Revision #4ab51e7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4ab51e7)\
  2019-03-08 18:38:14 +0100
  * Fix for [CONC-301](https://jira.mariadb.org/browse/CONC-301):
* [Revision #255f343](https://github.com/mariadb-corporation/mariadb-connector-c/commit/255f343)\
  2019-03-05 05:56:12 +0100
  * Fixed year in copyright notice
* [Revision #8473246](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8473246)\
  2019-03-04 17:06:00 +0100
  * Fix authentication tests:
* [Revision #af47d1b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/af47d1b)\
  2019-03-03 14:03:20 +0100
  * Merge branch '3.0' into 3.1
* [Revision #f249150](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f249150)\
  2019-03-02 14:49:27 +0100
  * Don't close default connection in test\_conc392 in case we have to skip test
* [Revision #0cc2df4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0cc2df4)\
  2019-03-02 14:26:55 +0100
  * Follow up of 68d05007bbf0dd9ef725bddf312fbb72ed0c7d52:
* [Revision #68d0500](https://github.com/mariadb-corporation/mariadb-connector-c/commit/68d0500)\
  2019-03-02 07:54:06 +0100
  * Fix for [CONC-392](https://jira.mariadb.org/browse/CONC-392):
* [Revision #31ae127](https://github.com/mariadb-corporation/mariadb-connector-c/commit/31ae127)\
  2019-02-24 20:00:02 +0100
  * Fix for [MDEV-18721](https://jira.mariadb.org/browse/MDEV-18721) (Host option in configuration file is ignored.)
* [Revision #0acf529](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0acf529)\
  2019-02-19 08:44:19 +0100
  * Fix for [MDEV-18634](https://jira.mariadb.org/browse/MDEV-18634):
* [Revision #b6fa103](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b6fa103)\
  2019-02-12 19:30:57 +0100
  * bump version number to 3.0.10
* [Revision #a1469b4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a1469b4)\
  2019-02-11 20:13:17 +0100
  * Fix test for expired password.
* [Revision #4aad20d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4aad20d)\
  2019-02-18 20:16:23 +0100
  * Merge tag 'v3.0.9' into 3.1
* [Revision #beb9d5e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/beb9d5e)\
  2019-01-29 12:54:30 +0100
  * [MDEV-11340](https://jira.mariadb.org/browse/MDEV-11340) Allow multiple alternative authentication methods for the same user
* [Revision #1e4b08b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1e4b08b)\
  2019-01-15 20:56:37 +0100
  * [MDEV-11340](https://jira.mariadb.org/browse/MDEV-11340) Allow multiple alternative authentication methods for the same user
* [Revision #a4effc4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a4effc4)\
  2019-02-01 13:01:28 +0100
  * fix connection unit test to work in mtr
* [Revision #82355ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/82355ad)\
  2019-01-31 22:00:11 +0100
  * .gitignore
* [Revision #62e79ba](https://github.com/mariadb-corporation/mariadb-connector-c/commit/62e79ba)\
  2019-02-03 09:18:59 +0100
  * compilation on windows
* [Revision #cdf5eab](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cdf5eab)\
  2019-02-02 22:43:57 +0100
  * compiler warnings - unused variables
* [Revision #b6c3895](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b6c3895)\
  2019-02-04 16:05:19 +0100
  * Merge tag 'v3.0.8-release' into 3.1
* [Revision #0eafcd1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0eafcd1)\
  2019-02-03 19:18:45 +0100
  * Merge pull request #94 from sthibaul/3.1
* [Revision #a71ec85](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a71ec85)\
  2019-01-04 01:33:56 +0100
  * Tune symbol visibility on GNU/Hurd too
* [Revision #eda93a8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/eda93a8)\
  2019-01-24 18:35:20 +0100
  * Merge pull request #100 from markus456/3.1
* [Revision #4fd787d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4fd787d)\
  2019-01-24 15:52:15 +0200
  * Fix ROWS\_EVENT size
* [Revision #be02158](https://github.com/mariadb-corporation/mariadb-connector-c/commit/be02158)\
  2019-01-24 10:00:01 +0200
  * Add binlog checksum support
* [Revision #be86fb4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/be86fb4)\
  2019-01-18 14:09:29 +0200
  * Install mariadb\_rpl.h
* [Revision #78abc1d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/78abc1d)\
  2019-01-18 08:23:36 +0100
  * Merge pull request #97 from markus456/3.1
* [Revision #cb013c2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb013c2)\
  2019-01-02 07:28:45 +0200
  * Fix table map event processing
* [Revision #3b3b492](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3b3b492)\
  2018-12-19 05:29:44 +0100
  * Travis: Fix path for plugins
* [Revision #56631c5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/56631c5)\
  2018-12-18 13:48:54 +0100
  * Fix test for ed25519
* [Revision #a4b1070](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a4b1070)\
  2018-12-06 11:35:19 +0100
  * Added missing sha512 provider
* [Revision #212a9f6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/212a9f6)\
  2018-12-05 13:40:58 +0100
  * Fixed prototype for ps callback functions Connectori/Python callback fixes
* [Revision #655d902](https://github.com/mariadb-corporation/mariadb-connector-c/commit/655d902)\
  2018-12-03 13:44:08 +0100
  * [CONC-347](https://jira.mariadb.org/browse/CONC-347): Add function mysql\_stmt\_fetch\_field
* [Revision #e9b3aef](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e9b3aef)\
  2018-12-03 13:04:16 +0100
  * [CONC-348](https://jira.mariadb.org/browse/CONC-348): Add callback support for prepared statements
* [Revision #1888c14](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1888c14)\
  2018-12-02 18:28:38 +0100
  * Manual merge from [CONC-325](https://jira.mariadb.org/browse/CONC-325) branch: Initial implementation for binlog/replication API
* [Revision #b87845b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b87845b)\
  2018-12-02 16:58:30 +0100
  * [CONC-366](https://jira.mariadb.org/browse/CONC-366): Implementation of ed25519 authentication plugin
* [Revision #7d5511c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7d5511c)\
  2018-12-01 18:07:20 +0100
  * Fix warning in misc.c unittest
* [Revision #abce2a3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/abce2a3)\
  2018-12-01 16:46:46 +0100
  * [CONC-377](https://jira.mariadb.org/browse/CONC-377): Add IO Callback
* [Revision #3ffa60d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3ffa60d)\
  2018-12-01 14:31:13 +0100
  * Bumped version number to 3.1.0

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
