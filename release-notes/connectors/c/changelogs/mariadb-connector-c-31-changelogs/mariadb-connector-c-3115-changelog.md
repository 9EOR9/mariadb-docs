# MariaDB Connector/C 3.1.15 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/#connectors)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3115-release-notes.md)[Changelog](mariadb-connector-c-3115-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 10 Nov 2021

For the highlights of this release, see the[release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3115-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #b2bb1b2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b2bb1b2)\
  2021-11-03 16:29:45 +0100
  * Fix for [CONC-570](https://jira.mariadb.org/browse/CONC-570):
* [Revision #735a729](https://github.com/mariadb-corporation/mariadb-connector-c/commit/735a729)\
  2021-10-18 15:17:01 +0200
  * Merge pull request #184 from mariadb-corporation/bb-3.1-[MDEV-19129](https://jira.mariadb.org/browse/MDEV-19129)
* [Revision #899d2d2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/899d2d2)\
  2021-09-29 12:57:54 +0300
  * Xcode compatibility update
* [Revision #9e1b3f5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9e1b3f5)\
  2021-10-11 17:47:03 -0700
  * Use dereferences in SET
* [Revision #62c7d5d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/62c7d5d)\
  2021-05-11 15:41:19 +0200
  * Fix typo in ConnectorName.cmake
* [Revision #15c7004](https://github.com/mariadb-corporation/mariadb-connector-c/commit/15c7004)\
  2021-10-11 20:06:35 +0200
  * Fix clang-cl warnings "variable initialized but unused"
* [Revision #f6b8fe1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f6b8fe1)\
  2021-10-08 10:20:23 +0200
  * Fix for [CONC-568](https://jira.mariadb.org/browse/CONC-568):
* [Revision #80188c3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/80188c3)\
  2021-10-06 07:06:55 +0300
  * [MDEV-26761](https://jira.mariadb.org/browse/MDEV-26761) test\_mdev19838() fixup: type mismatch on 64-bit Windows
* [Revision #3385303](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3385303)\
  2021-10-05 16:48:31 +0300
  * fixup 9c0250547406a6be3aee076cf0c0ba9630850a9e: build failure outside clang
* [Revision #f477215](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f477215)\
  2021-10-05 16:48:07 +0300
  * [CONC-566](https://jira.mariadb.org/browse/CONC-566) fixup: unit test cleanup
* [Revision #ae9f145](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ae9f145)\
  2021-10-05 14:54:16 +0200
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/mariadb-corporation/mariadb-connector-c) into 3.1
* [Revision #80215e2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/80215e2)\
  2021-10-05 05:26:31 -0400
  * Merge pull request #171 from pasha-bolokhov/patch-1
* [Revision #6710f59](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6710f59)\
  2021-05-17 07:54:50 -0700
  * Update async.c
* [Revision #9c02505](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9c02505)\
  2021-10-05 14:50:32 +0200
  * Fixed for [MDEV-26761](https://jira.mariadb.org/browse/MDEV-26761):
* [Revision #410d64d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/410d64d)\
  2021-09-27 13:27:40 +0200
  * Fix length calculation
* [Revision #4b9379b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4b9379b)\
  2021-09-25 16:07:24 +0200
  * Fix for [CONC-566](https://jira.mariadb.org/browse/CONC-566):
* [Revision #b991723](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b991723)\
  2021-09-21 14:39:17 +0200
  * Followup of fix for [CONC-565](https://jira.mariadb.org/browse/CONC-565)
* [Revision #62ce153](https://github.com/mariadb-corporation/mariadb-connector-c/commit/62ce153)\
  2021-08-31 18:43:16 +0200
  * \[misc] travis correction
* [Revision #d72b85c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d72b85c)\
  2021-08-30 15:54:29 +0200
  * \[misc] ensuring PR test suite runs correctly
* [Revision #42cb1e4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/42cb1e4)\
  2021-08-25 09:37:42 +0300
  * test\_bug38486(): Do not leave behind a garbage table
* [Revision #9990ab7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9990ab7)\
  2021-08-25 09:10:10 +0300
  * Fix clang -Wunused-but-set-variable
* [Revision #cc56a1c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cc56a1c)\
  2021-08-13 08:15:40 +0200
  * Fix MSVC/ASAN error
* [Revision #a78d404](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a78d404)\
  2021-08-11 16:44:05 -0400
  * bump the VERSION
