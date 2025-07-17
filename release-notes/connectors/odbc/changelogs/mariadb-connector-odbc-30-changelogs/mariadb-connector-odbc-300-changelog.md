# Connector/ODBC 3.0.0 Alpha Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/3.0.0)[Release Notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-300-release-notes.md)[Changelog](mariadb-connector-odbc-300-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 19 Jan 2017

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-30-release-notes/mariadb-connector-odbc-300-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #db72181](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/db72181)\
  2017-01-17 23:46:20 +0100
  * Fix of build problems on rhel5.
* [Revision #b2f32ca](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b2f32ca)\
  2017-01-17 00:46:27 +0100
  * MADB\_OPT\_FLAG\_PAD\_SPACE was doing what MADB\_OPT\_FLAG\_IGNORE\_SPACE is supposed to do. Fixed that + in the setup dialog. Changed FindMariaDB to skip search if directory values are set (in command line parameters).
* [Revision #766e375](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/766e375)\
  2017-01-13 18:21:55 +0100
  * Updated dll version to 3.0.0.
* [Revision #1bf80e2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1bf80e2)\
  2017-01-08 23:47:41 +0100
  * Added one more native error (specific to mariadb\_stmt\_execute\_direct) to be treated as "lost connection" Changed CMakeLists to configure odbc\*.ini only if tests directory is present.
* [Revision #0542505](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0542505)\
  2016-12-02 14:11:54 +0100
  * Slightly refined multi-statement query detection - it now allows having semicolons at the end of a single statement. Reset rs columns number before preparing query. Changed a few testcases in error.c to make output more informative
* [Revision #02bef5f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/02bef5f)\
  2016-12-01 17:31:27 +0100
  * mariadb\_stmt\_execute\_direct is not used in case of params array, since it even doesn't make sense, not talking about problems it causes. Once again fixed code around "where current of" execution - index fields count now added to ParamCount, and deducted after execution (in case of execute\_direct). Simpler and no problems with prepare+execute or older servers.
* [Revision #d777bf8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d777bf8)\
  2016-12-01 01:50:21 +0100
  * Some more fixes around "WHERE COUNT OF". Fixed params allocation and works in conjunction with DAE
* [Revision #81d5e44](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/81d5e44)\
  2016-11-30 16:55:54 +0100
  * Fixed "where current of" operation - there was error in total parameters count calculation. stmt is now closed and re-ignited before new Prepare on the same handle. Number of pre-bound parameters is set even if it is 0. ParamCount type is changed to SMALLINT.
* [Revision #e4ac5ec](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e4ac5ec)\
  2016-11-24 00:56:00 +0100
  * Removed couple of not really needed intermediate functions called by SQLFetch and SQLFetchScroll.
* [Revision #4242e3c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4242e3c)\
  2016-11-22 11:10:45 +0100
  * Changed max->MAX, min->MIN. Added more data to generated DSN config in odbc.ini. Added cmake macro to easier populate values (for ini generations so far).
* [Revision #7d73e86](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7d73e86)\
  2016-11-21 17:52:19 +0100
  * Added ini files generation for testing with UnixODBC Set correct version.
* [Revision #7cd56ca](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7cd56ca)\
  2016-11-17 15:01:39 +0100
  * As ma\_errormsg.h has been renamed in C/C back to errmsg.h, had to change its inclusion.
* [Revision #fbc65f3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/fbc65f3)\
  2016-11-17 00:30:07 +0200
  * Some more fixes for build on \*nix. Mainly addint defines for TRUE and FALSE does that. Also had to add dl to tests linking list in dirty way. Fixed warnings.
* [Revision #c5af166](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c5af166)\
  2016-11-16 22:41:01 +0100
  * Copied code for LIST, DYNAMIC\_ARRAY, DYNAMIC\_STRING from C/C to enable build on \*nix, there my\_global.h and my\_sys.h are not installed any more, and to eventually make dynamic linking of C/C possible. All types and functions naming patterns have been changed. Also copied some macros, defined in aforementioned headers, and used in either c/odbc or in newly copied code.
* [Revision #e58af25](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e58af25)\
  2016-11-14 20:52:19 +0100
  * Support of mariadb\_stmt\_execute\_direct in first approach([ODBC-63](https://jira.mariadb.org/browse/ODBC-63)).
* [Revision #ded6696](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ded6696)\
  2016-10-28 00:32:38 +0200
  * Merge branch '[ODBC-2](https://jira.mariadb.org/browse/ODBC-2).0' into [ODBC-3](https://jira.mariadb.org/browse/ODBC-3).0
* [Revision #572bdb1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/572bdb1)\
  2016-10-27 19:44:59 +0200
  * Fix and testcase for [ODBC-57](https://jira.mariadb.org/browse/ODBC-57). The problem was that MS Access adds parenthesis around each SELECT in the UNION. And the function determining query type wasn't ready for that. Now it skips query string characters till first alpha.
* [Revision #3f1bb8b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/3f1bb8b)\
  2016-10-21 18:55:37 +0200
  * Fix of problems with cursors and positional operations. Many things were relying on internal C/C stuff; that has been changed in C/C 3.0. That code had to be refactored. Removed unused fields from one of descriptor structures.
* [Revision #db232db](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/db232db)\
  2016-10-13 19:31:18 +0200
  * Enabling build against C/C 3.0
* [Revision #43c8d5a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/43c8d5a)\
  2016-08-16 01:02:24 +0200
  * Fixed some bugs in SQLSetPos with SQL\_COLUMN\_IGNORE - we had failing test in cursor.c Also fixed error it returns if there were errors on some of the updated rows.
* [Revision #48bc3e1](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/48bc3e1)\
  2016-10-15 00:31:19 +0200
  * mysql\_stmt\_bind\_param instead of direct copying of BIND structures to stmt handle property. mysql\_stmt\_row\_tell/row\_seek instead of direc MYSQL\_ROWS pointer manipulation. Removed couple of TODOs (simple or done). Fixed a bit my\_dynamic\_pos\_cursor1 test.
* [Revision #0c101a2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0c101a2)\
  2016-10-14 13:22:03 +0200
  * Changed MADB\_CALLOC to follow old ma\_malloc (MY\_ZEROFILL)) behavior in case of 0 length. Solves many problems comped to simple calloc.
* [Revision #609489d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/609489d)\
  2016-10-14 11:13:54 +0200
  * Fix of crashes caused by relying on C/C internal features, changed in 3.0. In this case that was setting length\_value of param bind structure, and not letting length buffer pointer. Older C/C does that, if length is NULL. Changed some helper functions parameters to "const" to avoid warnings, and just because that is right.
* [Revision #9eab0b8](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9eab0b8)\
  2016-10-13 19:31:18 +0200
  * Enabling build against C/C 3.0.
* [Revision #774a5a9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/774a5a9)\
  2016-04-29 14:00:01 +0200
  * Build with C/C 3.0 enabler.

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
