# MariaDB ColumnStore 23.02.13 Release Notes

## Overview

[MariaDB Enterprise ColumnStore](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb-columnstore/README.md) 23.02.13 is a maintenance release of [MariaDB Enterprise ColumnStore](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/mariadb-columnstore/README.md). MariaDB Enterprise ColumnStore is a columnar storage engine that is included with the [MariaDB Enterprise Server](https://github.com/mariadb-corporation/docs-release-notes/blob/test/columnstore/mariadb-columnstore-23-02-release-notes/MariaDB_Enterprise_Server/README.md).

MariaDB Enterprise ColumnStore 23.02.13 was released on 26 Mar 2025.\
This release is of General Availability (GA) maturity.\
MariaDB Enterprise ColumnStore 23.02.13 is a GA release in the 23.02 series.

This release of MariaDB Enterprise ColumnStore is included with MariaDB Enterprise Server 10.6.14-9.

Users of earlier MariaDB Enterprise ColumnStore releases are encouraged to upgrade.

## Notable Changes

* Improved memory management across JOIN, DISTINCT and ORDER BY operations to prevent out-of-memory events and related crashes ([MCOL-5797](https://jira.mariadb.org/browse/MCOL-5797))
* Introduced the mcs-load-brm-from-file utility to assist in manually resolving certain upgrade issues ([MCOL-5816](https://jira.mariadb.org/browse/MCOL-5816))

## Issues Fixed

* Multiplication between a GROUP BY key and an averaged value can error out ([MCOL-5889](https://jira.mariadb.org/browse/MCOL-5889))
* Control flow could fail resulting in hung queries ([MCOL-5835](https://jira.mariadb.org/browse/MCOL-5835))

## Platforms

In alignment with the [enterprise lifecycle](../../enterprise-server/enterprise-server-lifecycle.md), MariaDB Enterprise ColumnStore 23.02.13 is provided for:

* Debian 11 (x86\_64, ARM64)
* Red Hat Enterprise Linux 8 (x86\_64, ARM64)
* Red Hat Enterprise Linux 9 (x86\_64, ARM64)
* Rocky Linux 8 (x86\_64, ARM64)
* Rocky Linux 9 (x86\_64, ARM64)
* Ubuntu 20.04 (x86\_64, ARM64)
* Ubuntu 22.04 (x86\_64, ARM64)

## Installation Instructions

* [ColumnStore Object Storage Topology with MariaDB Enterprise Server 10.6 ](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/architecture/topologies/columnstore-object-storage)[and MariaDB Enterprise ColumnStore 23.10](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/architecture/topologies/columnstore-object-storage)
* [ColumnStore Shared Local Storage Topology with MariaDB Enterprise Server 10.6](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/architecture/topologies/columnstore-shared-local-storage)[ and MariaDB Enterprise ColumnStore 23.10](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/architecture/topologies/columnstore-shared-local-storage)
* [HTAP Topology with MariaDB Enterprise Server 10.6](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/architecture/topologies/htap)[ and MariaDB Enterprise ColumnStore 23.10](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/architecture/topologies/htap)
* [Single-Node Enterprise ColumnStore 23.10 with MariaDB Enterprise Server 10.6](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/architecture/topologies/single-node-topologies/enterprise-server-with-columnstore-object-storage)[ and Object Storage](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/architecture/topologies/single-node-topologies/enterprise-server-with-columnstore-object-storage)
* [Single-Node Enterprise ColumnStore 23.10 with MariaDB Enterprise Server 10.6](https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/architecture/topologies/single-node-topologies)

## Upgrade Instructions

* Upgrade Multi-Node MariaDB Enterprise ColumnStore from 6 to 23.10
* [Major Release Upgrades for MariaDB Enterprise ColumnStore](../)

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
