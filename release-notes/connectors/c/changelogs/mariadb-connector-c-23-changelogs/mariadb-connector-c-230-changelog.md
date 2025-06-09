# MariaDB Connector/C 2.3.0 Changelog

[Download](https://downloads.mariadb.org/connector-c/2.3.0)[Release Notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-230-release-notes.md)[Changelog](mariadb-connector-c-230-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 1 Jul 2016

For the highlights of this release, see the[release notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-230-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #0050d71](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0050d71)\
  2016-06-22 17:27:59 +0200
  * Windows fix: In case getaddrinfo() returns an error, we return the WSA Error code instead of gai error. (For more information please read [ms738520(v=vs.85).aspx](https://msdn.microsoft.com/en-us/library/windows/desktop/ms738520\(v=vs.85\).aspx))
* [Revision #1aa8720](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1aa8720)\
  2016-06-22 05:33:07 +0200
  *
    * When connecting via TLS socket is now set to non blocking and we try to reexecuete SSL\_connect in case SSL\_get\_error return WANT\_READ or WANT\_WRITE - Fixed compiler warnings - In case getaddrinfo returned EAI\_SYSTEM errno will be returned in error message
* [Revision #f618639](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f618639)\
  2016-06-17 16:10:58 +0200
  * Fixed compiler warnings
* [Revision #afed467](https://github.com/mariadb-corporation/mariadb-connector-c/commit/afed467)\
  2016-06-15 14:59:21 +0200
  * Windows build fix
* [Revision #948cde6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/948cde6)\
  2016-06-08 13:22:00 +0200
  * Fixed behaviour of getaddrinfo: If getaddrinfo returns EAI\_AGAIN we will try to resolve hostname again until connecttimeout seconds passed. If no connect timeout was specified, a default value of 30 seconds will be used.
* [Revision #f4c360b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f4c360b)\
  2016-06-06 00:45:00 +0200
  * Removed LONGLONG\_MIN/MAX definition from config-win.h as they are also defined in my\_global, and that causes any compilation warnings.
* [Revision #15c66c2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/15c66c2)\
  2016-06-04 14:15:56 +0200
  * Don't use new options by default (will break Server2008)
* [Revision #5cf10d8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5cf10d8)\
  2016-06-04 10:24:19 +0200
  * Fix for windows build: replace SIZEOF\_CHARP with sizeof(char \*)
* [Revision #66b5384](https://github.com/mariadb-corporation/mariadb-connector-c/commit/66b5384)\
  2016-06-04 09:38:13 +0200
  * Changed sign procedure (now supporting SHA-256)
* [Revision #ea60288](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ea60288)\
  2016-06-03 17:07:34 +0200
  * Fix for [CONC-190](https://jira.mariadb.org/browse/CONC-190): Don't use verify callback in global context, since it may cause bad/unexpected behaviour in threaded issues. Instead now verification of peer certificate will be processed by the OpenSSL library itself.
* [Revision #f77f101](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f77f101)\
  2016-06-02 10:59:00 +0200
  * Fixed memory overrun in my\_strdup\_root
* [Revision #7ccce9e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7ccce9e)\
  2016-05-31 08:29:47 +0200
  * Backport from 3.0: - fixed numeric precision bug for prepared statements - [CONC-177](https://jira.mariadb.org/browse/CONC-177): fixed zerofill issues (converting numeric to string)
* [Revision #b190e36](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b190e36)\
  2016-05-30 15:35:48 +0200
  * Added new license header for cmake helper files. All cmake files are now under new bsd license. Fixed minor iconv bugs
* [Revision #794de93](https://github.com/mariadb-corporation/mariadb-connector-c/commit/794de93)\
  2016-05-30 15:24:15 +0200
  * Bumped version number to 2.3.0
