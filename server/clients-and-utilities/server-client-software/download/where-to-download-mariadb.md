# Where to Download MariaDB

## The Latest Packages

Tarballs, binaries (Linux, Solaris, and Windows), and packages for some Linux\
distributions are available at [mariadb.com/downloads/](https://mariadb.com/downloads/) or[mariadb.org/download/](https://mariadb.org/download/) (which also contains a PDF version of the MariaDB Server documentation).

We hope that interested [community](../../../../en/community/) package maintainers will step forward, as\
others already have, to build packages for their distributions. We ask for\
strict adherence to your packaging system's best practices and invite you to\
create a [bug report](https://mariadb.org/jira) if our project impedes this in\
any way.

Instructions how to install the packages can be found[here](../../../server-management/getting-installing-and-upgrading-mariadb/binary-packages/).

## Distributions Which Include MariaDB

* Most distributions already include MariaDB. See [Distributions Which Include MariaDB](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/).

## Pre-Release Binaries

Binaries from our [Buildbot](https://buildbot.askmonty.org) system (see also\
the [Buildbot](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/training-and-tutorials/advanced-mariadb-articles/development-articles/tools/buildbot) page), are available at[archive](https://hasky.askmonty.org/archive). They are not suitable for use in\
production systems but may be of use for debugging.

Once at the above URL you will need to click on the MariaDB tree you are\
interested in, and then the build. The build number corresponds to the`tarbuildnum` variable in Buildbot.

For example, if you were interested in the bsd9-64 build of the [MariaDB 5.5](https://app.gitbook.com/s/aEnK0ZXmUbJzqQrTjFyb/mariadb-community-server-release-notes/old-releases/release-notes-mariadb-5-5-series/changes-improvements-in-mariadb-5-5)\
tree, revision 3497, the `tarbuildnum` is listed in the "Build Properties"\
table of the[Buildbot build report](https://buildbot.askmonty.org/buildbot/builders/bsd9-64/builds/337).\
In this case, the value is "2434".

## Getting the Source

You can find all the source code at [server](https://github.com/MariaDB/server)

To retrieve the code, the [Git](https://app.gitbook.com/s/WCInJQ9cmGjq1lsTG91E/training-and-tutorials/advanced-mariadb-articles/development-articles/tools/using-git-with-mariadb/using-git) source control software offers\
the path of least resistance. If you are unfamiliar with git, please refer to\
the [git documentation](https://git-scm.com/doc) for an understanding\
of version control with git.

For instructions on creating a local branch of MariaDB, see the[Getting the MariaDB Source Code](getting-the-mariadb-source-code.md) page.

See the [Generic Build Instructions](../../../server-management/getting-installing-and-upgrading-mariadb/compiling-mariadb-from-source/generic-build-instructions.md) page for\
general instructions on compiling MariaDB from the source.\
The [source](../../../server-management/getting-installing-and-upgrading-mariadb/compiling-mariadb-from-source/) page has links to platform and distribution-specific\
information, including information on how we build the release packages.

CC BY-SA / Gnu FDL
