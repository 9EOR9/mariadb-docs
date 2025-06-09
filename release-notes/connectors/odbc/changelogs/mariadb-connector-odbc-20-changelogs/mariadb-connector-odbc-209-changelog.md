# MariaDB Connector/ODBC 2.0.9 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/2.0.9)[Release Notes](../../mariadb-connector-odbc-20-release-notes/mariadb-connector-odbc-209-release-notes.md)[Changelog](mariadb-connector-odbc-209-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 16 Nov 2015

For the highlights of this release, see the[release notes](../../mariadb-connector-odbc-10-release-notes/mariadb-connector-odbc-105-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #f12c796](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f12c796)\
  2015-11-13 21:14:18 +0200
  * Made some changes in cpack configuration - added missing/changed wrong variables values
* [Revision #34fc6c4](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/34fc6c4)\
  2015-11-12 02:55:04 +0200
  * When looking for DM files, add check if /usr/lib64 exists, and also added lib/x86\_64-linux-gnu and i386-linux-gnu as possible path suffix in such case
* [Revision #a5d0f2d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a5d0f2d)\
  2015-11-10 23:20:30 +0200
  * cmake checks if there are tests, and allows to build driver without tests Also 'test' folder excluded from cpack source package
* [Revision #2559c94](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2559c94)\
  2015-11-05 18:24:47 +0200
  * Added connector quality(i.e. beta) to the package name
* [Revision #ca3af04](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ca3af04)\
  2015-11-01 16:24:06 +0200
  * Added errno.h inclusion to testst. Otherwise build failed on some platforms
* [Revision #ddac58b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ddac58b)\
  2015-10-31 02:06:50 +0200
  * Adding missing FindIconv.cmake
* [Revision #4e70214](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4e70214)\
  2015-10-31 00:37:21 +0200
  * Fixed driver and testsuite to work with Unicode with UnixODBC(i.e. 2-bytes SQLWCHAR) Driver internally uses utf16le, instead of just utf16, on le platforms. This is needed to avoid BOMs with iconv Fixed bug that could cause crash, when iconv returns -1(i.e. could not convert the string), it could be interpreted((size\_t)-1) as very long string length Fixed wrong length calculations when surrogate utf16 pairs involved Added to test framework means to work with widestrings(SQLWCHAR). Changed tests accordingly.
* [Revision #94dcdd0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/94dcdd0)\
  2015-09-28 19:32:47 +0200
  * Merge branch 'master'(1.0) into [ODBC-2](https://jira.mariadb.org/browse/ODBC-2).0 + Version bump(to 2.0.9)
* [Revision #97fd947](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/97fd947)\
  2015-09-24 23:30:08 +0200
  * Small changes/additions to ssl. Added clr and options for fp. Setting of plugins directory
* [Revision #0ec5851](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0ec5851)\
  2015-09-25 22:38:32 +0200
  * Merge branch 'master' into [ODBC-2](https://jira.mariadb.org/browse/ODBC-2).0 + version bump
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
* [Revision #ced574b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ced574b)\
  2015-09-09 13:29:03 +0300
  * Some amendments to let cpack build source package on linux, as it works a bit better than on windows.
* [Revision #0ba0fc5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0ba0fc5)\
  2015-06-12 19:21:19 +0200
  * Merge branch 'master' into 2.0 + version bump to 2.0.8
* [Revision #aaab313](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/aaab313)\
  2015-05-13 01:15:12 +0200
  * Merge branch 'master' into [ODBC-2](https://jira.mariadb.org/browse/ODBC-2).0
* [Revision #e5007cd](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e5007cd)\
  2015-05-06 16:29:17 +0200
  * Enhanced connector tracing Reworked code around "Free" API functions
* [Revision #c6d8a10](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c6d8a10)\
  2015-04-24 20:11:23 +0200
  * Merge branch 'master' into [ODBC-2](https://jira.mariadb.org/browse/ODBC-2).0 + version bump
* [Revision #6e5c8a5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6e5c8a5)\
  2015-04-09 20:50:41 +0300
  1. Removed erroneous dependency of the connector on libodbc, made some changes enabling direct liking of tests
  2. Changed pthread\_mutex to be of PTHREAD\_MUTEX\_RECURSIVE type to avoid deadlocks, removed lock in one place
  3. Enabled connector tracing(bit 4 in the OPTIONS), made small improvements to tracing 4) Fixed possible crash in the MADB\_ConvertFromWChar if passed Error pointer is Null
  4. Bumped version(2.0.6)
  5. Removed ma\_compatibility.h(moved all usedul from it to ma\_platform\_posix.\*
* [Revision #1b44b14](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1b44b14)\
  2015-03-30 18:47:53 +0200
  * Fix of test failure in error.c with unixODBC.
* [Revision #709b512](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/709b512)\
  2015-03-25 18:48:52 +0100
  * Merge branch 'master' into [ODBC-2](https://jira.mariadb.org/browse/ODBC-2).0
* [Revision #744613d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/744613d)\
  2015-03-19 21:00:04 +0100
  * To be compatible with server code modules, my\_free in Connector/C has changed and expects one parameter only
* [Revision #5b9766c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5b9766c)\
  2015-03-18 09:59:29 +0100
  * Bumped version number
* [Revision #89f94ee](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/89f94ee)\
  2015-03-17 19:41:54 +0200
  * Fixed error in few tests macros causing repeating of commands(in case of error) Added mysql\_init if mariadb handle is null to the connection routine
* [Revision #2e8fc0c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2e8fc0c)\
  2015-03-16 23:41:26 +0200
  * Added connection string SOCKET for connecting to unix sockets Added cmake option DIRECT\_LINK\_TESTS to link tests directly against the connector
* [Revision #f7a63dc](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f7a63dc)\
  2015-03-03 14:35:45 +0200
  * Substituted \_i64toa with \_snprintf call, bumped version to 2.0.3
* [Revision #1607c16](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1607c16)\
  2015-03-03 14:30:46 +0100
  * Fixes for unresolved externals: Replase \_ito64a by longong2str Replace atoi64 by strtoll Bumped version number
* [Revision #16355bd](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/16355bd)\
  2015-03-02 18:28:55 +0100
  *
    * Removed WITH\_REVNO option - Removed iconv stuff - Bumped version number: Like on windows we will build without OpenSSL support in Connector/C
* [Revision #4c54921](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4c54921)\
  2015-02-27 20:01:35 +0100
  * Version bump - 2.0.1
* [Revision #0d33104](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0d33104)\
  2015-02-26 13:14:10 +0100
  * Merge branch 'master' into 2.0 + fix of MbstrCharLen and couple of tests in unicode.c
* [Revision #122ea34](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/122ea34)\
  2015-02-18 20:42:46 +0200
  * Has moved MbstrOctetLen to ma\_string.c so it is visible on Windows as well
* [Revision #52e9aec](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/52e9aec)\
  2015-02-18 19:25:16 +0200
  * Small fixes in testcases
* [Revision #1df2358](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/1df2358)\
  2015-02-18 18:17:10 +0100
  * Fixed READNE
* [Revision #0fbcb68](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0fbcb68)\
  2015-02-17 12:44:13 +0100
  * Added packaging for non windows platforms
* [Revision #f4a3e73](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f4a3e73)\
  2015-02-17 00:07:24 +0200
  * Fix of a bug in MADB\_SetString on \*nix - strncpy that is used instead of strncpy\_s, does not write null byte if source string is truncated to the length of dest buffer Small fixes in tests/framework
* [Revision #b42167e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b42167e)\
  2015-02-16 18:14:00 +0200
  * Removed last reference of WIdeCharToMultiByte. Slightly fixed MbstrOctetLen. Small fixes in tests/testframework
* [Revision #699334f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/699334f)\
  2015-02-16 12:33:51 +0100
  * If precision of SQL\_NUMERIC was not specified, the default value should be used. See [en-us](https://support2.microsoft.com/kb/222831/en-us)
* [Revision #17fe70c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/17fe70c)\
  2015-02-16 12:29:23 +0100
  * fixed hard coded comparision for selected database in catalog test
* [Revision #e7a831f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e7a831f)\
  2015-02-16 12:03:25 +0100
  * Fixed crash in t\_msdev\_bug (info.c): SQLGetConnectOption requires buffer size of SQL\_MAX\_OPTION\_STRING\_LENGTH
* [Revision #983c240](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/983c240)\
  2015-02-16 11:38:28 +0100
  * Fixed t\_mult\_stmt\_free test case for non windows platforms
* [Revision #6833467](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6833467)\
  2015-02-16 01:43:02 +0200
  * Merge
* [Revision #011e68a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/011e68a)\
  2015-02-16 01:40:58 +0200
  * Fix of display length calculation. Fixes and amndments in/to testcases and testframework. Merge
* [Revision #de7fad9](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/de7fad9)\
  2015-02-14 16:14:04 +0100
  * Fixed name in README
* [Revision #6a41890](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6a41890)\
  2015-02-14 16:12:02 +0100
  * Merge branch '2.0' of [mariadb-connector-odbc](https://github.com/MariaDB/mariadb-connector-odbc) into 2.0
* [Revision #710b4ef](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/710b4ef)\
  2015-02-14 16:11:28 +0100
  * Add toolchain file for linux\_x86 cross compiling
* [Revision #b0672f3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b0672f3)\
  2015-02-13 21:40:32 +0200
  * Fix of bug in driver in work with UnixODBC. UnixODBC uses SQLError to fetch error messages until it returns not success. We mapped it to SQLGetDiagRec always trying to fetch 1st record. The patch introduces field of current record in MADB\_Error(ErrorNum), and SQLError increments it. All API calls reset it.
* [Revision #9b82f2c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9b82f2c)\
  2015-02-13 21:40:32 +0200
  * Fix of bug in driver in work with UnixODBC. UnixODBC uses SQLError to fetch error messages until it returns not success. We mapped it to SQLGetDiagRec always trying to fetch 1st record. The patch introduces field of current record in MADB\_Error(ErrorNum), and SQLError increments it. All API calls reset it.
* [Revision #b0103f5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b0103f5)\
  2015-02-12 20:41:35 +0100
  * More fixes of missing symbols. This time of newly introduced while fixed unixodbc problems with calls of odbc api from inside driver.
* [Revision #bd25021](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bd25021)\
  2015-02-12 17:22:05 +0200
  * Fixed one more missing symbol on linux Move MbstrCharLen to ma\_string.c, added one more parameter to MADB\_ConvertAnsi2Unicode - determining whether to copy terminating blank additionaly. That helps to resolve issue what lenght to returrn if source string length included terminating byte. Changed LengthIndicator type to SQLLEN\* Documented MADB\_ConvertAnsi2Unicode a bit.
* [Revision #9334392](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/9334392)\
  2015-02-12 13:05:04 +0100
  * Fixed more unresolved externals
* [Revision #0cfdfd7](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0cfdfd7)\
  2015-02-12 13:03:09 +0100
  * Changed lpszDefault to empty string. According to the ODBC specificatin this argument cannot be NULL.
* [Revision #db41617](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/db41617)\
  2015-02-12 10:06:43 +0100
  * On 64-bit SQLRowCount expects SQLLEN (not int)
* [Revision #b5c03c5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b5c03c5)\
  2015-02-12 09:57:27 +0100
  * Fixed crash on Linux: We need to make a copy of parameter before modifying
* [Revision #651f543](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/651f543)\
  2015-02-12 08:09:55 +0100
  * Prevent deadlocks during external Descriptor allocation
* [Revision #dc4e85f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/dc4e85f)\
  2015-02-11 19:56:25 +0200
  * Support of SQL\_DESC\_NULLABLE(merge)
* [Revision #038d5a5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/038d5a5)\
  2015-02-11 19:51:34 +0200
  * SQLGetPrivateProfileString result is now checked to be >0(required for UnixODBC)
* [Revision #f886f3a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f886f3a)\
  2015-02-11 16:35:03 +0200
  * Added more missing symbols, changed (one of) internal calls of odbc api calls to call of new separate function (or function from libodbc was called). Changed debug log to be written to different place(was c:maodbc.log) Now on windows that is %USERPROFILE% or %TMP% on Windows, and %HOME% or /tmp on \*nix
* [Revision #19348c3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/19348c3)\
  2015-02-11 12:24:32 +0100
  * Added support for SQL\_DESC\_NULLABLE in SQLColAttribute
* [Revision #d82480f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d82480f)\
  2015-02-11 11:22:23 +0100
  * Use strncasecmp instead of \_strnicmp on non Windows platforms
* [Revision #975d9e3](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/975d9e3)\
  2015-02-11 11:00:53 +0100
  * Added MA\_SQLAllocStmt
* [Revision #4dbf2d0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/4dbf2d0)\
  2015-02-11 09:59:15 +0100
  * Merge from 2.0
* [Revision #172020f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/172020f)\
  2015-02-11 09:50:38 +0100
  * More Linux fixes: - for now we don't build a unicode verion (to change this adjust CMakeList.txt - On non windows builds we use mariadb\_config (if not installed in a default directory please specify -DMARIADB\_DIR - To prevent name collision when calling SQL\* functions, we use now MA\_SQL\* function names. The prototypes (for AscII functions) are defined in ma\_odbc.h
* [Revision #6751718](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6751718)\
  2015-02-10 14:10:32 +0100
  * More Linux build fixes
* [Revision #327480b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/327480b)\
  2015-02-10 10:28:51 +0100
  * check if SQL\_CONVERT\_GUID is supported/defined
* [Revision #a7bec42](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a7bec42)\
  2015-02-10 10:21:22 +0100
  * Check if SQLColAttribute/W expects SQLPOINTER
* [Revision #7178d11](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/7178d11)\
  2015-02-10 09:00:00 +0100
  * If available we use odbc\_config to determine location of unixODBC include files and libraries
* [Revision #5a086e0](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5a086e0)\
  2015-02-10 07:55:37 +0100
  * Fixed lib suffix for 64-bit builds
* [Revision #a58636a](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/a58636a)\
  2015-02-09 18:37:33 +0200
  * Defined missing (on linux) symbols
* [Revision #8f9622b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/8f9622b)\
  2015-02-09 04:43:51 +0100
  * Lost during previous merge stuff
* [Revision #e3ccb3b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/e3ccb3b)\
  2015-02-09 01:46:07 +0100
  * DM requests ODBC version when charset is not initialized - that caused error in encoding, and for DM it was incorrect value.
* [Revision #ac78915](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ac78915)\
  2015-02-08 23:22:13 +0100
  * Fix of compilation warnings on linux and fix of setup lib build on Windows Some small additions to .gitignore
* [Revision #c546073](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/c546073)\
  2015-02-07 03:56:01 +0100
  * Adding missing FindDM.cmake plus some fixes in linux specific files
* [Revision #72c905e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/72c905e)\
  2015-02-07 02:24:28 +0100
  * Stuff for linux - mostly charsets conversion
* [Revision #bb2cf76](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/bb2cf76)\
  2015-02-04 16:44:35 +0100
  * Added freeing of explicitly allocated descriptors on disconnect. That is required by ODBC specs "...after it successfully disconnects from the data source, frees those statements and all descriptors that have been explicitly allocated on the connection"
* [Revision #2aa408d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/2aa408d)\
  2015-02-01 16:07:48 +0100
  * Fix of crashes in the DS setup dialog and in freeing explicit descriptor, if statement that used it has been free'd prior to that. Setup dialog crashed after test of connection. The reason was that connection function in driver after successful stored pointer to the DSN structure it used in the DBC object. And setup lib passed pointer to the structure allocated on stack. The patch makes caller decide whether to store DSN pointer or not. Stmt destructor did not check if ard and apd are explicitly allocated, and always free'd them. That lead to the crash when application attempted to free such descriptor afterwards. Also patch contains minor changes such as change of the project name and amendments to couple of testcases.
* [Revision #223ec8b](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/223ec8b)\
  2015-02-07 04:46:33 +0200
  * Adding missing FindDM.cmake plus some fixes in linux specific files
* [Revision #aaf494e](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/aaf494e)\
  2015-02-07 02:24:28 +0100
  * Stuff for linux - mostly charsets conversion

{% @marketo/form formid="4316" formId="4316" %}
