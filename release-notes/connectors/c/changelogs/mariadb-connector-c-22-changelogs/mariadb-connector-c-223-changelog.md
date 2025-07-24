# Connector/C 2.2.3 Changelog

The most recent [_**Stable**_](../../../../community-server/about/release-criteria.md) _**(GA)**_ release of MariaDB Connector/C is:[**MariaDB Connector/C 3.4.5**](../../mariadb-connector-c-3-4-release-notes/mariadb-connector-c-3-4-5-release-notes.md)

[Download](https://downloads.mariadb.org/connector-c/2.2.3)[Release Notes](../../mariadb-connector-c-22-release-notes/mariadb-connector-c-223-release-notes.md)[Changelog](mariadb-connector-c-223-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 26 Apr 2016

For the highlights of this release, see the [release notes](../../mariadb-connector-c-22-release-notes/mariadb-connector-c-223-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #5b7facb](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5b7facb)\
  2016-04-12 12:34:11 +0200
  * Fix for [CONC-167](https://jira.mariadb.org/browse/CONC-167): fix crash when fetching MYSQL\_TYPE\_BIT data. MYSQL\_TYPE\_BIT has no fixed packlength, so we need to check net\_field\_length instead
* [Revision #8026708](https://github.com/mariadb-corporation/mariadb-connector-c/commit/8026708)\
  2016-03-24 07:29:04 +0100
  * Fix for [CONC-169](https://jira.mariadb.org/browse/CONC-169): Memory corruption in mariadb\_dyncol\_unpack
* [Revision #7bda455](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7bda455)\
  2016-03-24 07:12:54 +0100
  * Fix for [CONC-168](https://jira.mariadb.org/browse/CONC-168): string conversion of timestamps is broken When converting datetime with microseconds to string (binary protocol) number of decimal places was ignored. Thanks to Patrick Huesmann for providing a fix.
* [Revision #7fd72df](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7fd72df)\
  2016-03-14 17:13:10 +0100
  * Make sure that on windows we include iconv.h from win-iconv, not a system one
* [Revision #7bfe860](https://github.com/mariadb-corporation/mariadb-connector-c/commit/7bfe860)\
  2016-03-14 14:37:27 +0100
  * OpenSSL fix: remove warnings when using OPENSSL\_NO\_DEPRECATED versions
* [Revision #33589a3](https://github.com/mariadb-corporation/mariadb-connector-c/commit/33589a3)\
  2016-03-01 13:27:51 +0100
  * Fixed timeouts (since asynchronous we store them in milliseconds internally)
* [Revision #ee10b55](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ee10b55)\
  2016-02-23 13:22:45 +0100
  * Fix for [CONC-163](https://jira.mariadb.org/browse/CONC-163): mysql->info returns garbage if no row was updated.
* [Revision #d4241c4](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d4241c4)\
  2016-02-21 17:44:29 +0100
  * [CONC-161](https://jira.mariadb.org/browse/CONC-161): Increase username length to 128
* [Revision #52e07f5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/52e07f5)\
  2016-02-20 11:52:17 +0100
  * Fix for [CONC-160](https://jira.mariadb.org/browse/CONC-160): field metadata doesn't show NUM\_FLAG for NEWDECIMAL columns
* [Revision #f1cde3d](https://github.com/mariadb-corporation/mariadb-connector-c/commit/f1cde3d)\
  2016-02-11 09:27:41 +0100\
  \*
  * Fix for [CONC-156](https://jira.mariadb.org/browse/CONC-156): CONC 2.2.2 build fails on FreeBSD due to not including necessary header. Thanks to Andie H. Hwang for providing this patch!
* [Revision #804129c](https://github.com/mariadb-corporation/mariadb-connector-c/commit/804129c)\
  2016-02-09 08:43:16 +0100
  * Fix for CONC155: return trailing zero when fetching from binary columns into string
* [Revision #6a70af5](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6a70af5)\
  2016-01-28 23:06:49 +0100
  * mysql\_options expected pointer to uint, while it has to be my\_bool\* according to specs. Also adding some VS specific service files/dirs templates to .gitignore
* [Revision #5dfcac6](https://github.com/mariadb-corporation/mariadb-connector-c/commit/5dfcac6)\
  2016-01-28 19:55:43 +0100
  * Do not set CMAKE\_INSTALL\_PREFIX to empty string on Windows
* [Revision #710e2b2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/710e2b2)\
  2016-01-25 13:53:06 +0100
  * bumped version number to 2.2.3
* [Revision #a89d465](https://github.com/mariadb-corporation/mariadb-connector-c/commit/a89d465)\
  2016-01-25 13:35:15 +0100
  * Fix for [CONC-154](https://jira.mariadb.org/browse/CONC-154): set stmt->state to MYSQL\_STMT\_FETCH\_DONE if - result set is empty (nothing to fetch) - when madb\_stmt\_reset was called
* [Revision #3ff4b75](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3ff4b75)\
  2015-12-10 06:48:26 +0100
  * Add prefix for source packages when building source package directly from git.

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
