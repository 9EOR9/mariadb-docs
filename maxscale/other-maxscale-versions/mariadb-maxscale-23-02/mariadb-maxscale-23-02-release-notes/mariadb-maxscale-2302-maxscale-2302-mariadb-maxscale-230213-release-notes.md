# MariaDB MaxScale 23.02.13 Release Notes

Release 23.02.13 is a GA release.

This document describes the changes in release 23.02.13, when compared to the\
previous release in the same series.

If you are upgrading from an older major version of MaxScale, please read the[upgrading document](../mariadb-maxscale-23-02-upgrading/mariadb-maxscale-2302-upgrading-mariadb-maxscale-from-2208-to-2302.md) for\
this MaxScale version.

For any problems you encounter, please consider submitting a bug\
report on [our Jira](https://jira.mariadb.org/projects/MXS).

### Bug fixes

* [MXS-5536](https://jira.mariadb.org/browse/MXS-5536) Early mismatched responses to session commands do not close connections
* [MXS-5533](https://jira.mariadb.org/browse/MXS-5533) Remove session\_trace parameter from services section
* [MXS-5529](https://jira.mariadb.org/browse/MXS-5529) Session commands with max\_slave\_connections=0 after switchover do not discard stale connections
* [MXS-5527](https://jira.mariadb.org/browse/MXS-5527) The "INSERT INTO...RETURNING" syntax breaks causal\_reads
* [MXS-5522](https://jira.mariadb.org/browse/MXS-5522) config sync does not ignore port for listeners
* [MXS-5520](https://jira.mariadb.org/browse/MXS-5520) config\_sync\_password infinitely doubles after maxscale restart & alter command
* [MXS-5511](https://jira.mariadb.org/browse/MXS-5511) The Contact view in the GUI has outdated information
* [MXS-5508](https://jira.mariadb.org/browse/MXS-5508) Relationship selections auto-cleared when creating a new monitor object
* [MXS-5507](https://jira.mariadb.org/browse/MXS-5507) readwritesplit enables multi-statements regardless of the state of causal\_reads
* [MXS-5493](https://jira.mariadb.org/browse/MXS-5493) Cluster tree is not visualized accurately
* [MXS-5492](https://jira.mariadb.org/browse/MXS-5492) idle\_session\_pool\_time=0s does not fairly share connections
* [MXS-5488](https://jira.mariadb.org/browse/MXS-5488) Need Documentation updates for Maxscale install recommendation
* [MXS-5466](https://jira.mariadb.org/browse/MXS-5466) MaxCtrl warnings are very verbose
* [MXS-5455](https://jira.mariadb.org/browse/MXS-5455) Errors during loading of users lack the service name
* [MXS-5450](https://jira.mariadb.org/browse/MXS-5450) maxctrl list queries fails
* [MXS-5449](https://jira.mariadb.org/browse/MXS-5449) Encrypted passwords cannot be used with maxctrl
* [MXS-5443](https://jira.mariadb.org/browse/MXS-5443) Log message: Unknown prepared statement handler given to MaxScale
* [MXS-5439](https://jira.mariadb.org/browse/MXS-5439) Backend connections with fail with EAGAIN
* [MXS-5437](https://jira.mariadb.org/browse/MXS-5437) Failed authentication warnings do not mention lack of client-side SSL as the reason of the failure
* [MXS-5432](https://jira.mariadb.org/browse/MXS-5432) MaxScale 24.02.04 not closing DB Connections properly
* [MXS-5419](https://jira.mariadb.org/browse/MXS-5419) Duration types that only take seconds return ms as units instead of s
* [MXS-5415](https://jira.mariadb.org/browse/MXS-5415) retry\_failed\_reads is not affected by delayed\_retry\_timeout
* [MXS-5409](https://jira.mariadb.org/browse/MXS-5409) list session in GUI shows wrong amount of sessions
* [MXS-5408](https://jira.mariadb.org/browse/MXS-5408) rebuild-server does not work with MariaDB 11.4
* [MXS-5403](https://jira.mariadb.org/browse/MXS-5403) Debug assertion on very large binary protocol prepared statements
* [MXS-5397](https://jira.mariadb.org/browse/MXS-5397) NVL and NVL2 are not detected as builtin functions outside of sql\_mode=ORACLE
* [MXS-5395](https://jira.mariadb.org/browse/MXS-5395) Kafkacdc errors for wrong GTID positions are not clear
* [MXS-5382](https://jira.mariadb.org/browse/MXS-5382) Errors due to max\_connections being exceeded are always fatal errors
* [MXS-5366](https://jira.mariadb.org/browse/MXS-5366) Certain special characters in the maxscale user causes async-rebuild-server to fail
* [MXS-5340](https://jira.mariadb.org/browse/MXS-5340) ed25519 socket droped when no user\_mapping\_file
* [MXS-5314](https://jira.mariadb.org/browse/MXS-5314) Resultset table not fully expanded for inactive query tab

### Known Issues and Limitations

There are some limitations and known issues within this version of MaxScale.\
For more information, please refer to the [Limitations](../mariadb-maxscale-23-02-about/mariadb-maxscale-2302-limitations-and-known-issues-within-mariadb-maxscale.md) document.

### Packaging

RPM and Debian packages are provided for the supported Linux distributions.

Packages can be downloaded [here](https://mariadb.com/downloads/#mariadb_platform-mariadb_maxscale).

### Source Code

The source code of MaxScale is tagged at GitHub with a tag, which is identical\
with the version of MaxScale. For instance, the tag of version X.Y.Z of MaxScale\
is `maxscale-X.Y.Z`. Further, the default branch is always the latest GA version\
of MaxScale.

The source code is available [here](https://github.com/mariadb-corporation/MaxScale).

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
