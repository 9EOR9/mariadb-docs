---
hidden: true
---

# MariaDB 12.0.2 Changelog

<!--
<a href="https://mariadb.com/downloads" class="button primary">Download</a> <a href="../../release-notes-mariadb-12.0-rolling-releases/mariadb-12.0.2-release-notes.md" class="button secondary">Release Notes</a> <a href="mariadb-12.0.2-changelog.md" class="button secondary">Changelog</a> <a href="../../release-notes-mariadb-12.0-rolling-releases/what-is-mariadb-120.md" class="button secondary">Overview of 12.0</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/12.0.2/)

**Release date:** ?
-->

For the highlights of this release, see the [release notes](../../release-notes-mariadb-12.0-rolling-releases/mariadb-12.0.2-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On [GitHub](https://github.com/MariaDB/server/tree/11.8) you can view more details of the revision and view diffs of the code modified in that revision.

* Includes all fixes from [MariaDB 11.8.3](../changelogs-mariadb-11-8-series/mariadb-11.8.3-changelog.md)
* <sup>_Merge_</sup> [<sup>_Revision #aab83aecdc_</sup>](https://github.com/MariaDB/server/commit/aab83aecdc) <sup>_2025-07-31 20:55:47 +0200 - Merge branch '11.8' into 12.0_</sup>
* [Revision #5008e33eac](https://github.com/MariaDB/server/commit/5008e33eac) <sup>_2025-07-31 20:42:40 +0200_</sup>
  * fix sporadic failures of rpl.rpl\_drop\_temp test
* [Revision #dfe4f82ebf](https://github.com/MariaDB/server/commit/dfe4f82ebf) <sup>_2025-07-30 19:46:53 +0200_</sup>
  * update engines/funcs.rpl\_stm\_reset\_slave
* [Revision #f984eecef8](https://github.com/MariaDB/server/commit/f984eecef8) <sup>_2025-07-29 19:44:17 +0200_</sup>
  * bump the VERSION
* [Revision #51602dcc99](https://github.com/MariaDB/server/commit/51602dcc99) <sup>_2025-07-14 08:50:53 +0300_</sup>
  * MDEV-36980 Assertion 'thd-\>mdl\_context.is\_lock\_owner()...fails in close\_thread\_table
* [Revision #ef3d171e7e](https://github.com/MariaDB/server/commit/ef3d171e7e) <sup>_2025-07-09 08:03:21 +1100_</sup>
  * MDEV-37044 derived\_wth\_keys optimization not applied where it should
* [Revision #107291bf98](https://github.com/MariaDB/server/commit/107291bf98) <sup>_2025-06-27 16:27:28 +0200_</sup>
  * MDEV-37031 Fix broken server\_audit.test on Windows
* <sup>_Merge_</sup> [<sup>_Revision #dfcb5c91e0_</sup>](https://github.com/MariaDB/server/commit/dfcb5c91e0) <sup>_2025-06-18 07:50:39 +0200 - Merge branch '11.8' into 12.0_</sup>

{% include "../../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
