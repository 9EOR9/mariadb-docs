# About Mroonga

| Mroonga Version | Introduced                                                                                                                                                                                                                                                                                                                   | Maturity |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 7.07            | [MariaDB 10.2.11](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/old-releases/release-notes-mariadb-10-2-series/mariadb-10211-release-notes), [MariaDB 10.1.29](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/old-releases/release-notes-mariadb-10-1-series/mariadb-10129-release-notes) | Stable   |
| 5.04            | [MariaDB 10.1.6](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/old-releases/release-notes-mariadb-10-1-series/mariadb-10-1-6-release-notes)                                                                                                                                                                | Stable   |
| 5.02            | [MariaDB 10.0.18](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/old-releases/release-notes-mariadb-10-0-series/mariadb-10018-release-notes), [MariaDB 10.1.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/old-releases/release-notes-mariadb-10-1-series/mariadb-10-1-5-release-notes) | Stable   |
| 5.0             | [MariaDB 10.0.17](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/old-releases/release-notes-mariadb-10-0-series/mariadb-10017-release-notes)                                                                                                                                                                | Stable   |
| 4.06            | [MariaDB 10.0.15](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/community-server/old-releases/release-notes-mariadb-10-0-series/mariadb-10015-release-notes)                                                                                                                                                                | Stable   |

Mroonga is a full text search storage engine based on Groonga, which is an open-source CJK-ready (Chinese, Japanese, and Korean) fulltext search engine using column base. See [groonga.org](https://groonga.org) for more.

With Mroonga, you can have a CJK-ready full text search feature, and it is faster than the [MyISAM](../myisam-storage-engine/) and [InnoDB](../innodb/) [full text search](../../../ha-and-performance/optimization-and-tuning/optimization-and-indexes/full-text-indexes/) for both updating and searching.

Mroonga also supports Groonga's fast geolocation search by using MariaDB's geolocation SQL syntax.

Mroonga currently only supports Linux x86\_64 (Intel64/AMD64).

## How to Install

Enable Mroonga with the following statement:

```sql
INSTALL SONAME 'ha_mroonga';
```

On Debian and Ubuntu mroonga engine are installed with

```bash
sudo apt-get install mariadb-plugin-mroonga
```

See [Plugin overview](../../../reference/plugins/plugin-overview.md) for details on installing and uninstalling plugins.

[SHOW ENGINES](../../../reference/sql-statements/administrative-sql-statements/show/show-engines.md) can be used to check whether Mroonga is installed correctly:

```sql
SHOW ENGINES;
...
*************************** 8. row ***************************
      Engine: Mroonga
     Support: YES
     Comment: CJK-ready fulltext search, column store
Transactions: NO
          XA: NO
  Savepoints: NO
...
```

Once the plugin is installed, add a UDF (User-Defined Function) named "last\_insert\_grn\_id", that returns the record ID assigned by groonga in INSERT, by the following SQL.

```sql
CREATE FUNCTION last_insert_grn_id RETURNS INTEGER SONAME 'ha_mroonga.so';
```

## Limitations

* The maximum size of a single key is 4096 bytes.
* The maximum size of all keys is 4GB.
* The maximum number of records in a fulltext index is 268,435,455
* The maximum number of distinct terms in a fulltext index is 268,435,455
* The maximum size of a fulltext index is 256GB

Note that the maximum sizes are not hard limits, and may vary according to circumstance.

For more details, see [limitations.html](https://mroonga.org/docs/reference/limitations.html).

## Available Character Sets

Mroonga supports a limited number of [character sets](../../../reference/data-types/string-data-types/character-sets/). These include:

* ASCII
* BINARY
* CP932
* EUCJPMS
* KOI8R
* LATIN1
* SJIS
* UJIS
* UTF8
* UTF8MB4

## More Information

Further documentation for Mroonga can be found at

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
