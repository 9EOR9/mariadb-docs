# MariaDB Connector/J 3.1.0 Release Notes

{% include "../../../.gitbook/includes/latest-java.md" %}

[Download](https://mariadb.com/downloads/connectors/connectors-data-access/java8-connector)[Release Notes](mariadb-connector-j-3-1-0-release-notes.md)[Changelog](../changelogs/3.1/mariadb-connector-j-3-1-0-changelog.md)[Connector/J Overview](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-j/README.md)

**Release date:** 15 Nov 2022

MariaDB Connector/J 3.1.0 is a [_**Stable**_](../../../mariadb-release-criteria.md) _**(GA)**_ release.

**For an overview of MariaDB Connector/J see the**[**About MariaDB Connector/J**](https://github.com/mariadb-corporation/docs-release-notes/blob/test/kb/en/about-mariadb-connector-j/README.md) **page**

## Performance

Other than features, connector permit significant performance improvements, reaching the same level of performance than c connector

Most significant change are :

* [CONJ-1009](https://jira.mariadb.org/browse/CONJ-1009) improve performance reading big result-set
* [CONJ-1014](https://jira.mariadb.org/browse/CONJ-1014) avoid creating array when receiving server packet
* [CONJ-1015](https://jira.mariadb.org/browse/CONJ-1015) pipelining sent (PREPARE+EXECUTE) are now sent into a single buffer, permitting in some case to have only one TCP-IP packet for 2 mysql packet.

Benchmark using JMH one a single 4 core ubuntu 22.04 server (AWS c5.xlarge) shows :

**simple resultset command : "Select 1"**

```java
@Benchmark
  public int run(MyState state) throws Throwable {
    try (Statement st = state.connectionText.createStatement()) {
      ResultSet rs = st.executeQuery("select 1");
      rs.next();
      return rs.getInt(1);
    }
  }
```

![select1](../../../.gitbook/assets/select1.png)

**Client side prepared statement parsing : "DO 1000 parameters"**

```java
private static final String sql;

  static {
    StringBuilder sb = new StringBuilder("do ?");
    for (int i = 1; i < 1000; i++) {
      sb.append(",?");
    }
    sql = sb.toString();
  }

  @Benchmark
  public int text(MyState state) throws Throwable {
    try (PreparedStatement st = state.connectionText.prepareStatement(sql)) {
      for (int i = 1; i <= 1000; i++) {
        st.setInt(i, i);
      }
      return st.executeUpdate();
    }
  }
```

![do1000params](../../../.gitbook/assets/do1000params.png)

**resultset with lots of columns : ""select 1 row from a 100 int columns"**

```java
@Benchmark
  public int[] text(MyState state) throws Throwable {
    try (PreparedStatement prep = state.connectionText.prepareStatement("select * FROM test100")) {
      ResultSet rs = prep.executeQuery();
      rs.next();
      int[] objs = new int[100];
      for (int i = 0; i < 100; i++) {
        objs[i] = rs.getInt(i + 1);
      }
      return objs;
    }
  }
```

![select100intcols](../../../.gitbook/assets/select100intcols.png)

### UUID Object support

Since MariaDB server 10.7, a new UUID data format is supported.\
getter and setter can now pass java.util.UUID parameter (i.e. PrepareStatement setObject(index, ) / Resultset getObject(index, UUID.class) )

Resultset.getObject without class or type precision will now return UUID object for UUID fields by default

**UUID metadata**

Metadata for UUID fields will now return\
ResultSetMetaData.getColumnTypeName(index) => "uuid"\
ResultSetMetaData.getColumnClassName(index) => "java.util.UUID"\
ResultSetMetaData.getColumnType(index) => Types.OTHER

replacing :

ResultSetMetaData.getColumnTypeName(index) => "CHAR"\
ResultSetMetaData.getColumnClassName(index) => "java.lang.String"\
ResultSetMetaData.getColumnType(index) => Types.CHAR

For compatibility, a new option `uuidAsString` permit to consider UUID as String like previously.

### Other changes

* [CONJ-992](https://jira.mariadb.org/browse/CONJ-992) load balance hosts are now chosen using ROUND ROBIN in place of RANDOM
* [CONJ-1008](https://jira.mariadb.org/browse/CONJ-1008) default value for socket option useReadAheadInput change to false.

## Changelog

For a complete list of changes made in MariaDB Connector/J 3.1.0, with links to detailed\
information on each push, see the [changelog](../changelogs/3.1/mariadb-connector-j-3-1-0-changelog.md).

{% include "https://app.gitbook.com/s/SsmexDFPv2xG2OTyO5yV/~/reusable/pNHZQXPP5OEz2TgvhFva/" %}

{% @marketo/form formid="4316" formId="4316" %}
