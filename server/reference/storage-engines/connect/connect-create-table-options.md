
# CONNECT Create Table Options

Create Table statements for “CONNECT” tables are standard MariaDB create statements specifying
`engine=CONNECT`. There are a few additional table and column options specific to CONNECT.


### Table Options



| Table Option | Type | Description |
| --- | --- | --- |
| Table Option | Type | Description |
| AVG_ROW_LENGTH | Integer | Can be specified to help CONNECT estimate the size of a variable record table length. |
| BLOCK_SIZE | Integer | The number of rows each block of a [FIX](connect-table-types/connect-dos-and-fix-table-types.md), [BIN](connect-table-types/connect-bin-table-type.md), [DBF](connect-table-types/connect-dbf-table-type.md), or [VEC](connect-table-types/connect-vec-table-type.md) table contains. For an [ODBC](connect-table-types/connect-odbc-table-type-accessing-tables-from-another-dbms.md) table this is the RowSet size option. For a [JDBC](connect-table-types/connect-jdbc-table-type-accessing-tables-from-another-dbms.md) table this is the fetch size. |
| CATFUNC | String | The catalog function used by a [catalog table](connect-table-types/connect-table-types-catalog-tables.md). |
| COLIST | String | The column list of [OCCUR](connect-table-types/connect-occur-table-type.md) tables or $project of [MONGO](connect-table-types/connect-mongo-table-type.md) tables. |
| COMPRESS | Number | 1 or 2 if the data file is g-zip compressed. Defaults to 0. Before CONNECT 1.05.0001, this was boolean, and true if the data file is compressed. |
| CONNECTION | String | Specifies the connection of an [ODBC](connect-table-types/connect-odbc-table-type-accessing-tables-from-another-dbms.md), [JDBC](connect-table-types/connect-jdbc-table-type-accessing-tables-from-another-dbms.md) or [MYSQL](connect-table-types/connect-mysql-table-type-accessing-mysqlmariadb-tables.md) table. |
| DATA_CHARSET | String | The character set used in the external file or data source. |
| DBNAME | String | The target database for [ODBC](connect-table-types/connect-odbc-table-type-accessing-tables-from-another-dbms.md), [JDBC](connect-table-types/connect-jdbc-table-type-accessing-tables-from-another-dbms.md), [MYSQL](connect-table-types/connect-mysql-table-type-accessing-mysqlmariadb-tables.md), [catalog](connect-table-types/connect-table-types-catalog-tables.md), and [PROXY](connect-table-types/connect-proxy-table-type.md) based tables. The database concept is sometimes known as a schema. |
| ENGINE | String | Must be specfied as CONNECT. |
| ENDING | Integer | End of line length. Defaults to 1 for Unix/Linux and 2 for Windows. |
| FILE_NAME | String | The file (path) name for all table types based on files. Can be absolute or relative to the current data directory. If not specified, this is an [Inward table](connect-table-types/inward-and-outward-tables.md#inward-tables) and a default value is used. |
| FILTER | String | To filter an external table. Currently MONGO tables only. |
| HEADER | Integer | Applies to [CSV](connect-table-types/connect-csv-and-fmt-table-types.md), [VEC](connect-table-types/connect-vec-table-type.md), and HTML files. Its meaning depends on the table type. |
| HTTP | String | The HTTP of the client of REST queries. From [Connect 1.06.0010](README.md). |
| HUGE | Boolean | To specify that a table file can be larger than 2GB. For a [MYSQL](connect-table-types/connect-mysql-table-type-accessing-mysqlmariadb-tables.md) table, prevents the result set from being stored in memory. |
| LRECL | Integer | The file record size (often calculated by default). |
| MAPPED | Boolean | Specifies whether file mapping is used to handle the table file. |
| MODULE | String | The (path) name of the DLL or shared lib implementing the access of a non-standard ([OEM](connect-table-types/connect-table-types-oem.md)) table type. |
| MULTIPLE | Integer | Used to specify multiple file tables. |
| OPTION_LIST | String | Used to specify all other options not yet directly defined. |
| QCHAR | String | Specifies the character used for quoting some fields of a [CSV](connect-table-types/connect-csv-and-fmt-table-types.md) table or the identifiers of an [ODBC](connect-table-types/connect-odbc-table-type-accessing-tables-from-another-dbms.md)/[JDBC](connect-table-types/connect-jdbc-table-type-accessing-tables-from-another-dbms.md) tables. |
| QUOTED | Integer | The level of quoting used in [CSV](connect-table-types/connect-csv-and-fmt-table-types.md) table files. |
| READONLY | Boolean | True if the data file must not be modified or erased. |
| SEP_CHAR | String | Specifies the field separator character of a [CSV](connect-table-types/connect-csv-and-fmt-table-types.md) or [XCOL](connect-table-types/connect-xcol-table-type.md) table. Also, used to specify the Jpath separator for [JSON tables](connect-table-types/connect-json-table-type.md). |
| SEPINDEX | Boolean | When true, indexes are saved in separate files. |
| SPLIT | Boolean | True for a [VEC](connect-table-types/connect-vec-table-type.md) table when all columns are in separate files. |
| SRCDEF | String | The source definition of a table retrieved via [ODBC](connect-table-types/connect-odbc-table-type-accessing-tables-from-another-dbms.md), [JDBC](connect-table-types/connect-jdbc-table-type-accessing-tables-from-another-dbms.md) or the MySQL API or used by a [PIVOT](connect-table-types/connect-pivot-table-type.md) table. |
| SUBTYPE | String | The subtype of an [OEM](connect-table-types/connect-table-types-oem.md) table type. |
| TABLE_LIST | String | The comma separated list of TBL table sub-tables. |
| TABLE_TYPE | String | The external table [type](connect-table-types/connect-table-types-overview.md): [DOS](connect-table-types/connect-dos-and-fix-table-types.md), [FIX](connect-table-types/connect-dos-and-fix-table-types.md), [BIN](connect-table-types/connect-bin-table-type.md), [CSV](connect-table-types/connect-csv-and-fmt-table-types.md), [FMT](connect-table-types/connect-csv-and-fmt-table-types.md), [XML](connect-table-types/connect-xml-table-type.md), [JSON](connect-table-types/connect-json-table-type.md), [INI](connect-table-types/connect-ini-table-type.md), [DBF](connect-table-types/connect-dbf-table-type.md), [VEC](connect-table-types/connect-vec-table-type.md), [ODBC](connect-table-types/connect-odbc-table-type-accessing-tables-from-another-dbms.md), [JDBC](connect-table-types/connect-jdbc-table-type-accessing-tables-from-another-dbms.md), [MYSQL](connect-table-types/connect-mysql-table-type-accessing-mysqlmariadb-tables.md), [TBL](connect-table-types/connect-tbl-table-type-table-list.md), [PROXY](connect-table-types/connect-proxy-table-type.md), [XCOL](connect-table-types/connect-xcol-table-type.md), [OCCUR](connect-table-types/connect-occur-table-type.md), [PIVOT](connect-table-types/connect-pivot-table-type.md), [ZIP](connect-table-types/connect-zipped-file-tables.md), [VIR](connect-table-types/connect-table-types-vir.md), [DIR](connect-table-types/connect-table-types-special-virtual-tables.md#dir-type), [WMI](connect-table-types/connect-table-types-special-virtual-tables.md#windows-management-instrumentation-table-type-wmi), [MAC](connect-table-types/connect-table-types-special-virtual-tables.md#mac-address-table-type-mac), and [OEM](connect-table-types/connect-table-types-oem.md). Defaults to [DOS](connect-table-types/connect-dos-and-fix-table-types.md), [MYSQL](connect-table-types/connect-mysql-table-type-accessing-mysqlmariadb-tables.md), or [PROXY](connect-table-types/connect-proxy-table-type.md) depending on what options are used. |
| TABNAME | String | The target table or node for [ODBC](connect-table-types/connect-odbc-table-type-accessing-tables-from-another-dbms.md), [JDBC](connect-table-types/connect-jdbc-table-type-accessing-tables-from-another-dbms.md), [MYSQL](connect-table-types/connect-mysql-table-type-accessing-mysqlmariadb-tables.md), [PROXY](connect-table-types/connect-proxy-table-type.md), or [catalog tables](connect-table-types/connect-table-types-catalog-tables.md); or the top node name for [XML](connect-table-types/connect-xml-table-type.md) tables. |
| URI | String | The URI of a REST request.. From [Connect 1.06.0010](README.md). |
| XFILE_NAME | String | The file (path) base name for table index files. Can be absolute or relative to the data directory. Defaults to the file name. |
| ZIPPED | Boolean | True if the table file(s) is/are zipped in one or several zip files. |



All integers in the above table are unsigned big integers.


Because CONNECT handles many table types; many table type specific options are
not in the above list and must be entered using the `OPTION_LIST` option. The
syntax to use is:


```
... option_list='opname1=opvalue1,opname2=opvalue2...'
```

Be aware that until Connect 1.5.5, no blanks should be inserted before or after the '`=`' and
'`,`' characters. The option name is all that is between the start of the
string or the last '`,`' character and the next '`=`' character, and the
option value is all that is between this '`=`' character and the next '`,`'
or end of string. For instance:


```
option_list='name=TABLE,coltype=HTML,attribute=border=1;cellpadding=5,headattr=bgcolor=yellow';
```

This defines four options, '`name`', '`coltype`', '`attribute`', and
'`headattr`'; with values '`TABLE`', '`HTML`',
'`border=1;cellpadding=5`', and '`bgcolor=yellow`', respectively. The only
restriction is that values cannot contain commas, but they can contain equal
signs.


### Column Options



| Column Option | Type | Description |
| --- | --- | --- |
| Column Option | Type | Description |
| DATE_FORMAT | String | The format indicating how a date is stored in the file. |
| DISTRIB | Enum | “scattered”, “clustered”, “sorted” (ascending). |
| FIELD_FORMAT | String | The column format for some table types. |
| FIELD_LENGTH | Integer | Set the internal field length for DATE columns. |
| FLAG | Integer | An integer value whose meaning depends on the table type. |
| JPATH | String | The Json path of JSON table columns. |
| MAX_DIST | Integer | Maximum number of distinct values in this column. |
| SPECIAL | String | The name of the SPECIAL column that set this column value. |
| XPATH | String | The XML path of XML table columns. |



* The `MAX_DIST` and `DISTRIB` column options are used for block indexing.
* All integers in the above table are unsigned big integers.
* JPATH and XPATH were added to make CREATE TABLE statements more readable, but they do the same thing as FIELD_FORMAT and any of them can be used with the same result.


### Index Options



| Index Option | Type | Description |
| --- | --- | --- |
| Index Option | Type | Description |
| DYNAM | Boolean | Set the index as “dynamic”. |
| MAPPED | Boolean | Use index file mapping. |



**Note 1:** Creating a CONNECT table based on file does not erase or create the
file if the file name is specified in the CREATE TABLE statement ([“outward”](connect-table-types/inward-and-outward-tables.md#outward-tables) table). If the file does not exist, it will be populated by subsequent INSERT or LOAD
commands or by the “AS select statement” of the [CREATE TABLE](../../sql-statements-and-structure/sql-statements/data-definition/create/create-table.md)
command. Unlike the CSV engine, CONNECT easily permits the creation of tables
based on already existing files, for instance files made by other applications.
However, if the file name is not specified, a file with a name defaulting to
`tablename.tabletype` will be created in the data directory ([“inward”](connect-table-types/inward-and-outward-tables.md#inward-tables) table).


**Note 2:** Dropping a CONNECT table is done with a standard DROP statement.
For [outward tables](connect-table-types/inward-and-outward-tables.md#inward-tables), this drops only the CONNECT table definition but does not
erase the corresponding data file and index files. Use `DELETE` or
`TRUNCATE` to do so. This is contrary to data and index files of [inward
tables](connect-table-types/inward-and-outward-tables.md#inward-tables) are erased on DROP like for other MariaDB engines.

