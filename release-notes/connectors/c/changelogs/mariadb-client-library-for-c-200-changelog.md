# MariaDB Client Library for C 2.0.0 Changelog

The most recent [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/2.0.0)[Release Notes](../mariadb-client-library-for-c-200-release-notes.md)[Changelog](mariadb-client-library-for-c-200-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 2 Apr 2014

For the highlights of this release, see the [release notes](../mariadb-client-library-for-c-200-release-notes.md).

The revision number links will take you to the revision's page on Launchpad. On\
Launchpad you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #130](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/130)\
  Tue 2014-04-01 17:49:26 +0200
  * Recommit test fixes (for buildbot test)
* [Revision #129](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/129)\
  Wed 2014-03-19 09:40:44 +0100
  * Include code signing process in vs build (disabled clude\_from\_all)
* [Revision #128](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/128)\
  Wed 2014-03-19 08:22:39 +0100
  * Added signtool support to digitally sign files
* [Revision #127](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/127)\
  Tue 2014-03-18 21:12:50 +0100
  * bump version number to 2.0.0 (release prepare) fixed rtf formatting of license
* [Revision #126](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/126)\
  Tue 2014-03-18 20:50:34 +0100
  * Added different upgrade codes for 32 and 64bit packages
* [Revision #125](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/125)\
  Tue 2014-03-18 20:09:00 +0100
  * Fix msi package name
* [Revision #124](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/124)\
  Tue 2014-03-18 17:53:50 +0100
  * buildbot and msi fixes
* [Revision #123](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/123)\
  Mon 2014-03-17 12:57:40 +0100
  * Replaced mysql\_options4 by mysql\_optionsv For libmysql compatibility mysql\_options4 macro was added
* [Revision #122](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/122)\
  Thu 2014-03-13 16:44:55 +0100
  * Fix for [CONC-83](https://jira.mariadb.org/browse/CONC-83): Crash in prepared statements after reconnect save stmt->mysql, since it will be set to NULL during reconnect and retrieve error code from saved pointer.
* [Revision #121](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/121)\
  Wed 2014-03-05 19:00:59 +0100
  * Fixed dbug enter/return in mysql\_find\_charset\_name
* [Revision #120](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/120)\
  Mon 2014-03-03 17:10:00 +0100
  * Fix for [CONC-81](https://jira.mariadb.org/browse/CONC-81): crash in ssl connection (caused by fix for [CONC-79](https://jira.mariadb.org/browse/CONC-79)) - prevent zeroing cache paraemters in vio\_reset
* [Revision #119](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/119)\
  Mon 2014-03-03 11:19:47 +0100
  * Fix for CONC79: Performance issue with c client library Added read-ahed cache for vio to reduce the number of reads
* [Revision #118](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/118)\
  Mon 2014-02-10 09:04:01 +0100
  * Fix for [CONC-77](https://jira.mariadb.org/browse/CONC-77): Backslash escaped quotes (', "") are not parsed correctly
* [Revision #117](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/117)\
  Fri 2014-02-07 11:31:30 +0100
  * Fix for [CONC-75](https://jira.mariadb.org/browse/CONC-75): options not handled correctly after a reconnect occured
* [Revision #116](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/116)\
  Thu 2014-02-06 12:49:39 +0100
  * Fix for [CONC-74](https://jira.mariadb.org/browse/CONC-74): Local infile handler crashes due to missing initialization of handler functions.
* [Revision #115](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/115)\
  Tue 2014-02-04 20:20:33 +0100
  * Fixed path for symbolic links on non Windows platforms when MySQL compatibility mode was set: All libraries including symlinks are now in ${CMAKE\_INSTALL\_PREFIX}/lib/mariadb
* [Revision #114](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/114)\
  Tue 2014-02-04 20:09:23 +0100
  * Fix for [CONC-71](https://jira.mariadb.org/browse/CONC-71): mysql\_real\_query crashes after server restart - We now check socket status before net\_flush (and return error if the socket is dead)
* [Revision #113](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/113)\
  Mon 2014-01-27 21:14:02 +0100
  * Fix for [CONC-70](https://jira.mariadb.org/browse/CONC-70): Unknown error when reading large packets via conpressed protocol
* [Revision #112](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/112)\
  Sat 2014-01-25 18:16:36 +0100
  * Fix for [CONC-67](https://jira.mariadb.org/browse/CONC-67): mysql\_stmt\_fetch returns error instead of MYSQL\_NO\_DATA when using cursors
* [Revision #111](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/111)\
  Fri 2014-01-24 09:02:03 +0100
  * Fix for [CONC-68](https://jira.mariadb.org/browse/CONC-68): SELECT fails with "Got packet bigger than 'max\_allowed\_packet'" on a table with longblob column with fields greater than 15MB
* [Revision #110](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/110)\
  Wed 2014-01-22 22:31:08 +0100
  * Fix for [CONC-66](https://jira.mariadb.org/browse/CONC-66): Support for quoted values in configuration file
* [Revision #109](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/109)\
  Sat 2014-01-11 20:09:32 +0100
  * Added mingw support (Win32). Special thanks to Eric Trinh for his patch!
* [Revision #108](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/108)\
  Fri 2014-01-03 01:19:44 +0100
  * Fix for [CONC-65](https://jira.mariadb.org/browse/CONC-65): Apples libiconv doesn't provide libiconv\_open so we need to link against the macports library instead
* [Revision #107](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/107)\
  Wed 2013-11-20 20:37:30 +0100
  * Fix for [CONC-60](https://jira.mariadb.org/browse/CONC-60): crash when STMT\_ATTR\_UPDATE\_MAX\_LENGTH attribute was set and new date formats are used. Special thanks to Lionel Elie Mamane and Daniel Bart for their tremendous help.
* [Revision #106](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/106)\
  Sun 2013-11-10 19:54:00 +0100
  * Added windows code page to CHARSET\_INFO structure
* [Revision #105](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/105)\
  Sun 2013-10-27 19:38:11 +0100
  * Fixed bug in prepared statements: wrong length for MYSQL\_TYPE{TIME,DATETIME,TIMESTAMP} renewed test certificates for ssl tests
* [Revision #104](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/104)\
  Sat 2013-10-26 18:55:24 +0200
  * Minor prepared statement fixes for time/date/datetime/timestamp types Added flag MADB\_BIND\_DUMMY which allows binding empty buffers
* [Revision #103](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/103)\
  Sun 2013-10-20 09:14:48 +0200
  * Fix for [CONC-58](https://jira.mariadb.org/browse/CONC-58): support OpenSSL version < 1.0.1
* [Revision #102](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/102)\
  Sun 2013-10-20 09:08:05 +0200
  * Fixed my\_error: my\_error used wrong offset (ignore EE\_FIRSTERROR)
* [Revision #101](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/101)\
  Mon 2013-10-14 14:17:54 +0200
  * Fixes for DBD:mysql ([CONC-57](https://jira.mariadb.org/browse/CONC-57)) added missing functions mysql\_read\_query\_result and mysql\_get\_parameters
* [Revision #100](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/100)\
  Thu 2013-10-10 15:14:15 +0200
  * Fixes for Win64 build
* [Revision #99](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/99)\
  Sat 2013-10-05 08:30:54 +0200
  * Fixed window compile error (removed uint from mysql.h)
* [Revision #98](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/98)\
  Fri 2013-10-04 20:55:23 +0200
  * Fix for [CONC-56](https://jira.mariadb.org/browse/CONC-56): provide MAX constants used by PHP's pdo extension
* [Revision #97](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/97)\
  Fri 2013-10-04 19:09:08 +0200
  * Windows build fixes - use /MT flag instead of /MD - add debug libraries to package
* [Revision #96](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/96)\
  Tue 2013-10-01 09:53:41 +0200
  * Removed all internal dependencies from ma\_dyncol. Fixed compiler warnings
* [Revision #95](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/95)\
  Mon 2013-09-30 12:23:13 +0200
  * Fixed warnings (Thanks to Evan Miller)
* [Revision #94](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/94)\
  Mon 2013-09-30 06:25:27 +0200
  * Fixed missing exported symbols
* [Revision #93](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/93)\
  Sat 2013-09-28 10:38:56 +0200
  * Added support for connection attributes
* [Revision #92](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/92)\
  Thu 2013-09-26 14:35:14 +0200
  * Added support for SSL related parameters in mysql\_option function
* [Revision #91](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/91)\
  Thu 2013-09-26 08:40:20 +0200
  * Fix for [CONC-53](https://jira.mariadb.org/browse/CONC-53): Fix C++ compiler errors
* [Revision #90](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/90)\
  Fri 2013-09-20 16:21:53 +0200
  * Minor fixes in ssl test
* [Revision #89](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/89)\
  Fri 2013-09-20 15:23:20 +0200
  * Fixed windows compile error in dynamic columns
* [Revision #88](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/88)\
  Fri 2013-09-20 14:48:20 +0200
  * Merge from 10.0 dynamic column implemenetation: - functions which operate with numeric keys now have suffix \_num - Fixes for MDEV 4993-4995
* [Revision #87](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/87)\
  Thu 2013-09-19 15:14:11 +0200
  * More SSL fixes: - verification functions for key and cert now use SSL\_context - Added support for server cert verification (hostname must match) - minor bug fixes
* [Revision #86](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/86)\
  Tue 2013-09-17 18:47:07 +0200
  * Added support for ssl server certification: mysql\_options: Added support MYSQL\_OPT\_SSL\_VALIDATE\_SERVER\_CERT flag added my\_ssl\_verify\_server\_cert which extracts the hostname and compares it with mysql->host
* [Revision #85](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/85)\
  Mon 2013-09-16 16:19:16 +0200
  * Fix for [CONC-50](https://jira.mariadb.org/browse/CONC-50): mysql\_real\_connect doesn't return an error if a an invalid ca file was specified.
* [Revision #84](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/84)\
  Wed 2013-09-04 18:45:54 +0200
  * Fix for [CONC-49](https://jira.mariadb.org/browse/CONC-49): local\_infile\_init didn't open files with binary flag
* [Revision #83](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/83)\
  Mon 2013-09-02 15:31:12 +0200
  * Windows fixes for dynamic columns
* [Revision #82](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/82)\
  Sat 2013-08-31 07:37:01 +0200
  * Fix for [CONC-48](https://jira.mariadb.org/browse/CONC-48): Allocate one more byte for trailing zero to prevent crash if the total lengths of compressed packages is equal to the value of net buffer size
* [Revision #81](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/81)\
  Fri 2013-08-23 18:35:07 +0200
  * Added dyamic column api Added character set conversion
* [Revision #80](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/80)\
  Tue 2013-08-20 16:40:03 +0200
  * Fix for [CONC-44](https://jira.mariadb.org/browse/CONC-44): LOAD DATA INFILE can't open utf16le encoded filenames
* [Revision #79](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/79)\
  Wed 2013-08-14 16:08:21 +0200
  * Fix for [CONC-46](https://jira.mariadb.org/browse/CONC-46): cleanup of my\_win\_init(), removed setlocale and server specific stuff
* [Revision #78](https://bazaar.launchpad.net/~maria-captains/mariadb-native-client/trunk/revision/78)\
  Wed 2013-08-14 06:12:23 +0200
  * removed safe\_malloc implementation

{% @marketo/form formid="4316" formId="4316" %}
