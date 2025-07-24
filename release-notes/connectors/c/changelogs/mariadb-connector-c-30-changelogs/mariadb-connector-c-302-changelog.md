# Connector/C 3.0.2 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.2)[Release Notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-302-release-notes.md)[Changelog](mariadb-connector-c-302-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 20 Jul 2017

For the highlights of this release, see the [release notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-302-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #35d6fb1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/35d6fb1)\
  2017-07-19 11:29:42 +0200
  * Fixed windows build: taget name for sha256 password plugin wasn't specified
* [Revision #d9bc990](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d9bc990)\
  2017-07-18 16:15:36 +0200
  * Fix for [MDEV-13317](https://jira.mariadb.org/browse/MDEV-13317): PHP5 crashes
* [Revision #e9b7f21](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e9b7f21)\
  2017-07-12 06:32:35 +0200
  * added my.cnf option server-public-key-path for sha256 authentication plugin
* [Revision #ae06903](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ae06903)\
  2017-07-04 11:42:05 +0200
  * followup for e2df6d2: default directories, files, and groups
* [Revision #3f356c0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3f356c0)\
  2017-07-07 11:18:24 +0200
  * Fix for [MDEV-13270](https://jira.mariadb.org/browse/MDEV-13270): Wrong output for mariadb\_config on OSX
* [Revision #0f11352](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0f11352)\
  2017-07-04 13:56:38 +0200
  * Fixed compiler warnings
* [Revision #c596c16](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c596c16)\
  2017-07-01 15:39:08 +0200
  * Fix for [CONC-252](https://jira.mariadb.org/browse/CONC-252): All functions which are supported by libmysql use now unsigned long as length parameter instead of size\_t
* [Revision #3fab8ce](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3fab8ce)\
  2017-07-01 15:36:47 +0200
  * Fix for [MDEV-12889](https://jira.mariadb.org/browse/MDEV-12889): Added version info for shared object: libmysqlclient\_18 node contains all symbols for libmysql compatibiliry libmariadb\_3 node contains all mariadb specific symbols which are not supported by libmysql
* [Revision #2d27bd7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2d27bd7)\
  2017-06-30 14:02:47 +0200
  * Merge remote-tracking branch 'origin/10.2-server'
* [Revision #f50c465](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f50c465)\
  2017-06-30 14:01:11 +0200
  * Merge branch '10.2-server' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 10.2-server
* [Revision #b9b030f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b9b030f)\
  2017-06-27 16:30:58 +0200
  * compilation failure
* [Revision #6e156a6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6e156a6)\
  2017-06-30 14:00:28 +0200
  * Fixes for bigendian systems ([CONC-252](https://jira.mariadb.org/browse/CONC-252), [CONC-265](https://jira.mariadb.org/browse/CONC-265))
* [Revision #28f4832](https://github.com/mariadb-corporation/mariadb-connector-c/commit/28f4832)\
  2017-06-25 14:26:24 +0200
  * Merge branch '10.2-server' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 10.2-server
* [Revision #1ffe387](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1ffe387)\
  2017-06-24 12:07:54 +0200
  * fix server version detection
* [Revision #1c8ccfe](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1c8ccfe)\
  2017-06-24 01:10:40 +0200
  * [MDEV-12423](https://jira.mariadb.org/browse/MDEV-12423) install fails to create/install symlinks to mysqlclient compat libs
* [Revision #e2df6d2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e2df6d2)\
  2017-06-25 14:14:55 +0200
  * Fix for [MDEV-12965](https://jira.mariadb.org/browse/MDEV-12965) and [MDEV-13100](https://jira.mariadb.org/browse/MDEV-13100): If no configuration file and no configuration group was specified, Connector/C ddoesn't read any configurationm files. By default the follwing groups will be read: - client - client-server - client-mariadb
* [Revision #6f113bb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6f113bb)\
  2017-06-14 14:55:05 +0200
  * Merge remote-tracking branch 'origin/master' into 10.2-server
* [Revision #e5ce85b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e5ce85b)\
  2017-06-08 16:39:04 +0200
  * Fix for [MDEV-13040](https://jira.mariadb.org/browse/MDEV-13040): mariadb\_stmt.h contains C++ comments
* [Revision #6fde63f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6fde63f)\
  2017-06-07 14:09:41 +0200
  * Added autogenerated file mysqld\_errmsg.h
* [Revision #422d0f7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/422d0f7)\
  2017-06-07 10:35:35 +0200
  * Added MYSQL\_VERSION\_ID (beside MARIADB\_VERSION\_ID)
* [Revision #90fd0cd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/90fd0cd)\
  2017-06-25 14:14:55 +0200
  * Fix for [MDEV-12965](https://jira.mariadb.org/browse/MDEV-12965) and [MDEV-13100](https://jira.mariadb.org/browse/MDEV-13100): If no configuration file and no configuration group was specified, Connector/C ddoesn't read any configurationm files. By default the follwing groups will be read: - client - client-server - client-mariadb
* [Revision #ff4bfdf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ff4bfdf)\
  2017-06-14 14:04:00 +0200
  * Added conversion tests for bulk
* [Revision #1ea7be3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1ea7be3)\
  2017-06-14 11:12:59 +0200
  * Merge remote-tracking branch 'origin/[MDEV-12471](https://jira.mariadb.org/browse/MDEV-12471)'
* [Revision #e50571e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e50571e)\
  2017-05-15 14:11:59 +0200
  * Disallow bulk execution if parameter count is 0
* [Revision #d0f9234](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d0f9234)\
  2017-05-01 15:05:49 +0200
  * [MDEV-12471](https://jira.mariadb.org/browse/MDEV-12471): BULK Command
* [Revision #08450df](https://github.com/mariadb-corporation/mariadb-connector-c/commit/08450df)\
  2017-04-24 15:45:58 +0200
  * initial implementation for [MDEV-12471](https://jira.mariadb.org/browse/MDEV-12471)
* [Revision #06d2490](https://github.com/mariadb-corporation/mariadb-connector-c/commit/06d2490)\
  2017-06-13 18:19:07 +0000
  * [MDEV-11159](https://jira.mariadb.org/browse/MDEV-11159) Add support for sending proxy protocol header
* [Revision #dce70b6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dce70b6)\
  2017-05-26 15:14:29 +0000
  * On Windows, link static libmariadbclient to shared library, instead of using object libraries.
* [Revision #b359d2d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b359d2d)\
  2017-05-11 17:20:51 +0200
  * Fix for [CONC-253](https://jira.mariadb.org/browse/CONC-253): Fixed compiler warnings in gssapi\_client.c Since trace\_example, aurora and replication plugins have experimental status, they are no longer build by default (=OFF).
* [Revision #467a193](https://github.com/mariadb-corporation/mariadb-connector-c/commit/467a193)\
  2017-05-10 13:29:58 +0200
  * Windows fixes: fix for timeout failures in buildbot fixed sha256 password plugin: instead of using mysql\_ssl\_cipher, we rely on client\_flag & CLIENT\_SSL to check if a secure connection is used.
* [Revision #4db860e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4db860e)\
  2017-05-10 13:28:25 +0200
  * Fix for [MDEV-12763](https://jira.mariadb.org/browse/MDEV-12763): Don't use deprecated API calls with OpenSSL 1.1
* [Revision #10d3269](https://github.com/mariadb-corporation/mariadb-connector-c/commit/10d3269)\
  2017-05-10 00:45:25 +0200
  * Fix build on Windows. Due to linking issue - unresolved symbol mysql\_get\_ssl\_cipher(), disable building sha32\_password pluugin on Windows for now.
* [Revision #e14ed01](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e14ed01)\
  2017-05-09 18:27:52 +0200
  * fix connection unit test
* [Revision #d2aec41](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d2aec41)\
  2017-05-09 16:40:09 +0200
  * Minor fixes: fixed compiler warnings in openssl.c and dialog.c fixed timeout setting (was wrong in a previous commit) disabled session tracking test
* [Revision #25a97fc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/25a97fc)\
  2017-05-08 18:47:57 +0200
  * Fix for [CONC-250](https://jira.mariadb.org/browse/CONC-250): Added support for wildcards and SAN
* [Revision #5c4cf7a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5c4cf7a)\
  2017-05-08 14:12:17 +0200
  * Implementation of SHA256 authentication plugin ([CONC-229](https://jira.mariadb.org/browse/CONC-229)). On Windows the sha256 plugin doesn't need any external TLS/Crypto libraries, it uses windows cryto library. On non Windws platforms the plugin requires OpenSSL (GnuTLS doesn't support OAEP v2.0 padding yet)
* [Revision #a86b36d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a86b36d)\
  2017-05-08 13:55:21 +0200
  * [CONC-250](https://jira.mariadb.org/browse/CONC-250): SSL hostname verification for SubjectAltNames Add hostname verification for SAN (OpenSSL)
* [Revision #6846f6a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6846f6a)\
  2017-05-07 07:50:29 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #b4681a2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b4681a2)\
  2017-05-02 11:58:50 +0200
  * Removed dump information, which was previously added by mistake
* [Revision #99d054e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/99d054e)\
  2017-05-07 07:46:43 +0200
  * Fix for [MDEV-12578](https://jira.mariadb.org/browse/MDEV-12578): Connector/C doesn't read .my.cnf file in home directory.
* [Revision #44a740c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/44a740c)\
  2017-04-10 06:23:25 +0200
  * Fix for [CONC-247](https://jira.mariadb.org/browse/CONC-247): merge 8b3695271c (error check for timeout on sockets=
* [Revision #bde93e8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bde93e8)\
  2017-04-03 18:12:13 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #d138735](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d138735)\
  2017-04-01 18:15:48 +0200
  * avoid undefined behavior in ma\_ll2str
* [Revision #be34e12](https://github.com/mariadb-corporation/mariadb-connector-c/commit/be34e12)\
  2017-03-31 14:30:04 +0200
  * remove ctx hooks after the successful reconnect
* [Revision #e9868bf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e9868bf)\
  2017-03-26 17:04:23 +0200
  * correct mthd\_stmt\_flush\_unbuffered() logic
* [Revision #8220d0b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8220d0b)\
  2017-03-27 14:03:39 +0200
  * .gitignore
* [Revision #50fb1b2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/50fb1b2)\
  2017-03-29 21:02:10 +0000
  * Fix calculation of fcntl flags in pvio\_socket\_blocking().
* [Revision #ba22ae8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ba22ae8)\
  2017-03-28 21:56:34 +0000
  * Fix schannel and other socket io bugs on Windows.
* [Revision #424c542](https://github.com/mariadb-corporation/mariadb-connector-c/commit/424c542)\
  2017-03-25 22:44:05 +0100
  * compiler warning
* [Revision #c042c1d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c042c1d)\
  2017-03-25 22:41:03 +0100
  * add forgotten async ctxt initialization on reconnects
* [Revision #92871e8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/92871e8)\
  2017-03-23 22:17:33 +0100
  * Fix compile failure: handshake\_complete member for tls struct was added for debugging purposes but not removed in a previous commit
* [Revision #6220d9c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6220d9c)\
  2017-03-23 17:42:50 +0100
  * Fix for Windows socket communication: Use send/recv instead of corresponding WSA\* functions
* [Revision #4974bac](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4974bac)\
  2017-03-23 17:04:33 +0100
  * Schannel fixes To obtain the correct cipher suite name, we use the (undocumented) flag SECPKG\_ATTR\_CIPHER\_INFO, which delivers cipher suite id and IANA cipher suite name. Added more cipher suites and mappings between IANA and OpenSSL cipher suite names
* [Revision #d7936b7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d7936b7)\
  2017-03-23 16:53:54 +0100
  * Fix for [MDEV-12245](https://jira.mariadb.org/browse/MDEV-12245): Use Server version if build inside server tree
* [Revision #082b165](https://github.com/mariadb-corporation/mariadb-connector-c/commit/082b165)\
  2017-03-23 16:53:00 +0100
  * Smaller test case fixes
* [Revision #63e0897](https://github.com/mariadb-corporation/mariadb-connector-c/commit/63e0897)\
  2017-03-21 17:26:19 +0100
  * Fix for [MDEV-12247](https://jira.mariadb.org/browse/MDEV-12247): If a statement with open (read only) cursor is executed there is no buffered result set (result set rows will be fetched directly from server), so we need to skip reading unbuffered result sets if a cursor is open.
* [Revision #6bec920](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6bec920)\
  2017-03-20 07:29:51 +0100
  * Fix for [MDEV-12446](https://jira.mariadb.org/browse/MDEV-12446): When no default configuration is present, C/C crashed due to double free in ma\_default.c
* [Revision #9a865bc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9a865bc)\
  2017-03-14 16:11:04 +0100
  * Fix for [CONC-243](https://jira.mariadb.org/browse/CONC-243): ABI breakage: Revert parameter length from size\_t to unsigned long. (affects mysql\_stmt\_prepare, mysql\_real\_query, mysql\_send\_query)
* [Revision #a1315d2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a1315d2)\
  2017-03-06 15:04:47 +0100
  * Fixed compiler warnings in bulk1.c and features-10\_2.c
* [Revision #aae1d2d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aae1d2d)\
  2017-03-06 06:33:19 +0100
  * Fixed test case for reset\_connection: We need to cast with my\_ulonglong instead of ulong
* [Revision #5b50a93](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5b50a93)\
  2017-03-04 21:37:16 +0100
  * Build fix: source directory needs to be CC\_SOURCE\_DIR instead of CMAKE\_SOURCE\_DIR. Otherwise server build will fail
* [Revision #e9b4b22](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e9b4b22)\
  2017-03-04 21:04:00 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #4ab155c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4ab155c)\
  2017-03-04 17:37:39 +0100
  * Unit test fixes for server integration - SSL tests require CERT\_PATH. Subdirectory certs was removed. If Connector/C is build outside of the server tree, certification path has to be specified manually (-DCERT\_PATH=/path/to/certs). - All tables and users will removed, if the test passed (otherwise mtr will complain).
* [Revision #e3faccf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e3faccf)\
  2017-03-04 21:02:36 +0100
  * Added missing file from previous commit to detect correct libressl version
* [Revision #27d8116](https://github.com/mariadb-corporation/mariadb-connector-c/commit/27d8116)\
  2017-02-25 08:09:00 +0100
  * Fix for LibreSSL version number: We need to read LIBRESSL\_VERSION\_TEXT, since OPENSSL\_VERSION\_NUMBER is always 2.0.0 Bumped the client version number to 10.2.5 (same as current 10.2 server version)
* [Revision #6e097a6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6e097a6)\
  2017-02-24 15:32:28 +0100
  * Check if we are using LibreSSL instead of OpenSSL
* [Revision #261d95a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/261d95a)\
  2017-02-23 20:08:57 +0100
  * Added option --tlsinfo for mariadb\_config which returns the linked tls library and version, e.g - Schannel (without version number) - OpenSSL 1.1.0c - GnuTLS 3.4.10
* [Revision #a40c41a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a40c41a)\
  2017-02-15 13:03:04 +0100
  * [MDEV-11708](https://jira.mariadb.org/browse/MDEV-11708) cmake -DWITH\_ASAN no longer works
* [Revision #fa17692](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fa17692)\
  2017-02-13 12:13:30 +0100
  * Added check for gcc options, so older gcc versions will not fail
* [Revision #4a55a6d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4a55a6d)\
  2017-02-12 20:19:18 +0100
  * Fixes for LibreSSL
* [Revision #b10c4f9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b10c4f9)\
  2017-02-05 11:35:11 +0100
  * Fix for [CONC-231](https://jira.mariadb.org/browse/CONC-231): Incorrect FSF address
* [Revision #8c34f69](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8c34f69)\
  2017-02-02 18:03:13 +0100
  * Fix cipher mapping (tls 1.2 ciphers were missing)
* [Revision #8c6413c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8c6413c)\
  2017-01-21 19:37:44 +0100
  * Merge branch 'connector\_c\_3.0' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into connector\_c\_3.0
* [Revision #7f9d27c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7f9d27c)\
  2017-01-18 16:09:26 +0100
  * Merge branch 'connector\_c\_3.0' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into HEAD
* [Revision #a54d812](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a54d812)\
  2017-01-18 16:08:21 +0100
  * Fix static build for dialog plugin
* [Revision #6655a81](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6655a81)\
  2017-01-21 19:36:16 +0100
  * Remove unused include file remove link to mariadbclient library
* [Revision #d202c98](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d202c98)\
  2017-01-17 19:30:34 +0100
  * Bumped version number to 3.0.2

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
