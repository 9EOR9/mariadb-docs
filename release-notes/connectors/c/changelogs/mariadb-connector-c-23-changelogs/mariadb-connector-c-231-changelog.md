# MariaDB Connector/C 2.3.1 Changelog

[Download](https://downloads.mariadb.org/connector-c/2.3.1)[Release Notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-231-release-notes.md)[Changelog](mariadb-connector-c-231-changelog.md)[About MariaDB Connector/C](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-c/README.md)

**Release date:** 4 Aug 2016

For the highlights of this release, see the [release notes](../../mariadb-connector-c-23-release-notes/mariadb-connector-c-231-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/mariadb-connector-c/) you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #c531a87](https://github.com/mariadb-corporation/mariadb-connector-c/commit/c531a87)\
  2016-08-03 17:39:12 +0200
  * Don't use SHA256 in code signing since we still need to support Vista (until 2017)
* [Revision #697a0d2](https://github.com/mariadb-corporation/mariadb-connector-c/commit/697a0d2)\
  2016-08-03 16:12:16 +0200
  * Set sign options for new windows build box
* [Revision #d5762da](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d5762da)\
  2016-08-03 14:09:29 +0200
  * Don't export mariadb\_deinitialize\_ssl if package has no openssl support
* [Revision #6382c08](https://github.com/mariadb-corporation/mariadb-connector-c/commit/6382c08)\
  2016-08-03 13:47:11 +0200
  * removed timer from performance - ctest already tells us execution time
* [Revision #66ab41e](https://github.com/mariadb-corporation/mariadb-connector-c/commit/66ab41e)\
  2016-08-03 13:22:20 +0200
  * Fixes OpenSSL version checking
* [Revision #9dc2a48](https://github.com/mariadb-corporation/mariadb-connector-c/commit/9dc2a48)\
  2016-08-03 12:57:33 +0200
  * Removed ma\_assert stuff
* [Revision #d3b8289](https://github.com/mariadb-corporation/mariadb-connector-c/commit/d3b8289)\
  2016-08-03 12:37:29 +0200
  * Fix for [CONC-194](https://jira.mariadb.org/browse/CONC-194): mysql\_stmt\_fetch\_column ignores offset when retrieving binary/blob data
* [Revision #ac60780](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ac60780)\
  2016-08-03 12:03:20 +0200
  * Fix for [CONC-196](https://jira.mariadb.org/browse/CONC-196): Avoid unnecessary extra loops in alloc\_root() function.\
    Added performance test which requires employees database.
* [Revision #ba1308b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/ba1308b)\
  2016-08-01 14:37:52 +0200
  * Revert "Fix for [CONC-194](https://jira.mariadb.org/browse/CONC-194): mysql\_stmt\_fetch\_column does not respect 'offset' parameter for blob fields"
* [Revision #36b6178](https://github.com/mariadb-corporation/mariadb-connector-c/commit/36b6178)\
  2016-08-01 14:22:43 +0200
  * Fix for [CONC-194](https://jira.mariadb.org/browse/CONC-194): mysql\_stmt\_fetch\_column does not respect 'offset' parameter for blob fields
* [Revision #2b02a10](https://github.com/mariadb-corporation/mariadb-connector-c/commit/2b02a10)\
  2016-07-10 13:33:25 +0200
  * replaced #if sizeof by ma\_assert macro since sizeof is not supported by all kind of preprocessors
* [Revision #3d5cb4b](https://github.com/mariadb-corporation/mariadb-connector-c/commit/3d5cb4b)\
  2016-07-03 09:44:36 +0200
  * Bumped minor version number. Version is now 2.3.1
  * Added support for OpenSSL 1.1.0
  * Fixed ssl test: We don't check for a specific cipher unless we have\
    specified a specific cipher. Depending on server configuration and TLS\
    library in use (yassl/openssl) default ciphers might change.

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
