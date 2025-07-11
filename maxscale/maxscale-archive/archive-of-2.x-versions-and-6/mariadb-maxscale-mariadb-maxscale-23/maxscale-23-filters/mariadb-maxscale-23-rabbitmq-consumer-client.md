# RabbitMQ Consumer Client

### Overview

This utility tool is used to read messages from a RabbitMQ broker sent by the[RabbitMQ Filter](mariadb-maxscale-23-rabbitmq-filter.md) and forward these messages into an\
SQL database as queries.

### Command Line Arguments

The **RabbitMQ Consumer Client** only has one command line argument.

| Command | Argument                                             |
| ------- | ---------------------------------------------------- |
| Command | Argument                                             |
| -c      | Path to the folder containing the configuration file |

### Installation

To install the RabbitMQ Consumer Client you can either use the provided packages\
or you can compile it from source code. The source code is included as a part of the\
MariaDB MaxScale source code and can be found in the `rabbitmq_consumer` folder.

### Building from source

This program requires the librabbitmq and libmysqlclient libraries.

* [librabbitmq-c](https://github.com/alanxz/rabbitmq-c)
* [MariaDB Client Library for C 2.0 Series](https://app.gitbook.com/s/CjGYMsT2MVP4nd3IyW2L/mariadb-connector-c)

Building with CMake:

```
cmake .
```

Variables to pass for CMake:

Path to headers -DCMAKE\_INCLUDE\_PATH=\
Path to libraries -DCMAKE\_LIBRARY\_PATH=\
Install prefix -DCMAKE\_INSTALL\_PREFIX=

Separate multiple folders with colons, for example:

```
path1:path2:path3
```

After running CMake run `make` to build the binaries and `make package` to build RPMs.

To build without CMake, use the provided makefile and update the\
include and library directories 'in buildvars.inc'

### Configuration

The consumer client requires that the `consumer.cnf` configuration file is either\
be present in the `etc` folder of the installation directory or in the folder\
specified by the `-c` argument.

The source broker, the destination database and the message log file can be\
configured into the separate `consumer.cnf` file.

| Option   | Description                                  |
| -------- | -------------------------------------------- |
| Option   | Description                                  |
| hostname | Hostname of the RabbitMQ server              |
| port     | Port of the RabbitMQ server                  |
| vhost    | Virtual host location of the RabbitMQ server |
| user     | Username for the RabbitMQ server             |
| passwd   | Password for the RabbitMQ server             |
| queue    | Queue to consume from                        |
| dbserver | Hostname of the SQL server                   |
| dbport   | Port of the SQL server                       |
| dbname   | Name of the SQL database to use              |
| dbuser   | Database username                            |
| dbpasswd | Database password                            |
| logfile  | Message log filename                         |

<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>

{% @marketo/form formId="4316" %}
