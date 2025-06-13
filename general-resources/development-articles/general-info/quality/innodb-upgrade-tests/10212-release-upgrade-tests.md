
# 10.2.12 Release Upgrade Tests

### Tested revision


d361401bc26f49480daec8b0307afff6edae2ecc


### Test date


2018-01-07 07:34:24


### Summary


Some tests failed due to [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103), [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094) as usual.
Crash recovery with encryption also fails due to [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103).


### Details



| type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| type | pagesize | OLD version | file format | encrypted | compressed |  | NEW version | file format | encrypted | compressed | readonly | result | notes |
| recovery | 16 | 10.2.12 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 16 | 10.2.12 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| recovery | 4 | 10.2.12 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 4 | 10.2.12 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| recovery | 32 | 10.2.12 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| recovery | 32 | 10.2.12 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 64 | 10.2.12 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 64 | 10.2.12 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| recovery | 8 | 10.2.12 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| recovery | 8 | 10.2.12 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| recovery | 16 | 10.2.12 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 16 | 10.2.12 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 4 | 10.2.12 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 4 | 10.2.12 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 32 | 10.2.12 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 32 | 10.2.12 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 64 | 10.2.12 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 64 | 10.2.12 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| recovery | 8 | 10.2.12 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| recovery | 8 | 10.2.12 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 16 | 10.2.12 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 4 | 10.2.12 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 32 | 10.2.12 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 64 | 10.2.12 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 8 | 10.2.12 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo-recovery | 16 | 10.2.12 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 4 | 10.2.12 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 32 | 10.2.12 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 64 | 10.2.12 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 8 | 10.2.12 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo-recovery | 16 | 10.2.12 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | TEST_FAILURE |
| undo-recovery | 4 | 10.2.12 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | TEST_FAILURE |
| undo-recovery | 32 | 10.2.12 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | TEST_FAILURE |
| undo-recovery | 64 | 10.2.12 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | TEST_FAILURE |
| undo-recovery | 8 | 10.2.12 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | TEST_FAILURE |
| undo-recovery | 16 | 10.2.12 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 4 | 10.2.12 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 32 | 10.2.12 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 64 | 10.2.12 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo-recovery | 8 | 10.2.12 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 16 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 4 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 4 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 32 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 32 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 64 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 64 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 8 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 8 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 16 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 16 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 4 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 4 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 32 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 32 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 64 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 64 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 8 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 8 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| crash | 16 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 16 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| crash | 4 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 4 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| crash | 32 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| crash | 32 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| crash | 8 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 8 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| crash | 16 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 16 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 4 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 4 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 8 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 8 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 16 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 4 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 32 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 64 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 8 | 10.2.11 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 16 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 4 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 32 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 64 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 8 | 10.2.11 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 16 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 4 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 32 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 64 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 8 | 10.2.11 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 16 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 4 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 32 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 64 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 8 | 10.2.11 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 16 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 4 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 4 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 32 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 32 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 64 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 64 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 8 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 8 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 16 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 16 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 4 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 4 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 32 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 32 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 64 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 64 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 8 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| normal | 8 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | FAIL | KNOWN_BUGS [MDEV-13094](https://jira.mariadb.org/browse/MDEV-13094)(1) |
| crash | 16 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 16 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| crash | 4 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 4 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| crash | 32 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| crash | 32 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 64 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| crash | 8 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| crash | 8 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | FAIL | KNOWN_BUGS [MDEV-13103](https://jira.mariadb.org/browse/MDEV-13103)(1) |
| crash | 16 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 16 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 4 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 4 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 32 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 64 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| crash | 8 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| crash | 8 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 16 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 4 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 32 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 64 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 8 | 10.2.6 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 16 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 4 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 32 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 64 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 8 | 10.2.6 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 16 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 4 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 32 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 64 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 8 | 10.2.6 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 16 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 4 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 32 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 64 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 8 | 10.2.6 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 16 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 4 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 4 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 8 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 8 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 16 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 16 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 4 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 4 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 8 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 8 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 16 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 4 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 32 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 64 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 8 | 10.1.30 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 16 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 4 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 32 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 64 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 8 | 10.1.30 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 16 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 4 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 32 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 64 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 8 | 10.1.30 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 16 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 4 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 32 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 64 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 8 | 10.1.30 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 16 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 16 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 4 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 4 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 32 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 64 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 8 | 10.1.13 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| normal | 8 | 10.1.13 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| normal | 16 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 16 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 4 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 4 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 32 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 64 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 8 | 10.1.10 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| normal | 8 | 10.1.10 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | on | - | => | 10.2.12 (inbuilt) | Barracuda | on | - | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | - | - | => | 10.2.12 (inbuilt) | Barracuda | - | - | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | on | zlib | => | 10.2.12 (inbuilt) | Barracuda | on | zlib | - | OK |  |
| undo | 16 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 4 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 32 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 64 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| undo | 8 | 10.1.22 (inbuilt) | Barracuda | - | zlib | => | 10.2.12 (inbuilt) | Barracuda | - | zlib | - | OK |  |
| normal | 4 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| normal | 4 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 4 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 8 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| undo | 4 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| undo | 8 | 10.0.33 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| normal | 4 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 10.0.14 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 4 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 8 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| undo | 4 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| undo | 8 | 10.0.18 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 64 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 32 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| normal | 16 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| normal | 64 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| normal | 32 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| crash | 64 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| crash | 8 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| crash | 16 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| crash | 32 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| crash | 4 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| crash | 4 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| crash | 8 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| crash | 16 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| crash | 64 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| crash | 32 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 4 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 32 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 64 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 8 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| undo | 4 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| undo | 32 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| undo | 64 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| undo | 8 | 5.7.20 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 4 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 8 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| normal | 16 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| normal | 4 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| normal | 8 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 4 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 8 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | on | - | - | OK |  |
| undo | 16 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| undo | 4 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |
| undo | 8 | 5.6.38 (inbuilt) |  | - | - | => | 10.2.12 (inbuilt) |  | - | - | - | OK |  |




<sub>_This page is licensed: CC BY-SA / Gnu FDL_</sub>


{% @marketo/form formId="4316" %}
