# MariaDB 11.4.6 Changelog

{% include "../../../.gitbook/includes/latest-11-4.md" %}

&#x20;<a href="../../mariadb-11-4-series/mariadb-11-4-6-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-11-4-6-changelog.md" class="button secondary">Changelog</a> <a href="../../mariadb-11-4-series/what-is-mariadb-114.md" class="button secondary">Overview of 11.4</a>

**Release date:** ?

For the highlights of this release, see the [release notes](https://mariadb.com/docs/release-notes/mariadb-community-server-release-notes/mariadb-11-4-series).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/11.4) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 10.11.12](../changelogs-mariadb-10-11-series/mariadb-10-11-12-changelog.md)
* Includes all fixes from [MariaDB 11.2.6](../changelogs-mariadb-11-2-series/mariadb-11-2-6-changelog.md)
* Includes all fixes from [MariaDB 11.3.2](../changelogs-mariadb-11-3-series/mariadb-11-3-2-changelog.md)
* Merge [Revision #63a5552e76](https://github.com/MariaDB/server/commit/63a5552e76) 2025-04-28 17:08:53 +0200 - Merge branch '10.11' into 11.4
* Merge [Revision #a8d4642375](https://github.com/MariaDB/server/commit/a8d4642375) 2025-04-26 10:53:02 +0200 - Merge branch '10.11' into 11.4
* [Revision #1c09b5eadb](https://github.com/MariaDB/server/commit/1c09b5eadb)\
  2025-04-24 13:07:12 +1000
  * packaging prep for Ubuntu Plucky
* [Revision #820114bd25](https://github.com/MariaDB/server/commit/820114bd25)\
  2025-04-20 11:06:52 +0200
  * new CC
* [Revision #616fb6831d](https://github.com/MariaDB/server/commit/616fb6831d)\
  2025-04-16 09:09:43 +0200
  * new libfmt
* [Revision #f844f65492](https://github.com/MariaDB/server/commit/f844f65492)\
  2025-04-20 12:56:15 +0300
  * mtr backup tests should not read local .my.cnf files
* [Revision #c76d17a917](https://github.com/MariaDB/server/commit/c76d17a917)\
  2025-03-27 18:02:37 +0700
  * [MDEV-36390](https://jira.mariadb.org/browse/MDEV-36390): Minor refactoring of the method get\_expr\_query at the classes sp\_instr\_cpush/sp\_instr\_cursor\_copy\_struct
* [Revision #7b3e02e1aa](https://github.com/MariaDB/server/commit/7b3e02e1aa)\
  2025-04-15 19:30:44 +0400
  * [MDEV-36565](https://jira.mariadb.org/browse/MDEV-36565) Assertion \`src != ((void \*)0)' failed in my\_casedn\_8bit
* [Revision #b6391d4e03](https://github.com/MariaDB/server/commit/b6391d4e03)\
  2025-04-14 23:07:07 -0400
  * [MDEV-36463](https://jira.mariadb.org/browse/MDEV-36463) Change expression\_cache name to subquery\_cache, and make appropriate changes to the test files
* [Revision #10c063f9f0](https://github.com/MariaDB/server/commit/10c063f9f0)\
  2025-03-22 12:45:13 +0400
  * [MDEV-36213](https://jira.mariadb.org/browse/MDEV-36213) Doubled memory usage (11.4.4 <-> 11.4.5)
* [Revision #0dad1458e7](https://github.com/MariaDB/server/commit/0dad1458e7)\
  2025-03-09 22:15:23 +0200
  * Add memory allocated by my\_once\_alloc() to memory status
* [Revision #75e11ec52c](https://github.com/MariaDB/server/commit/75e11ec52c)\
  2025-04-06 15:55:12 -0600
  * [MDEV-36238](https://jira.mariadb.org/browse/MDEV-36238) 11.4 follow-up: `Master_SSL_Verify_Server_Cert=0`
* [Revision #11324875b4](https://github.com/MariaDB/server/commit/11324875b4)\
  2025-04-14 16:50:16 +0200
  * [MDEV-33474](https://jira.mariadb.org/browse/MDEV-33474) Windows packaging - install runtime dependencies
* [Revision #2dc9b8b78e](https://github.com/MariaDB/server/commit/2dc9b8b78e)\
  2025-04-07 17:17:44 +0400
  * [MDEV-36216](https://jira.mariadb.org/browse/MDEV-36216) TO\_CHAR FM format not recognized in SQL\_MODE=Oracle
* [Revision #d3c9a2ee21](https://github.com/MariaDB/server/commit/d3c9a2ee21)\
  2025-02-03 10:42:16 -0500
  * [MDEV-35510](https://jira.mariadb.org/browse/MDEV-35510) ASAN build crashes during bootstrap
* [Revision #6cff704e57](https://github.com/MariaDB/server/commit/6cff704e57)\
  2024-11-27 16:10:09 +1100
  * [MDEV-35512](https://jira.mariadb.org/browse/MDEV-35512) remove all RPM compat packages
* [Revision #4a701e8ce4](https://github.com/MariaDB/server/commit/4a701e8ce4)\
  2024-12-12 14:39:09 +1100
  * [MDEV-35640](https://jira.mariadb.org/browse/MDEV-35640) Protocol\_text: handle errors in allocation
* [Revision #c6de1267dd](https://github.com/MariaDB/server/commit/c6de1267dd)\
  2025-04-10 10:04:14 +0530
  * [MDEV-35689](https://jira.mariadb.org/browse/MDEV-35689) InnoDB system tables cannot be optimized or defragmented
* [Revision #e176066a9e](https://github.com/MariaDB/server/commit/e176066a9e)\
  2025-04-04 11:16:31 +0700
  * [MDEV-36462](https://jira.mariadb.org/browse/MDEV-36462): Crash on `DECLARE spvar1 ROW TYPE OF cursor1` after a table recreation
* Merge [Revision #3ae8f114e2](https://github.com/MariaDB/server/commit/3ae8f114e2) 2025-04-02 10:15:08 +0300 - Merge 10.11 into 11.4
* [Revision #8a05f45bc3](https://github.com/MariaDB/server/commit/8a05f45bc3)\
  2025-03-31 18:07:15 +0400
  * [MDEV-36361](https://jira.mariadb.org/browse/MDEV-36361) Wrong utf8mb4\_0900\_bin alias for utf8mb4\_bin (should be utf8mb4\_nopad\_bin)
* [Revision #d9ff22063a](https://github.com/MariaDB/server/commit/d9ff22063a)\
  2025-03-25 10:20:00 +1100
  * update C/C
* Merge [Revision #28425cc276](https://github.com/MariaDB/server/commit/28425cc276) 2025-03-31 20:18:05 +0200 - Merge branch '10.11' into 11.4
* [Revision #30140c066d](https://github.com/MariaDB/server/commit/30140c066d)\
  2025-03-29 12:17:47 +0200
  * [MDEV-32148](https://jira.mariadb.org/browse/MDEV-32148) fixup: replace timestamp on Windows
* [Revision #f56099a95d](https://github.com/MariaDB/server/commit/f56099a95d)\
  2025-03-29 10:14:56 +0200
  * Fix some tests mainly on Valgrind
* [Revision #8010a4128d](https://github.com/MariaDB/server/commit/8010a4128d)\
  2025-03-28 19:20:16 +0100
  * [MDEV-36424](https://jira.mariadb.org/browse/MDEV-36424): binlog\_encryption.encrypted\_master\_switch\_to\_unencrypted\_gtid Fails in BB 11.4+
* Merge [Revision #f5bd250f5b](https://github.com/MariaDB/server/commit/f5bd250f5b) 2025-03-28 13:55:21 +0200 - Merge 10.11 into 11.4
* [Revision #3bbe11acd9](https://github.com/MariaDB/server/commit/3bbe11acd9)\
  2025-03-24 18:54:45 +0400
  * [MDEV-20912](https://jira.mariadb.org/browse/MDEV-20912) Add support for utf8mb4\_0900\_\* collations in MariaDB Server
* [Revision #02893e875b](https://github.com/MariaDB/server/commit/02893e875b)\
  2025-01-29 11:45:15 +0100
  * [MDEV-35969](https://jira.mariadb.org/browse/MDEV-35969) wsrep: set new status for service manager
* [Revision #0b8762822e](https://github.com/MariaDB/server/commit/0b8762822e)\
  2025-01-29 11:42:56 +0100
  * [MDEV-35969](https://jira.mariadb.org/browse/MDEV-35969) wsrep: add more details in service manager status
* Merge [Revision #38e420ba6e](https://github.com/MariaDB/server/commit/38e420ba6e) 2025-03-11 13:47:46 +0200 - Merge 10.11 into 11.4
* [Revision #e1277845a4](https://github.com/MariaDB/server/commit/e1277845a4)\
  2025-03-08 21:19:29 +0200
  * [MDEV-36206](https://jira.mariadb.org/browse/MDEV-36206): Fix mysqld deprecation warning
* [Revision #2183f302c8](https://github.com/MariaDB/server/commit/2183f302c8)\
  2025-03-05 11:44:38 +0200
  * [MDEV-33489](https://jira.mariadb.org/browse/MDEV-33489) atomic.alter\_table is too slow with SSL
* Merge [Revision #49a6baec56](https://github.com/MariaDB/server/commit/49a6baec56) 2025-03-03 11:07:56 +0200 - Merge 10.11 into 11.4
* [Revision #ef966af801](https://github.com/MariaDB/server/commit/ef966af801)\
  2025-01-23 20:20:00 +0200
  * [MDEV-30877](https://jira.mariadb.org/browse/MDEV-30877): Output cardinality for derived table ignores GROUP BY
* [Revision #cd03bf5c53](https://github.com/MariaDB/server/commit/cd03bf5c53)\
  2025-02-04 21:35:55 +0200
  * Fixed costs in JOIN\_TAB::estimate\_scan\_time() and HEAP
* [Revision #b7d67ceb5f](https://github.com/MariaDB/server/commit/b7d67ceb5f)\
  2025-02-08 17:39:27 +0400
  * [MDEV-36047](https://jira.mariadb.org/browse/MDEV-36047) Package body variables are not allowed as FETCH targets
* [Revision #6be0940f10](https://github.com/MariaDB/server/commit/6be0940f10)\
  2025-02-04 12:36:00 -0500
  * bump the VERSION

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
