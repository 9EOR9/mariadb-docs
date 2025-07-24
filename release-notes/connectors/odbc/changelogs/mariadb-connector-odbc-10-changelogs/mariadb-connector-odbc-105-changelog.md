# Connector/ODBC 1.0.5 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/ODBC is:[**MariaDB Connector/ODBC 3.2.5**](../../mariadb-connector-odbc-3-2-release-notes/mariadb-connector-odbc-3-2-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-odbc/1.0.5)[Release Notes](../../mariadb-connector-odbc-10-release-notes/mariadb-connector-odbc-105-release-notes.md)[Changelog](mariadb-connector-odbc-105-changelog.md)[About MariaDB Connector/ODBC](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-odbc/README.md)

**Release date:** 10 Sep 2015

For the highlights of this release, see the [release notes](../../mariadb-connector-odbc-10-release-notes/mariadb-connector-odbc-105-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-odbc) you can view more details of the revision and view diffs of the code modified in that revision.

* [Revision #6bb4c099](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/6bb4c099)\
  Sun Sep 6 07:06:07 2015 +0200
  * SQLGetTypeInfo incorrectly reported whether the type is signed or unsigned\
    for many types.
  * Fixed once again returned data length for fixed length types in SQLGetData -\
    affected work with MS Access. Made buffer length returned rather than field\
    size. It happens that for some column types Access does not use default C\
    type for binding.
* [Revision #d470ee7f](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/d470ee7f)\
  Tue Aug 25 22:28:32 2015 +0200
  * Made debug log available in all build types and controled solely by\
    connection option.
  * Did sort of merg of debug log enhancements from 2.0 + added date to the\
    timestamp, and added timestamp to the error message.
* [Revision #f3f4751d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f3f4751d)\
  Tue Aug 18 12:48:47 2015 +0200
  * Fix of small bug in the reading of DS information into data structure that\
    caused not displaying of the TCP protocol selection in the DS dialog.
  * Also removed from the dialog not supported options.
* [Revision #b93bc66c](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/b93bc66c)\
  Tue Aug 11 21:00:20 2015 +0200
  * Functionality for fixing rs column types. Access needs that in catalog\
    functions while linking external ODBC table.
  * Our catalo functions + SQLGetTypeInfo return all integer fields as int,\
    while many of them are smallint. MariaDB/MySQL do not allow to cast to\
    short, thus needed to add some client side magic. Access gets those data as\
    SQL\_C\_DEFAULT type, and yilds error if retrned data length differs from\
    default size(even though standard does not require to return it for fixed\
    length types).
* [Revision #51c95a77](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/51c95a77)\
  Thu Jul 2 00:48:11 2015 +0200
  * Fixed bug in display lenght calcualtion for binary fields, and for string\
    fields in case of multibyte charset.
* [Revision #0591b924](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/0591b924)\
  Fri Jun 12 00:33:39 2015 +0200
  * Fix of bug in string length calculation in the SQLGetData
  * Small fix in SQLTables - TABLE\_TYPE could be "BASE\_TABLE" instead of "TABLE"
* [Revision #23f13a8d](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/23f13a8d)\
  Wed May 13 00:44:13 2015 +0200
  * The fix and the testcase for [ODBC-21](https://jira.mariadb.org/browse/ODBC-21) if stmt prepare fails while the handle\
    reused, further use of the handler rather impossible with the server error\
    of unknown stmt handler in mysqld\_stmt\_reset Some amends/fixes in the main\
    cmake file.
* [Revision #22e2a6a6](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/22e2a6a6)\
  Wed May 6 01:36:45 2015 +0200
  * Fix of the crash in 64bit setup lib.
  * Address was casted to LONG for passing to other function(s)
* [Revision #09dd03d5](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/09dd03d5)\
  Fri Apr 24 18:27:18 2015 +0200
  1. Fix of flaw in logic in SQLError - now if more than 1 handle passed, it\
     takes lower level handle first(the API call is deprecated, but some app\
     still use it)
  2. Fixed some column and octet size computation bugs - there could be errors in\
     case of mb charsets.
* [Revision #ee79ec17](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/ee79ec17)\
  Mon Mar 23 22:13:52 2015 +0100
  * Optimization for statements without parameters if statement does not contain\
    parameter placeholders, i.e. unlikely to be executed more than once, and it\
    does not return resultset, and it is not a batch of statements, the\
    connector does not use PS for such a query, and executes it with\
    mysql\_real\_query
* [Revision #5153ef11](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/5153ef11)\
  Thu Mar 5 00:04:50 2015 +0100
  * Added lock/critical section to places where they seem to be missing.
  * Removed writing to debug file by default.
* [Revision #f34d8151](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/f34d8151)\
  Tue Feb 24 22:08:21 2015 +0100
  * Added fetch of metadata after prepare and execute - there was the bug caused\
    by (not doing) that. Made re-initializing of ird unconditional after\
    execute.
  * Added fix of SQL\_NUMERIC's precision from 2.0
* [Revision #318fcfe2](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/318fcfe2)\
  Wed Feb 4 16:44:35 2015 +0100
  * Added freeing of explicitly allocated descriptors on disconnect. That is\
    required by ODBC specs "...after it successfully disconnects from the data\
    source, frees those statements and all descriptors that have been explicitly\
    allocated on the connection"
* [Revision #afe145ed](https://github.com/mariadb-corporation/mariadb-connector-odbc/commit/afe145ed)\
  Sun Feb 1 16:07:48 2015 +0100
  * Fix of crashes in the DS setup dialog and in freeing explicit descriptor, if\
    statement that used it has been free'd prior to that. Setup dialog crashed\
    after test of connection. The reason was that connection function in driver\
    after successful stored pointer to the DSN structure it used in the DBC\
    object. And setup lib passed pointer to the structure allocated on stack.\
    The patch makes caller decide whether to store DSN pointer or not.
  * Stmt destructor did not check if ard and apd are explicitly allocated, and\
    always free'd them. That lead to the crash when application attempted to\
    free such descriptor afterwards.

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
