# MariaDB Connector/C 3.3.13 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors)[Release Notes](../../mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-13-release-notes.md)[Changelog](mariadb-connector-c-3-3-13-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 12 Nov 2024

For the highlights of this release, see the[release notes](../../mariadb-connector-c-33-release-notes/mariadb-connector-c-3-3-13-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* Revisions for both Connector/C 3.3.12 and 3.3.13 are included here
* [Revision #ad9cc274](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ad9cc274)\
  2024-11-08 06:58:54 +0100
  * Bump version number -> 3.3.13
* [Revision #76564675](https://github.com/mariadb-corporation/mariadb-connector-c/commit/76564675)\
  2024-11-07 08:47:12 +0100
  * Merge 3.1 into 3.3
* [Revision #b1f12678](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b1f12678)\
  2024-11-06 23:11:06 +0100
  * [CONC-527](https://jira.mariadb.org/browse/CONC-527) post-fix.
* [Revision #3e96ab92](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3e96ab92)\
  2024-11-06 11:56:12 -0500
  * bump the VERSION
* [Revision #3f2196d8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3f2196d8)\
  2024-10-25 07:38:00 +0200
  * Set manpage version to 3.3
* [Revision #e06ff35f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e06ff35f)\
  2024-10-24 20:50:13 +0200
  * Updated man pages (rebuilt with pandoc 3.5)
* [Revision #e8234ba7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e8234ba7)\
  2024-10-24 20:34:23 +0200
  * remove "find\_package(Doxygen)", it not used here
* [Revision #d9082c72](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d9082c72)\
  2024-10-24 20:20:54 +0200
  * restore manpages to allow builds w/o pandoc
* [Revision #6635e4bd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6635e4bd)\
  2024-10-22 13:26:50 +0200
  * Fix for [CONC-735](https://jira.mariadb.org/browse/CONC-735)
* [Revision #3b29ff9c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3b29ff9c)\
  2024-10-18 13:51:52 +0200
  * [MDEV-34859](https://jira.mariadb.org/browse/MDEV-34859): Failed to initialise non-blocking API on OpenBSD arm64
* [Revision #6c0e755e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6c0e755e)\
  2023-11-05 12:34:37 +0100
  * fix compilation errors with -flto
* [Revision #61ef765c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/61ef765c)\
  2023-11-05 12:32:35 +0100
  * change plugin TYPE in the REGISTER\_PLUGIN to something useful
* [Revision #8ace383f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8ace383f)\
  2023-11-05 12:31:13 +0100
  * fix meaningless code in mariadb\_time\_to\_string()
* [Revision #9e1155a1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9e1155a1)\
  2024-10-08 14:58:55 +0200
  * Merge pull request #257 from knielsen/mdev34859\_non\_blocking\_api\_aarch64\_boost\_context
* [Revision #da0a0136](https://github.com/mariadb-corporation/mariadb-connector-c/commit/da0a0136)\
  2024-09-05 13:56:44 +0200
  * Implement boost::context as a fallback for non-blocking API support
* [Revision #d2285fb8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d2285fb8)\
  2024-09-04 21:30:22 +0200
  * [MDEV-34859](https://jira.mariadb.org/browse/MDEV-34859): Failed to initialise non-blocking API on OpenBSD arm64
* [Revision #ae385415](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ae385415)\
  2024-09-21 15:33:49 +0200
  * Merge branch '3.1' into 3.3
* [Revision #9a400793](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9a400793)\
  2024-09-20 16:52:46 +0200
  * Fix possible crash, if no default plugin was loaded.
* [Revision #f705f346](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f705f346)\
  2024-09-20 08:35:24 +0200
  * Merge branch '3.1' into 3.3
* [Revision #289eaf2a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/289eaf2a)\
  2024-09-20 08:32:21 +0200
  * Merge pull request #254 from grooverdan/3.1-[CONC-730](https://jira.mariadb.org/browse/CONC-730)-undef-behaviour
* [Revision #c4153aa8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c4153aa8)\
  2024-09-18 17:19:43 +1000
  * [CONC-730](https://jira.mariadb.org/browse/CONC-730) Undefined behavior in the reference Ed25519 implementation
* [Revision #56178db1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/56178db1)\
  2024-09-14 16:16:04 +0200
  * Fix for [CONC-726](https://jira.mariadb.org/browse/CONC-726):
* [Revision #858a3e36](https://github.com/mariadb-corporation/mariadb-connector-c/commit/858a3e36)\
  2024-09-12 18:44:51 +0200
  * Fix typo (thanks to OttoK).
* [Revision #cd81266f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cd81266f)\
  2024-09-12 14:21:10 +0200
  * Fixed build of manpages
* [Revision #312b7eab](https://github.com/mariadb-corporation/mariadb-connector-c/commit/312b7eab)\
  2024-08-06 13:48:14 +0200
  * Folow up of [CONC-567](https://jira.mariadb.org/browse/CONC-567) Schannel:
* [Revision #7df01d4b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7df01d4b)\
  2024-08-05 13:26:36 +0200
  * Merge branch '3.3-wlad-schannel' into 3.3
* [Revision #1e8e1f4f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1e8e1f4f)\
  2024-07-31 13:49:30 +0200
  * Fix "set but not used" warnings.
* [Revision #3ceb310e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3ceb310e)\
  2024-07-30 11:53:57 +0200
  * [CONC-567](https://jira.mariadb.org/browse/CONC-567) Schannel : support TLSv1.3
* [Revision #d15c7385](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d15c7385)\
  2024-07-29 21:55:08 +0200
  * [CONC-567](https://jira.mariadb.org/browse/CONC-567) Schannel - handle SEC\_I\_RENEGOTIATE, prepare for TLSv1.3
* [Revision #72116a30](https://github.com/mariadb-corporation/mariadb-connector-c/commit/72116a30)\
  2024-07-29 11:53:15 +0200
  * Merge branch '3.1' into 3.3
* [Revision #6a67a34f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6a67a34f)\
  2024-07-28 03:46:50 +0200
  * [CONC-527](https://jira.mariadb.org/browse/CONC-527) "SEC\_E\_ALGORITHM\_MISMATCH" connecting Windows client to Ubuntu
* [Revision #01b6b321](https://github.com/mariadb-corporation/mariadb-connector-c/commit/01b6b321)\
  2024-07-19 10:16:56 +0200
  * Travis fix: use export instead of set command
* [Revision #6dfc071d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6dfc071d)\
  2024-06-18 11:01:17 -0400
  * bump the VERSION
* [Revision #551e1e39](https://github.com/mariadb-corporation/mariadb-connector-c/commit/551e1e39)\
  2024-05-14 13:58:20 +0200
  * travis: removed skysql
* [Revision #95d5623d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/95d5623d)\
  2024-07-31 06:01:21 +0200
  * Bump version number -> 3.3.12
* [Revision #998a8da4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/998a8da4)\
  2024-03-12 13:18:47 +0100
  * [MDEV-33513](https://jira.mariadb.org/browse/MDEV-33513) On Windows, build auth\_gssapi\_client statically and dynamically.
