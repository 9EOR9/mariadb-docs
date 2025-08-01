# MaxScale 21.06 Database Firewall filter

This filter is deprecated in MariaDB MaxScale 6 and will be removed in MaxScale 22.08.

* [Database Firewall filter](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#database-firewall-filter)
  * [Overview](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#overview)
  * [Configuration](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#configuration)
    * [Filter Parameters](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#filter-parameters)
      * [rules](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#rules)
      * [action](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#action)
      * [log\_match](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#log_match)
      * [log\_no\_match](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#log_no_match)
      * [treat\_string\_as\_field](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#treat_string_as_field)
      * [treat\_string\_arg\_as\_field](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#treat_string_arg_as_field)
      * [strict](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#strict)
  * [Rule syntax](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#rule-syntax)
    * [Mandatory rule parameters](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#mandatory-rule-parameters)
      * [wildcard](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#wildcard)
        * [Example](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#example)
      * [columns](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#columns)
        * [Example](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#example_1)
      * [function](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#function)
        * [Example](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#example_2)
      * [not\_function](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#not_function)
      * [Example](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#example_3)
      * [uses\_function](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#uses_function)
        * [Example](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#example_4)
      * [function and columns](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#function-and-columns)
        * [Example](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#example_5)
      * [not\_function and columns](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#not_function-and-columns)
        * [Example](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#example_6)
      * [regex](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#regex)
        * [Example](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#example_7)
      * [limit\_queries](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#limit_queries)
        * [Example](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#example_8)
      * [no\_where\_clause](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#no_where_clause)
        * [Example](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#example_9)
    * [Optional rule parameters](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#optional-rule-parameters)
      * [at\_times](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#at_times)
      * [on\_queries](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#on_queries)
    * [Applying rules to users](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#applying-rules-to-users)
  * [Module commands](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#module-commands)
    * [rules/reload FILTER \[FILE\]](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#rulesreload-filter-file)
    * [rules FILTER](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#rules-filter)
  * [Use Cases](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#use-cases)
    * [Use Case 1 - Prevent rapid execution of specific queries](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#use-case-1-prevent-rapid-execution-of-specific-queries)
    * [Use Case 2 - Only allow deletes with a where clause](mariadb-maxscale-2106-maxscale-2106-database-firewall-filter.md#use-case-2-only-allow-deletes-with-a-where-clause)

### Overview

The Database Firewall filter is used to block queries that match a set of\
rules. It can be used to prevent harmful queries from reaching the backend\
database instances or to limit access to the database based on a more flexible\
set of rules compared to the traditional GRANT-based privilege system. Currently\
the filter does not support multi-statements.

Note that the firewall filter should be viewed as a best-effort solution\
intended for protecting against accidental misuse rather than malicious\
attacks.

### Configuration

The Database Firewall filter only requires minimal configuration in the\
maxscale.cnf file. The actual rules of the Database Firewall filter are located\
in a separate text file. The following is an example of a Database Firewall\
filter configuration in maxscale.cnf.

```
[DatabaseFirewall]
type=filter
module=dbfwfilter
rules=/home/user/rules.txt

[Firewalled-Routing-Service]
type=service
router=readconnroute
servers=server1
user=myuser
password=mypasswd
filters=DatabaseFirewall
```

#### Filter Parameters

The Database Firewall filter has one mandatory parameter, `rules`.

**`rules`**

A path to a file with the rule definitions in it. The file should be readable by\
the user MariaDB MaxScale is run with. If a relative path is given, the path is\
interpreted relative to the module configuration directory. The default module\
configuration directory is _/etc/maxscale.modules.d_.

**`action`**

This parameter is optional and determines what action is taken when a query\
matches a rule. The value can be either `allow`, which allows all matching\
queries to proceed but blocks those that don't match, or `block`, which blocks\
all matching queries, or `ignore` which allows all queries to proceed.

The following statement types will always be allowed through when `action` is\
set to `allow`:

* COM\_CHANGE\_USER: The user is changed for an active connection
* COM\_FIELD\_LIST: Alias for the `SHOW TABLES;` query
* COM\_INIT\_DB: Alias for `USE <db>;`
* COM\_PING: Server is pinged
* COM\_PROCESS\_INFO: Alias for `SHOW PROCESSLIST;`
* COM\_PROCESS\_KILL: Alias for `KILL <id>;` query
* COM\_QUIT: Client closes connection
* COM\_SET\_OPTION: Client multi-statements are being configured

You can have both blacklist and whitelist functionality by configuring one\
filter with `action=allow` and another one with `action=block`. You can then use\
different rule files with each filter, one for blacklisting and another one for\
whitelisting. After this you only have to add both of these filters to a service\
in the following way.

```
[my-firewall-service]
type=service
servers=server1
router=readconnroute
user=maxuser
password=maxpwd
filters=dbfw-whitelist|dbfw-blacklist

[dbfw-whitelist]
type=filter
module=dbfwfilter
action=allow
rules=/home/user/whitelist-rules.txt

[dbfw-blacklist]
type=filter
module=dbfwfilter
action=block
rules=/home/user/blacklist-rules.txt
```

If a query is blocked, the filter will return an error to the client with the\
error number 1141 and an SQL state of HY000.

**`log_match`**

Log all queries that match a rule. For the `any` matching mode, the name of the\
rule that matched is logged and for other matching modes, the name of the last\
matching rule is logged. In addition to the rule name the matched user and the\
query itself is logged. The log messages are logged at the notice level.

**`log_no_match`**

Log all queries that do not match a rule. The matched user and the query is\
logged. The log messages are logged at the notice level.

**`treat_string_as_field`**

This optional parameter specifies how the database firewall should treat\
strings. If true, they will be handled as fields, which will cause column\
blocking rules to match even if `ANSI_QUOTES` has been enabled and `"` is\
used instead of backtick.

```
treat_string_as_field=false
```

The default value is `true`.

Note that this may cause a false positive, if a "true" string contains the\
name of a column to be blocked.

**`treat_string_arg_as_field`**

This optional parameter specifies how the database firewall should treat\
strings used as arguments to functions. If true, they will be handled\
as fields, which will cause function column blocking rules to match even\
even if `ANSI_QUOTES` has been enabled and `"` is used instead of backtick.

```
treat_string_arg_as_field=false
```

The default value is `true`.

Note that this may cause a false positive, if a "true" string contains the\
name of a column to be blocked.

**`strict`**

Whether to treat unsupported SQL or multi-statement SQL as an error. This is a\
boolean parameter and the default value is `true`.

When disabled, SQL that cannot be fully parsed is allowed to pass if the rules\
do not cause it to be blocked. This can be used to provide a best-effort mode\
where uncertainly about the SQL is allowed.

### Rule syntax

The rules are defined by using the following syntax:

```
rule NAME match RULE [at_times VALUE...] [on_queries {select|update|insert|delete|grant|revoke|drop|create|alter|use|load}]
```

Where _NAME_ is the identifier for this rule and _RULE_ is the mandatory rule definition.

Rules are identified by their name and have mandatory parts and optional parts.\
You can add comments to the rule files by adding the `#` character at\
the beginning of the line. Trailing comments are not supported.

The first step of defining a rule is to start with the keyword `rule` which\
identifies this line of text as a rule. The second token is identified as\
the name of the rule. After that the mandatory token `match` is required\
to mark the start of the actual rule definition.

The rule definition must contain exactly one mandatory rule parameter. It can\
also contain one of each type of optional rule parameter.

#### Mandatory rule parameters

The Database Firewall filter's rules expect a single mandatory parameter for a\
rule. You can define multiple rules to cover situations where you would like to\
apply multiple mandatory rules to a query.

**`wildcard`**

This rule blocks all queries that use the wildcard character `*`.

**Example**

Use of the wildcard is not allowed:

```
rule examplerule match wildcard
```

**`columns`**

This rule expects a list of values after the `columns` keyword. These values are\
interpreted as column names and if a query targets any of these, it is matched.

**Example**

Deny name and salary columns:

```
rule examplerule match columns name salary
```

**`function`**

This rule expects a list of values after the `function` keyword. These values\
are interpreted as function names and if a query uses any of these, it is\
matched. The symbolic comparison operators (`<`, `>`, `>=` etc.) are also\
considered functions whereas the text versions (`NOT`, `IS`, `IS NOT` etc.) are\
not considered functions.

**Example**

Match queries using the _sum_ and _count_ functions:

```
rule examplerule match function sum count
```

**`not_function`**

This rule expects a list of values after the `not_function` keyword. These values\
are interpreted as function names and if a query uses any function other than these,\
it is matched. The symbolic comparison operators (`<`, `>`, `>=` etc.) are also\
considered functions whereas the text versions (`NOT`, `IS`, `IS NOT` etc.) are\
not considered functions.

If the rule is given no values, then the rule will match a query using any function.

**Example**

Match queries using other functions but the _length_ function:

```
rule examplerule match not_function length
```

Match queries using functions:

```
rule examplerule match not_function
```

**`uses_function`**

This rule expects a list of column names after the keyword. If any of the\
columns are used with a function, the rule will match. This rule can be\
used to prevent the use of a column with a function.

**Example**

Deny function usage with _name_ and _address_ columns:

```
rule examplerule match uses_function name address
```

**`function` and `columns`**

This rule combines the `function` and `columns` type rules to match if one\
of the listed columns uses one of the listed functions. The rule expects\
the `function` and `columns` keywords both followed by a list of values.

**Example**

Deny use of the _sum_ function with _name_ or _address_ columns:

```
rule examplerule match function sum columns name address
```

**`not_function` and `columns`**

This rule combines the `not_function` and `columns` type rules to match if\
one of the listed columns is used in conjunction with functions other than\
the listed ones. The rule expects the `not_function` and `columns` keywords\
both followed by a list of values.

If `not_function` is not provided with a list of values, then the rule\
matches if any of the columns is used with any function.

**Example**

Match if any other function but _length_ is used with the _name_ or _address_\
columns:

```
rule examplerule match not_function length columns name address
```

Match if any function is used with the \_ssn\_column:

```
rule examplerule match not_function columns ssn
```

**`regex`**

This rule blocks all queries matching the regular expression. The regex string expects a\
PCRE2 syntax regular expression. For more information about PCRE2 syntax, read the[PCRE2 documentation](https://www.pcre.org/current/doc/html/pcre2syntax.html). Unlike\
typical MaxScale regex parameters, the value should be enclosed in single or double\
quotes, not in `/.../`. Any compilation options must be included in the pattern itself.

**Example**

Block selects to accounts:

```
rule examplerule match regex '.*select.*from.*accounts.*'
```

**`limit_queries`**

This rule has been DEPRECATED. Please use the Throttle Filter instead.

The limit\_queries rule expects three parameters. The first parameter is the\
number of allowed queries during the time period. The second is the time period\
in seconds and the third is the amount of time in seconds for which the rule is\
considered active and blocking.

**WARNING:** Using `limit_queries` in `action=allow` is not supported.

**Example**

Over 50 queries within a window of 5 seconds will block for 100 seconds:

```
rule examplerule match limit_queries 50 5 100
```

**`no_where_clause`**

This rule inspects the query and blocks it if it has no WHERE clause. For\
example, this would disallow a `DELETE FROM ...` query without a `WHERE`\
clause. This does not prevent wrongful usage of the `WHERE` clause e.g. `DELETE FROM ... WHERE 1=1`.

**Example**

Queries must have a where clause:

```
rule examplerule match no_where_clause
```

#### Optional rule parameters

Each mandatory rule accepts one or more optional parameters. These are to be\
defined after the mandatory part of the rule.

**`at_times`**

This rule expects a list of time ranges that define the times when the rule in\
question is active. The time formats are expected to be ISO-8601 compliant and\
to be separated by a single dash (the - character). For example, to define the\
active period of a rule to be 5pm to 7pm, you would include `at times 17:00:00-19:00:00` in the rule definition. The rule uses local time to check if\
the rule is active and has a precision of one second.

**`on_queries`**

This limits the rule to be active only on certain types of queries. The possible\
values are:

| Keyword | Matching operations   |
| ------- | --------------------- |
| select  | SELECT statements     |
| insert  | INSERT statements     |
| update  | UPDATE statements     |
| delete  | DELETE statements     |
| grant   | All grant operations  |
| revoke  | All revoke operations |
| create  | All create operations |
| alter   | All alter operations  |
| drop    | All drop operations   |
| use     | USE operations        |
| load    | LOAD DATA operations  |

Multiple values can be combined using the pipe character `|` e.g.`on_queries select|insert|update`.

#### Applying rules to users

The `users` directive defines the users to which the rule should be applied.

`users NAME... match { any | all | strict_all } rules RULE...`

The first keyword is `users`, which identifies this line as a user definition\
line.

The second component is a list of user names and network addresses in the forma&#x74;_`user`_`@`_`0.0.0.0`_. The first part is the user name and the second part is\
the network address. You can use the `%` character as the wildcard to enable\
user name matching from any address or network matching for all users. After the\
list of users and networks the keyword match is expected. This means that the\
following user definitions are supported:

* `user@host`
* `user@%`
* `%@host`

Partial wildcards, e.g. `user@192.%` are not supported.

As MaxScale listens to the IPv6 all address by default, IPv4 addresses will be\
mapped into the IPv6 space. This means that the IPv4 address `192.168.0.1` will\
show up in MaxScale as `::ffff:192.168.0.1`. Take this into account when\
defining the `users` directives.

After this either the keyword `any`, `all` or `strict_all` is expected. This\
defined how the rules are matched. If `any` is used when the first rule is\
matched the query is considered as matched and the rest of the rules are\
skipped. If instead the `all` keyword is used all rules must match for the query\
to be considered as matched. The `strict_all` is the same as `all` but it checks the rules\
from left to right in the order they were listed. If one of these does not\
match, the rest of the rules are not checked. This could be useful in situations\
where you would for example combine `limit_queries` and `regex` rules. By using`strict_all` you can have the `regex` rule first and the `limit_queries` rule\
second. This way the rule only matches if the `regex` rule matches enough times\
for the `limit_queries` rule to match.

After the matching part comes the rules keyword after which a list of rule names\
is expected. This allows reusing of the rules and enables varying levels of\
query restriction.

If a particular _NAME_ appears on several `users` lines, then when an\
actual user matches that name, the rules of each line are checked\
independently until there is a match for the statement in question. That\
is, the rules of each `users` line are treated in an _OR_ fashion with\
respect to each other.

### Module commands

Read [Module Commands](../mariadb-maxscale-21-06-reference/mariadb-maxscale-2106-maxscale-2106-module-commands.md) documentation for\
details about module commands.

The dbfwfilter supports the following module commands.

#### `rules/reload FILTER [FILE]`

Load a new rule file or reload the current rules. New rules are only taken into\
use if they are successfully loaded and in cases where loading of the rules\
fail, the old rules remain in use. The _FILTER_ parameter is the filter instance\
whose rules are reloaded. The _FILE_ argument is an optional path to a rule file\
and if it is not defined, the current rule file is used.

#### `rules FILTER`

Shows the current statistics of the rules. The _FILTER_ parameter is the filter\
instance to inspect.

### Use Cases

#### Use Case 1 - Prevent rapid execution of specific queries

To prevent the excessive use of a database we want to set a limit on the rate of\
queries. We only want to apply this limit to certain queries that cause unwanted\
behaviour. To achieve this we can use a regular expression.

First we define the limit on the rate of queries. The first parameter for the\
rule sets the number of allowed queries to 10 queries and the second parameter\
sets the rate of sampling to 5 seconds. If a user executes queries faster than\
this, any further queries that match the regular expression are blocked for 60\
seconds.

```
rule limit_rate_of_queries match limit_queries 10 5 60
rule query_regex match regex '.*select.*from.*user_data.*'
```

To apply these rules we combine them into a single rule by adding a `users` line\
to the rule file.

```
users %@% match all rules limit_rate_of_queries query_regex
```

#### Use Case 2 - Only allow deletes with a where clause

We have a table which contains all the managers of a company. We want to prevent\
accidental deletes into this table where the where clause is missing. This poses\
a problem, we don't want to require all the delete queries to have a where\
clause. We only want to prevent the data in the managers table from being\
deleted without a where clause.

To achieve this, we need two rules. The first rule defines that all delete\
operations must have a where clause. This rule alone does us no good so we need\
a second one. The second rule blocks all queries that match a regular\
expression.

```
rule safe_delete match no_where_clause on_queries delete
rule managers_table match regex '.*from.*managers.*'
```

When we combine these two rules we get the result we want. To combine these two\
rules add the following line to the rule file.

```
users %@% match all rules safe_delete managers_table
```

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
