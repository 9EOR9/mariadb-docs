
# 10.1.30 Release Upgrade Tests

### Tested revision


461cf3e5a3c2d346d75b1407b285f8daf9d01f67


### Test date


2017-12-23


### Summary


Some tests failed with known bug [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112).
Undo upgrade from 10.0.18 failed because the old server hang on shutdown (a known problem with old servers). 
Crash upgrade from 10.1.10 (4K, zlib, XtraDB, Barracuda) failed ([MDEV-14759](https://jira.mariadb.org/browse/MDEV-14759)).


### Details



| type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| recovery | 16 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 16 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(52) |
| recovery | 4 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 4 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(59) |
| recovery | 32 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| recovery | 32 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 64 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 64 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(20) |
| recovery | 8 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 8 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(71) |
| recovery | 16 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 16 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 4 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 4 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 32 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 32 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 64 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 64 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 8 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 8 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 16 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 4 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 32 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 64 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 8 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 16 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 4 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 32 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 64 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 8 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 16 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo-recovery | 4 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo-recovery | 32 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo-recovery | 64 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo-recovery | 8 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo-recovery | 16 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 4 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 32 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 64 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 8 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 16 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 4 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 4 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 8 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 8 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 16 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 16 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 4 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 4 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 8 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 8 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 16 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 16 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(17) |
| crash | 4 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 4 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(43) |
| crash | 32 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(36) |
| crash | 32 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(47) |
| crash | 8 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 8 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(60) |
| crash | 16 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 16 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 4 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 4 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 8 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 8 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 16 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 4 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 32 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 64 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 8 | 10.1.29 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 16 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 4 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 32 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 64 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 8 | 10.1.29 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 16 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 4 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 32 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 64 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 8 | 10.1.29 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 16 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 4 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 32 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 64 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 8 | 10.1.29 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 16 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 4 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 4 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 8 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 8 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 16 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 16 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 4 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 4 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 8 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 8 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 16 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 16 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(33) |
| crash | 4 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 4 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(19) |
| crash | 32 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(44) |
| crash | 32 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(29) |
| crash | 8 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 8 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13112](https://jira.mariadb.org/browse/MDEV-13112)(66) |
| crash | 16 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 16 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 4 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 4 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | FAIL | UPGRADE_FAILURE |
| crash | 32 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 8 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 8 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.1.30 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.1.30 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.1.30 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.1.30 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| normal | 4 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| normal | 16 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| crash | 16 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| crash | 4 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| crash | 8 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| crash | 16 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| crash | 4 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| crash | 8 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| undo | 16 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| undo | 4 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| undo | 8 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| undo | 4 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| undo | 8 | 10.0.33 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| normal | 4 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| normal | 16 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| crash | 16 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| crash | 4 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| crash | 8 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| crash | 16 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| crash | 4 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| crash | 8 | 10.0.14 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| undo | 16 | 10.0.18 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| undo | 4 | 10.0.18 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| undo | 8 | 10.0.18 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | FAIL | TEST_FAILURE |
| undo | 16 | 10.0.18 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| undo | 4 | 10.0.18 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| undo | 8 | 10.0.18 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| normal | 4 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| normal | 16 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| crash | 16 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| crash | 4 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| crash | 8 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| crash | 16 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| crash | 4 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| crash | 8 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| undo | 16 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| undo | 4 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| undo | 8 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| undo | 4 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |
| undo | 8 | 5.6.38 (inbuilt) |  | - | - | => | 10.1.30 (inbuilt) |  | - | - | - | OK |  |




CC BY-SA / Gnu FDL

