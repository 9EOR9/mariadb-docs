
# Protocol data types


## List of possible types


Unknown type:



|   |   |
| --- | --- |
| [byte<1>](#fixed-length-bytes) | Fixed-length bytes |
| [byte<lenenc>](#length-encoded-bytes) | Length-encoded bytes |
| [byte<EOF>](#end-of-file-length-bytes) | End-of-file length bytes |



Integer type:



|   |   |
| --- | --- |
| [int<1>](#fixed-length-integers) | Fixed-length integers |
| [int<lenenc>](#length-encoded-integers) | Length-encoded integers |



String type:



|   |   |
| --- | --- |
| [string<fix>](#fixed-length-strings) | Fixed-length strings |
| [string<NUL>](#null-terminated-strings) | Null-terminated strings |
| [string<lenenc>](#length-encoded-strings) | Length-encoded strings |
| [string<EOF>](#end-of-file-length-strings) | End-of-file length strings |






### Fixed length bytes


The notation is "byte<n>"


A fixed-length bytes stores the value in a series of n bytes.





### Length encoded bytes


The notation is "byte<lenenc>"
Length encoded bytes are prefixed by a length-encoded integer which describes the length of the byte value, followed by the bytes value.





### End of file length bytes


The notation is "byte<EOF>"
Bytes whose length will be calculated by the packet remaining length.


### Fixed length integers


Notation is "int<n>"


A fixed-length integer stores the value in a series of n bytes. The least significant byte is
always the first byte (little-endian format).


#### Example


An int<4> with value 2 is stored as
`02 00 00 00`


### Length encoded integers


The notation is "int<lenenc>"
An integer which depending on its value is represented by n bytes.


The first byte represents the size of the integer:


If the value of first byte is


* < 0xFB - Integer value is this 1 byte integer
* 0xFB - NULL value
* 0xFC - Integer value is encoded in the next 2 bytes (3 bytes total)
* 0xFD - Integer value is encoded in the next 3 bytes (4 bytes total)
* 0xFE - Integer value is encoded in the next 8 bytes (9 bytes total)


### Fixed-length strings


The notation is "string<fix>"
Fixed-length strings have a known hardcoded length.


### Null-terminated strings


The notation is "string<NUL>"
Null-terminated strings have a variable size and are terminated by a 0x00 character


### Length-encoded strings


The notation is "string<lenenc>"
Length-encoded strings are prefixed by a length-encoded integer which describes the length of the string, followed by the string value.





#### Example


An string of 512 "a" will be encoded in 515 bytes :



|   |   |
| --- | --- |
| fc 00 02 97 97 97 97 97 97 97 97 97 97 97 97 97 | ² .. a a a a a a a a a a a a a |

...
Null value will be encoded using null (0xfb) length. 
Empty value will be encoded with a 0 (0x00) length. 





### End of file length strings


The notation is "string<EOF>"
Strings whose length will be calculated by the packet remaining length. 
For an example see [COM_STMT_PREPARE](3-binary-protocol-prepared-statements/com_stmt_prepare.md) packet.

