# MariaDB 11.4.1 Changelog

The most recent release of [MariaDB 11.4](../../mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114.md) is:[**MariaDB 11.4.5**](../../mariadb-community-server-release-notes/mariadb-11-4-series/mariadb-11-4-5-release-notes.md) Stable (GA) [Download Now](https://mariadb.com/downloads/)[_Alternate download from mariadb.org_](https://downloads.mariadb.org/mariadb/11.4.5/)

[Download 11.4.1](https://downloads.mariadb.org/mariadb/11.4.1)[Release Notes](../../mariadb-community-server-release-notes/mariadb-11-4-series/mariadb-11-4-1-release-notes.md)[Changelog](mariadb-11-4-1-changelog.md)[Overview of 11.4](../../mariadb-community-server-release-notes/mariadb-11-4-series/what-is-mariadb-114.md)

**Release date:** 16 Feb 2024

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/mariadb-11-4-series/mariadb-11-4-1-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/server/tree/11.1) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Changes from [11.4.0](../../mariadb-community-server-release-notes/mariadb-11-4-series/mariadb-11-4-0-release-notes.md) are also included in this changelog
* Includes all fixes from [MariaDB 11.3.2](../changelogs-mariadb-11-3-series/mariadb-11-3-2-changelog.md)
* Merge [Revision #fa69b085b1](https://github.com/MariaDB/server/commit/fa69b085b1) 2024-02-15 13:53:21 +0100 - Merge branch '11.3' into 11.4
* [Revision #3ae6680eec](https://github.com/MariaDB/server/commit/3ae6680eec)\
  2024-02-14 23:49:33 +0100
  * update 32bit rdiffs
* [Revision #fe07ac31b1](https://github.com/MariaDB/server/commit/fe07ac31b1)\
  2024-02-14 16:19:01 +0100
  * [MDEV-31857](https://jira.mariadb.org/browse/MDEV-31857) fix galera.MW-284
* [Revision #8dee23cdee](https://github.com/MariaDB/server/commit/8dee23cdee)\
  2024-02-14 16:13:02 +0100
  * [MDEV-31857](https://jira.mariadb.org/browse/MDEV-31857) fix galera.galera\_var\_notify\_ssl\_ipv6
* [Revision #d6794aa410](https://github.com/MariaDB/server/commit/d6794aa410)\
  2023-12-20 17:52:52 +0200
  * Improve error message in mysqltest when sync\_with\_master fails
* [Revision #18dfcfdecf](https://github.com/MariaDB/server/commit/18dfcfdecf)\
  2023-12-03 21:42:44 +0200
  * [MDEV-31404](https://jira.mariadb.org/browse/MDEV-31404) Implement binlog\_space\_limit
* [Revision #9933a8cc88](https://github.com/MariaDB/server/commit/9933a8cc88)\
  2024-02-14 01:22:32 +0100
  * update C/C
* [Revision #2c445b5962](https://github.com/MariaDB/server/commit/2c445b5962)\
  2024-02-13 15:50:07 +0100
  * fix debian dependencies for mariadb-test
* [Revision #eeb5cbaece](https://github.com/MariaDB/server/commit/eeb5cbaece)\
  2024-02-14 14:59:16 +0100
  * [MDEV-33326](https://jira.mariadb.org/browse/MDEV-33326) Port Spider/ODBC from ES
* [Revision #9945d482af](https://github.com/MariaDB/server/commit/9945d482af)\
  2023-10-07 21:08:43 -0700
  * Deb: Stop shipping mariadb-plugin-spider separately, include in server
* [Revision #22e41dae88](https://github.com/MariaDB/server/commit/22e41dae88)\
  2024-01-04 23:46:52 +0100
  * [MDEV-32501](https://jira.mariadb.org/browse/MDEV-32501) KEY\_PERIOD\_USAGE reveals information to unprivileged user
* [Revision #5c2f8c017c](https://github.com/MariaDB/server/commit/5c2f8c017c)\
  2023-12-30 02:34:59 +0100
  * [MDEV-32503](https://jira.mariadb.org/browse/MDEV-32503) Queries from I\_S.KEY\_PERIOD\_USAGE do not obey case-sensitivity
* [Revision #261993f568](https://github.com/MariaDB/server/commit/261993f568)\
  2023-10-19 21:58:26 +0400
  * add period to buildbot\_suites.bat
* [Revision #d4b5f7a503](https://github.com/MariaDB/server/commit/d4b5f7a503)\
  2023-09-20 23:27:30 +0400
  * [MDEV-32205](https://jira.mariadb.org/browse/MDEV-32205) crash in get\_schema\_key\_period\_usage\_record without InnoDB
* [Revision #62d35a074f](https://github.com/MariaDB/server/commit/62d35a074f)\
  2023-09-20 18:23:16 +0400
  * Add Statement::sql\_command\_flags() function.
* [Revision #4246c0fa01](https://github.com/MariaDB/server/commit/4246c0fa01)\
  2023-08-30 01:04:34 +0400
  * [MDEV-22597](https://jira.mariadb.org/browse/MDEV-22597) Add views for periods in information\_schema
* [Revision #85f9df29c0](https://github.com/MariaDB/server/commit/85f9df29c0)\
  2024-01-14 15:24:31 +0100
  * sql\_show: reduce ifdefs around grants checks
* [Revision #ba1c5914aa](https://github.com/MariaDB/server/commit/ba1c5914aa)\
  2024-02-12 15:59:32 +0100
  * fix get\_schema\_privileges\_for\_show
* [Revision #16ad26a367](https://github.com/MariaDB/server/commit/16ad26a367)\
  2024-01-12 21:22:35 +0100
  * sql\_show: extract get\_schema\_privileges\_for\_show
* [Revision #eb2481280f](https://github.com/MariaDB/server/commit/eb2481280f)\
  2024-01-12 21:22:16 +0100
  * sql\_show: Fix narrowing conversion from the get\_column\_grant return result.
* [Revision #8a882827ff](https://github.com/MariaDB/server/commit/8a882827ff)\
  2023-08-29 20:41:12 +0400
  * cleanup: add store\_yesno() for fields that can only take "YES"/"NO" values
* [Revision #711b8671be](https://github.com/MariaDB/server/commit/711b8671be)\
  2023-11-16 11:58:01 +1100
  * pr template: ask about release notes
* [Revision #4eac842c8f](https://github.com/MariaDB/server/commit/4eac842c8f)\
  2024-02-09 02:18:32 +0100
  * [MDEV-33430](https://jira.mariadb.org/browse/MDEV-33430) - Fix self-signed certificate errors on Windows
* [Revision #9500575f0a](https://github.com/MariaDB/server/commit/9500575f0a)\
  2024-02-08 15:58:26 +0400
  * [MDEV-33428](https://jira.mariadb.org/browse/MDEV-33428) Error messages ER\_PACKAGE\_ROUTINE\_\* are not good enough
* [Revision #9b1ea69049](https://github.com/MariaDB/server/commit/9b1ea69049)\
  2024-02-05 05:56:53 -0700
  * Revert "[MDEV-7850](https://jira.mariadb.org/browse/MDEV-7850): Extend GTID Binlog Events with Thread Id"
* [Revision #e30e9fc628](https://github.com/MariaDB/server/commit/e30e9fc628)\
  2024-02-05 14:41:44 +0400
  * [MDEV-33386](https://jira.mariadb.org/browse/MDEV-33386) Wrong error message on `GRANT .. ON PACKAGE no_such_package ..`
* [Revision #2e83ab4126](https://github.com/MariaDB/server/commit/2e83ab4126)\
  2023-10-15 16:03:14 +0200
  * [MDEV-32473](https://jira.mariadb.org/browse/MDEV-32473) --disable-ssl doesn't disable it
* [Revision #6b900330b9](https://github.com/MariaDB/server/commit/6b900330b9)\
  2023-09-22 13:16:35 +0200
  * show in mariadb cli whether server cert was verified
* [Revision #853bdf576f](https://github.com/MariaDB/server/commit/853bdf576f)\
  2023-09-15 12:33:52 +0200
  * auto-disable --ssl-verify-server-cert in clients, if
* [Revision #abcd23add2](https://github.com/MariaDB/server/commit/abcd23add2)\
  2023-09-04 15:32:36 +0200
  * [MDEV-31857](https://jira.mariadb.org/browse/MDEV-31857) enable --ssl-verify-server-cert by default in the internal client
* [Revision #e0c30390a7](https://github.com/MariaDB/server/commit/e0c30390a7)\
  2023-09-03 09:44:01 +0200
  * [MDEV-31855](https://jira.mariadb.org/browse/MDEV-31855) validate ssl certificates using client password in the internal client
* [Revision #386df8793b](https://github.com/MariaDB/server/commit/386df8793b)\
  2023-09-08 12:29:48 +0200
  * disable SSL via named pipes in the internal client
* [Revision #3c36ed18ba](https://github.com/MariaDB/server/commit/3c36ed18ba)\
  2023-09-04 15:35:08 +0200
  * free mysql->connector\_fd correctly in the internal client
* [Revision #2f13f7d78f](https://github.com/MariaDB/server/commit/2f13f7d78f)\
  2023-09-03 22:34:03 +0200
  * change how self-signed certs are accepted by internal client
* [Revision #05a421eb36](https://github.com/MariaDB/server/commit/05a421eb36)\
  2023-09-02 21:43:36 +0200
  * cleanup: X509\_check\_host() in the internal client
* [Revision #f4e174e113](https://github.com/MariaDB/server/commit/f4e174e113)\
  2023-09-02 15:09:48 +0200
  * cleanup: ssl handling in the internal rpl client
* [Revision #e951edd80b](https://github.com/MariaDB/server/commit/e951edd80b)\
  2023-08-30 14:41:32 +0200
  * [MDEV-31857](https://jira.mariadb.org/browse/MDEV-31857) enable --ssl-verify-server-cert by default
* [Revision #ea921fd836](https://github.com/MariaDB/server/commit/ea921fd836)\
  2023-08-30 22:17:26 +0200
  * enable --ssl in the server by default
* [Revision #9f93630ded](https://github.com/MariaDB/server/commit/9f93630ded)\
  2023-08-23 17:45:57 +0200
  * [MDEV-31856](https://jira.mariadb.org/browse/MDEV-31856) use ephemeral ssl certificates
* [Revision #d33a8ab107](https://github.com/MariaDB/server/commit/d33a8ab107)\
  2023-08-23 17:45:21 +0200
  * wrong error for bare --ssl on the server side
* [Revision #d772c4fb04](https://github.com/MariaDB/server/commit/d772c4fb04)\
  2023-08-23 15:23:22 +0200
  * cleanup
* [Revision #68f0af2bf1](https://github.com/MariaDB/server/commit/68f0af2bf1)\
  2023-08-22 22:49:14 +0200
  * test SSL MitM attack
* [Revision #bac0f8999d](https://github.com/MariaDB/server/commit/bac0f8999d)\
  2023-09-01 10:25:53 +0200
  * client support for --ssl-fp and --ssl--fplist
* [Revision #1ef1bab99e](https://github.com/MariaDB/server/commit/1ef1bab99e)\
  2023-08-21 16:25:56 +0200
  * [MDEV-31855](https://jira.mariadb.org/browse/MDEV-31855) validate ssl certificates using client password
* [Revision #585c096aa5](https://github.com/MariaDB/server/commit/585c096aa5)\
  2023-08-30 16:56:23 +0200
  * cleanup: unify client's setting of ssl options
* [Revision #03094bbc8a](https://github.com/MariaDB/server/commit/03094bbc8a)\
  2023-09-27 16:03:11 +0200
  * cleanup: octet2hex takes an uchar\* argument
* [Revision #d7699c51eb](https://github.com/MariaDB/server/commit/d7699c51eb)\
  2023-08-30 10:00:30 +0200
  * test.cnf files should !include default\_my.cnf
* [Revision #ec5403ffb3](https://github.com/MariaDB/server/commit/ec5403ffb3)\
  2023-08-21 11:08:37 +0200
  * clarify CR\_OK\_HANDSHAKE\_COMPLETE
* [Revision #75bfb4b8a3](https://github.com/MariaDB/server/commit/75bfb4b8a3)\
  2023-09-20 18:48:22 +0200
  * deprecate SQL\_NOTES variable in favor of NOTE\_VERBOSITY
* [Revision #22da0de6d9](https://github.com/MariaDB/server/commit/22da0de6d9)\
  2023-08-31 13:43:22 +0200
  * gitignore scripts/mariadb\_sys\_schema.sql
* [Revision #2f5174e556](https://github.com/MariaDB/server/commit/2f5174e556)\
  2024-02-01 02:14:23 +0100
  * [MDEV-33075](https://jira.mariadb.org/browse/MDEV-33075) Resolve server shutdown issues on macOS, Solaris, and FreeBSD
* [Revision #b0e77c08e5](https://github.com/MariaDB/server/commit/b0e77c08e5)\
  2023-12-06 15:09:44 +0100
  * [MDEV-32216](https://jira.mariadb.org/browse/MDEV-32216) Option --parallel in mariadb-import
* [Revision #a5802ed51e](https://github.com/MariaDB/server/commit/a5802ed51e)\
  2023-11-23 23:33:28 +0100
  * [MDEV-32216](https://jira.mariadb.org/browse/MDEV-32216) add tests for mariadb-dump --parallel
* [Revision #4532dae016](https://github.com/MariaDB/server/commit/4532dae016)\
  2023-11-23 17:26:12 +0100
  * [MDEV-32216](https://jira.mariadb.org/browse/MDEV-32216) option --parallel/-j for mariadb-dump to increase parallelism
* [Revision #ec5db6409d](https://github.com/MariaDB/server/commit/ec5db6409d)\
  2023-11-23 16:58:28 +0100
  * [MDEV-32216](https://jira.mariadb.org/browse/MDEV-32216) Connection pool with asynchronous query execution.
* [Revision #9766a834f7](https://github.com/MariaDB/server/commit/9766a834f7)\
  2023-11-16 17:19:25 +0100
  * [MDEV-32216](https://jira.mariadb.org/browse/MDEV-32216) preparation - cleanup mysqldump.cc code
* [Revision #a553d55bb6](https://github.com/MariaDB/server/commit/a553d55bb6)\
  2023-11-13 09:32:51 +0100
  * [MDEV-32216](https://jira.mariadb.org/browse/MDEV-32216) Compile mysqldump as C++ (preparation for using connection pool)
* [Revision #d039346a7a](https://github.com/MariaDB/server/commit/d039346a7a)\
  2023-09-08 13:12:49 +0200
  * [MDEV-4991](https://jira.mariadb.org/browse/MDEV-4991): GTID binlog indexing
* [Revision #20741b9237](https://github.com/MariaDB/server/commit/20741b9237)\
  2024-01-24 12:18:18 +1100
  * [MDEV-28861](https://jira.mariadb.org/browse/MDEV-28861) Deprecate spider table options by comment/connection
* [Revision #d07908609f](https://github.com/MariaDB/server/commit/d07908609f)\
  2024-01-23 10:57:31 +0200
  * Update 11.4 HELP
* [Revision #c37b2087b4](https://github.com/MariaDB/server/commit/c37b2087b4)\
  2023-07-10 18:53:19 +0300
  * [MDEV-7850](https://jira.mariadb.org/browse/MDEV-7850): Extend GTID Binlog Events with Thread Id
* [Revision #8bf9f21855](https://github.com/MariaDB/server/commit/8bf9f21855)\
  2023-11-24 22:31:18 +0800
  * [MDEV-32894](https://jira.mariadb.org/browse/MDEV-32894) mysqlbinlog flashback support binlog\_row\_image FULL\_NODUP mode
* [Revision #f552febe43](https://github.com/MariaDB/server/commit/f552febe43)\
  2023-11-17 17:41:23 +0000
  * [MDEV-30879](https://jira.mariadb.org/browse/MDEV-30879) Add support for up to BASE 62 to CONV()
* [Revision #be6d48fd53](https://github.com/MariaDB/server/commit/be6d48fd53)\
  2023-12-20 08:17:02 +0800
  * [MDEV-33049](https://jira.mariadb.org/browse/MDEV-33049) Assertion \`marked\_for\_write\_or\_computed()' failed in bool Field\_new\_decimal::store\_value(const my\_decimal\*, int\*)
* Merge [Revision #d136169e39](https://github.com/MariaDB/server/commit/d136169e39) 2024-01-10 15:30:42 +0200 - Merge 11.3 into 11.4
* [Revision #c0c1c80346](https://github.com/MariaDB/server/commit/c0c1c80346)\
  2024-01-08 13:06:16 +0100
  * [MDEV-22164](https://jira.mariadb.org/browse/MDEV-22164) log a warning when WITHOUT VALIDATION was used
* [Revision #4089296a57](https://github.com/MariaDB/server/commit/4089296a57)\
  2024-01-08 10:13:03 +0100
  * [MDEV-22164](https://jira.mariadb.org/browse/MDEV-22164) revert "make THAN optional"
* Merge [Revision #7ee16b1e29](https://github.com/MariaDB/server/commit/7ee16b1e29) 2024-01-05 14:53:03 +0200 - Merge 11.3 into 11.4
* [Revision #3fad2b1155](https://github.com/MariaDB/server/commit/3fad2b1155)\
  2023-12-22 13:17:55 +0100
  * [MDEV-33096](https://jira.mariadb.org/browse/MDEV-33096) mysys/my\_timezone.cc does not compile on AIX
* [Revision #03fa2c3487](https://github.com/MariaDB/server/commit/03fa2c3487)\
  2023-12-21 23:50:59 +0100
  * fix sporadic test failures caused by InnoDB #record estimation
* Merge [Revision #c154aafe1a](https://github.com/MariaDB/server/commit/c154aafe1a) 2023-12-21 15:40:55 +0100 - Merge remote-tracking branch '11.3' into 11.4
* [Revision #aed9c656a9](https://github.com/MariaDB/server/commit/aed9c656a9)\
  2023-09-04 15:28:50 +0400
  * [MDEV-32101](https://jira.mariadb.org/browse/MDEV-32101) CREATE PACKAGE \[BODY] for sql\_mode=DEFAULT
* [Revision #9bd95e914f](https://github.com/MariaDB/server/commit/9bd95e914f)\
  2023-12-01 19:14:13 +1100
  * [MDEV-32923](https://jira.mariadb.org/browse/MDEV-32923): drop errmsg-utf8.txt from packaging
* [Revision #875377ad82](https://github.com/MariaDB/server/commit/875377ad82)\
  2023-12-14 17:04:54 +1100
  * [MDEV-27576](https://jira.mariadb.org/browse/MDEV-27576) Use reverse index for max/min optimization
* [Revision #70de4075a1](https://github.com/MariaDB/server/commit/70de4075a1)\
  2023-12-07 17:28:45 +0300
  * [MDEV-24486](https://jira.mariadb.org/browse/MDEV-24486) Rename the view sys.table\_privileges to sys.privileges\_by\_table\_by\_level
* [Revision #5462b61b0c](https://github.com/MariaDB/server/commit/5462b61b0c)\
  2023-12-06 18:44:38 +0300
  * [MDEV-22164](https://jira.mariadb.org/browse/MDEV-22164) without validation for exchange partition/convert in
* [Revision #485773adce](https://github.com/MariaDB/server/commit/485773adce)\
  2023-12-07 13:09:31 +0300
  * check\_digest() tests
* [Revision #1a5e69b42b](https://github.com/MariaDB/server/commit/1a5e69b42b)\
  2023-11-16 16:54:16 +0700
  * [MDEV-24486](https://jira.mariadb.org/browse/MDEV-24486) Add `table_privileges` view to the `sys` schema
* [Revision #6b2287fff2](https://github.com/MariaDB/server/commit/6b2287fff2)\
  2023-09-19 15:47:29 +1000
  * [MDEV-15543](https://jira.mariadb.org/browse/MDEV-15543): tmpfile.d not for datadir
* [Revision #a119c5f998](https://github.com/MariaDB/server/commit/a119c5f998)\
  2023-10-26 17:24:22 +0800
  * [MDEV-32589](https://jira.mariadb.org/browse/MDEV-32589) FULL\_NODUP mode for binlog\_row\_image
* [Revision #6218b5f7cb](https://github.com/MariaDB/server/commit/6218b5f7cb)\
  2023-11-22 18:40:53 +1100
  * [MDEV-32567](https://jira.mariadb.org/browse/MDEV-32567) Remove thr\_alarm from server codebase - socket activation fix
* [Revision #f8600b1755](https://github.com/MariaDB/server/commit/f8600b1755)\
  2023-10-26 18:12:09 +0200
  * [MDEV-32567](https://jira.mariadb.org/browse/MDEV-32567) Remove thr\_alarm from server codebase
* [Revision #013fc02a23](https://github.com/MariaDB/server/commit/013fc02a23)\
  2023-10-26 15:02:35 +0200
  * [MDEV-32567](https://jira.mariadb.org/browse/MDEV-32567) Remove thr\_alarm from server codebase
* [Revision #3424ed7d42](https://github.com/MariaDB/server/commit/3424ed7d42)\
  2023-09-29 12:37:10 +0200
  * [MDEV-32189](https://jira.mariadb.org/browse/MDEV-32189) Use icu for timezones on windows
* Merge [Revision #bb8e1bf7a2](https://github.com/MariaDB/server/commit/bb8e1bf7a2) 2023-11-21 15:43:20 +0100 - Merge 11.3 into 11.4
* [Revision #99a3fe54d9](https://github.com/MariaDB/server/commit/99a3fe54d9)\
  2023-11-14 09:24:46 +0200
  * [MDEV-31273](https://jira.mariadb.org/browse/MDEV-31273): Precompute binlog checksums
* [Revision #9e457cbe50](https://github.com/MariaDB/server/commit/9e457cbe50)\
  2023-10-12 12:53:55 +1100
  * [MDEV-32439](https://jira.mariadb.org/browse/MDEV-32439) INSERT IGNORE on constraints result in ERROR rather than warning
* [Revision #b0379ea4b3](https://github.com/MariaDB/server/commit/b0379ea4b3)\
  2023-11-10 12:45:55 +0400
  * Cleanup: Adding "const" to the member Spvar\_definition::m\_column\_type\_ref
* [Revision #b8f9f796ff](https://github.com/MariaDB/server/commit/b8f9f796ff)\
  2023-06-13 11:41:44 +0200
  * [MDEV-31273](https://jira.mariadb.org/browse/MDEV-31273): Precompute binlog checksums
* [Revision #24c923d498](https://github.com/MariaDB/server/commit/24c923d498)\
  2023-08-23 11:48:08 +0200
  * [MDEV-31273](https://jira.mariadb.org/browse/MDEV-31273): Refactor MYSQL\_BIN\_LOG::write\_cache()
* [Revision #8eee9806fb](https://github.com/MariaDB/server/commit/8eee9806fb)\
  2023-07-27 15:46:57 +0200
  * [MDEV-31273](https://jira.mariadb.org/browse/MDEV-31273): Eliminate Log\_event::checksum\_alg
* [Revision #77bd1beac8](https://github.com/MariaDB/server/commit/77bd1beac8)\
  2023-07-11 23:30:04 +0200
  * [MDEV-31273](https://jira.mariadb.org/browse/MDEV-31273): Replace Log\_event::writer with function parameter
* [Revision #d8dda7c14f](https://github.com/MariaDB/server/commit/d8dda7c14f)\
  2023-10-09 13:43:10 +0200
  * 11.4 branch
