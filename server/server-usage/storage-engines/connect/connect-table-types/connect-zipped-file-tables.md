# CONNECT Zipped File Tables

#### Note

Connect can work on table files that are compressed in one or several zip files.

The specific options used when creating tables based on zip files are:

| Table Option | Type    | Description                                                                                                                                                                                                                                               |
| ------------ | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Table Option | Type    | Description                                                                                                                                                                                                                                               |
| ZIPPED       | Boolean | Required to be set as true.                                                                                                                                                                                                                               |
| ENTRY\*      | String  | The optional name or pattern of the zip entry or entries to be used with the table. If not specified, all entries or only the first one will be used depending on the mulentries option setting.                                                          |
| MULENTRIES\* | Boolean | True if several entries are part of the table. If not specified, it defaults to false if the entry option is not specified. If the entry option is specified, it defaults to true if the entry name contains wildcard characters or false if it does not. |
| APPEND\*     | Boolean | Used when creating new zipped tables (see below)                                                                                                                                                                                                          |
| LOAD\*       | String  | Used when creating new zipped tables (see below)                                                                                                                                                                                                          |

Options marked with a ‘\*’ must be specified in the option list.

Examples of use:

#### Example 1: Single CSV File Included in a Single ZIP File

Let's suppose you have a CSV file from which you would create a table by:

```
create table emp
... optional column definition
engine=connect table_type=CSV file_name='E:/Data/employee.csv'
sep_char=';' header=1;
```

If the CSV file is included in a ZIP file, the CREATE TABLE becomes:

```
create table empzip
... optional column definition
engine=connect table_type=CSV file_name='E:/Data/employee.zip'
sep_char=';' header=1 zipped=1 option_list='Entry=emp.csv';
```

The _file\_name_ option is the name of the zip file. The _entry_ option is the name of the entry inside the zip file. If there is only one entry file inside the zip file, this option can be omitted.

#### Example 2: Several CSV Files Included in a Single ZIP File

If the table is made from several files such as emp01.csv, emp02.csv, etc., the standard create table would be:

```
create table empmul (
... required column definition
) engine=connect table_type=CSV file_name='E:/Data/emp*.csv' 
sep_char=';' header=1 multiple=1;
```

But if these files are all zipped inside a unique zip file, it becomes:

```
create table empzmul
... required column definition
engine=connect table_type=CSV file_name='E:/Data/emp.zip'
sep_char=';' header=1 zipped=1 option_list='Entry=emp*.csv';
```

Here the _entry_ option is the pattern that the files inside the zip file must match. If all entry files are ok, the _entry_ option can be omitted but the Boolean option _mulentries_ must be specified as true.

#### Example 3: Single CSV File included in Multiple ZIP Files (Without considering subfolders)

If the table is created on several zip files, it is specified as for all other multiple tables:

```
create table zempmul (
... required column definition
) engine=connect table_type=CSV file_name='E:/Data/emp*.zip' 
sep_char=';' header=1 multiple=1 zipped=yes 
option_list='Entry=employee.csv';
```

Here again the _entry_ option is used to restrict the entry file(s) to be used inside the zip files and can be omitted if all are ok.

The column descriptions can be retrieved by the discovery process for table types allowing it. It cannot be done for multiple tables or multiple entries.

A catalog table can be created by adding _catfunc=columns_. This can be used to show the column definitions of multiple tables. _Multiple_ must be set to false and the column definitions will be the ones of the first table or entry.

This first implementation has some restrictions:

1. Zipped tables are read-only. [UPDATE](../../../../reference/sql-statements/data-manipulation/changing-deleting-data/update.md) and [DELETE](../../../../reference/sql-statements/data-manipulation/changing-deleting-data/delete.md) are not supported. However, [INSERT](../../../../reference/sql-statements/data-manipulation/inserting-loading-data/insert.md) is supported in a specific way when making tables.
2. The inside files are decompressed into memory. Memory problems may arise with huge files.
3. Only file types that can be handled from memory are eligible for this. This includes [DOS](connect-dos-and-fix-table-types.md), [FIX](connect-dos-and-fix-table-types.md), [BIN](connect-bin-table-type.md), [CSV](connect-csv-and-fmt-table-types.md), [FMT](connect-csv-and-fmt-table-types.md), [DBF](connect-dbf-table-type.md), [JSON](connect-json-table-type.md), and [XML](connect-xml-table-type.md) table types, as well as types based on these such as [XCOL](connect-xcol-table-type.md), [OCCUR](connect-occur-table-type.md) and [PIVOT](connect-pivot-table-type.md).

Optimization by indexing or block indexing is possible for table types supporting it. However, it applies to the uncompressed table. This means that the whole table is always uncompressed.

Partitioning is also supported. See how to do it in the section about partitioning.

### Creating New Zipped Tables

Tables can be created to access already existing zip files. However, is it also possible to make the zip file from an existing file or table. Two ways are available to make the zip file:

#### Insert Method

insert can be used to make the table file for table types based on records (this excludes DBF, XML and JSON when pretty is not 0). However, the current implementation of the used package (minizip) does not support adding to an already existing zip entry. This means that when executing an insert statement the inserted records are not added but replace the existing ones. CONNECT protects existing data by not allowing such inserts, Therefore, only three ways are available to do so:

1. Using only one insert statement to make the whole table. This is possible only for small tables and is principally useful when making tests.
2. Making the table from the data of another table. This can be done by executing an “insert into table select \* from another\_table” or by specifying “as select \* from another\_table” in the create table statement.
3. Making the table from a file whose format enables to use the “load data infile” statement.

To add a new entry in an existing zip file, specify “append=YES” in the option list. When inserting several entries, use ALTER to specify the required options, for instance:

```
create table znumul (
Chiffre int(3) not null,
Lettre char(16) not null)
engine=CONNECT table_type=CSV
file_name='C:/Data/FMT/mnum.zip' header=1 lrecl=20 zipped=1
option_list='Entry=Num1';
insert into znumul select * from num1;
alter table znumul option_list='Entry=Num2,Append=YES';
insert into znumul select * from num2;
alter table znumul option_list='Entry=Num3,Append=YES';
insert into znumul select * from num3;
alter table znumul option_list='Entry=Num*,Append=YES';
select * from znumul;
```

The last ALTER is needed to display all the entries.

#### File Zipping Method

This method enables to make the zip file from another file when creating the table. It applies to all table types including DBF, XML and JSON. It is specified in the create table statement with the load option. For example:

```
create table XSERVZIP (
NUMERO varchar(4) not null,
LIEU varchar(15) not null,
CHEF varchar(5) not null,
FONCTION varchar(12) not null,
NOM varchar(21) not null)
engine=CONNECT table_type=XML file_name='E:/Xml/perso.zip' zipped=1
option_list='entry=services,load=E:/Xml/serv2.xml';
```

When executing this statement, the _serv2.xml_ file will be zipped as /perso.zip\*. The entry name can be specified or defaults to the source file name.\*

If the column descriptions are specified, the table can be used later to read from the zipped table, but they are not used when creating the zip file. Thus, a fake column (there must be one) can be specified and another table created to read the zip file. This one can take advantage of the discovery process to avoid providing the columns description for table types allowing it. For instance:

```
create table mkzq (whatever int)
engine=connect table_type=DBF zipped=1
file_name='C:/Data/EAUX/dbf/CQUART.ZIP'
option_list='Load=C:/Data/EAUX/dbf/CQUART.DBF';

create table zquart
engine=connect table_type=DBF zipped=1
file_name='C:/Data/EAUX/dbf/CQUART.ZIP';
```

It is also possible to create a multi-entries table from several files:

```
CREATE TABLE znewcities (
  _id char(5) NOT NULL,
  city char(16) NOT NULL,
  lat double(18,6) NOT NULL `FIELD_FORMAT`='loc:[0]',
  lng double(18,6) NOT NULL `FIELD_FORMAT`='loc:[1]',
  pop int(6) NOT NULL,
  state char(2) NOT NULL
) ENGINE=CONNECT TABLE_TYPE=JSON FILE_NAME='E:/Json/newcities.zip' ZIPPED=1 LRECL=1000 OPTION_LIST='Load=E:/Json/city_*.json,mulentries=YES,pretty=0';
```

Here the files to load are specified with wildcard characters and the _mulentries_ options must be specified. However, the _entry_ option must not be specified, entry names will be made from the file names. Provide a fake column description if the files have different column layout, but specific tables will have to be created to read each of them.

### ZIP Table Type

A ZIP table type is also available. It is not meant to read the inside files but to display information about the zip file contents. For instance:

```
create table xzipinfo2 (
entry varchar(256)not null,
cmpsize bigint not null flag=1,
uncsize bigint not null flag=2,
method int not null flag=3,
date datetime not null flag=4)
engine=connect table_type=ZIP file_name='E:/Data/Json/cities.zip';
```

This will display the name, compressed size, uncompressed size, and compress method of all entries inside the zip file. Column names are irrelevant; these are flag values that mean what information to retrieve.

It is possible to retrieve this information from several zip files by specifying the multiple option:

```
create table TestZip1 (
entry varchar(260)not null,
cmpsize bigint not null flag=1,
uncsize bigint not null flag=2,
method int not null flag=3,
date datetime not null flag=4,
zipname varchar(256) special='FILEID')
engine=connect table_type=ZIP multiple=1
file_name='C:/Data/Ziptest/CCAM06300_DBF_PART*.zip';
```

Here we added the special column zipname to get the name of the zip file for each entry.

CC BY-SA / Gnu FDL

{% @marketo/form formId="4316" %}
