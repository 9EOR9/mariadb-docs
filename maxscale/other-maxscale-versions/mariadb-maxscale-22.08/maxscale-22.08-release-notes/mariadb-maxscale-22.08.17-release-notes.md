# MariaDB MaxScale 22.08.17 Release Notes

## MariaDB MaxScale 22.08.17 Release Notes <a href="#mariadb-maxscale-220817-release-notes" id="mariadb-maxscale-220817-release-notes"></a>

Release 22.08.17 is a GA release.

This document describes the changes in release 22.08.17, when compared to the previous release in the same series.

If you are upgrading from an older major version of MaxScale, please read the [upgrading document](../../mariadb-maxscale-mariadb-maxscale-20/mariadb-maxscale-20-upgrading-maxscale/) for this MaxScale version.

For any problems you encounter, please consider submitting a bug report on [our Jira](https://jira.mariadb.org/projects/MXS).

### Bug fixes <a href="#bug-fixes" id="bug-fixes"></a>

* [MXS-5618](https://jira.mariadb.org/browse/MXS-5618) Maxctrl interactive mode doesn't use --tls-verify-server-cert=false
* [MXS-5613](https://jira.mariadb.org/browse/MXS-5613) The logout screen is shown when accessing the MaxGUI login view.
* [MXS-5608](https://jira.mariadb.org/browse/MXS-5608) optimistic\_trx causes a query to hang
* [MXS-5599](https://jira.mariadb.org/browse/MXS-5599) Processing of conditional headers is incorrect
* [MXS-5598](https://jira.mariadb.org/browse/MXS-5598) MaxCtrl fails to read large inputs from stdin
* [MXS-5597](https://jira.mariadb.org/browse/MXS-5597) admin\_oidc\_url is documented to not be dynamic when in fact it is
* [MXS-5590](https://jira.mariadb.org/browse/MXS-5590) REST-API always sends a Connection: close header
* [MXS-5588](https://jira.mariadb.org/browse/MXS-5588) Signal 11 crash when enabling causal reads with Galera
* [MXS-5582](https://jira.mariadb.org/browse/MXS-5582) Add a Service with a CLUSTER as its target breaks CONFIG SYNC
* [MXS-5577](https://jira.mariadb.org/browse/MXS-5577) Aborted connection on backend mariadb with persistpool maxscale
* [MXS-5576](https://jira.mariadb.org/browse/MXS-5576) Maxctrl config permission check error message is misleading
* [MXS-5567](https://jira.mariadb.org/browse/MXS-5567) Wrong password in interactive mode is only seen after the first command
* [MXS-5566](https://jira.mariadb.org/browse/MXS-5566) --secretsdir has no default value
* [MXS-5563](https://jira.mariadb.org/browse/MXS-5563) Using PKCS#1 private key in the REST-API results in cryptic errors
* [MXS-5556](https://jira.mariadb.org/browse/MXS-5556) Trailing parts of large session command are not routed correctly
* [MXS-5542](https://jira.mariadb.org/browse/MXS-5542) kafkacdc commits offsets when it probes GTIDs from Kafka
* [MXS-5541](https://jira.mariadb.org/browse/MXS-5541) Logs Archive page doesn't show useful API error
* [MXS-5525](https://jira.mariadb.org/browse/MXS-5525) Masking with functions uses wrong rule settings

### Known Issues and Limitations <a href="#known-issues-and-limitations" id="known-issues-and-limitations"></a>

There are some limitations and known issues within this version of MaxScale. For more information, please refer to the [Limitations](../../mariadb-maxscale-14/about-maxscale-14/limitations-and-known-issues-within-maxscale.md) document.

### Packaging <a href="#packaging" id="packaging"></a>

RPM and Debian packages are provided for the supported Linux distributions.

Packages can be downloaded [here](https://mariadb.com/downloads/#mariadb_platform-mariadb_maxscale).

### Source Code <a href="#source-code" id="source-code"></a>

The source code of MaxScale is tagged at GitHub with a tag, which is identical with the version of MaxScale. For instance, the tag of version X.Y.Z of MaxScale is `maxscale-X.Y.Z`. Further, the default branch is always the latest GA version of MaxScale.

The source code is available [here](https://github.com/mariadb-corporation/MaxScale).
