---
hidden: true
---

# MariaDB 12.0.2 Release Notes

<!--
<a href="https://mariadb.com/downloads" class="button primary">Download</a> <a href="mariadb-12.0.2-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-12.0-series/mariadb-12.0.2-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-120.md" class="button secondary">Overview of 12.0</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/12.0.2/)

**Release date:** ?
-->

MariaDB 12.0.2 is a [_**Stable (GA)**_](../about/release-criteria.md) release. It is an evolution of [MariaDB 11.8](../mariadb-11-8-series/what-is-mariadb-118.md) with several entirely new features.

MariaDB 12.0 is a [rolling release](../about/release-model.md). One is expected to upgrade to MariaDB 12.1.2, there will be no 12.0.3.

Thanks, and enjoy MariaDB!

{% hint style="success" %}
**For an overview of MariaDB 12.0 see the** [**Changes and Improvements in MariaDB 12.0**](what-is-mariadb-120.md) **page.**
{% endhint %}

Thanks, and enjoy MariaDB!

## Notable Items

### Storage Engines

#### InnoDB

* After SET GLOBAL innodb\_buffer\_pool\_size was aborted while attempting to shrink the buffer pool, executing SET GLOBAL innodb\_adaptive\_hash\_index=ON could lead to corruption of the adaptive hash index. ([MDEV-36863](https://jira.mariadb.org/browse/MDEV-36863))
* Fatal InnoDB error: Unknown error Temp file write failure ([MDEV-36017](https://jira.mariadb.org/browse/MDEV-36017))
* When innodb\_buffer\_pool\_size is being shrunk while there are no data pages cached, InnoDB could hang or crash. ([MDEV-37263](https://jira.mariadb.org/browse/MDEV-37263))
* After a successful shrinking of innodb\_buffer\_pool\_size, there will be no message about it in the server error log.
  * After a failed shrinking of innodb\_buffer\_pool\_size, the adaptive hash index will not be re-enabled if innodb\_adaptive\_hash\_index was ON when SET GLOBAL innodb\_buffer\_pool\_size=... started to execute. ([MDEV-36868](https://jira.mariadb.org/browse/MDEV-36868))
* AUTO\_INCREMENT leads to non-serializable on results ([MDEV-36330](https://jira.mariadb.org/browse/MDEV-36330))
* Vector index was corrupted if one statement was rolled back (e.g. insert violating a unique constraint) in the middle of a larger transaction. ([MDEV-37068](https://jira.mariadb.org/browse/MDEV-37068))
* The new parameter innodb\_linux\_aio controls which Linux implementation to use for innodb\_use\_native\_aio=ON. ([MDEV-36234](https://jira.mariadb.org/browse/MDEV-36234))
  * innodb\_linux\_aio=auto is equivalent to innodb\_linux\_aio=io\_uring when it is available, and falling back to innodb\_linux\_aio=aio when not.
  * Previously, only one implementation (libaio or io\_uring) was available. Currently, if io\_uring is disabled in the environment, we will fall back to the older libaio interface.

#### Aria

* Assertion when adding FK to MyISAM/Aria table with a vector index ([MDEV-37022](https://jira.mariadb.org/browse/MDEV-37022))

### Data Definition - Alter Table

* Adding (with ALTER TABLE) a UNIQUE constraint that is USING HASH to a table with foreign keys could've caused the table to become corrupted. ([MDEV-36852](https://jira.mariadb.org/browse/MDEV-36852))
* DROP DEFAULT makes SHOW CREATE non-idempotent ([MDEV-29001](https://jira.mariadb.org/browse/MDEV-29001))

### Partitioning

* Server crashes in do\_mark\_index\_columns instead of ER\_DUP\_ENTRY on partitioned table ([MDEV-36817](https://jira.mariadb.org/browse/MDEV-36817))
* A replica would crash while replicating UPDATE and DELETE DML statements that target a table which previously had a partition that was converted to a separate table via ALTER TABLE .. CONVERT PARTITION .. TO TABLE. For example, if the command looked like ALTER TABLE t1 CONVERT PARTITION p1 TO TABLE t\_new; the replica would crash when trying to update/deleterows in table t1 after running the command. ([MDEV-36906](https://jira.mariadb.org/browse/MDEV-36906))

### Data Definition - Create Table

* CREATE OR REPLACE with self-referencing CHECK hangs forever, cannot be killed ([MDEV-29155](https://jira.mariadb.org/browse/MDEV-29155))

### Server

* Segfault on INTERSECT ALL with UNION in Oracle mode ([MDEV-25158](https://jira.mariadb.org/browse/MDEV-25158))
* In certain cases privileges on sequences were too restrictive, for example, SELECT on a table might've erroneously required INSERT privilege on a sequences ([MDEV-36870](https://jira.mariadb.org/browse/MDEV-36870))

### mariabackup

* This commit fixes a bug where Aria tables are used in (master->slave1->slave2) and a backup is taken on slave2. In this case it is possible that the replication position in the backup, stored in mysql.gtid\_slave\_pos, will be wrong. This will lead to replication errors if one is trying to use the backup as a new slave. ([MDEV-36143](https://jira.mariadb.org/browse/MDEV-36143))
* Maria-backup would crash during the 'maria\_recovery' part. This could happen if server was doing repair or creating indexes while the backup was running. ([MDEV-36860](https://jira.mariadb.org/browse/MDEV-36860))

### Optimizer

* MariaDB server crash when a query includes a derived table containing unnamed column. ([MDEV-24588](https://jira.mariadb.org/browse/MDEV-24588))
* Crash in add\_keyuses\_for\_splitting() when joining with a derived table ([MDEV-30711](https://jira.mariadb.org/browse/MDEV-30711))
* Split Materialized code: last\_refills is never set in 11.0+ ([MDEV-36323](https://jira.mariadb.org/browse/MDEV-36323))
* Don't generate index\_merge plans, if a column is present in both Secondary Key and Primary Key indexes and either of the indexes include it with DESC order (as the scan itself is not a ROR scan). ([MDEV-36410](https://jira.mariadb.org/browse/MDEV-36410))
* Incorrect handling of null values on join conditions. ([MDEV-37057](https://jira.mariadb.org/browse/MDEV-37057))

### JSON

* Starting from 10.11.12, Incorrect handling of UTF-8 characters (and other character sets requiring more than a single byte representation) in the minimum/maximum positions of a table during the execution of ANALYZE TABLE tbl PERSISTENT FOR ALL resulted in an endless loop consuming more memory and prevented the server from terminating. ([MDEV-36765](https://jira.mariadb.org/browse/MDEV-36765))

### Galera

* galera\_3nodes.inconsistency\_shutdown test occasionally hangs ([MDEV-36968](https://jira.mariadb.org/browse/MDEV-36968))
* Galera-26.4.23 corrects an incompatibility with OpenZFS >= 2.3.0 enabling the use of galera on this filesystem.

### Replication

* semi sync makes the master unresponsive when a replica is stopped ([MDEV-36934](https://jira.mariadb.org/browse/MDEV-36934))
* parallel slave ALTER-SEQUNCE attempted to binlog out-of-order ([MDEV-35570](https://jira.mariadb.org/browse/MDEV-35570))
* mysqldump --dump-slave always starts stopped slave ([MDEV-7611](https://jira.mariadb.org/browse/MDEV-7611))
* Optimize Rows\_log\_event Reporting of Process Info ([MDEV-36839](https://jira.mariadb.org/browse/MDEV-36839))
* Seconds\_Behind\_Master Spike at Log Rotation on Parallel Replication ([MDEV-36840](https://jira.mariadb.org/browse/MDEV-36840))

### Stored routines

* Crash when calling stored function in FOR loop argument ([MDEV-26115](https://jira.mariadb.org/browse/MDEV-26115))

### Authentication and Privilege System

* ALTER TABLE require ALTER privilege on sequence from DEFAULT value expression ([MDEV-36280](https://jira.mariadb.org/browse/MDEV-36280))

### Locking

* Deadlock does not rollback transaction fully ([MDEV-36959](https://jira.mariadb.org/browse/MDEV-36959))

### Data Manipulation - Insert

* UNIQUE constraint that was USING HASH and UNIQUE constrant WITHOUT OVERLAPS could be violated under heavy load in READ COMMITTED transaction isolation mode. ([MDEV-37199](https://jira.mariadb.org/browse/MDEV-37199))

### Character Sets

* Fresh MariaDB installation gives errors when configuring utf8 ([MDEV-36815](https://jira.mariadb.org/browse/MDEV-36815))

### Plugin - AWS key management

* aws\_key\_management compilation was previously broken, is now fixed. plugin can be compiled again. As before, -DNOT\_FOR\_DISTRIBUTION=ON is necessary to build it. ([MDEV-30831](https://jira.mariadb.org/browse/MDEV-30831))

### Packaging

* mariadb systemd mult-instance service was changed to not attempt changes to the permissions on its pam helper server. This prevented unconstructive behaviour and errors in the systemd journal when starting the mariadb@.service. ([MDEV-36738](https://jira.mariadb.org/browse/MDEV-36738))

### Sequences

* Remove the error codes added to 10.11 by the MDEV-36032 patch ([MDEV-36856](https://jira.mariadb.org/browse/MDEV-36856))

### XA

* DML committed within XA transaction block after deadlock error and implicit rollback ([MDEV-37141](https://jira.mariadb.org/browse/MDEV-37141))

### General

* Packages for RHEL8 no longer depend on liburing. The RHEL8 kernel had insufficient kernel support so linking was an unneeded dependency. libaio was sufficient ([MDBF-1042](https://jira.mariadb.org/browse/MDBF-1042))
* SLES 15 SP6 and SLES 15 SP7 are new packages in this release. Because of incompatibilities of packages between SLES service pack versions there are now separate packages for 15sp6 and 15sp7. An upgradeable repo file should include "sles/$releasever/$basearch" rather than the "sles15-amd64" or "sles/15/x86\_64" path that may exist currently. ([MDBF-1067](https://jira.mariadb.org/browse/MDBF-1067), [MDEV-36945](https://jira.mariadb.org/browse/MDEV-36945))
* Fedora 42 is a new release version and x86\_64 and aarch64 packages are available ([MDBF-1060](https://jira.mariadb.org/browse/MDBF-1060))
* Red Hat Enterprise Linux 10 packages are available for x86\_64, aarch64, ppc64le, and s390x hardware platforms ([MDBF-995](https://jira.mariadb.org/browse/MDBF-995))
* Centos Stream 9 previously missed building a MariaDB-provider-lzo package and this has been corrected ([MDBF-1038](https://jira.mariadb.org/browse/MDBF-1038))
* This is the last release of the interim Ubuntu 24.10 which ended its standard support in July 2025 ([MDBF-1090](https://jira.mariadb.org/browse/MDBF-1090))
* Ubuntu 25.04 (Plucky Puffin) packages are available for amd64 and arm64 ([MDBF-849](https://jira.mariadb.org/browse/MDBF-849))
* Debian 13 (Trixie) packages are available for amd64, arm64, ppc64le and i386 ([MDBF-848](https://jira.mariadb.org/browse/MDBF-848))

## Changelog

For a complete list of changes made in MariaDB 12.0.1, with links to detailed information on each push, see the [changelog](../changelogs/changelogs-mariadb-12.0-series/mariadb-12.0.2-changelog.md).

***

{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}

{% @marketo/form formid="4316" formId="4316" %}
