# MariaDB Connector/C 3.1.10 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3110-release-notes.md)[Changelog](mariadb-connector-c-3110-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-c/README.md)

**Release date:** 15 Sep 2020

For the highlights of this release, see the[release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3110-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #159540f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/159540f)\
  2020-09-17 10:41:01 +0200
  * OpenSSL fixes
* [Revision #086f810](https://github.com/mariadb-corporation/mariadb-connector-c/commit/086f810)\
  2020-09-16 07:44:05 +0200
  * Build fix for FreeBSD
* [Revision #f885593](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f885593)\
  2020-09-16 07:42:06 +0200
  * Don't load certificates in global context.
* [Revision #0157f3d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0157f3d)\
  2020-09-16 07:28:41 +0200
  * Revert "Follow up of [Revision #7b8b5dd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7b8b5dd)"
* [Revision #db385af](https://github.com/mariadb-corporation/mariadb-connector-c/commit/db385af)\
  2020-09-15 17:14:15 +0200
  * Follow up of [Revision #7b8b5dd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7b8b5dd)
* [Revision #7b8b5dd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7b8b5dd)\
  2020-09-14 17:21:19 +0200
  * Fix for [CONC-500](https://jira.mariadb.org/browse/CONC-500): Only use SSL\_CTX\_use\_certificate\_chain\_file to load and check the certificate.
* [Revision #0a97a81](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0a97a81)\
  2020-09-14 13:22:17 +0200
  * Fix build
* [Revision #7052619](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7052619)\
  2020-09-14 12:01:06 +0200
  * Added build option WITH\_ICONV.
* [Revision #ed9a6d4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ed9a6d4)\
  2020-09-14 10:00:03 +0200
  * Added missing MYSQL\_PORT in mariadb\_version.h
* [Revision #f73e9e8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f73e9e8)\
  2020-09-13 15:54:06 +0200
  * Merge pull request #145 from grooverdan/slash-run
* [Revision #3853baf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3853baf)\
  2020-08-24 10:42:24 +1000
  * nit change of /var/run -> /run
* [Revision #828f37e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/828f37e)\
  2020-09-13 15:47:41 +0200
  * Merge pull request #148 from EGuesnet/AIX2
* [Revision #4938864](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4938864)\
  2020-09-11 17:03:54 +0200
  * Parse GSSAPI flags on AIX
* [Revision #63c3ca5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/63c3ca5)\
  2020-09-11 17:03:23 +0200
  * Do not build static and shared library with the same name on AIX
* [Revision #fed2384](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fed2384)\
  2020-09-13 15:46:16 +0200
  * Merge pull request #149 from xantares/patch-1
* [Revision #9d7c233](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9d7c233)\
  2020-09-12 14:29:56 +0200
  * Fix include on case-sensitive fs
* [Revision #081ccbe](https://github.com/mariadb-corporation/mariadb-connector-c/commit/081ccbe)\
  2020-09-13 15:43:38 +0200
  * Add a temporary solution for travis
* [Revision #fb4e99f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fb4e99f)\
  2020-09-13 14:48:18 +0200
  * Fix for [CONC-498](https://jira.mariadb.org/browse/CONC-498)
* [Revision #448514a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/448514a)\
  2020-09-13 11:12:36 +0200
  * Some rework on mariadb\_config
* [Revision #29a3396](https://github.com/mariadb-corporation/mariadb-connector-c/commit/29a3396)\
  2020-09-12 10:58:33 +0200
  * [CONC-302](https://jira.mariadb.org/browse/CONC-302): Added support for SESSION\_TRACK\_GTIDS (MySQL server)
* [Revision #2c22f8e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2c22f8e)\
  2020-09-10 17:27:39 +0200
  * Don't test session tracking for character set against server < 10.3
* [Revision #a17e73f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a17e73f)\
  2020-09-10 16:30:04 +0200
  * Skip test\_conc496 if session\_tracking\_transaction\_info variable is not available/supported.
* [Revision #3e699a1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3e699a1)\
  2020-09-10 14:03:00 +0200
  * [CONC-496](https://jira.mariadb.org/browse/CONC-496): Added support for SESSION\_TRACK\_TRANSACTION\_STATE in ok packet
* [Revision #64a4212](https://github.com/mariadb-corporation/mariadb-connector-c/commit/64a4212)\
  2020-09-10 07:17:44 +0200
  * Fix for [CONC-495](https://jira.mariadb.org/browse/CONC-495)
* [Revision #d756d7b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d756d7b)\
  2020-09-09 12:20:45 +0200
  * Fix for [CONC-494](https://jira.mariadb.org/browse/CONC-494)
* [Revision #0185995](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0185995)\
  2020-09-09 12:19:27 +0200
  * Revert "Fix for [CONC-494](https://jira.mariadb.org/browse/CONC-494):"
* [Revision #8581caf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8581caf)\
  2020-09-09 10:24:55 +0200
  * Fix for [CONC-494](https://jira.mariadb.org/browse/CONC-494)
* [Revision #e66e45b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e66e45b)\
  2020-09-06 16:59:45 +0200
  * Travis fix
* [Revision #8102851](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8102851)\
  2020-09-06 14:26:34 +0200
  * Increase timeout for cursor and ps\_new
* [Revision #23005c6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/23005c6)\
  2020-09-06 07:50:35 +0200
  * Follow up of FIX for [CONC-492](https://jira.mariadb.org/browse/CONC-492)
* [Revision #8222338](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8222338)\
  2020-09-05 16:23:38 +0200
  * Fix for [CONC-492](https://jira.mariadb.org/browse/CONC-492)
* [Revision #804bf08](https://github.com/mariadb-corporation/mariadb-connector-c/commit/804bf08)\
  2020-09-03 17:49:42 +0200
  * removed additional check for ZLIB\_FOUND, since option REQIRED was specified before.
* [Revision #f3ed42f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f3ed42f)\
  2020-09-03 17:34:55 +0200
  * Fix for [MDEV-18818](https://jira.mariadb.org/browse/MDEV-18818)
* [Revision #abe3b1d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/abe3b1d)\
  2020-09-03 06:47:30 +0200
  * Bumped year in mariadb\_config
* [Revision #7decbb8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7decbb8)\
  2020-09-02 15:56:18 +0200
  * Travis fix for SkySQL test
* [Revision #9637689](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9637689)\
  2020-09-02 14:08:19 +0200
  * Test and travis modification for testing against SkySQL
* [Revision #c1c5a73](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c1c5a73)\
  2020-08-30 15:52:39 +0200
  * remove 10.0 tests from travis (10.0 is eoled)
* [Revision #f7fa090](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f7fa090)\
  2020-08-30 11:51:20 +0200
  * Merge pull request #144 from dfskoll/null-out-freed-pointers-to-avoid-potential-use-after-free
* [Revision #73dfd1e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/73dfd1e)\
  2020-08-13 14:16:29 -0400
  * Clear out free'd pointers for safety.
* [Revision #cc40655](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cc40655)\
  2020-08-30 11:49:53 +0200
  * Merge pull request #146 from grooverdan/redundant-gssapi-check
* [Revision #a22d942](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a22d942)\
  2020-08-26 10:29:13 +1000
  * [CONC-489](https://jira.mariadb.org/browse/CONC-489): FindGSSAPI occurs twice in CMakeList.txt
* [Revision #5e5e7b8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5e5e7b8)\
  2020-08-30 10:23:25 +0200
  * Skip SSL tests for TRAVIS
* [Revision #2019740](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2019740)\
  2020-08-29 14:51:30 +0200
  * Fix certificate generation for travis
* [Revision #49be7b2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/49be7b2)\
  2020-08-13 14:38:48 +0200
  * Merge pull request #124 from EGuesnet/AIX
* [Revision #5bd45f5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5bd45f5)\
  2020-01-23 11:38:30 +0100
  * iconv does not support LIBICONV\_PLUG flag on AIX
* [Revision #870540a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/870540a)\
  2020-01-23 11:33:32 +0100
  * getopt provided by a compatibility library on AIX
* [Revision #448dfbc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/448dfbc)\
  2020-01-09 17:14:56 +0100
  * AIX macro
* [Revision #a564133](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a564133)\
  2020-01-09 17:12:31 +0100
  * Correct compatibility typedef
* [Revision #5328f70](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5328f70)\
  2020-01-09 17:10:00 +0100
  * AIX specific code no more needed
* [Revision #a610ed5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a610ed5)\
  2020-07-08 06:44:54 +0200
  * Merge pull request #141 from evanmiller/strict-prototypes
* [Revision #70843c0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/70843c0)\
  2020-07-07 11:56:47 -0400
  * \[[CONC-381](https://jira.mariadb.org/browse/CONC-381)] Fix strict prototypes warning
* [Revision #24d71ce](https://github.com/mariadb-corporation/mariadb-connector-c/commit/24d71ce)\
  2020-06-27 07:08:26 +0200
  * Merge pull request #140 from cvicentiu/3.1-vicentiu
* [Revision #ee5c10b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ee5c10b)\
  2020-06-18 21:34:03 +0300
  * [MDEV-14811](https://jira.mariadb.org/browse/MDEV-14811) unit.conc\_misc fails in buildbot on bld-starfs-release in test\_conc49
* [Revision #5f21467](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5f21467)\
  2020-06-24 06:24:25 -0400
  * bump the VERSION

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
