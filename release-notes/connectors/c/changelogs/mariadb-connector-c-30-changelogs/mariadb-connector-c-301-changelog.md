# MariaDB Connector/C 3.0.1 Changelog

The most recent [_**Stable**_](../../../../mariadb-release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/3.0.1)[Release Notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-301-release-notes.md)[Changelog](mariadb-connector-c-301-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-c/README.md)

**Release date:** 18 Jan 2017

For the highlights of this release, see the[release notes](../../mariadb-connector-c-30-release-notes/mariadb-connector-c-301-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #ef9a4d2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ef9a4d2)\
  2017-01-17 13:23:34 +0100
  * Fixed version number to 3.0.1 (was 3.1.0)
* [Revision #097cd84](https://github.com/mariadb-corporation/mariadb-connector-c/commit/097cd84)\
  2017-01-12 17:44:28 +0100
  * removed MY\_MUTEX\_INIT\_FAST due to build errors
* [Revision #8232550](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8232550)\
  2017-01-11 15:24:19 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #aa7c9a7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aa7c9a7)\
  2017-01-06 11:35:53 +0300
  * Remove plugins/trace/.trace\_example.c.swo
* [Revision #65d2c41](https://github.com/mariadb-corporation/mariadb-connector-c/commit/65d2c41)\
  2017-01-11 15:17:53 +0100
  * [CONC-224](https://jira.mariadb.org/browse/CONC-224): Allow to build Connector/C without TLS/SSL support. - CMake option -DWITH\_SSL=OFF disables TLS/SSL support for connector/c - Fixed warning when building with OpenSSL 1.1.0c
* [Revision #ee6f05c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ee6f05c)\
  2017-01-04 16:34:15 +0100
  * fixed output for --plugindir: plugindir option now prints PLUGIN\_DIR instead of MARIADB\_PLUGINDIR
* [Revision #18fd29b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/18fd29b)\
  2017-01-04 12:45:11 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #0f38ae6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0f38ae6)\
  2017-01-02 22:33:03 +0100
  * update .gitignore
* [Revision #fd005f9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fd005f9)\
  2017-01-04 12:44:08 +0100
  * Fixed exit code in case the test can't connect
* [Revision #99419d3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/99419d3)\
  2017-01-02 12:47:52 +0100
  * Fix for [CONC-223](https://jira.mariadb.org/browse/CONC-223): Add client support for missing collations If a collation is not available the client will not be able to set correct character set.
* [Revision #cb8d9d8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb8d9d8)\
  2017-01-02 00:52:25 -0800
  * Fix for [CONC-222](https://jira.mariadb.org/browse/CONC-222): Fix installation of include files (bug was introduced by commit d0a0e4c898bf10d33d7dbfa1efbea024a9aa1a4a)
* [Revision #2261808](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2261808)\
  2016-12-30 08:05:50 +0100
  * Added async support for mysql\_reset\_connection
* [Revision #87e861c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/87e861c)\
  2016-12-29 19:10:35 +0100
  * client side implemetation for [MDEV-10340](https://jira.mariadb.org/browse/MDEV-10340): int STDCALL mysql\_reset\_connection(MYSQL \*mysql)
* [Revision #cae391f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cae391f)\
  2016-12-21 19:21:37 +0100
  * Lowered required GnuTLS version number to bugfix/security release 3.3.24 reverted last commit which lowered GnuTLS version number to 3.3.0 (which is a nogo!)
* [Revision #b4b0f78](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b4b0f78)\
  2016-12-19 13:48:05 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #13171b2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/13171b2)\
  2016-12-19 03:41:11 -0800
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #d0a0e4c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d0a0e4c)\
  2016-12-19 03:40:14 -0800
  * Windows packaging fixes
* [Revision #00fb9ac](https://github.com/mariadb-corporation/mariadb-connector-c/commit/00fb9ac)\
  2016-12-19 13:47:19 +0100
  * Stop build if gnutls version doesn't fit
* [Revision #ca7d4ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ca7d4ad)\
  2016-12-19 07:18:12 +0100
  * Fixed typo for msi build
* [Revision #413b8bc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/413b8bc)\
  2016-12-13 12:39:32 +0100
  * Build fix for OpenSSL\_1.1 Fixed connection error message on windows (deliver correct error code)
* [Revision #ab3ffdc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ab3ffdc)\
  2016-12-13 07:09:06 +0100
  * removed api function mysql\_get\_server\_status (introduced in last commit). Instead of mariadb\_get\_infov now supports additional parameters: \* MARIADB\_CONNECTION\_SERVER\_STATUS \* MARIADB\_CONNECTION\_SERVER\_CAPABILITIES \* MARIADB\_CONNECTION\_EXTENDED\_SERVER\_CAPABILITIES \* MARIADB\_CONNECTION\_CLIENT\_CAPABILITIES
* [Revision #7a1e3a6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7a1e3a6)\
  2016-12-10 14:09:53 +0100
  *
    * Fixed crash in prepared statement: Indicator variable should be checked only if we are in bulk operation mode (=stmt->array\_size > 0 and bulk is supported by server - Added new api function mysql\_get\_server\_status, so client applications no longer need to access members of the mysql structure
* [Revision #070fb30](https://github.com/mariadb-corporation/mariadb-connector-c/commit/070fb30)\
  2016-12-03 09:21:32 +0100
  * If a kill statement was prepared and executed we need to check return code of net\_stmt\_close in case the connection which belongs to the statement was killed.
* [Revision #326e719](https://github.com/mariadb-corporation/mariadb-connector-c/commit/326e719)\
  2016-11-29 18:22:38 +0100
  * Removed strndup from trace-example (not available on all platforms)
* [Revision #6453670](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6453670)\
  2016-11-29 13:30:17 +0100
  * Fix for [CONC-218](https://jira.mariadb.org/browse/CONC-218): To prevent unexpected behavior when reusing a statement with mariadb\_stmt\_execute\_direct a call to mysql\_stmt\_attr\_set with option STMT\_ATTR\_PREBIND\_PARAMS will reset the statement before.
* [Revision #dad2cf6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dad2cf6)\
  2016-11-28 18:32:26 +0100
  * remove async\_example
* [Revision #c89d5d3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c89d5d3)\
  2016-11-26 13:47:43 +0100
  * Fix for [CONC-217](https://jira.mariadb.org/browse/CONC-217): mariadb\_stmt\_execute\_direct: Clear error message from mysql\_stmt\_execute if mysql\_stmt\_prepare failed
* [Revision #8695a17](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8695a17)\
  2016-11-26 13:23:57 +0100
  * Added support for STMT\_INDICATE\_IGNORE indicator - please note that the counter part for indicator type ignore is not pushed in server repo yet.
* [Revision #aabaac0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/aabaac0)\
  2016-11-24 08:56:27 +0100
  * Plugin fixes - include ma\_errmsg.h if plugin is built dynamically - trace\_example fixes
* [Revision #3e624e5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3e624e5)\
  2016-11-17 16:04:33 +0100
  * removed definition of SQLSTATE\_UNKNOWN (10.2 integration)
* [Revision #e5384dd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e5384dd)\
  2016-11-17 12:34:36 +0100
  * renamed ma\_errmsg to errmsg.h in .in file
* [Revision #a11382a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a11382a)\
  2016-11-17 10:47:15 +0100
  * Row wise binding fixes for prepared statements (bulk) - Fixed offset calculation for length and indicator - Ignore null values if indicator is STMT\_INDICATOR\_DEFAULT
* [Revision #967b283](https://github.com/mariadb-corporation/mariadb-connector-c/commit/967b283)\
  2016-11-16 18:13:59 +0100
  * renamed ma\_errmsg.h back to errmsg.h
* [Revision #a499722](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a499722)\
  2016-11-16 17:27:59 +0100
  * removed ma\_errmsg from mysql.h
* [Revision #3378c0d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3378c0d)\
  2016-11-13 18:37:22 +0100
  * Fixed array\_binding for MYSQL\_TYPE\_NULL
* [Revision #03a7ec1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/03a7ec1)\
  2016-11-12 17:51:01 +0100
  * Support mariadb\_stmt\_execute\_direct also for versions < 10.2 Bundled COM\_CLOSE and COM\_PREPARE packets
* [Revision #6486232](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6486232)\
  2016-11-10 05:49:11 +0100
  * Removed com\_multi for mariadb\_stmt\_execute\_direct added support for pre 10.2-servers in mariadb\_stmt\_execute\_direct
* [Revision #4d1af73](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4d1af73)\
  2016-11-04 16:02:08 +0100
  * Set stmt\_id to -1 only for mariadb\_stmt\_execute\_direct
* [Revision #884ee22](https://github.com/mariadb-corporation/mariadb-connector-c/commit/884ee22)\
  2016-10-23 15:53:24 +0200
  * Smaller fixes for LibreOffice integration: - added type MYSQL\_TYPE\_JSON (=245) - include error numbers (ma\_errmsg.h) via mysql.h - convert MYSQL\_TYPE\_JSON to string (prepared statements) - added error message number 2034 (invalid buffer)
* [Revision #6306c9f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6306c9f)\
  2016-10-20 08:47:51 +0200
  *
    * removed COM\_MULTI from options COM\_MULTI is now available for internal use only, e.g. in mariadb\_stmt\_execute\_direct
* [Revision #468cda3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/468cda3)\
  2016-10-18 10:53:31 +0200
  * Fixed compilation errors introduced by 629ec646303..
* [Revision #532ad45](https://github.com/mariadb-corporation/mariadb-connector-c/commit/532ad45)\
  2016-10-17 16:05:25 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #93af3ae](https://github.com/mariadb-corporation/mariadb-connector-c/commit/93af3ae)\
  2016-10-14 17:49:30 +0000
  * Simplify and fix ma\_schannel\_read\_decrypt() to cache state between the calls.
* [Revision #629ec64](https://github.com/mariadb-corporation/mariadb-connector-c/commit/629ec64)\
  2016-10-13 15:17:45 +0000
  * Fix PVIO to return number of bytes read/written as "signed" integer since there is a lot of checks for return code being < 0 or -1.
* [Revision #c20974b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c20974b)\
  2016-10-17 16:02:51 +0200
  *
    * removed global context for tls, so code can be used also with no yassl branch in 10.2 - added new gnutls cipher mapping - fixed ssl test case: skip hostname verification if both server and client run on localhost - added server certificates
* [Revision #7cb8479](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7cb8479)\
  2016-10-12 21:04:55 +0000
  * Fix Win64 warnings. Correctly define my\_socket in ma\_global.h
* [Revision #e34a595](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e34a595)\
  2016-10-12 10:48:31 +0000
  * [MDEV-11008](https://jira.mariadb.org/browse/MDEV-11008) Connector/C integration does not respect INSTALL\_LIBDIR or INSTALL\_DOCDIR
* [Revision #7e2804f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7e2804f)\
  2016-10-11 14:25:49 +0200
  * Fix for [CONC-207](https://jira.mariadb.org/browse/CONC-207): Minimum version for CMake is 3.4.0 (gnutls\_set\_priority\_direct)
* [Revision #3837442](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3837442)\
  2016-10-11 13:55:01 +0200
  * Fix for bug [MDEV-10894](https://jira.mariadb.org/browse/MDEV-10894): fixed conversion for big-endian platforms
* [Revision #b0d41a8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b0d41a8)\
  2016-10-07 08:10:08 +0200
  * Updated .gitignore
* [Revision #b98083c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b98083c)\
  2016-10-06 09:45:24 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #fcb8da5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fcb8da5)\
  2016-09-30 17:40:58 +0000
  * [MDEV-10357](https://jira.mariadb.org/browse/MDEV-10357) my\_context\_continue() does not store current fiber on Windows
* [Revision #04c05ea](https://github.com/mariadb-corporation/mariadb-connector-c/commit/04c05ea)\
  2016-09-30 13:54:04 +0000
  * Do not remove PROJECT() from MariaDB Connector/C, there is no need
* [Revision #be8f507](https://github.com/mariadb-corporation/mariadb-connector-c/commit/be8f507)\
  2016-09-27 09:35:12 +0000
  * Fix broken compilation on buildbot
* [Revision #6723c52](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6723c52)\
  2016-10-06 09:44:57 +0200
  * Fixed function declaration for mysql\_error and mysql\_info (const char \* instead of char \*)
* [Revision #85185da](https://github.com/mariadb-corporation/mariadb-connector-c/commit/85185da)\
  2016-09-27 08:22:23 +0200
  * move closesocket to error label
* [Revision #f750c8f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f750c8f)\
  2016-09-26 17:08:31 +0200
  * Fix for [CONC-202](https://jira.mariadb.org/browse/CONC-202): Compile error with Visual Studio Visual Studio 15 returns an error if sprintf was defined for mapping to the recommended \_snprintf function. Definition was removed which might result in a compiler warning.
* [Revision #c8dd089](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c8dd089)\
  2016-09-24 11:14:53 +0200
  * When an attempt to open a unix sucket failed, the socket was not properly closed.
* [Revision #878f143](https://github.com/mariadb-corporation/mariadb-connector-c/commit/878f143)\
  2016-09-22 21:48:54 +0000
  * Fix misc.warnings.
* [Revision #63bdcec](https://github.com/mariadb-corporation/mariadb-connector-c/commit/63bdcec)\
  2016-09-22 13:20:36 +0200
  * Merge branch 'serg-integr'
* [Revision #4ff192b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4ff192b)\
  2016-09-21 17:35:54 +0200
  * few bugs in the tracker support
* [Revision #f968c04](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f968c04)\
  2016-09-16 12:19:44 +0200
  * a couple of PS bugs in ps\_fetch\_bin
* [Revision #0fa6b16](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0fa6b16)\
  2016-09-15 12:30:44 +0200
  * comments, use CR\_CONNECTION\_ERROR also for tcpip
* [Revision #f95877d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f95877d)\
  2016-09-15 09:21:30 +0200
  * Merge branch 'master' into serg-integr
* [Revision #b9d6bea](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b9d6bea)\
  2016-09-13 14:28:23 +0200
  * fix the installation layout
* [Revision #a4ce80d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a4ce80d)\
  2016-09-12 22:58:28 +0200
  * fix fetching TEXT parameters in PS protocol
* [Revision #2e6c9b9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2e6c9b9)\
  2016-09-12 16:21:12 +0000
  * Remove gcc -Wvla option , is not there in old gcc
* [Revision #110aa7d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/110aa7d)\
  2016-09-12 16:05:02 +0000
  * Windows : Do not default connection protocol to SHM,only if mysql->options.shared\_memory\_base\_name is set.
* [Revision #15693a6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/15693a6)\
  2016-09-12 13:50:02 +0000
  * Remove wrong cached value for HAVE\_CXX\_NEW
* [Revision #da8977d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/da8977d)\
  2016-09-12 11:47:14 +0000
  * Merge branch 'master' into serg-integr
* [Revision #55c0896](https://github.com/mariadb-corporation/mariadb-connector-c/commit/55c0896)\
  2016-09-08 20:09:51 +0200
  * openssl config
* [Revision #3e924b3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3e924b3)\
  2016-09-08 15:41:41 +0200
  * compilation failure on linux
* [Revision #38b5e40](https://github.com/mariadb-corporation/mariadb-connector-c/commit/38b5e40)\
  2016-09-07 17:14:02 +0000
  * C/C integration : Fix mysql\_test\_client test - #include \<stdlib.h> for strtod and other prototypes - remove ma\_config\_win.h as it redefines things from ma\_config.h - fix compile warnings
* [Revision #c87193a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c87193a)\
  2016-09-07 08:33:03 +0200
  * use ssl as libmysqlclient did
* [Revision #11a47c5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/11a47c5)\
  2016-09-06 19:50:38 +0200
  * fix two bugs in dialog plugin
* [Revision #090a047](https://github.com/mariadb-corporation/mariadb-connector-c/commit/090a047)\
  2016-09-06 13:18:22 +0000
  * fix path to generated header file
* [Revision #6c582c0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6c582c0)\
  2016-09-05 18:03:23 +0000
  * fix C/C integration, Windows build
* [Revision #7a787b1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7a787b1)\
  2016-09-04 13:17:24 +0200
  * C/C integration in MariaDB Server builds
* [Revision #4fe8d96](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4fe8d96)\
  2016-09-04 13:08:22 +0200
  * correct the bugtracker url
* [Revision #0780933](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0780933)\
  2016-09-04 13:07:59 +0200
  * really disable safe mutex
* [Revision #105fc56](https://github.com/mariadb-corporation/mariadb-connector-c/commit/105fc56)\
  2016-09-04 13:07:39 +0200
  * compiler warnings
* [Revision #0d975f6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0d975f6)\
  2016-09-04 13:05:52 +0200
  * .gitignore
* [Revision #3f2fe93](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3f2fe93)\
  2016-09-15 12:14:58 +0000
  * Revert "Implement mysql\_stmt\_execute\_direct without COM\_MULTI."
* [Revision #9b436ea](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9b436ea)\
  2016-09-13 16:12:34 +0200
  * TLS fixes: - don't use password in global context - load keys and certs via callback functions - don't use gnutls\_bye since server is not able to detect dead socket - fixed valgrind errors in gnutls
* [Revision #4ed1ca0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4ed1ca0)\
  2016-09-10 13:21:02 +0000
  * Simplify rand\_str()function
* [Revision #1279753](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1279753)\
  2016-09-10 13:19:55 +0000
  * schannel cleanups - use CertFreeCertificateContext() to free memory allocated by QueryContextAttributes(SECPKG\_ATTR\_REMOTE\_CERT\_CONTEXT) - consistently use "SSL connection error: " prefix for schannel errors
* [Revision #895b2eb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/895b2eb)\
  2016-09-09 20:22:38 +0000
  * Fix warnings
* [Revision #2157642](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2157642)\
  2016-09-09 20:17:30 +0000
  * Cleanup/fix schannel TLS implementation - remove global variables - remove in memory certificate stores that cache all CRL and all CA - verify certificate against ssl\_ca and ssl\_crl specified in connection options (not against all CRL/CA in store)
* [Revision #8afde21](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8afde21)\
  2016-09-09 20:03:16 +0000
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/mariadb/mariadb-connector-c)
* [Revision #571dc5f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/571dc5f)\
  2016-09-08 09:45:37 +0200
  * Fixed crash in gnutls: In case handshake will fail a further call to gnutls\_bye function will lead in a crash. Therefore we free the ssl handle immediately after handshake failed.
* [Revision #7d26557](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7d26557)\
  2016-09-08 08:36:07 +0200
  * GnuTLS: Added support for cipher mapping The following openssl cipher names are supported and will be mapped to gnutls priority: DHE-RSA-AES256-GCM-SHA384 DHE-RSA-AES256-SHA256 DHE-RSA-AES256-SHA DHE-RSA-CAMELLIA256-SHA AES256-GCM-SHA384 AES256-SHA256 AES256-SHA CAMELLIA256-SHA DHE-RSA-AES128-GCM-SHA256 DHE-RSA-AES128-SHA256 DHE-RSA-AES128-SHA DHE-RSA-CAMELLIA128-SHA AES128-GCM-SHA256 AES128-SHA256 AES128-SHA CAMELLIA128-SHA EDH-RSA-DES-CBC3-SHA DES-CBC3-SHA DHE-RSA-AES256-SHA DHE-RSA-CAMELLIA256-SHA AES256-SHA CAMELLIA256-SHA
* [Revision #c68c5dc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c68c5dc)\
  2016-09-08 08:01:21 +0200
  * Part for fix of [CONC-200](https://jira.mariadb.org/browse/CONC-200): declare type of my\_ulonglong
* [Revision #b0506f6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b0506f6)\
  2016-09-08 07:59:34 +0200
  * Instead of mysql\_real\_connect in tests we call now my\_test\_connect to apply global options like tls usage
* [Revision #9f88e25](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9f88e25)\
  2016-09-03 12:46:50 +0200
  * Compiler warning fixes
* [Revision #7615dc7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7615dc7)\
  2016-08-31 19:08:59 +0200
  * Fixed length packet for COM\_MULTI parts (kudos to Sanja Byelkin)
* [Revision #454e524](https://github.com/mariadb-corporation/mariadb-connector-c/commit/454e524)\
  2016-08-25 06:22:29 +0200
  * Fixed test build
* [Revision #2a7cc97](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2a7cc97)\
  2016-08-24 19:25:15 +0200
  * Shared memory fixes
* [Revision #fbf6fd1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fbf6fd1)\
  2016-08-21 20:35:13 +0200
  * Valgrind fixes: - fixed 2 unitialized memory errors - fixed leak in client test
* [Revision #b07a173](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b07a173)\
  2016-08-19 08:26:51 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #03d35ac](https://github.com/mariadb-corporation/mariadb-connector-c/commit/03d35ac)\
  2016-08-18 14:42:50 +0000
  * fix compile error
* [Revision #d76e0f1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d76e0f1)\
  2016-08-18 15:06:55 +0200
  * Fix compiler errors in headers (undefined uchar, attribute)
* [Revision #238f769](https://github.com/mariadb-corporation/mariadb-connector-c/commit/238f769)\
  2016-08-18 13:01:18 +0200
  * C/C integration, client library versioning
* [Revision #c374386](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c374386)\
  2016-08-19 08:24:47 +0200
  * Fix crash (introduced by CLIENT\_REMEMBER\_OPTIONS leak fix) see also [009643.html](https://lists.askmonty.org/pipermail/commits/2016-August/009643.html)
* [Revision #9207626](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9207626)\
  2016-08-18 12:24:32 +0200
  * 10.2-integration readded api functions - mysql\_debug (dummy) - mysql\_get\_parameters added low level api functions - mysql\_net\_field\_length - mysql\_net\_read
* [Revision #405bb92](https://github.com/mariadb-corporation/mariadb-connector-c/commit/405bb92)\
  2016-08-18 08:04:46 +0200
  * Fix for [CONC-198](https://jira.mariadb.org/browse/CONC-198): can't use two statements per connection If we have multiple open cursors we need to check the server\_status per statement (not per connection)
* [Revision #b68843a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b68843a)\
  2016-08-16 18:38:41 +0200
  * Merge from 2.3: Free options if CLIENT\_REMEMBER\_OPTIONS wasn't set
* [Revision #429b166](https://github.com/mariadb-corporation/mariadb-connector-c/commit/429b166)\
  2016-08-16 14:58:15 +0200
  * Move mariadb specific client flags and server capabilities to mysql->extension
* [Revision #b92b37c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b92b37c)\
  2016-08-16 14:56:39 +0200
  * manual merge from 2.2: if getaddrinfo returns EAI\_AGAIN we need to try again until connection timeout passed.
* [Revision #8f388ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8f388ad)\
  2016-08-15 20:52:15 +0200
  * Changed MYSQL\_BIND structure (so it will have the same size as in 2.3 and libmysql
* [Revision #2dc848e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2dc848e)\
  2016-08-12 19:24:03 +0000
  * C/C server integration - pass PLUGIN\_DIR and other config time variagbles from server build
* [Revision #1cefbbe](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1cefbbe)\
  2016-08-12 13:12:49 +0200
  * C/C integration
* [Revision #beea350](https://github.com/mariadb-corporation/mariadb-connector-c/commit/beea350)\
  2016-08-11 19:46:24 +0200
  * correctly identify multiconfig generator
* [Revision #be73859](https://github.com/mariadb-corporation/mariadb-connector-c/commit/be73859)\
  2016-08-11 16:34:57 +0000
  * server integration
* [Revision #6c0ae00](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6c0ae00)\
  2016-08-11 15:32:18 +0200
  * Fix for [CONC-197](https://jira.mariadb.org/browse/CONC-197): manual merge form 2.2.3 branch
* [Revision #2fcdff1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2fcdff1)\
  2016-08-10 13:37:40 +0200
  * 10.2-integration: Add embedded support for st\_mysql\_data structure.
* [Revision #8be7a3c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8be7a3c)\
  2016-08-09 16:26:13 +0200
  * manually merged from 2.2.3 - remove time measurement, total execution time will be shown after ctest execution
* [Revision #256dc4b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/256dc4b)\
  2016-08-09 14:15:37 +0200
  * Disable BIO methods for read/write by default
* [Revision #dd9ebcf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dd9ebcf)\
  2016-08-05 07:39:10 +0200
  *
    * Fixed license header - More OpenSSL 1.1 fixes
* [Revision #4f2c9da](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4f2c9da)\
  2016-08-03 12:41:52 +0200
  * Fix for [CONC-194](https://jira.mariadb.org/browse/CONC-194): (merged from connector\_c\_2.3)
* [Revision #7b14603](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7b14603)\
  2016-08-03 12:30:54 +0200
  * Fix for [CONC-196](https://jira.mariadb.org/browse/CONC-196): merged manually from connector\_c\_2.3 branch
* [Revision #69cc2c4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/69cc2c4)\
  2016-07-10 17:55:22 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #63d7014](https://github.com/mariadb-corporation/mariadb-connector-c/commit/63d7014)\
  2016-07-09 14:03:23 +0200
  * Moved c++ish declaration in the ma\_tls\_connect(libmariadb/secure/schannel.c) to other declarations on top of the function. It prevernted build at least with vs2010
* [Revision #6470533](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6470533)\
  2016-07-10 17:54:09 +0200
  * Replace SIZEOF\_CHARP by ma\_assert macro (windows fix)
* [Revision #a06574a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a06574a)\
  2016-07-09 20:21:44 +0000
  * Implement mysql\_stmt\_execute\_direct without COM\_MULTI. Network roundtrip is avoided, but no other optimization done in this commit. Like, possible to accumulate send 2 command packets in single send(), and it is trivial to do, but ommited here on reasons of clarity
* [Revision #f0601e0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f0601e0)\
  2016-07-09 10:53:09 +0200
  * Manual merge from 2.3 branch: put cmake helper scripts under new BSD license
* [Revision #e328467](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e328467)\
  2016-07-08 14:28:44 +0200
  * Fixed c++i style declarations in bulk test
* [Revision #0ab2af5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0ab2af5)\
  2016-07-08 14:09:32 +0200
  * Windows build fix: cast to char \* instead of using void\*
* [Revision #cb413ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cb413ad)\
  2016-07-08 14:03:48 +0200
  * Added bulk test
* [Revision #ecf26f7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ecf26f7)\
  2016-07-08 12:51:26 +0200
  * Added support for indicator variables Fixed windows compilation bug
* [Revision #ba0ed07](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ba0ed07)\
  2016-07-07 14:44:19 +0200
  * Implemented read/write bio functions, so we don't need sigpipe handler anymore.
* [Revision #da38af3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/da38af3)\
  2016-07-04 09:11:30 +0200
  * Fixes for OpenSSL 1.1.0
* [Revision #3754ccb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3754ccb)\
  2016-07-01 10:11:10 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #95101b9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/95101b9)\
  2016-06-29 18:02:17 +0000
  * Fix compilation error if MYSQL\_SERVER is defined
* [Revision #8e44202](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8e44202)\
  2016-07-01 10:10:11 +0200
  * Initial implementation for bulk operations/array binding in prepared statements
* [Revision #45a635d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/45a635d)\
  2016-06-29 15:22:01 +0200
  * Fixed compiler warnings removed latest test for ssl threads (test.c)
* [Revision #26d3192](https://github.com/mariadb-corporation/mariadb-connector-c/commit/26d3192)\
  2016-06-18 14:07:28 +0200
  * several fixes for mariadb\_stmt\_execute\_direct: - allow param binding via mysql\_stmt\_attr\_set: mysql\_stmt\_attr\_set(stmt, STMT\_ATTR\_PREBIND\_PARAMS, ¶m\_count); - If a prepared statement will be reexecuted, we send COM\_STMT\_CLOSE together with COM\_STMT\_PREPARE and COM\_STMT\_EXECUTE
* [Revision #31113af](https://github.com/mariadb-corporation/mariadb-connector-c/commit/31113af)\
  2016-06-06 12:14:48 +0200
  * Fixed possible buffer overrun for multi\_commands: update current position after reallocating buffer
* [Revision #4fd0ad4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4fd0ad4)\
  2016-06-04 09:00:20 +0200
  * Fix for [CONC-190](https://jira.mariadb.org/browse/CONC-190) (ported from 2.2 branch)
* [Revision #392dc4d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/392dc4d)\
  2016-06-03 10:58:52 +0200
  * Fix for [MDEV-10173](https://jira.mariadb.org/browse/MDEV-10173): Ignore decimals if the value exceeds the type specifc maximum of 6 digits
* [Revision #3192cd4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3192cd4)\
  2016-06-03 08:17:24 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #8ca494e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8ca494e)\
  2016-06-02 15:28:08 +0300
  * [CONC-181](https://jira.mariadb.org/browse/CONC-181) : Fix testing for truncation from double/float to integral types
* [Revision #ff5b86a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ff5b86a)\
  2016-06-03 08:16:38 +0200
  * Fixed maximum display length for MYSQL\_TYPE\_TIME
* [Revision #d5c5f9a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d5c5f9a)\
  2016-06-02 10:59:00 +0200
  * Fixed memory overrun in my\_strdup\_root
* [Revision #ac65121](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ac65121)\
  2016-06-01 20:23:57 +0200
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #7496789](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7496789)\
  2016-05-31 14:24:55 +0200
  * Fix openssl sigpipe correctly, move signal handler to openssl.c
* [Revision #7080d96](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7080d96)\
  2016-05-30 19:01:25 +0000
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #b825154](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b825154)\
  2016-05-30 19:01:13 +0000
  * fix compile error
* [Revision #3d83b9b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3d83b9b)\
  2016-06-01 20:21:03 +0200
  * Fix for repreparing statement: Don't send COM\_STMT\_RESET if we will send COM\_STMT\_CLOSE afterwards
* [Revision #b90b178](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b90b178)\
  2016-05-30 20:46:29 +0200
  * Another fix for [CONC-177](https://jira.mariadb.org/browse/CONC-177): ps-protocol with integer values and zerofill weren't correctly converted to strings
* [Revision #ec383d5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ec383d5)\
  2016-05-30 17:50:59 +0000
  * check mysql->extension for NULL before referencing it
* [Revision #f8aad3d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f8aad3d)\
  2016-05-25 19:31:25 +0200
  * Added missing export for mysql\_cancel api function
* [Revision #b54783f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b54783f)\
  2016-05-25 17:10:22 +0200
  * Fix for OpenSSL: Since OpenSSL doesn't use setsockopt/MSG\_NOSIGNAL we need to install a sigpipe handler (in case the application didn't install one already)
* [Revision #e62a4ea](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e62a4ea)\
  2016-05-25 09:52:22 +0000
  * Merge pull request #18 from GeorgyKirichenko/master
* [Revision #56505d8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/56505d8)\
  2016-04-27 17:54:07 +0300
  * Use PROJECT\_SOURCE\_DIR instead of CMAKE\_SOURCE\_DIR. Client library can be used as subdirectory in another cmake project.
* [Revision #0b49408](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0b49408)\
  2016-05-23 17:40:35 +0000
  * Fix warnings
* [Revision #437b9cd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/437b9cd)\
  2016-05-21 12:35:06 +0000
  * [CONC-184](https://jira.mariadb.org/browse/CONC-184) : provide a function to cancel a current connection (without invalidating MYSQL struct, without sending KILL) This apparently is useful for replication handling in the server
* [Revision #07877e6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/07877e6)\
  2016-05-15 15:41:45 +0200
  * Fix for [CONC-180](https://jira.mariadb.org/browse/CONC-180) In case handshake ended with Errorcode SEC\_E\_INTERNAL\_ERROR we check LastErrorCode (if it was set) and return system errormessage. For timeout during SSL handshake we return the following error message:
* [Revision #9d51d5e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9d51d5e)\
  2016-05-15 12:04:10 +0200
  * Fix for [CONC-179](https://jira.mariadb.org/browse/CONC-179): - Fixed offset for warning\_count in ps protocol - Added new api function mysql\_stmt\_warning\_count - For backwards compatibility we also update the value for mysql\_warning\_count function
* [Revision #ca68323](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ca68323)\
  2016-05-14 17:58:13 +0200
  * Fix for [CONC-177](https://jira.mariadb.org/browse/CONC-177): Fixed length calculation for zerofill conversion from float/double to string
* [Revision #3823a0f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3823a0f)\
  2016-05-14 14:13:33 +0200
  * Fix of unit test print output format.
* [Revision #ab42f58](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ab42f58)\
  2016-05-14 14:11:06 +0200
  * Test of mass batching (re [MDEV-9947](https://jira.mariadb.org/browse/MDEV-9947)).
* [Revision #80714f3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/80714f3)\
  2016-05-14 11:20:09 +0200
  * Fix multi com bug: Don't change current multi buffer position after reallcating multi buffer
* [Revision #c84de83](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c84de83)\
  2016-05-11 17:11:09 +0000
  * Start all SSL bugs with 'SSL connection error' for common messaging across TLS implementation, and to pass the openssl\_1 test cross-plattform
* [Revision #49527f7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/49527f7)\
  2016-05-11 12:41:57 +0000
  * Fix errors in openssl\_1 test suite. Provide mapping between openssl and schannel test suite ids. This mapping is currently incomplete
* [Revision #e1280ab](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e1280ab)\
  2016-05-09 16:47:37 +0200
  * Use case-insensitive comparision for character set names
* [Revision #6126e66](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6126e66)\
  2016-05-08 12:28:37 +0200
  * 10.2-integration: Added support for character set "auto": character set auto sets the character set to the corresponding locale or codepage (windows)
* [Revision #c70128b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c70128b)\
  2016-04-18 09:32:25 +0200
  * Fix for [CONC-173](https://jira.mariadb.org/browse/CONC-173): Fixed memory leak in mysql\_real\_connect fixed warning in pthread\_once
* [Revision #01f1854](https://github.com/mariadb-corporation/mariadb-connector-c/commit/01f1854)\
  2016-04-12 12:34:11 +0200
  * Fix for [CONC-167](https://jira.mariadb.org/browse/CONC-167): fix crash when fetching MYSQL\_TYPE\_BIT data. MYSQL\_TYPE\_BIT has no fixed packlength, so we need to check net\_field\_length instead
* [Revision #72a3142](https://github.com/mariadb-corporation/mariadb-connector-c/commit/72a3142)\
  2016-04-09 17:01:03 +0200
  * thread safe libray initialization
* [Revision #a57406c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a57406c)\
  2016-04-09 01:15:31 +0300
  * fix iconv search paths. define LIBICONV\_PLUG to workaround GNU iconv.h redefinition of libiconv exports
* [Revision #6190f60](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6190f60)\
  2016-04-05 19:39:42 +0000
  * Fix schannel problems that popup on Win2012 R2 buildbot - Do not acquire a named context, because this might run into permissions problem. - Avoid sending TLS1.2 version by default. Yassl wrongfully rejects it with a bad handshake (it should consider that 1.1 and 1.0 are supported too but it does not)
* [Revision #ec878da](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ec878da)\
  2016-04-05 16:08:36 +0000
  * Fix duplicate CertFreeCertificateContext() in case ma\_schannel\_load\_private\_key() fails
* [Revision #b4efe73](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b4efe73)\
  2016-03-31 08:41:12 +0200
  * session tracking implementation (10.2-integration): - At the moment the following session tracking types are supported: SESSION\_TRACK\_SCHEMA SESSION\_TRACK\_SYSTEM\_VARIABLES SESSION\_TRACK\_STATE\_CHANGE SESSION\_TRACK\_TRANSACTION\_CHARACTERISTICS - New API functions mysql\_session\_track\_get\_next mysql\_session\_track\_get\_first
* [Revision #21be8f4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/21be8f4)\
  2016-03-29 09:44:03 +0200
  * Moved connection\_handler to mysql->extension
* [Revision #bea035a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bea035a)\
  2016-03-28 10:29:55 +0200
  *
    * Unittests: link static library instead of dynamic - TLS/SSL: renamed HAVE\_SSL to HAVE\_TLS to avoid trouble in 10.2-integration - Fixed wrong timeout in non-blocking mode - Fixed valgrind error in prepared statement
* [Revision #2004962](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2004962)\
  2016-03-24 18:10:06 +0100
  * Fix for [CONC-170](https://jira.mariadb.org/browse/CONC-170): missing blank in mariadb\_config --libs output
* [Revision #4c0af43](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4c0af43)\
  2016-03-24 07:29:04 +0100
  * Fix for [CONC-169](https://jira.mariadb.org/browse/CONC-169): Memory corruption in mariadb\_dyncol\_unpack
* [Revision #b6d3af1](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b6d3af1)\
  2016-03-24 07:12:54 +0100
  * Fix for [CONC-168](https://jira.mariadb.org/browse/CONC-168): string conversion of timestamps is broken When converting datetime with microseconds to string (binary protocol) number of decimal places was ignored. Thanks to Patrick Huesmann for providing a fix.
* [Revision #68caac8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/68caac8)\
  2016-03-17 17:46:58 +0100
  * fix install broken by last commits
* [Revision #ab393c9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ab393c9)\
  2016-03-16 18:30:28 +0100
  * Added tls\_version support for schannel. tls\_version has to be specified via mysql\_options(mysql, MARIADB\_OPT\_TLS\_VERSION, ...)
* [Revision #d78cba3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d78cba3)\
  2016-03-16 18:21:09 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #6669f22](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6669f22)\
  2016-03-15 20:12:47 +0100
  * fix link error on solaris x64
* [Revision #8bf85da](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8bf85da)\
  2016-03-15 18:52:29 +0100
  * Fix build errors on Solaris 10 with gcc 3.4.3
* [Revision #4b1e94b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4b1e94b)\
  2016-03-16 18:20:08 +0100
  * Since we use TLS and not SSL functions and structures were renamed from SSL to TLS
* [Revision #f68b89b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f68b89b)\
  2016-03-15 09:01:02 +0100
  *
    * Back off CMake version requirements. - Fix plugin extension on OSX (it is .so, not .dylib) - add SKIP\_TESTS to skip compiling test
* [Revision #91ad315](https://github.com/mariadb-corporation/mariadb-connector-c/commit/91ad315)\
  2016-03-14 17:13:10 +0100
  * Make sure that on windows we include iconv.h from win-iconv, not a system one
* [Revision #bb365dd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bb365dd)\
  2016-03-14 12:11:36 +0100
  * SSL fixes: - wrong incude directory for OpenSSL - added errormessage for SEC\_E\_ILLEGAL\_MESSAGE
* [Revision #5eaeb24](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5eaeb24)\
  2016-03-12 09:52:40 +0100
  * Fixed timeout when using named\_pipe: - if timeout is 0, we need to specifiy INFINITE (overlapped) - don't set read/write timeout before connection was established successfully
* [Revision #ad65d69](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ad65d69)\
  2016-03-11 10:48:19 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #61e2dc2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/61e2dc2)\
  2016-03-11 08:02:19 +0100
  * Windows build fixes for 10.2-integration Removed unused functions from ma\_dtoa.c
* [Revision #4e31be7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4e31be7)\
  2016-03-11 10:28:59 +0100
  * Fixed possible buffer overrun in authentication
* [Revision #2f67911](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2f67911)\
  2016-03-11 07:08:34 +0100
  * changed plugin library types from SHARED to MODULE Fixed float/double/decimal converion for prepared statements: since \_gcvt (Windows) and gcvt (\*nix) deliver different results we use now dtoa.c from server package, which is licensed under LGPL.
* [Revision #826da74](https://github.com/mariadb-corporation/mariadb-connector-c/commit/826da74)\
  2016-03-10 15:18:00 +0100
  * 10.2-integration: add definition of MYSQL\_CLIENT
* [Revision #06e5422](https://github.com/mariadb-corporation/mariadb-connector-c/commit/06e5422)\
  2016-03-10 14:02:30 +0100
  * 10.2-integration fixes: - always send COM\_STMT\_RESET if specified - prevent double free of context buffer
* [Revision #3cfc5f8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3cfc5f8)\
  2016-03-10 09:51:53 +0100
  * Removed option WITH\_NONBLOCK
* [Revision #454a957](https://github.com/mariadb-corporation/mariadb-connector-c/commit/454a957)\
  2016-03-09 18:27:48 +0100
  * Fix error message (hostname max. 100 characters)
* [Revision #cc0c345](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cc0c345)\
  2016-03-08 17:08:01 +0100
  *
    * Fixes for 10.2-integration - As requested by Wlad we use connect timeout for read/write unless the connection was established. - Added experimental session cache support for OpenSSL. It's currently disabled
* [Revision #05eeef7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/05eeef7)\
  2016-03-02 17:30:44 +0100
  * Fix for windows build (hide ma\_send function by #ifndef \_WIN32)
* [Revision #0a187a0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0a187a0)\
  2016-03-02 16:43:39 +0100
  * Build remote\_io as dynamic plugin to avoid build problems on several machines with broken OpenSSL installation
* [Revision #ea0f2e6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ea0f2e6)\
  2016-03-02 16:23:27 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c)
* [Revision #33ebe89](https://github.com/mariadb-corporation/mariadb-connector-c/commit/33ebe89)\
  2016-03-02 15:33:30 +0200
  * Fix build on OSX
* [Revision #89c33d8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/89c33d8)\
  2016-03-01 19:37:34 +0100
  * Fixed crash introduced by last fix from Wlad: getsockopt expects integer ptr as last parameter
* [Revision #e157d4f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e157d4f)\
  2016-03-02 16:22:34 +0100
  * Fix for Solaris builds
* [Revision #32eff12](https://github.com/mariadb-corporation/mariadb-connector-c/commit/32eff12)\
  2016-03-01 18:36:18 +0100
  * Patch by Wlad: check exceptfds after select() call on windows platforms
* [Revision #c67bb51](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c67bb51)\
  2016-03-01 15:27:22 +0100
  * Fix openssl detection and compile errors for old openssl versions
* [Revision #5431247](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5431247)\
  2016-03-01 14:13:19 +0100
  * FindOpenSSL module from older cmake packages doesn't set OPENSSL\_VERSION\_MAJOR so we will set this variable after FindOpenSSL.
* [Revision #89fce62](https://github.com/mariadb-corporation/mariadb-connector-c/commit/89fce62)\
  2016-03-01 13:54:33 +0100
  * Build fixes for 10.2 integration
* [Revision #c433c30](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c433c30)\
  2016-03-01 13:37:55 +0100
  * Added session ticket support for OpenSSL (experimental) Build fixes: - Build requires OpenSSL v. 1.0.1 or higher - Fixed win64 build (missing target properties for static lib)
* [Revision #1eb4416](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1eb4416)\
  2016-02-29 20:19:58 +0100
  * include stdarg.h (for va\_list)
* [Revision #ee004a8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ee004a8)\
  2016-02-29 15:47:50 +0100
  * GnuTLS fix: we need to check server certificate if no ca was specified but verify\_server flag was set
* [Revision #7a27c4c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7a27c4c)\
  2016-02-29 15:38:37 +0100
  * Build fix for MacOSX
* [Revision #ab70a87](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ab70a87)\
  2016-02-29 14:56:00 +0100
  * Fix my\_atoll for older Visual C++ compilers
* [Revision #3401cca](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3401cca)\
  2016-02-25 20:44:06 +0100
  * fix build for c89 compilers
* [Revision #ca72014](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ca72014)\
  2016-02-25 18:45:09 +0100
  * fix variable declaration in the middle of function - error on pre-C99 compilers
* [Revision #b1e2101](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b1e2101)\
  2016-02-25 18:38:57 +0100
  * Use IF(POLICY CMP00XX), to prevent errors for old cmake due to unknown policy
* [Revision #2f6cc35](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2f6cc35)\
  2016-02-24 10:41:17 +0100
  * Disable TLSv\_1.2 in schannel for now, we need a separate option for, since we will not be able to talk to servers built with yassl
* [Revision #a1a178e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a1a178e)\
  2016-02-24 08:37:04 +0100
  * Fixed missing export symbol for windows build
* [Revision #f7d7730](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f7d7730)\
  2016-02-24 08:26:34 +0100
  * renamed exported function mysql\_reconnect to mariadb\_reconnect
* [Revision #d316a29](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d316a29)\
  2016-02-24 07:52:04 +0100
  * Since Windows doesn't use ma\_config.h, we need to move MARIADB\_PLUGINDIR definition to mariadb\_version.h
* [Revision #8620b75](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8620b75)\
  2016-02-23 13:50:14 +0100
  * Added missing error messages for wrong protocol moved connection handler into net->extension (ABI break)
* [Revision #38b7870](https://github.com/mariadb-corporation/mariadb-connector-c/commit/38b7870)\
  2016-02-23 13:25:03 +0100
  * Fix for read/write timeout for sockets on non Windows platforms
* [Revision #d68b48f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d68b48f)\
  2016-02-22 10:43:11 +0100
  * 10.2 integration fixes - changed plugin API to avoid crashes: Oracle/MariaDB changed structure several times without updating interface version. - ABI fixes: moved additional net items to net->extension (connection handler and com\_multi buffer)
* [Revision #dc1a871](https://github.com/mariadb-corporation/mariadb-connector-c/commit/dc1a871)\
  2016-02-21 17:44:29 +0100
  * [CONC-161](https://jira.mariadb.org/browse/CONC-161): Increase username length to 128
* [Revision #9818a85](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9818a85)\
  2016-02-20 11:52:17 +0100
  * Fix for [CONC-160](https://jira.mariadb.org/browse/CONC-160): field metadata doesn't show NUM\_FLAG for NEWDECIMAL columns
* [Revision #27a66aa](https://github.com/mariadb-corporation/mariadb-connector-c/commit/27a66aa)\
  2016-02-20 11:55:58 +0100
  * 10.2 fixes old pathword plugin is now static by default prefixed PLUGINDIR (now MARIADB\_PLUGINDIR)
* [Revision #c014b9f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c014b9f)\
  2016-02-19 22:23:00 +0100
  * 10.2 integration fixes: - renamed/prefixed password functions - prepared statement fixes for mysql\_client\_test
* [Revision #56f9809](https://github.com/mariadb-corporation/mariadb-connector-c/commit/56f9809)\
  2016-02-18 14:03:17 +0100
  * 10.2-fixes: export asynchronous version of mysql\_list\_fields don't convert days to hours when fetch date in bind with type MYSQL\_TYPE\_TIME
* [Revision #542a6f7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/542a6f7)\
  2016-02-18 11:24:07 +0100
  * 10.2-integration: Avoid redefinition of plugin structure (mysql\_client\_test)
* [Revision #409d673](https://github.com/mariadb-corporation/mariadb-connector-c/commit/409d673)\
  2016-02-18 10:45:26 +0100
  * 10.2 - integration fixes - enable data truncation reporting for ps by default - added plugin protoype definitions to mysql.h10.2 - integration fixes
* [Revision #d303cf7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d303cf7)\
  2016-02-17 10:00:53 +0100
  * More 10.2-integ fixes: - renamed my\_net functions (ma\_net) - fixed wrong types in ma\_schannel.c - fixed wrong parameter in client\_plugin when building load string
* [Revision #7287229](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7287229)\
  2016-02-17 07:59:23 +0100
  * Windows build fixes
* [Revision #28edd6d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/28edd6d)\
  2016-02-17 07:42:11 +0100
  * 10.2-integration renamed duplicate symbols in mariadb\_version.h
* [Revision #85525c2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/85525c2)\
  2016-02-16 17:40:03 +0100
  * Merge remote-tracking branch 'origin/3.1'
* [Revision #c60923b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c60923b)\
  2016-02-09 10:24:53 +0100
  * Added option WITH\_MSI for building MSI package
* [Revision #1cf84e7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1cf84e7)\
  2016-02-09 10:02:21 +0100
  * Windows packaging fixes for includes and plugins
* [Revision #5c19385](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5c19385)\
  2016-02-09 09:02:36 +0100
  * Always provide prototypes for non blocking functions in mysql.h
* [Revision #74ce606](https://github.com/mariadb-corporation/mariadb-connector-c/commit/74ce606)\
  2016-02-09 08:43:16 +0100
  * Fix for CONC155: return trailing zero when fetching from binary columns into string
* [Revision #62e69c8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/62e69c8)\
  2016-02-08 19:19:33 +0100
  * Prevent multiple inclusion of mariadb\_version.h in client tools
* [Revision #61daa7a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/61daa7a)\
  2016-02-08 19:00:54 +0100
  * fixed installation of include files
* [Revision #1d0402a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/1d0402a)\
  2016-02-08 18:47:44 +0100
  * Added ma\_pthread.h
* [Revision #4ca933b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4ca933b)\
  2016-02-08 18:43:02 +0100
  * Global cleanup: removed global locks removed dead code and files removed dbug
* [Revision #f3577ba](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f3577ba)\
  2016-02-05 16:31:49 +0100
  * Disable dbug by default (to enable it specify cmake option -DWITH\_DBUG=ON) minor fixes for 10.2 integration (windows)
* [Revision #0c3c789](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0c3c789)\
  2016-02-05 12:19:45 +0100
  * More 10.2 windows fixes
* [Revision #f0b1561](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f0b1561)\
  2016-02-05 09:54:22 +0100
  * More windows fixes for 10.2 integration
* [Revision #26b56d9](https://github.com/mariadb-corporation/mariadb-connector-c/commit/26b56d9)\
  2016-02-05 07:52:24 +0100
  * Windows fixes for 10.2 integration
* [Revision #bd3c6dd](https://github.com/mariadb-corporation/mariadb-connector-c/commit/bd3c6dd)\
  2016-02-05 06:53:56 +0100
  * Fixed memory leak in mysql\_real\_connect Prefixed more functions (fn\_format, strlength)
* [Revision #485af02](https://github.com/mariadb-corporation/mariadb-connector-c/commit/485af02)\
  2016-02-04 20:30:17 +0100
  * More fixes for 10.2 integration
* [Revision #3c03d3b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3c03d3b)\
  2016-02-04 16:53:51 +0100
  * Added prototypes for mysql\_dump\_debug\_info\_cont/start to mysql.h
* [Revision #8801567](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8801567)\
  2016-02-04 14:22:27 +0100
  * removed my\_vsnprintf removed llstr.c renamed int2string function with prefix ma\_
* [Revision #5cd3d2d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5cd3d2d)\
  2016-02-04 13:43:48 +0100
  * moved ma\_error to errmsg.c and removed my\_error.c
* [Revision #ad58fa7](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ad58fa7)\
  2016-02-04 13:11:44 +0100
  * More cleanup for 10.2 integration
* [Revision #79d0b29](https://github.com/mariadb-corporation/mariadb-connector-c/commit/79d0b29)\
  2016-02-03 11:53:39 +0100
  * More 10.2 fixes for integration
* [Revision #9e4bd29](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9e4bd29)\
  2016-02-03 09:14:01 +0100
  * More fixes and renames for 10.2 integration
* [Revision #3c8889d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3c8889d)\
  2016-02-02 20:10:29 +0100
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 3.1
* [Revision #ecf92d3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ecf92d3)\
  2016-02-02 17:10:56 +0100
  * removed obsolete have\_tcpip stuff
* [Revision #ab67ef2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ab67ef2)\
  2016-02-02 14:08:20 +0100
  * fix compilation with gcc 4.8
* [Revision #e138995](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e138995)\
  2016-02-02 20:09:42 +0100
  * more fixes for 10.2 integration
* [Revision #4ecc4c0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/4ecc4c0)\
  2016-02-02 12:43:03 +0100
  * Merge branch '3.1' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 3.1
* [Revision #e794883](https://github.com/mariadb-corporation/mariadb-connector-c/commit/e794883)\
  2016-02-02 12:38:06 +0100
  * fix export symbols
* [Revision #49a0a89](https://github.com/mariadb-corporation/mariadb-connector-c/commit/49a0a89)\
  2016-02-02 12:41:53 +0100
  *
    1. added missing export function mariadb\_load\_defaults 2) added option WITH\_UNITEST=ON/OFF to disable build of unittests
* [Revision #c5ca735](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c5ca735)\
  2016-02-02 12:12:04 +0100
  * Renamed prefixes for 10.2 integration
* [Revision #ccb8798](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ccb8798)\
  2016-02-02 10:11:15 +0100
  * Added mysql\_options4 (was #define before)
* [Revision #a442a5f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a442a5f)\
  2016-02-02 10:06:38 +0100
  * Merge branch 'master' of [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 3.1
* [Revision #a7e31ad](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a7e31ad)\
  2016-01-28 19:55:43 +0100
  * Do not set CMAKE\_INSTALL\_PREFIX to empty string on Windows
* [Revision #8845fcb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8845fcb)\
  2016-01-28 16:58:30 +0100
  * First implementation of mariadb\_stmt\_execute\_direct
* [Revision #25e610c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/25e610c)\
  2016-01-27 18:19:35 +0100
  * Removed deprecated API functions: - mysql\_close - mysql\_create\_db - mysql\_drop\_db - mysql\_get\_parameters Fixed build error when SSL is disabled max\_allowed\_packet and net\_buffer size needs to be retrieved via mysql\_get\_option now (instead of mariadb\_get\_info)
* [Revision #b00a0e2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b00a0e2)\
  2016-01-27 06:45:49 +0100
  * Merge [mariadb-connector-c](https://github.com/MariaDB/mariadb-connector-c) into 10.2-georg
* [Revision #6236637](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6236637)\
  2016-01-13 19:37:46 +0100
  * [MDEV-9058](https://jira.mariadb.org/browse/MDEV-9058) post-review fix
* [Revision #0c7fabc](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0c7fabc)\
  2016-01-08 13:08:47 +0100
  * More control over results in the unittest.
* [Revision #0518bd6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/0518bd6)\
  2016-01-05 20:41:37 +0100
  * Very simple test of COM\_MULTI
* [Revision #b6e1e36](https://github.com/mariadb-corporation/mariadb-connector-c/commit/b6e1e36)\
  2016-01-05 16:48:37 +0100
  * Georg's changes to make mariadb\_flush\_multi\_command working (reading result of multi-command).
* [Revision #45729a2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/45729a2)\
  2016-01-05 16:46:45 +0100
  * Fix building.
* [Revision #a3bb1d2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a3bb1d2)\
  2015-12-29 21:06:23 +0100
  * merge from 3.0.0 fixes
* [Revision #c8648cf](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c8648cf)\
  2015-12-17 19:21:52 +0100
  * Initial implementation for COM\_MULTI
* [Revision #955bb8d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/955bb8d)\
  2015-11-20 19:20:22 +0100
  * 10.2 protocol fixes: exclude trailing 0 when checking for RPL\_HACK in version number. Shift extended client flags up instead of down
* [Revision #5fca341](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5fca341)\
  2015-11-20 18:34:35 +0100
  * Initial implementation for [MDEV-9117](https://jira.mariadb.org/browse/MDEV-9117): 10.2 protocol changes - exchanging mariadb specific client/server capabilities during handshake
* [Revision #509b948](https://github.com/mariadb-corporation/mariadb-connector-c/commit/509b948)\
  2016-02-16 13:04:16 +0100
  * SSL fixes: - added MARIADB\_OPT\_SSL\_CIPHER\_STRENGTH (value uint) for Schannel - fixed mutes in all ssl variants
* [Revision #448b680](https://github.com/mariadb-corporation/mariadb-connector-c/commit/448b680)\
  2016-02-09 08:43:16 +0100
  * Fix for CONC155: return trailing zero when fetching from binary columns into string
* [Revision #a56d193](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a56d193)\
  2016-02-04 16:53:51 +0100
  * Added prototypes for mysql\_dump\_debug\_info\_cont/start to mysql.h
* [Revision #3baf4a0](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3baf4a0)\
  2016-01-28 19:55:43 +0100
  * Do not set CMAKE\_INSTALL\_PREFIX to empty string on Windows
* [Revision #2cc5728](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2cc5728)\
  2016-01-28 16:53:26 +0100
  * removed mysql\_get\_parameters from export list disable creation of certificates if SSL is disabled or OpenSSL is not available
* [Revision #29163e8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/29163e8)\
  2016-01-27 18:19:35 +0100
  * Removed deprecated API functions: - mysql\_close - mysql\_create\_db - mysql\_drop\_db - mysql\_get\_parameters Fixed build error when SSL is disabled max\_allowed\_packet and net\_buffer size needs to be retrieved via mysql\_get\_option now (instead of mariadb\_get\_info)
* [Revision #6bed75b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6bed75b)\
  2016-01-25 13:51:52 +0100
  * Bumped version number to 3.0.1
* [Revision #6b5ff86](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6b5ff86)\
  2016-01-25 13:40:07 +0100
  * Fixed SSL test (option was renamed before)
* [Revision #736913d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/736913d)\
  2016-01-25 13:35:15 +0100
  * Fix for [CONC-154](https://jira.mariadb.org/browse/CONC-154): set stmt->state to MYSQL\_STMT\_FETCH\_DONE if - result set is empty (nothing to fetch) - when madb\_stmt\_reset was called
* [Revision #56b4bde](https://github.com/mariadb-corporation/mariadb-connector-c/commit/56b4bde)\
  2016-01-25 13:37:14 +0100
  * Renamed option for mysql\_get\_infov from MARIADB\_CONNECTION\_SSL\_LIBRARY to MARIADB\_SSL\_LIBRARY
* [Revision #17ab9f8](https://github.com/mariadb-corporation/mariadb-connector-c/commit/17ab9f8)\
  2016-01-23 15:57:33 +0100
  * Added missing FindGSSAPI.cmake for non windows builds
* [Revision #cbef19f](https://github.com/mariadb-corporation/mariadb-connector-c/commit/cbef19f)\
  2016-01-22 20:14:55 +0100
  * Windows fixes for GSSAPI plugin
* [Revision #f0215ab](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f0215ab)\
  2016-01-22 20:00:40 +0100
  * Added GSSAPI authentication plugin
* [Revision #8b3099b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8b3099b)\
  2016-01-18 13:22:34 +0100
  * Fix unsresolved external for remoteio plugin (windows)
* [Revision #9a5904a](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9a5904a)\
  2016-01-18 11:32:41 +0100
  * Don't build remote io on Windows as "static", since curl libraries are not installed by default on Windows
* [Revision #7c7fae2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7c7fae2)\
  2016-01-18 10:42:12 +0100
  * Added include path for connection plugins
* [Revision #fdaa90e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/fdaa90e)\
  2016-01-18 10:34:45 +0100
  * Wix installer fixes Added lib and lib/plugin to PATH
