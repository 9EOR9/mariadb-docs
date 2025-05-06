
# 10.1.26 Release Upgrade Tests


## Upgrade from 10.0


### Tested revision


535910ae5f20e36405631030e9c0eb22fe40a7c4


### Test date


2017-08-09 14:16:17


### Summary (PASS)


All tests passed


### Details



| # | type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| # | type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| 1 | crash | 4 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 2 | crash | 4 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 3 | crash | 4 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 4 | crash | 4 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 5 | crash | 8 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 6 | crash | 8 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 7 | crash | 8 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 8 | crash | 8 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 9 | crash | 16 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 10 | crash | 16 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 11 | crash | 16 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 12 | crash | 16 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 13 | normal | 4 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 14 | normal | 4 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 15 | normal | 4 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 16 | normal | 4 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 17 | normal | 8 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 18 | normal | 8 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 19 | normal | 8 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 20 | normal | 8 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 21 | normal | 16 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 22 | normal | 16 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 23 | normal | 16 | 10.0.28 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 24 | normal | 16 | 10.0.28 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |



## Upgrade from 10.1


### Tested revision


535910ae5f20e36405631030e9c0eb22fe40a7c4


### Test date


2017-08-09 15:06:34


### Summary (FAIL)


[MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112), [MDEV-13165](https://jira.mariadb.org/browse/MDEV-13165)


### Details



| # | type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| # | type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| 1 | crash | 64 | 10.1.20 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 2 | crash | 64 | 10.1.20 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 3 | crash | 64 | 10.1.20 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(49) |
| 4 | crash | 64 | 10.1.20 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 5 | crash | 64 | 10.1.20 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 6 | crash | 64 | 10.1.20 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 7 | crash | 64 | 10.1.20 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 8 | crash | 64 | 10.1.20 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 9 | crash | 8 | 10.1.20 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 10 | crash | 8 | 10.1.20 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 11 | crash | 8 | 10.1.20 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 12 | crash | 8 | 10.1.20 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(14) |
| 13 | crash | 8 | 10.1.20 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 14 | crash | 8 | 10.1.20 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 15 | crash | 8 | 10.1.20 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 16 | crash | 8 | 10.1.20 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 17 | crash | 16 | 10.1.20 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 18 | crash | 16 | 10.1.20 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 19 | crash | 16 | 10.1.20 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(37) |
| 20 | crash | 16 | 10.1.20 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 21 | crash | 16 | 10.1.20 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 22 | crash | 16 | 10.1.20 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 23 | crash | 16 | 10.1.20 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 24 | crash | 16 | 10.1.20 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 25 | crash | 32 | 10.1.20 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 26 | crash | 32 | 10.1.20 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 27 | crash | 32 | 10.1.20 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 28 | crash | 32 | 10.1.20 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 29 | crash | 32 | 10.1.20 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(29) |
| 30 | crash | 32 | 10.1.20 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 31 | crash | 32 | 10.1.20 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 32 | crash | 32 | 10.1.20 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 33 | crash | 4 | 10.1.20 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(43) |
| 34 | crash | 4 | 10.1.20 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 35 | crash | 4 | 10.1.20 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | FAIL | UPGRADE_FAILURE [MDEV-13165](https://jira.mariadb.org/browse/MDEV-13165) |
| 36 | crash | 4 | 10.1.20 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 37 | crash | 4 | 10.1.20 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 38 | crash | 4 | 10.1.20 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 39 | crash | 4 | 10.1.20 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 40 | crash | 4 | 10.1.20 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 41 | normal | 8 | 10.1.20 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 42 | normal | 8 | 10.1.20 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 43 | normal | 8 | 10.1.20 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 44 | normal | 8 | 10.1.20 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 45 | normal | 8 | 10.1.20 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 46 | normal | 8 | 10.1.20 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 47 | normal | 8 | 10.1.20 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| 48 | normal | 8 | 10.1.20 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 49 | normal | 64 | 10.1.20 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 50 | normal | 64 | 10.1.20 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| 51 | normal | 64 | 10.1.20 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 52 | normal | 64 | 10.1.20 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 53 | normal | 64 | 10.1.20 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 54 | normal | 64 | 10.1.20 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 55 | normal | 64 | 10.1.20 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 56 | normal | 64 | 10.1.20 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 57 | normal | 32 | 10.1.20 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 58 | normal | 32 | 10.1.20 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| 59 | normal | 32 | 10.1.20 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 60 | normal | 32 | 10.1.20 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 61 | normal | 32 | 10.1.20 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 62 | normal | 32 | 10.1.20 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 63 | normal | 32 | 10.1.20 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 64 | normal | 32 | 10.1.20 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 65 | normal | 16 | 10.1.20 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 66 | normal | 16 | 10.1.20 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| 67 | normal | 16 | 10.1.20 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 68 | normal | 16 | 10.1.20 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 69 | normal | 16 | 10.1.20 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 70 | normal | 16 | 10.1.20 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 71 | normal | 16 | 10.1.20 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 72 | normal | 16 | 10.1.20 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 73 | normal | 4 | 10.1.20 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 74 | normal | 4 | 10.1.20 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 75 | normal | 4 | 10.1.20 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 76 | normal | 4 | 10.1.20 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 77 | normal | 4 | 10.1.20 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 78 | normal | 4 | 10.1.20 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| 79 | normal | 4 | 10.1.20 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 80 | normal | 4 | 10.1.20 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |



## Upgrade from MySQL 5.6


### Tested revision


535910ae5f20e36405631030e9c0eb22fe40a7c4


### Test date


2017-08-09 18:24:38


### Summary (PASS)


All tests passed


### Details



| # | type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| # | type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| 1 | normal | 16 | 5.6.35 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 2 | normal | 16 | 5.6.35 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 3 | normal | 16 | 5.6.35 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 4 | normal | 16 | 5.6.35 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 5 | normal | 4 | 5.6.35 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 6 | normal | 4 | 5.6.35 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 7 | normal | 4 | 5.6.35 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 8 | normal | 4 | 5.6.35 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 9 | normal | 8 | 5.6.35 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 10 | normal | 8 | 5.6.35 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 11 | normal | 8 | 5.6.35 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 12 | normal | 8 | 5.6.35 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |



## Crash Recovery


### Tested revision


535910ae5f20e36405631030e9c0eb22fe40a7c4


### Test date


2017-08-09 18:52:03


### Summary (FAIL)


[MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)


### Details



| # | type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| # | type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| 1 | crash | 16 | 10.1.26 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 2 | crash | 16 | 10.1.26 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 3 | crash | 16 | 10.1.26 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 4 | crash | 16 | 10.1.26 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 5 | crash | 16 | 10.1.26 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 6 | crash | 16 | 10.1.26 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(54) |
| 7 | crash | 16 | 10.1.26 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 8 | crash | 16 | 10.1.26 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 9 | crash | 4 | 10.1.26 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 10 | crash | 4 | 10.1.26 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 11 | crash | 4 | 10.1.26 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 12 | crash | 4 | 10.1.26 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 13 | crash | 4 | 10.1.26 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(48) |
| 14 | crash | 4 | 10.1.26 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 15 | crash | 4 | 10.1.26 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 16 | crash | 4 | 10.1.26 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 17 | crash | 32 | 10.1.26 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 18 | crash | 32 | 10.1.26 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(16) |
| 19 | crash | 32 | 10.1.26 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 20 | crash | 32 | 10.1.26 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 21 | crash | 32 | 10.1.26 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 22 | crash | 32 | 10.1.26 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 23 | crash | 32 | 10.1.26 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 24 | crash | 32 | 10.1.26 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 25 | crash | 64 | 10.1.26 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |
| 26 | crash | 64 | 10.1.26 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 27 | crash | 64 | 10.1.26 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 28 | crash | 64 | 10.1.26 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 29 | crash | 64 | 10.1.26 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(21) |
| 30 | crash | 64 | 10.1.26 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 31 | crash | 64 | 10.1.26 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 32 | crash | 64 | 10.1.26 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 33 | crash | 8 | 10.1.26 (inbuilt) | Barracuda | on | zlib | => | 10.1.26 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(18) |
| 34 | crash | 8 | 10.1.26 (inbuilt) | Antelope | on | zlib | => | 10.1.26 (inbuilt) | Antelope | on | zlib | - | OK |  |
| 35 | crash | 8 | 10.1.26 (inbuilt) | Antelope | - | zlib | => | 10.1.26 (inbuilt) | Antelope | - | zlib | - | OK |  |
| 36 | crash | 8 | 10.1.26 (inbuilt) | Barracuda | - | zlib | => | 10.1.26 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| 37 | crash | 8 | 10.1.26 (inbuilt) | Antelope | on | - | => | 10.1.26 (inbuilt) | Antelope | on | - | - | OK |  |
| 38 | crash | 8 | 10.1.26 (inbuilt) | Barracuda | on | - | => | 10.1.26 (inbuilt) | Barracuda | on | - | - | OK |  |
| 39 | crash | 8 | 10.1.26 (inbuilt) | Barracuda | - | - | => | 10.1.26 (inbuilt) | Barracuda | - | - | - | OK |  |
| 40 | crash | 8 | 10.1.26 (inbuilt) | Antelope | - | - | => | 10.1.26 (inbuilt) | Antelope | - | - | - | OK |  |


