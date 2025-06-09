# MariaDB Connector/C 3.1.23 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://mariadb.com/downloads/connectors)[Release Notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3-1-23-release-notes.md)[Changelog](mariadb-connector-c-3-1-23-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 29 Nov 2023

For the highlights of this release, see the[release notes](../../mariadb-connector-c-31-release-notes/mariadb-connector-c-3-1-23-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #f1a7276](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f1a7276)\
  2023-11-23 07:11:13 +0100
  * Bump version to 3.1.23
* [Revision #ae565ee](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ae565ee)\
  2023-10-23 13:32:45 +0200
  * Use safer snprintf call.
* [Revision #8320f0d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8320f0d)\
  2023-10-21 19:43:42 +0200
  * Fix error on 32-bit systems
* [Revision #642bc31](https://github.com/mariadb-corporation/mariadb-connector-c/commit/642bc31)\
  2023-10-21 08:09:40 +0200
  * Follow up of PR-236 (update ma\_context)
* [Revision #808312f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/808312f)\
  2023-09-23 02:33:37 +0200
  * Update ma\_context.c
* [Revision #35cd69b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/35cd69b)\
  2023-10-20 06:44:38 +0200
  * Fix for [CONC-672](https://jira.mariadb.org/browse/CONC-672): my\_auth.c:153:5: error: 'strncpy' output may be truncated copying
* [Revision #ab38a07](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ab38a07)\
  2023-10-11 10:43:25 +0200
  * Fix for [CONC-670](https://jira.mariadb.org/browse/CONC-670): Syscall param socketcall.setsockopt(optval) points to uninitialised byte(s)
* [Revision #1b3cf6b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1b3cf6b)\
  2023-09-21 13:36:23 +0200
  * [CONC-669](https://jira.mariadb.org/browse/CONC-669) Cache bcrypt algorithm providers in win\_crypt.c
* [Revision #a6d8ef5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a6d8ef5)\
  2023-09-21 07:08:37 +0200
  * Merge pull request #235 from grooverdan/3.1-remove-words\_big\_endian
* [Revision #07ae949](https://github.com/mariadb-corporation/mariadb-connector-c/commit/07ae949)\
  2023-09-09 08:20:45 +1000
  * [MDEV-19511](https://jira.mariadb.org/browse/MDEV-19511) Remove WORDS\_BIGENDIAN - HAVE\_BIGENDIAN replaced it
* [Revision #d9626e3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d9626e3)\
  2023-09-13 10:36:15 +0200
  * [CONC-666](https://jira.mariadb.org/browse/CONC-666): Fix memory allocation issue with prepared statement reexecution.
* [Revision #04b3d83](https://github.com/mariadb-corporation/mariadb-connector-c/commit/04b3d83)\
  2023-09-20 14:13:19 +0200
  * Added -Wno-stringop-truncation to the default gcc options
* [Revision #9f37c27](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9f37c27)\
  2023-09-18 16:05:00 +0200
  * Fix for [CONC-668](https://jira.mariadb.org/browse/CONC-668): 32bit compile of 3.3.7 fails - error: right shift count >= width of type
* [Revision #4e3905c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4e3905c)\
  2023-08-23 16:18:50 +0200
  * Fix for bcrypt hash functions
* [Revision #5000bc7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5000bc7)\
  2023-08-10 11:18:22 +0200
  * Test fix: Always specify the socketname when calling my\_test\_connect()

{% @marketo/form formid="4316" formId="4316" %}
