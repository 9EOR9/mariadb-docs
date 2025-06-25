# MariaDB Connector/C 2.3.2 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/2.3.2)[Release Notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-232-release-notes.md)[Changelog](mariadb-connector-c-232-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 18 Jan 2017

For the highlights of this release, see the[release notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-232-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #5f7ac6b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5f7ac6b)\
  2017-01-17 10:53:54 +0100
  * Changed interface version back to 0x0100 for compatibility reasons. Older client plugins < C/C 2.3.2 cannot be used anymore - we will document this behavior.
* [Revision #93bb6bf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/93bb6bf)\
  2017-01-16 17:05:36 +0100
  * Fixed plugin interface - it's now compatible with MariaDB server and Connector/C. The interface version number was bumped to 0x101 - which means older plugins cannot be used anymore with Connector/C 2.3.1
* [Revision #9958387](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9958387)\
  2017-01-02 12:47:52 +0100
  * Fix for [CONC-223](https://jira.mariadb.org/browse/CONC-223): Add client support for missing collations If a collation is not available the client will not be able to set correct character set.
* [Revision #aea5762](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aea5762)\
  2017-01-04 16:34:15 +0100
  * fixed output for --plugindir: plugindir option now prints PLUGIN\_DIR instead of PLUGINDIR (merge from master)
* [Revision #2d26dd1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2d26dd1)\
  2016-10-11 13:55:01 +0200\
  \*
  * Fix for bug [MDEV-10894](https://jira.mariadb.org/browse/MDEV-10894): fixed conversion for big-endian platforms (back ported from 3.0) - fixed test case
* [Revision #e56b8d4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e56b8d4)\
  2016-12-23 16:53:14 +0100
  * Fix for debian Bug#849125: fix include of my\_stmt.h
* [Revision #6b32499](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6b32499)\
  2016-12-21 18:14:16 +0100
  * Fix for read\_timeout. (Thanks to Netik Agarwal for reporting this issue)
* [Revision #2cbd10a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2cbd10a)\
  2016-09-06 19:50:38 +0200
  * fix two bugs in dialog plugin
* [Revision #c32c117](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c32c117)\
  2016-10-26 06:06:45 +0200
  * Fix for [CONC-205](https://jira.mariadb.org/browse/CONC-205): (manually merged from master)
* [Revision #2e14b0a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2e14b0a)\
  2016-10-06 09:46:41 +0200
  * Fixed function declarations for mysql\_error and mysql\_info (const char\* instead of char \*)
* [Revision #caa245d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/caa245d)\
  2016-09-26 10:06:39 +0200
  * timeout fixes for async Patch provided by Kristian Nielsen
* [Revision #be20fec](https://github.com/mariadb-corporation/mariadb-connector-c/commit/be20fec)\
  2016-08-23 18:42:11 +0200
  * Removed extra check for non binary result types in fetch\_bin
* [Revision #ce95343](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ce95343)\
  2016-08-18 08:01:16 +0200
  * Fix for [CONC-198](https://jira.mariadb.org/browse/CONC-198): can't use two statements per connection If we have multiple open cursors we need to check the server\_status per statement (not per connection)
* [Revision #84e0f5c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/84e0f5c)\
  2016-08-11 14:44:22 +0200
  * Fix for [CONC-197](https://jira.mariadb.org/browse/CONC-197): Coredump if length ptr is NULL. Assigned address of length\_value if length ptr in bind structure is zero/null.
* [Revision #5debd70](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5debd70)\
  2016-08-05 07:29:11 +0200
  * bumped version number fixed license header for plugin\_auth\_common.h

{% @marketo/form formid="4316" formId="4316" %}
