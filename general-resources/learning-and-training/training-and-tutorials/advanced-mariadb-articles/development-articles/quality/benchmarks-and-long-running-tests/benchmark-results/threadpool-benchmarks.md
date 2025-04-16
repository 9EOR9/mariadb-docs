
# Threadpool Benchmarks

Here are some benchmarks of some development threadpool code (the [5.5 threadpool](../../../../../../../../server/server-usage/replication-cluster-multi-master/optimization-and-tuning/buffers-caches-and-threads/thread-pool/thread-pool-in-mariadb-51-53.md)).


The benchmarks were run on three machines:


* facebook-maria1 (Linux, 16 cores)
* pitbull (Linux, 24 cores)
* windows (Windows, 8 cores)


Sysbench 0.4 was used to run some "unit" OLTP tests (point-select and
update-nokey), as well as the "classic" OLTP-readonly and OLTP-readwrite. All
tests were run with the number of concurrent clients ranging from 16 to 4096,
with warm cache, with the sysbench table having 1M records.


The results are quite different on all of the machines tested (the machines are
very different, in terms of cores, IO etc), yet threadpool has a positive
effect on all 3 machines, and the positive effect seems to grow with the number
of cores.


Some notes on how the benchmarks were run:


1. The benchmark client and server used different CPUs - ('taskset'
 (Linux), or 'start /affinity' (Windows) were used to run the benchmark client
 on `#CPUs/4`, the rest of CPUs were used by the server). On
 the Linux boxes, `--thread_pool_size=<N>` (where N is number
 of cores dedicated to the server) was used.
1. `innodb_flush_log_at_trx_commit=0` and `innodb_flush_method=ALL_O_DIRECT`
 was used to avoid extensive fsyncing, which is ok for the purposes of the
 testing for this.
1. Every "write" benchmark (`oltp_rw` and `update_nokey`) started with a new
 server (i.e. kill mysqld, remove innodb files, and restart mysqld for each
 test). Every "read" benchmark, on the other hand, reused the same running
 server instance. Starting afresh with a new server on write benchmarks is
 done mainly to eliminate the effects of the purge lag.
1. The results are in queries-per-second (QPS).


## OLTP_RO


### OLTP_RO facebook-maria1



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 3944 | 4725 | 4878 | 4863 | 4732 | 4554 | 4345 | 4103 | 1670 |
| threadpool | 3822 | 4955 | 4991 | 5017 | 4908 | 4716 | 4610 | 4307 | 2962 |



![oltp-ro-facebook-maria1](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/oltp-ro-facebook-maria1.png "oltp-ro-facebook-maria1")


### OLTP_RO pitbull



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 6754 | 7905 | 8152 | 7948 | 7924 | 7587 | 5313 | 3827 | 208 |
| threadpool | 6566 | 7725 | 8108 | 8079 | 7976 | 7793 | 7429 | 6523 | 4456 |



![oltp_ro-pitbull](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/oltp_ro-pitbull.png "oltp_ro-pitbull")


### OLTP_RO Windows



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 1822 | 1831 | 1825 | 1829 | 1816 | 1879 | 1866 | 1783 | 987 |
| threadpool | 2019 | 2049 | 2024 | 1992 | 1924 | 1897 | 1855 | 1825 | 1403 |



![oltp_ro-windows](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/oltp_ro-windows.png "oltp_ro-windows")


## OLTP_RW


### OLTP_RW facebook-maria1



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 2833 | 3510 | 3545 | 3420 | 3259 | 2818 | 1788 | 820 | 113 |
| threadpool | 3163 | 3590 | 3498 | 3459 | 3354 | 3117 | 2190 | 1064 | 506 |



![oltp_rw-facebook-maria1](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/oltp_rw-facebook-maria1.png "oltp_rw-facebook-maria1")


### OLTP_RW pitbull



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 4561 | 5316 | 5332 | 3512 | 2874 | 2476 | 1380 | 265 | 53 |
| threadpool | 4504 | 5382 | 5694 | 5567 | 5302 | 4514 | 2548 | 1186 | 484 |



![oltp_rw-pitbull](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/oltp_rw-pitbull.png "oltp_rw-pitbull")


### OLTP_RW Windows



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 1480 | 1498 | 1472 | 1477 | 1456 | 1371 | 731 | 328 | 82 |
| threadpool | 1449 | 1523 | 1527 | 1492 | 1443 | 1409 | 1365 | 1240 | 862 |



![oltp_rw-windows](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/oltp_rw-windows.png "oltp_rw-windows")


## POINT_SELECT


### POINT_SELECT facebook-maria1



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 91322 | 113116 | 115418 | 114484 | 111169 | 104612 | 26902 | 12843 | 5038 |
| threadpool | 100359 | 115618 | 118115 | 120136 | 119165 | 113931 | 110787 | 109970 | 104985 |



![point_select-facebook-maria1](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/point_select-facebook-maria1.png "point_select-facebook-maria1")


### POINT_SELECT pitbull



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 148673 | 161547 | 169747 | 172083 | 69036 | 42041 | 21775 | 4368 | 282 |
| threadpool | 143222 | 167069 | 167270 | 165977 | 164983 | 158410 | 148690 | 147107 | 143934 |



![point_select-pitbull](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/point_select-pitbull.png "point_select-pitbull")


### POINT_SELECT Windows



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 39734 | 42885 | 44448 | 44478 | 41720 | 38196 | 36844 | 35404 | 23306 |
| threadpool | 42143 | 45679 | 47066 | 47753 | 46720 | 44215 | 43677 | 43093 | 44364 |



![point_select-windows](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/point_select-windows.png "point_select-windows")


## UPDATE_NOKEY


### UPDATE_NOKEY facebook-maria1



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 60165 | 65761 | 67727 | 57232 | 47612 | 26341 | 8981 | 3265 | 389 |
| threadpool | 65092 | 68683 | 67053 | 64141 | 64815 | 63047 | 63346 | 63638 | 62843 |



![update_nokey-facebook-maria1](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/update_nokey-facebook-maria1.png "update_nokey-facebook-maria1")


### UPDATE_NOKEY pitbull



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 65213 | 71680 | 19418 | 13008 | 11155 | 8742 | 5645 | 635 | 332 |
| threadpool | 64902 | 70236 | 70037 | 68926 | 69930 | 69929 | 67099 | 62376 | 17766 |



![update_nokey-pitbull](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/update_nokey-pitbull.png "update_nokey-pitbull")


### UPDATE_NOKEY Windows



| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 | thread per connection | threadpool |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| concurrent clients | 16 | 32 | 64 | 128 | 256 | 512 | 1024 | 2048 | 4096 |
| thread per connection | 24790 | 25634 | 25639 | 25309 | 24754 | 19420 | 5249 | 2361 | 824 |
| threadpool | 25251 | 25259 | 25406 | 25327 | 24850 | 23818 | 23137 | 23003 | 22047 |



![update_nokey-windows](../../../../../../../.gitbook/assets/threadpool-benchmarks/+image/update_nokey-windows.png "update_nokey-windows")

