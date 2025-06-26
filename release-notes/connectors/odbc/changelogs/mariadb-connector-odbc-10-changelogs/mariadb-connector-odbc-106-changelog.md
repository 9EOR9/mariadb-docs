# MariaDB Connector/ODBC 1.0.6 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/1.0.6)[Release Notes](../../mariadb-connector-odbc-10-release-notes/mariadb-connector-odbc-106-release-notes.md)[Changelog](mariadb-connector-odbc-106-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-odbc/README.md)

**Release date:** 11 Apr 2016

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-10-release-notes/mariadb-connector-odbc-106-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #ab1b3e7](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ab1b3e7)\
  2016-04-09 01:12:39 +0200
  * Cherrypicking of latest(after the last merge) chahges from 2.0 Mainly tests fixes, minor code restructuring(introduced ma\_common, less dependencies in maodbcs etc)
* [Revision #14951e8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/14951e8)\
  2016-03-30 23:44:55 +0200
  * Cherrypicking from [ODBC-2](https://jira.mariadb.org/browse/ODBC-2).0 branch
    * Fix of several memory leaks and of some previous merge mistakes.\
      There was a leak in the SQLConnect - uid/pwd strings were leaked.\
      Leak in the internal routine re-getting current db name.\
      Some SQLSetPos operations leaked.\
      Some fields in Stmt and descriptors were leaked in some conditions.
* [Revision #1afa0a5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1afa0a5)\
  2016-03-14 17:27:44 +0100
  * Added optional support of SSL. Since at least at the moment, C/C does not link OpenSsl statically, we need to link against it in case of SSL support selected. Added search of OpenSsl files. Ssl settings page in the setup dialog displayed only if ssl support selected
* [Revision #91825b7](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/91825b7)\
  2016-03-11 12:00:30 +0100
  * Made possible to turn off ssl certificate verification(for the case when it is turned on by default)
* [Revision #9e8bca5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9e8bca5)\
  2016-03-04 23:34:59 +0100
  * Changed the dialog to use IFileDialog instead of SHBrowseForFolder Added push buttons for file/folder dialog opening, where they were missing
* [Revision #d47f21d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d47f21d)\
  2016-02-29 22:30:32 +0100
  * Fix + test case(s) for the [ODBC-27](https://jira.mariadb.org/browse/ODBC-27). Also fixes other things around dialog invocation logic. In particular for COMPLETE/\_REQUIRED completion types. Change(or call it a fix) in connection string parsing - if DRIVER keyword is given, DSN(if given too) won't be expanded. I think that is what specs say.
* [Revision #734531f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/734531f)\
  2016-02-10 16:33:24 +0100
  * Connection string processing - many changes/fixes, that among others, should allow to fix [ODBC-30](https://jira.mariadb.org/browse/ODBC-30)(after merging to 2.0) Connection string is now parsed, then if DSN is present, DSN info is read and connection string is parsed again. Introduced dependencies between fields, like setting TCPIP resets NamedPipe. Introducing connstring.c tests suite, whick compiles in ma\_dsn.c, to effectively test connection string operations. Also adding interactive.c for interactive tests, i.e. tests of connector behaviors when dialog invocation is involved. BUILD\_INTERACTIVE\_TESTS and USE\_INTERACTIVE\_TESTS control whether to build and run those tests automatically.
* [Revision #f8a58cd](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f8a58cd)\
  2016-01-17 00:28:13 +0100
  * Fix of the bug in connection string parsing - if options were set by their individual name(currently those NO\_PROMPT, NamedPipe and AUTO\_RECONNECT, they would not have any effect. Add calling convention to DSNPrompt function pointer type definition
* [Revision #ff29265](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ff29265)\
  2016-01-16 15:53:37 +0100
  * Fix and the testcase for the part of [ODBC-29](https://jira.mariadb.org/browse/ODBC-29) - the problem with query with leading >1 spaces. Connector trimmed the query, but did not updat the length accordingly.
* [Revision #34d62c7](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/34d62c7)\
  2016-01-10 23:04:34 +0100
  * Fix and testcase for the Bug [ODBC-26](https://jira.mariadb.org/browse/ODBC-26) The patch fixes various problems around DAE functionality, and in particular with WCHAR type at DAE
* [Revision #d5130e7](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d5130e7)\
  2015-12-12 13:44:09 +0100
  * Fix of the build problem in the VS 2015. Fix of some compilation warnings in VS2015
* [Revision #96e7aeb](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/96e7aeb)\
  2015-12-10 19:17:29 +0100
  * Fixed 2 tests in the types suite - they could fail in case of specific connection charsets. Added to the framework functions to facilitate obtaining of additional connection by tests.
* [Revision #98a0e8d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/98a0e8d)\
  2015-12-08 16:13:14 +0100
  * Cherry-picking from 2.0 branch. Couple of tests were fixed along the way
* [Revision #b0bfe58](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b0bfe58)\
  2015-11-19 00:26:40 +0100
  * Fixed possible crash - in some conditions TypeName in the ird record could freed, but never allocated before
* [Revision #97fd947](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/97fd947)\
  2015-09-24 23:30:08 +0200
  * Small changes/additions to ssl functionality. Added clr and options for fp. Setting of plugins directory
* [Revision #f353854](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f353854)\
  2015-09-23 16:59:30 +0200
  * Basic SSL connection support
* [Revision #715d0b6](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/715d0b6)\
  2015-09-23 04:21:40 +0200
  * Connection string options for SSL settings and their simplistic support in the GUI dialog.
* [Revision #9b4a852](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9b4a852)\
  2015-09-23 03:08:45 +0200
  * ([ODBC-23](https://jira.mariadb.org/browse/ODBC-23))Added connection string option PLUGIN\_DIR for pointing to c/c plugins directory. Added support of this function to the gui dialog.
* [Revision #06d8df4](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/06d8df4)\
  2015-09-15 17:37:53 +0200
  * Version bump - 1.0.6

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
