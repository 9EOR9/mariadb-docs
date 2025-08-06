# MariaDB 10.6.23 Release Notes

{% include "../../.gitbook/includes/unreleased-10-6.md" %}

<a href="https://mariadb.com/downloads/community" class="button primary">Download</a> <a href="mariadb-10.6.23-release-notes.md" class="button secondary">Release Notes</a> <a href="../changelogs/changelogs-mariadb-106-series/mariadb-10.6.23-changelog.md" class="button secondary">Changelog</a> <a href="what-is-mariadb-106.md" class="button secondary">Overview of 10.6</a>

[<sup>_Alternate download from mariadb.org_</sup>](https://downloads.mariadb.org/mariadb/10.6.23/)

**Release date:** 6 Aug 2025

[MariaDB 10.6](what-is-mariadb-106.md) is a current long-term series of MariaDB, [maintained until](https://mariadb.org/about/#maintenance-policy) July 2026. It is an evolution of [MariaDB 10.5](../old-releases/mariadb-10-5-series/what-is-mariadb-105.md) with several entirely new features.

MariaDB 10.6.23 is a [_**Stable (GA)**_](../about/release-criteria.md) release.

{% hint style="success" %}
**For an overview of MariaDB 10.6 see the** [**MariaDB 10.6 Changes & Improvements**](what-is-mariadb-106.md) **page.**
{% endhint %}

Thanks, and enjoy MariaDB!

## Notable Items

### Storage Engines

#### InnoDB

* Fatal InnoDB error: Unknown error Temp file write failure ([MDEV-36017](https://jira.mariadb.org/browse/MDEV-36017))
* AUTO\_INCREMENT leads to non-serializable on results ([MDEV-36330](https://jira.mariadb.org/browse/MDEV-36330))

### Data Definition - Alter Table

* Adding (with ALTER TABLE) a UNIQUE constraint that is USING HASH to a table with foreign keys could've caused the table to become corrupted. ([MDEV-36852](https://jira.mariadb.org/browse/MDEV-36852))

### Partitioning

* Server crashes in do\_mark\_index\_columns instead of ER\_DUP\_ENTRY on partitioned table ([MDEV-36817](https://jira.mariadb.org/browse/MDEV-36817))

### Data Definition - Create Table

* CREATE OR REPLACE with self-referencing CHECK hangs forever, cannot be killed ([MDEV-29155](https://jira.mariadb.org/browse/MDEV-29155))

### Server

* Segfault on INTERSECT ALL with UNION in Oracle mode ([MDEV-25158](https://jira.mariadb.org/browse/MDEV-25158))
* In certain cases privileges on sequences were too restrictive, for example, SELECT on a table might've erroneously required INSERT privilege on a sequences ([MDEV-36870](https://jira.mariadb.org/browse/MDEV-36870))

### mariabackup

* This commit fixes a bug where Aria tables are used in (master-\>slave1-\>slave2) and a backup is taken on slave2. In this case it is possible that the replication position in the backup, stored in mysql.gtid\_slave\_pos, will be wrong. This will lead to replication errors if one is trying to use the backup as a new slave. ([MDEV-36143](https://jira.mariadb.org/browse/MDEV-36143))

### Galera

* galera\_3nodes.inconsistency\_shutdown test occasionally hangs ([MDEV-36968](https://jira.mariadb.org/browse/MDEV-36968))

### Replication

* semi sync makes the master unresponsive when a replica is stopped ([MDEV-36934](https://jira.mariadb.org/browse/MDEV-36934))

### Authentication and Privilege System

* ALTER TABLE require ALTER privilege on sequence from DEFAULT value expression ([MDEV-36280](https://jira.mariadb.org/browse/MDEV-36280))

### Data Manipulation - Insert

* UNIQUE constraint that was USING HASH and UNIQUE constrant WITHOUT OVERLAPS could be violated under heavy load in READ COMMITTED transaction isolation mode. ([MDEV-37199](https://jira.mariadb.org/browse/MDEV-37199))

## Changelog

For a complete list of changes made in MariaDB 10.6.23, with links to detailed information on each push, see the [changelog](../changelogs/changelogs-mariadb-106-series/mariadb-10.6.23-changelog.md).


{% include "../../.gitbook/includes/announce.md" %}

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/7hzG0V6AUK8DqF4oiVaW/" %}
<!-- This page is licensed: CC BY-SA / Gnu FDL -->

{% @marketo/form formid="4316" formId="4316" %}
