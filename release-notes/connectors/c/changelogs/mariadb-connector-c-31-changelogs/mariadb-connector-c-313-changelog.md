# MariaDB Connector/C 3.1.3 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-313-release-notes.md)[Changelog](mariadb-connector-c-313-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 1 Aug 2019

For the highlights of this release, see the[release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-313-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #ed3a91c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ed3a91c)\
  2019-07-25 11:50:31 +0200
  * [CONC-429](https://jira.mariadb.org/browse/CONC-429): Don't allow to load unknown authentication plugins
* [Revision #59780f9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/59780f9)\
  2019-07-25 11:27:25 +0200
  * Revert "[CONC-429](https://jira.mariadb.org/browse/CONC-429): Don't allow to load unknown authentication plugins"
* [Revision #783fd10](https://github.com/mariadb-corporation/mariadb-connector-c/commit/783fd10)\
  2019-07-24 15:22:24 +0200
  * ed25519
* [Revision #59d214e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/59d214e)\
  2019-07-23 17:51:55 +0200
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 3.1
* [Revision #158a2d7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/158a2d7)\
  2019-07-22 09:40:53 +0200
  * \[MENT-26] Adding Azure CI testing
* [Revision #73c4cde](https://github.com/mariadb-corporation/mariadb-connector-c/commit/73c4cde)\
  2019-07-23 17:49:59 +0200
  * Fixed typo in CMakeLists.txt
* [Revision #acc270b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/acc270b)\
  2019-07-22 07:27:48 +0200
  * [CONC-429](https://jira.mariadb.org/browse/CONC-429): Don't allow to load unknown authentication plugins
* [Revision #5fa9c46](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5fa9c46)\
  2019-07-18 13:51:03 +0200
  * Merge branch '3.0' into 3.1
* [Revision #0c20765](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0c20765)\
  2019-07-18 13:42:29 +0200
  * Fix of memory leack in the test and end spaces.
* [Revision #07f6f95](https://github.com/mariadb-corporation/mariadb-connector-c/commit/07f6f95)\
  2019-07-17 08:22:19 +0200
  * Fix for Windows OpenSSL build: Link crypt and ws2\_32 in case OpenSSL is a newer version which was build with capi engine support
* [Revision #b396e76](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b396e76)\
  2019-07-16 17:33:57 +0200
  * Merge commit '970e929a09327fe5e642c0b5cb9f54a38677c855' into 3.1
* [Revision #970e929](https://github.com/mariadb-corporation/mariadb-connector-c/commit/970e929)\
  2019-07-16 17:30:57 +0200
  * Fix for [CONC-380](https://jira.mariadb.org/browse/CONC-380): Fix cmake warnings (CMake Policy CMP0077)
* [Revision #b5bd0e5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b5bd0e5)\
  2019-07-16 17:33:00 +0200
  * Merge commit '77d051e89d0b342333d951e66e53f2aea43f6e36' into 3.1
* [Revision #77d051e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/77d051e)\
  2019-07-16 08:52:24 +0200
  * Windows build fixes for OpenSSL
* [Revision #dc0f66f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dc0f66f)\
  2019-07-05 14:09:00 +0200
  * Post fix for [CONC-345](https://jira.mariadb.org/browse/CONC-345): removed semicolon
* [Revision #0f48913](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0f48913)\
  2019-07-05 11:42:12 +0200
  * Fix for [CONC-345](https://jira.mariadb.org/browse/CONC-345): heap-use-after-free in client\_mpvio\_read\_packet
* [Revision #2674447](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2674447)\
  2019-07-05 11:14:37 +0200
  * Fix short options
* [Revision #7406241](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7406241)\
  2019-07-05 08:25:21 +0200
  * Merge pull request #108 from nunojpg/3.1
* [Revision #88a6d82](https://github.com/mariadb-corporation/mariadb-connector-c/commit/88a6d82)\
  2019-04-08 07:46:29 +0200
  * Quote cmake variable as it might be empty
* [Revision #86829ab](https://github.com/mariadb-corporation/mariadb-connector-c/commit/86829ab)\
  2019-07-05 08:24:21 +0200
  * Merge pull request #115 from anklean/3.1
* [Revision #9cb1322](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9cb1322)\
  2019-06-19 10:09:39 +0800
  * fix bug [CONC-400](https://jira.mariadb.org/browse/CONC-400) error with sizeof("commit") in function mysql\_commit
* [Revision #7ba08bc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7ba08bc)\
  2019-07-05 08:23:26 +0200
  * Merge pull request #114 from EGuesnet/Fix-Big-Endian-Issue
* [Revision #3e5e318](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3e5e318)\
  2019-06-05 14:44:50 +0200
  * Big endian issue in libmariadb
* [Revision #723d58d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/723d58d)\
  2019-07-05 08:20:37 +0200
  * Merge pull request #110 from ykopel/patch-1
* [Revision #c6724de](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c6724de)\
  2019-05-13 17:03:20 +0300
  * Fix supporting in external curl
* [Revision #8c6c5e0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8c6c5e0)\
  2019-06-30 17:34:04 +0200
  * Merge commit '8823607e299d6028df87d3c389a44ca004311de5' into 3.1
* [Revision #8823607](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8823607)\
  2019-06-30 17:32:03 +0200
  * Follow up for [CONC-424](https://jira.mariadb.org/browse/CONC-424):
* [Revision #1e6919b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1e6919b)\
  2019-06-30 12:46:39 +0200
  * Merge branch '3.0' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 3.0
* [Revision #86a9e07](https://github.com/mariadb-corporation/mariadb-connector-c/commit/86a9e07)\
  2019-06-30 12:47:17 +0200
  * Merge commit 'd09ac51df3c35e569e91313affb58ae74fd3470a' into 3.1
* [Revision #d09ac51](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d09ac51)\
  2019-06-30 12:41:42 +0200
  * Workaround/Fix for [CONC-424](https://jira.mariadb.org/browse/CONC-424):
* [Revision #a0f0db4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a0f0db4)\
  2019-06-29 00:30:03 +0200
  * Merge branch '3.0' into 3.1
* [Revision #7305318](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7305318)\
  2019-06-26 20:58:29 +0200
  * take into account server's EXTRA\_VERSION
* [Revision #3927466](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3927466)\
  2019-06-26 13:01:45 +0200
  * Merge commit 'a0d2974bf29bf49fb8f9d1fd75fd2fa211df883d' into 3.1
* [Revision #a0d2974](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a0d2974)\
  2019-06-26 12:55:17 +0200
  * Merge pull request #111 from FaramosCZ/3.0
* [Revision #cc5489f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cc5489f)\
  2019-05-21 15:02:48 +0200
  * Fix overlinking issues
* [Revision #808f48a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/808f48a)\
  2019-06-26 12:43:22 +0200
  * Merge pull request #112 from Thermi/stringop-truncation
* [Revision #fe117c1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fe117c1)\
  2019-05-29 20:37:29 +0200
  * Do not overwrite final byte of array to make sure it's always zero
* [Revision #5e5bb66](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5e5bb66)\
  2019-06-26 09:18:38 +0200
  * Merge commit 'c6b344d730885051fdaf347f0d33c54ec22c415c' into 3.1
* [Revision #c6b344d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c6b344d)\
  2019-06-26 09:13:00 +0200
  * Fix for [CONC-423](https://jira.mariadb.org/browse/CONC-423): GnuTLS fails with "error reading authentication packet" with a TLSv1.3 connection
* [Revision #94d87e8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/94d87e8)\
  2019-06-24 18:10:30 +0200
  * Merge commit 'ff13dd446dcd6dd861026a8aa3cd23f3a9c759d3' into 3.1
* [Revision #ff13dd4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ff13dd4)\
  2019-06-24 18:07:53 +0200
  * [CONC-421](https://jira.mariadb.org/browse/CONC-421):
* [Revision #1c24dda](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1c24dda)\
  2019-06-15 09:26:08 +0200
  * Fix windows warning (missing prototype)
* [Revision #91a4352](https://github.com/mariadb-corporation/mariadb-connector-c/commit/91a4352)\
  2019-06-20 15:29:59 +0200
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 3.1
* [Revision #f5ac962](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f5ac962)\
  2019-06-19 11:08:30 -0400
  * bump the VERSION
* [Revision #690f74a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/690f74a)\
  2019-06-20 15:29:02 +0200
  * Fix for [MDEV-19807](https://jira.mariadb.org/browse/MDEV-19807)

{% @marketo/form formid="4316" formId="4316" %}
