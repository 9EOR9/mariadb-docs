# MariaDB Connector/J 2.5.0 Changelog

{% include "../../../../.gitbook/includes/latest-java.md" %}

[Download](https://downloads.mariadb.com/Connectors/java/connector-java-2.5.0)[Release Notes](../../2.5/mariadb-connector-j-250-release-notes.md)[Changelog](mariadb-connector-j-250-changelog.md)[Connector/J Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/en/about-mariadb-connector-j/README.md)

**Release date:** 3 Oct 2019

For the highlights of this release, see the[release notes](../../2.5/mariadb-connector-j-250-release-notes.md).

The revision number links will take you to the revision's page on GitHub. On[GitHub](https://github.com/MariaDB/mariadb-connector-j) you can view more\
details of the revision and view diffs of the code modified in that revision.

* [Revision #8c53983c](https://github.com/mariadb-corporation/mariadb-connector-j/commit/8c53983c) \[[CONJ-698](https://jira.mariadb.org/browse/CONJ-698)] statement#getGeneratedKeys() returns two rows if ON DUPLICATE KEY UPDATE statement updated a row
* [Revision #ae066948](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ae066948) \[misc] updating copyright
* [Revision #d4eecfbb](https://github.com/mariadb-corporation/mariadb-connector-j/commit/d4eecfbb) \[misc] code format standardization following google-java-format
* [Revision #533b1f8d](https://github.com/mariadb-corporation/mariadb-connector-j/commit/533b1f8d) \[[CONJ-692](https://jira.mariadb.org/browse/CONJ-692)] ConnectionPoolDataSource interface addition to MariaDbPoolDataSource
* [Revision #a0f2f42a](https://github.com/mariadb-corporation/mariadb-connector-j/commit/a0f2f42a) \[[CONJ-561](https://jira.mariadb.org/browse/CONJ-561)] JDBC 4.3 Statement enquoteLiteral, enquoteIdentifier, isSimpleIdentifier and enquoteNCharLiteral methods
* [Revision #4c894f94](https://github.com/mariadb-corporation/mariadb-connector-j/commit/4c894f94) \[[CONJ-727](https://jira.mariadb.org/browse/CONJ-727)] TLS socket factory service implementation Default implementation is provided.
* [Revision #d462f323](https://github.com/mariadb-corporation/mariadb-connector-j/commit/d462f323) \[misc] removing test for sha2 plugin for MySQL version before 5.7
* [Revision #a5cc2bf6](https://github.com/mariadb-corporation/mariadb-connector-j/commit/a5cc2bf6) \[misc] travis testing configuration correction for caching\_sha2\_password
* [Revision #4630edc3](https://github.com/mariadb-corporation/mariadb-connector-j/commit/4630edc3) \[[CONJ-663](https://jira.mariadb.org/browse/CONJ-663)] Implement caching\_sha2\_password and sha256\_password plugin
* [Revision #5549f4bb](https://github.com/mariadb-corporation/mariadb-connector-j/commit/5549f4bb) \[misc] remove multi-authentication test if using maxscale
* [Revision #9ad6dea0](https://github.com/mariadb-corporation/mariadb-connector-j/commit/9ad6dea0) \[[CONJ-734](https://jira.mariadb.org/browse/CONJ-734)] DatabaseMetaData.getSchemaTerm must return "schema"
* [Revision #67af2abb](https://github.com/mariadb-corporation/mariadb-connector-j/commit/67af2abb) \[misc] correcting appveyor MariaDB server version
* [Revision #6a3d4aa0](https://github.com/mariadb-corporation/mariadb-connector-j/commit/6a3d4aa0) \[misc] set default testing to 10.4, removing deprecated [MariaDB 10.0](../../../../mariadb-community-server-release-notes/old-releases/release-notes-mariadb-10-0-series/changes-improvements-in-mariadb-10-0.md)
* [Revision #b653d149](https://github.com/mariadb-corporation/mariadb-connector-j/commit/b653d149) \[[CONJ-733](https://jira.mariadb.org/browse/CONJ-733)] adding credential service implementation Credential service permits providing user / password just implementing CredentialPlugin interface. 3 default implementations : - using environment credential - using java system properties credential - using IAM authentication
* [Revision #7880c6a9](https://github.com/mariadb-corporation/mariadb-connector-j/commit/7880c6a9) \[[CONJ-733](https://jira.mariadb.org/browse/CONJ-733)] adding javadoc to Authentication plugin management classes moving Options class since available from external authentication plugin
* [Revision #bfaa6a24](https://github.com/mariadb-corporation/mariadb-connector-j/commit/bfaa6a24) \[[CONJ-733](https://jira.mariadb.org/browse/CONJ-733)] Authentication plugin management using service loader. Authentication plugins now implements AuthenticationPlugin and must be declared in services. This permits automatic loading if present in classpath
* [Revision #492c2e90](https://github.com/mariadb-corporation/mariadb-connector-j/commit/492c2e90) \[[CONJ-732](https://jira.mariadb.org/browse/CONJ-732)] Driver getPropertyInfo returns no options information for empty url
* [Revision #1b8c88ad](https://github.com/mariadb-corporation/mariadb-connector-j/commit/1b8c88ad) Merge branch 'master' into develop
* [Revision #1bcbc8c9](https://github.com/mariadb-corporation/mariadb-connector-j/commit/1bcbc8c9) \[misc] enwuring test stability for aurora
* [Revision #955d7a9e](https://github.com/mariadb-corporation/mariadb-connector-j/commit/955d7a9e) \[misc] test stability improvement on Driver deregisterDriver
* [Revision #d286f819](https://github.com/mariadb-corporation/mariadb-connector-j/commit/d286f819) \[[CONJ-729](https://jira.mariadb.org/browse/CONJ-729)] master-slave regression: commit on read-only server Executed only when there is an active transaction on master connection
* [Revision #0dba4723](https://github.com/mariadb-corporation/mariadb-connector-j/commit/0dba4723) \[[CONJ-563](https://jira.mariadb.org/browse/CONJ-563)] handling driver possible de-reregistration then new registration
* [Revision #6d55197b](https://github.com/mariadb-corporation/mariadb-connector-j/commit/6d55197b) \[misc] checktyle code correction
* [Revision #0831106b](https://github.com/mariadb-corporation/mariadb-connector-j/commit/0831106b) \[[CONJ-563](https://jira.mariadb.org/browse/CONJ-563)] ensure closing when using custom scheduler provider Removing race condition in case of Driver de-reregistration and new registration
* [Revision #cbe7f560](https://github.com/mariadb-corporation/mariadb-connector-j/commit/cbe7f560) \[[CONJ-563](https://jira.mariadb.org/browse/CONJ-563)] Driver deregistration now close active thread pools. Customs pool provided interface will have to implements a new close method.
* [Revision #6b473f7c](https://github.com/mariadb-corporation/mariadb-connector-j/commit/6b473f7c) \[misc] correction to return expected exception type on connection error
* [Revision #6caf2118](https://github.com/mariadb-corporation/mariadb-connector-j/commit/6caf2118) \[misc] travis jdk test
* [Revision #ad8b9752](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ad8b9752) Merge branch 'feature/[CONJ-724](https://jira.mariadb.org/browse/CONJ-724)' into develop
* [Revision #ffa77219](https://github.com/mariadb-corporation/mariadb-connector-j/commit/ffa77219) \[misc] connection refactoring for simplification This will a future proxy redirection evolution
* [Revision #57c36588](https://github.com/mariadb-corporation/mariadb-connector-j/commit/57c36588) \[[CONJ-725](https://jira.mariadb.org/browse/CONJ-725)] Connection Failure when using PAM authenticated user on 10.4 MariaDB server
* [Revision #501e3fbd](https://github.com/mariadb-corporation/mariadb-connector-j/commit/501e3fbd) \[[CONJ-724](https://jira.mariadb.org/browse/CONJ-724)] Do not ignore the Calendar parameter in ResultSet#getTime(int, Calendar)
* [Revision #89fcc879](https://github.com/mariadb-corporation/mariadb-connector-j/commit/89fcc879) \[[CONJ-724](https://jira.mariadb.org/browse/CONJ-724)] Test passing explicit calendars to setDate/getDate/setTime/getTime/etc.
* [Revision #b0ead1f1](https://github.com/mariadb-corporation/mariadb-connector-j/commit/b0ead1f1) Merge tag '2.4.3' into develop

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
