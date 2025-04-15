
# 4-Semi-Sync Replication

[Regular MariaDB replication](../../../../../server-usage/replication-cluster-multi-master/standard-replication/README.md) is asynchronous.
MariaDB, since [MariaDB 5.5](../../../../../../release-notes/mariadb-community-server/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5.md), has included [semisynchronous replication](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/semisynchronous-replication-plugin-status-variables.md) semi-synchronous Binlog Event.


### Event Header Changes


If the user variable `<code>@rpl_semi_sync_slave</code>` is set, 2 exta bytes are added after the status byte of a [binlog network stream](3-binlog-network-stream.md) and before the normal binlog event header.



* [uint<1>](../protocol-data-types.md#fixed-length-integers) semi-sync indicator, always 0xef
* [uint<1>](../protocol-data-types.md#fixed-length-integers) semi-sync flags, either 0x00 (no ACK) or 0x01 (ACK)



**Note** : The packet size, as in the network protocol header, is then: `<code>event_size + 1 byte status + 2 bytes semi-sync replication</code>`.


The MariaDB server sets the user variable whenever it is starting replication. For MariaDB Connector/C , the following query must be executed before the call to `<code>mariadb_rpl_open()</code>` is made to enable semi-sync replication.


```
SET @rpl_semi_sync_slave=1
```

If the semi-sync flag is set to 0x01, the master waits for a Semi Sync ACK packet from the slave and when the Semi Sync ACK is seen, the master acknowledges the client which has issued the transaction with a standard OK_Packet or a ERR_Packet.


The master can then write the transaction to the binary log and send the next events to the slave.


**Note** : The master only requests Semi Sync ACKs if [rpl_semi_sync_master_enabled](../../../../../server-usage/replication-cluster-multi-master/optimization-and-tuning/system-variables/semisynchronous-replication-plugin-status-variables.md#rpl_semi_sync_master_enabled) is enabled. If it is not enabled, the semi-sync flag will always be 0x00.


#### Semi Sync ACK Details


This event is sent by the slave **only if** the semi-sync flag is set to 0x01.



* [uint<1>](../protocol-data-types.md#fixed-length-integers) semi-sync indicator, always 0xef
* [uint<8>](../protocol-data-types.md#fixed-length-integers) the next position of received event
* [string<EOF>](../protocol-data-types.md#fixed-length-integers) binlog file name.



**Note**: this packet sent by the slave never includes the CRC32.


Sending an ACK when the semi-sync flag is set to 0x0 will cause an error and the connection is closed.


#### Example of Heartbeat Event With Semi-Sync Protocol and CRC32


We can clearly see:


* 2a 00 00 [3 bytes] packet size:
* 06 [1] sequence
* 00 [1] status byte = 00 => OK
* ef 00 [2] bytes => semi sync indicator (0xef) and semi-sync flag (00)


the ef 00 2 bytes after the OK byte 00


```
T 127.0.0.1:23240 -> 127.0.0.1:41054 [AP]
  2a 00 00 06 00 ef 00 00    00 00 00 1b d9 27 00 00    *............'..
  27 00 00 00 79 04 00 00    00 00 6d 79 73 71 6c 2d    '...y.....mysql-
  62 69 6e 2e 30 30 30 30    33 34 ed ef e1 f0          bin.000034....
```


#### Example of XID_EVENT, With CRC32


The master sets the Semi-Sync ACK request in the XID_EVENT event:


We see the 2 semi sync bytes: **ef** and **01**.
The latter, being 1, means the slave server must send the Semi Sync ACK packet.


We also see in the binlog event header:


* Event Type [1] = 10 XID_EVENT
* Next Event pos [4] = 4a 05 00 00 => 1354


```
22 00 00 0c 00 ef 01 17  d0 37 5a 17 d0 37 5a 10  "............7Z.
d9 27 00 00 1f 00 00 00  4a 05 00 00 00 00 6f 00  .?......J.....o.
00 00 00 00 00 00 44 30  aa fc                    ......D0..
```


#### Example of Semi-Sync ACK


This is sent by the slave server after the XID_EVENT receiving.


We see:


* the semi sync indicator [1] = 0xef, sent before anything else
* the Next Event position [8] = 4a 05 00 00 00 00 00 00 => 1354
which is the next position of the XID_EVENT above
* the binlog filename = mysql-bin.000034


Please note:


* there is no terminating CRC32
* the packet sequence now start starts from 0


```
19 00 00 00 ef 4a 05 00    00 00 00 00 00 6d 79 73    .....J.......mys
  71 6c 2d 62 69 6e 2e 30    30 30 30 33 34             ql-bin.000034
```

