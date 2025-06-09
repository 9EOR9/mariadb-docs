# MariaDB 5.2.12 Changelog

[Download](https://downloads.askmonty.org/mariadb/5.2.12) |[Release Notes](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-2-series/mariadb-5212-release-notes.md) |**Changelog** |[Overview of 5.2](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-2-series/changes-improvements-in-mariadb-5-2.md)

**Release date:** 6 Apr 2012

For the highlights of this release, see the[release notes](../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-2-series/mariadb-5212-release-notes.md).

The revision number links will take you to the revision's page on Launchpad. On\
Launchpad you can view more details of the revision and view diffs of the code\
modified in that revision.

* [Revision #3134](https://bazaar.launchpad.net/~maria-captains/maria/5.2/revision/3134) \[merge]\
  Thu 2012-04-05 12:01:52 +0200
  * merge
  * [Revision #2643.137.3](https://bazaar.launchpad.net/~maria-captains/maria/5.2/revision/2643.137.3) \[merge]\
    Thu 2012-04-05 10:49:38 +0200
    * mysql-5.1.62 merge
  * [Revision #2643.137.2](https://bazaar.launchpad.net/~maria-captains/maria/5.2/revision/2643.137.2)\
    Wed 2012-04-04 15:41:50 +0200
    * [MDEV-212](https://jira.mariadb.org/browse/MDEV-212) sporadic main.connect failures in 5.3
    * don't cast implicitly an int to a char, when a boolean value is desired.
* [Revision #3133](https://bazaar.launchpad.net/~maria-captains/maria/5.2/revision/3133) \[merge]\
  Wed 2012-04-04 13:50:24 +0300
  * Merge with 5.1
  * [Revision #2643.137.1](https://bazaar.launchpad.net/~maria-captains/maria/5.2/revision/2643.137.1) \[merge]\
    Wed 2012-04-04 13:38:19 +0300
    * Merge in deleted fixes
    * [Revision #2643.136.2](https://bazaar.launchpad.net/~maria-captains/maria/5.2/revision/2643.136.2)\
      Wed 2012-04-04 13:20:06 +0300
      * Fixed test cases that changed as part of fixing bugs with record count and partitioning
* [Revision #3132](https://bazaar.launchpad.net/~maria-captains/maria/5.2/revision/3132) \[merge]\
  Wed 2012-04-04 00:33:02 +0300
  * Merge with 5.1
  * [Revision #2643.136.1](https://bazaar.launchpad.net/~maria-captains/maria/5.2/revision/2643.136.1)\
    Wed 2012-04-04 00:14:07 +0300
  * Fixed [Bug #970528](https://bugs.launchpad.net/bugs/970528) "Server crashes in my\_strnncollsp\_simple on LEFT JOIN with CSV table, TEXT field"
  * The main problem was a bug in CSV where it provided wrong statistics (it claimed the table was empty when it wasn't)
  * I also fixed wrong freeing of blob's in the CSV handler. (Any call to handler::read\_first\_row() on a CSV table with blobs would fail)
* [Revision #3131](https://bazaar.launchpad.net/~maria-captains/maria/5.2/revision/3131)\
  Mon 2012-04-02 11:29:28 +0200
  * [MDEV-209](https://jira.mariadb.org/browse/MDEV-209) SET PASSWORD in 5.2 does not update user's auth plugin
