
# 10.2.17 Release Upgrade Tests

### Tested revision


5553d3f1f691a374124686946bd1f1cc4ef9fb45


### Test date


2018-08-30 01:21:02


### Summary


Known bug [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094). A few upgrades from MySQL and old MariaDB fail because the old versions hang on shutdown.


### Details



| type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| recovery | 16 | 10.2.17 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 16 | 10.2.17 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| recovery | 4 | 10.2.17 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 4 | 10.2.17 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| recovery | 32 | 10.2.17 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| recovery | 32 | 10.2.17 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 64 | 10.2.17 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 64 | 10.2.17 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| recovery | 8 | 10.2.17 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 8 | 10.2.17 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| recovery | 16 | 10.2.17 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 16 | 10.2.17 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 4 | 10.2.17 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 4 | 10.2.17 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 32 | 10.2.17 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 32 | 10.2.17 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 64 | 10.2.17 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 64 | 10.2.17 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 8 | 10.2.17 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 8 | 10.2.17 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 16 | 10.2.17 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 4 | 10.2.17 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 32 | 10.2.17 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 64 | 10.2.17 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 8 | 10.2.17 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 16 | 10.2.17 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 4 | 10.2.17 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 32 | 10.2.17 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 64 | 10.2.17 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 8 | 10.2.17 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 16 | 10.2.17 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo-recovery | 4 | 10.2.17 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo-recovery | 32 | 10.2.17 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo-recovery | 64 | 10.2.17 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo-recovery | 8 | 10.2.17 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo-recovery | 16 | 10.2.17 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 4 | 10.2.17 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 32 | 10.2.17 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 64 | 10.2.17 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 8 | 10.2.17 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 16 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 4 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 4 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 8 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 8 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 16 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 16 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 4 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 4 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 8 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 8 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 16 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 16 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| crash | 4 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 4 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| crash | 32 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| crash | 32 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| crash | 8 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 8 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| crash | 16 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 16 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 4 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 4 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 8 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 8 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 16 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 4 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 32 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 64 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 8 | 10.2.16 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 16 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 4 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 32 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 64 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 8 | 10.2.16 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 16 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 4 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 32 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 64 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 8 | 10.2.16 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 16 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 4 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 32 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 64 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 8 | 10.2.16 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 16 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 4 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 4 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 8 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 8 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 16 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 16 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 4 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 4 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 8 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 8 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| crash | 16 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 16 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| crash | 4 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 4 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| crash | 32 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| crash | 32 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| crash | 8 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 8 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| crash | 16 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 16 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 4 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 4 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 8 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 8 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 16 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 4 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 32 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 64 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 8 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 16 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 4 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 32 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 64 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 8 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 16 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 4 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 32 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 64 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 8 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 16 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 4 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 32 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 64 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 8 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.1.35 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 16 | 10.1.35 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 4 | 10.1.35 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 4 | 10.1.35 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.35 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.35 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.35 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.35 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 8 | 10.1.35 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 8 | 10.1.35 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 16 | 10.1.35 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 16 | 10.1.35 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 4 | 10.1.35 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 4 | 10.1.35 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.35 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.35 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.35 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.35 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 8 | 10.1.35 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 8 | 10.1.35 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 16 | 10.1.35 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 4 | 10.1.35 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 32 | 10.1.35 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 64 | 10.1.35 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 8 | 10.1.35 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 16 | 10.1.35 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 4 | 10.1.35 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 32 | 10.1.35 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 64 | 10.1.35 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 8 | 10.1.35 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 16 | 10.1.35 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 4 | 10.1.35 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 32 | 10.1.35 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 64 | 10.1.35 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 8 | 10.1.35 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 16 | 10.1.35 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 4 | 10.1.35 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 32 | 10.1.35 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 64 | 10.1.35 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 8 | 10.1.35 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 16 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 4 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 4 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 8 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 8 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 16 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 16 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 4 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 4 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 8 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 8 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.2.17 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.2.17 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.2.17 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.2.17 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 4 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| normal | 4 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 4 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 8 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| undo | 4 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| undo | 8 | 10.0.36 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| normal | 4 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | FAIL | TEST_FAILURE |
| undo | 4 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | FAIL | TEST_FAILURE |
| undo | 8 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | FAIL | TEST_FAILURE |
| undo | 16 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | FAIL | TEST_FAILURE |
| undo | 4 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | FAIL | TEST_FAILURE |
| undo | 8 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | FAIL | TEST_FAILURE |
| normal | 64 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 32 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| normal | 16 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| normal | 64 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| normal | 32 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| crash | 64 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| crash | 8 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| crash | 16 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| crash | 32 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| crash | 4 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| crash | 4 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| crash | 8 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| crash | 16 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| crash | 64 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| crash | 32 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 4 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 32 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 64 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 8 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| undo | 4 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| undo | 32 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| undo | 64 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| undo | 8 | 5.7.23 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| normal | 4 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 4 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | OK |  |
| undo | 8 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | on | - | - | FAIL | TEST_FAILURE |
| undo | 16 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | FAIL | TEST_FAILURE |
| undo | 4 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | OK |  |
| undo | 8 | 5.6.41 (inbuilt) |  | - | - | => | 10.2.17 (inbuilt) |  | - | - | - | FAIL | TEST_FAILURE |




CC BY-SA / Gnu FDL

