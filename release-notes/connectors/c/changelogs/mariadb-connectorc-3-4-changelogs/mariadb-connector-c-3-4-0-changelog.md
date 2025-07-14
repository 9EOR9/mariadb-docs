# MariaDB Connector/C 3.4.0 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Release Notes](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-0-release-notes.md)[Changelog](mariadb-connector-c-3-4-0-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 24 June 2024

For the highlights of this release, see the[release notes](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-0-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #5efe1e61](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5efe1e61)\
  2024-05-27 16:19:29 +0200
  * Merge branch '3.4' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.4
* [Revision #cc985fab](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cc985fab)\
  2024-05-26 15:45:54 +0200
  * fix the memory leak with gnutls (11K per connection)
* [Revision #875ef5ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/875ef5ad)\
  2024-05-26 11:34:52 +0200
  * fix the memory leak with openssl (8K per connection)
* [Revision #8b1019fc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8b1019fc)\
  2024-05-27 16:18:48 +0200
  * Travis: remove 10.6 and 11.3 unit testing
* [Revision #d9a50ace](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d9a50ace)\
  2024-05-16 13:53:14 +0200
  * ASN1\_TIME\_to\_tm was added in OpenSSL 1.1.1
* [Revision #deb38a3e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/deb38a3e)\
  2024-05-16 11:47:00 +0200
  * fix the code for OpenSSL 1.0
* [Revision #e5219742](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e5219742)\
  2024-05-15 16:39:18 +0200
  * TLS fingerprint is returned in hex!
* [Revision #4623d104](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4623d104)\
  2024-05-14 09:54:50 +0200
  * Merge branch '3.3' into 3.4
* [Revision #e69af190](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e69af190)\
  2024-05-14 09:48:52 +0200
  * Merge branch '3.1' into 3.3
* [Revision #6bd5b674](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6bd5b674)\
  2024-05-14 09:45:51 +0200
  * Follow up fix for [CONC-696](https://jira.mariadb.org/browse/CONC-696)
* [Revision #f578e359](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f578e359)\
  2024-05-13 16:09:47 +0200
  * Merge branch '3.1' into 3.3
* [Revision #d5394838](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d5394838)\
  2024-05-13 15:57:39 +0200
  * [CONC-696](https://jira.mariadb.org/browse/CONC-696): Replace COM\_PROCESS\_KILL by KILL command
* [Revision #96bedf00](https://github.com/mariadb-corporation/mariadb-connector-c/commit/96bedf00)\
  2024-05-13 15:57:00 +0200
  * bump version
* [Revision #072dadc3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/072dadc3)\
  2024-05-13 15:54:04 +0200
  * Disable test when running against MySQL server
* [Revision #def5dee9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/def5dee9)\
  2024-05-13 16:00:45 +0200
  * Merge remote-tracking branch 'origin/3.3' into 3.4-serg
* [Revision #11168e87](https://github.com/mariadb-corporation/mariadb-connector-c/commit/11168e87)\
  2024-05-13 15:53:23 +0200
  * Merge remote-tracking branch 'origin/3.4' into 3.4-serg
* [Revision #fc337784](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fc337784)\
  2024-05-10 11:06:37 +0200
  * Added new utf8 general1400\_as\_ci collations
* [Revision #23be94ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/23be94ad)\
  2024-02-22 16:24:20 +0100
  * Follow up for [CONC-505](https://jira.mariadb.org/browse/CONC-505)
* [Revision #55fe56fa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/55fe56fa)\
  2024-02-22 09:03:51 +0100
  * Fix for [CONC-505](https://jira.mariadb.org/browse/CONC-505):
* [Revision #3228ed2e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3228ed2e)\
  2024-05-07 15:13:15 +0200
  * Fix copy/paste error
* [Revision #dc160678](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dc160678)\
  2024-05-07 11:40:29 +0200
  * Fix build for OpenSSL < 1.1
* [Revision #989bd885](https://github.com/mariadb-corporation/mariadb-connector-c/commit/989bd885)\
  2024-05-07 07:23:32 +0200
  * Fix compile error (misleading-indentation)
* [Revision #ba137a4f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ba137a4f)\
  2024-05-06 14:32:31 +0200
  * Exclude server side cursors when checking for pending results
* [Revision #3f47c152](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3f47c152)\
  2024-05-06 14:31:49 +0200
  * Added missing support for restricted\_auth in conf files
* [Revision #3652e503](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3652e503)\
  2024-04-30 13:22:38 +0200
  * Disable test for MAXSCALE
* [Revision #bf0d299a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bf0d299a)\
  2024-04-30 12:04:15 +0200
  * Text fix: Avoid crash in non TLS connections
* [Revision #c6fa3730](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c6fa3730)\
  2024-04-30 11:33:04 +0200
  * Fix SKIP\_TLS macro (unittest)
* [Revision #a63b8261](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a63b8261)\
  2024-04-30 11:06:09 +0200
  * test fix: Always specify fingerprint for TLS connections
* [Revision #148eb0fe](https://github.com/mariadb-corporation/mariadb-connector-c/commit/148eb0fe)\
  2024-04-30 10:50:30 +0200
  * Merge branch '3.4-work' into 3.4
* [Revision #67cb58a2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/67cb58a2)\
  2024-04-30 10:48:41 +0200
  * [CONC-692](https://jira.mariadb.org/browse/CONC-692): Provide X509 peer certificate information
* [Revision #f7eab7d2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f7eab7d2)\
  2024-04-29 14:18:54 +0200
  * Merge branch '3.1' into 3.4
* [Revision #a25049ba](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a25049ba)\
  2024-04-29 11:17:35 +0200
  * Remove temp. diagnostic information
* [Revision #9644f527](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9644f527)\
  2024-04-29 11:15:32 +0200
  * Skip async test on Windows
* [Revision #45179cff](https://github.com/mariadb-corporation/mariadb-connector-c/commit/45179cff)\
  2024-04-29 11:15:02 +0200
  * Merge remote-tracking branch 'origin/3.1' into 3.4
* [Revision #20fbb3c3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/20fbb3c3)\
  2024-04-29 10:57:12 +0200
  * Avoid possible crash if connection was closed
* [Revision #7d0edc3d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7d0edc3d)\
  2024-04-29 10:24:12 +0200
  * Merge branch '3.4-work' into 3.4
* [Revision #ffd0a0e4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ffd0a0e4)\
  2024-04-27 20:52:13 +0200
  * Fix identation error.
* [Revision #19dffea4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/19dffea4)\
  2024-04-24 11:21:28 +0200
  * [CONC-692](https://jira.mariadb.org/browse/CONC-692): Provide X509 peer certificate information
* [Revision #f4e8c085](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f4e8c085)\
  2024-04-24 11:05:26 +0200
  * Fix compiler warnings
* [Revision #fef3e4ed](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fef3e4ed)\
  2024-03-23 12:53:24 +0100
  * [CONC-683](https://jira.mariadb.org/browse/CONC-683): Check pending results when closing statement.
* [Revision #b64282a9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b64282a9)\
  2024-03-23 12:27:55 +0100
  * [CONC-667](https://jira.mariadb.org/browse/CONC-667): Fix statement handling when unbuffered results are pending.
* [Revision #4a1c5ef5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4a1c5ef5)\
  2024-03-22 15:35:21 +0100
  * [CONC-688](https://jira.mariadb.org/browse/CONC-688): mariadb\_rpl\_fetch() crashes if table is partitioned
* [Revision #2fc64d79](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2fc64d79)\
  2024-03-18 08:09:02 +0100
  * [CONC-689](https://jira.mariadb.org/browse/CONC-689): Fix parsing of HEARTBEAT\_LOG\_EVENT:
* [Revision #d5973f77](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d5973f77)\
  2024-03-16 07:01:26 +0100
  * Merge commit '29041069dbc8704fa278cea3a049db52db937587' into 3.4
* [Revision #20737ac3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/20737ac3)\
  2024-03-16 06:47:57 +0100
  * Merge commit '86e2e87fa22ace6e46353c13a09fa4b8878b7992' into 3.4
* [Revision #86e2e87f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/86e2e87f)\
  2024-03-10 14:04:27 +0100
  * Follow up of fix for [CONC-680](https://jira.mariadb.org/browse/CONC-680):
* [Revision #b4d75e78](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b4d75e78)\
  2024-03-18 14:11:51 +0100
  * unitest bulk1: force a particular storage engine
* [Revision #29041069](https://github.com/mariadb-corporation/mariadb-connector-c/commit/29041069)\
  2024-03-15 19:45:55 +0100
  * fix the test for mtr
* [Revision #f7373974](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f7373974)\
  2024-03-15 14:42:27 +0100
  * copy-paste error fixed, wrong plugin name
* [Revision #d01d8c10](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d01d8c10)\
  2024-03-10 14:04:27 +0100
  * Follow up of fix for [CONC-680](https://jira.mariadb.org/browse/CONC-680):
* [Revision #1437ff04](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1437ff04)\
  2024-03-12 13:18:47 +0100
  * [MDEV-33513](https://jira.mariadb.org/browse/MDEV-33513) On Windows, build auth\_gssapi\_client statically and dynamically.
* [Revision #a66d3718](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a66d3718)\
  2024-03-12 06:01:54 +0100
  * Travis fix:
* [Revision #696fa732](https://github.com/mariadb-corporation/mariadb-connector-c/commit/696fa732)\
  2024-03-06 22:07:30 +0100
  * Merge pull request #242 from rusher/3.4
* [Revision #abce07da](https://github.com/mariadb-corporation/mariadb-connector-c/commit/abce07da)\
  2024-03-06 16:03:55 +0100
  * \[[MDEV-30366](https://jira.mariadb.org/browse/MDEV-30366)] Bulk unitary result flag client implementation part.
* [Revision #4a74f878](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4a74f878)\
  2024-02-23 06:54:22 +0100
  * Fix compiler warning in unittest/misc.c
* [Revision #66569ae9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/66569ae9)\
  2024-02-23 06:42:02 +0100
  * [CONC-680](https://jira.mariadb.org/browse/CONC-680):
* [Revision #fe411bf3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fe411bf3)\
  2024-02-20 09:52:07 +0100
  * [CONC-403](https://jira.mariadb.org/browse/CONC-403):
* [Revision #5a5a7275](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5a5a7275)\
  2024-02-20 08:41:28 +0100
  * Travis: Build MSI (windows)
* [Revision #1e2968ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1e2968ad)\
  2024-02-14 11:41:17 +0100
  * Windows compilation warning
* [Revision #6e20d356](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6e20d356)\
  2024-02-14 01:47:54 +0100
  * disable OPT\_SSL\_VERIFY\_SERVER\_CERT in travis
* [Revision #82983a30](https://github.com/mariadb-corporation/mariadb-connector-c/commit/82983a30)\
  2024-02-14 01:21:52 +0100
  * make DEFAULT\_SSL\_VERIFY\_SERVER\_CERT a cmake option
* [Revision #293f6df8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/293f6df8)\
  2024-02-13 16:40:44 +0100
  * Bump version to 3.4.0
* [Revision #3c60be95](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3c60be95)\
  2024-02-12 15:55:09 +0100
  * Added 11.4 server

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
