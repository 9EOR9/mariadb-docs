# RAND_EVENT

The SQL function [RAND()](rand_event.md) generates a random number.

A RAND_EVENT contains two seed values that set the [rand_seed1](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#rand_seed1) and [rand_seed2](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/server-system-variables.md#rand_seed2) system variables that are used to compute the random number.

**Note**: it is written only before a QUERY_EVENT and is not used with row-based logging.

#

### Header

* Event Type is 13 (0x0d)

#

### Fields

* [uint<8>](../protocol-data-types.md#fixed-length-integers) The value for the first seed
* [uint<8>](../protocol-data-types.md#fixed-length-integers) The value for the second seed

#

### Example From mysqlbinlog Utility, No CRC32

```
# at 389

#171206 13:46:56 server id 10116 end_log_pos 424 	Rand
SET @@RAND_SEED1=685157301, @@RAND_SEED2=758850369/*!*/;
# at 424

```

#

### Example Event As It's Written In The Binlog File

`
c0 e6 27 5a 0d 84 27 00 00 23 00 00 00 a8 01 00 ..'Z..'..#......
00 00 00 b5 ab d6 28 00 00 00 00 41 23 3b 2d 00 ......(.........
00 00 00 ....
`