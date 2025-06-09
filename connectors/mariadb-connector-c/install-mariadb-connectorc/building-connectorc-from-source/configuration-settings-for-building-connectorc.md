# Configuration Settings For Building Connector/C

### Configuration settings

Connector/C specifies its build process with platform-independent CMake listfiles included in each directory of a source tree with the name CMakeLists.txt.\
Configuration settings may be specified by passing the -D option to CMake command line interpreter.

Do not build Connector/C from root of the source tree: Either create a subdirectory "build" inside the source tree or create a subdirectory outside of the source tree.

Example:

```c
cmake ../connector_c -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr/local
```

#### Reconfiguration

In case Connector/C was already configured, the CMakeCache.txt file needs to be removed first. In several cases, e.g. when cross compiling CMakeFiles subfolders need to be removed too.

#### Generator options

If you want to use a different generator, e.g. for nmake on Windows, you need to specify the generator with the `-G` option. `cmake --help` lists the available generators for the used platform.

#### CMake-related configuration settings

|                        |                                              |
| ---------------------- | -------------------------------------------- |
| CMAKE\_BUILD\_TYPE     | Build type: Release, RelWithDebInfo or Debug |
| CMAKE\_INSTALL\_PREFIX | Installation base directory                  |
| CMAKE\_C\_FLAGS        | Flags for C-Compiler                         |

#### TLS/SSL options

|               |                                       |                                                                                                                        |
| ------------- | ------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Option        | Default                               | Description                                                                                                            |
| WITH\_OPENSSL | ON                                    | Possible values are ON or OFF. Not supported anymore since Connector/C 3.0                                             |
| WITH\_SSL     | SCHANNEL (windows), otherwise OPENSSL | Specifies type of TLS/SSL library. E.g. GNUTLS, OPENSSL or SCHANNEL (Windows only). OFF disables TLS/SSL functionality |

#### Client plugins

Client plugins can be configured as dynamic plugins (DYNAMIC) or built-in plugins (STATIC) by specifying the plugin name followed by suffix \_PLUGIN\_TYPE as key, and "DYNAMIC" or "STATIC" as value.

E.g. for building dialog plugin as a built-in plugin, for versions < Connector/C 3.0.4

```bash
cmake .. -D{PLUGIN_NAME}_PLUGIN_TYPE=[STATIC|DYNAMIC|OFF]
```

Beginning with C/C 3.0.4

```bash
cmake .. -DCLIENT_PLUGIN_{PLUGIN_NAME}=[STATIC|DYNAMIC|OFF]
```

Connector/C 3.0 supports the following plugins:

|                  |                |         |                                                            |
| ---------------- | -------------- | ------- | ---------------------------------------------------------- |
| Plugin           | Type           | Default | Description                                                |
| SOCKET           | IO             | static  | plugin for client server communication via socket          |
| SHMEM            | IO             | static  | plugin for client server communication via shared memory   |
| NPIPE            | IO             | static  | plugin for client server communication via named pipe      |
| DIALOG           | Authentication | dynamic | Authentication for user input, e.g. for PAM authentication |
| OLDPASSWORD      | Authentication | static  | Pre. 4.1 authentication (deprecated)                       |
| NATIVE           | Authentication | static  | Default authentication                                     |
| CLEARTEXT        | Authentication | dynamic | Sends password without hashing or encryption               |
| AUTH\_GSSAPI     | Authentication | dynamic | Kerberos/GSSAPI authentication plugin                      |
| SHA256\_PASSWORD | Authentication | dynamic | SHA256 password authentication plugin                      |
| AURORA           | Connection     | OFF     | Fail over plugin for Aurora (experimental)                 |
| REPLICATION      | Connection     | OFF     | Replication/fail over plugin (experimental)                |


{% @marketo/form formId="4316" %}
