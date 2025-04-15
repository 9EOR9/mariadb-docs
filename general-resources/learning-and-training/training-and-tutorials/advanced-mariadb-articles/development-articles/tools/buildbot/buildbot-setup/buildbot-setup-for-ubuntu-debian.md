
# Buildbot Setup for Ubuntu-Debian

## Setting up a Buildbot slave on Ubuntu and Debian



One great way to contribute to MariaDB development is to run a buildbot builder. These builders are used for running automated builds and tests of MariaDB. The instructions on this page should help you get a builder set up on Ubuntu and Debian.


### Setting up your MariaDB build environment


For Ubuntu and Debian, a quick way to install much of what you need is:


```
sudo apt-get build-dep mariadb-server
```

If you're running a version of Debian or Ubuntu that doesn't have MariaDB, then do the following:


```
sudo apt-get build-dep mysql-server
```

After running one (or both) of the above, run the following to catch things that they may have missed:


```
sudo apt-get install devscripts fakeroot doxygen texlive-latex-base ghostscript libevent-dev libssl-dev zlib1g-dev libpam0g-dev libreadline-gplv2-dev autoconf automake automake1.11 dpatch ghostscript-x libfontenc1 libjpeg62 libltdl-dev libltdl7 libmail-sendmail-perl libxfont1 lmodern texlive-latex-base-doc ttf-dejavu ttf-dejavu-extra libaio-dev xfonts-encodings xfonts-utils libxml2-dev unixodbc-dev bzr scons check libboost-all-dev openssl epm libjudy-dev libjemalloc-dev libcrack2-dev git libkrb5-dev libcurl4-openssl-dev thrift-compiler libsystemd-dev dh-systemd libssl1.0.2 openjdk-8-jdk uuid-dev libnuma-dev gdb libarchive-dev libasio-dev dh-exec
```

After setting up the build environment do a test build to confirm that things are working. First get the source code using the **git** instructions on the [Getting the MariaDB Source Code](../../../../../../../../server/clients-and-utilities/server-client-software/download/getting-the-mariadb-source-code.md) page, then follow the steps on the [Generic Build Instructions](../../../../../../../../server/server-management/getting-installing-and-upgrading-mariadb/compiling-mariadb-from-source/generic-build-instructions.md) page for building MariaDB using **cmake**. If your build succeeds, you're ready to move on to the next step of installing and configuring buildbot.


Do not hesitate to ask for help on the [maria-developers](https://launchpad.net/~maria-developers) mailing list or on [IRC](/kb/en/irc/).


### Buildbot installation and setup


#### Using APT


The easiest way to install buildbot on Ubuntu and Debian is to install the buildbot-slave package, like so:


```
sudo apt-get install buildbot-slave
```

#### Using Pip


Another way to install buildbot is using the Python **pip** package manager. Pip can be installed with:


```
sudo apt-get install python-pip
```

Next install twisted and the buildbot-slave package using pip:


```
sudo pip install twisted==11.0.0
sudo pip install buildbot-slave==0.8.9
```

#### Creating the Buildbot builder


After the buildbot-slave package is installed (either via apt or pip), you need to create the builder using the `<code>buildslave create-slave</code>` command. As part of this command you will need to specify a name for your buildslave and a password. Both need to be given to the MariaDB Buildbot maintainers so that they can add your builder to the build pool. Ask on the [maria-developers](https://launchpad.net/~maria-developers) mailing list or on [IRC](/kb/en/irc/) for who these people are.


An example command for creating the slave is:


```
sudo buildslave create-slave /var/lib/buildbot/slaves/maria buildbot.askmonty.org slavename password
```

If you installed buildbot using pip, the convention is to create a buildbot user and then, as that user, create the buildslave in the home directory like so:


```
sudo buildslave create-slave ~/maria-slave buildbot.askmonty.org slavename password
```

Put some appropriate info in info/admin and info/host files that are created, this will display on the information screen about your builder. See here for example: [bb01](https://buildbot.askmonty.org/buildbot/buildslaves/bb01)


Submit your builder information to the MariaDB Buildbot admins. Also let them know if your machine can run multiple builds at the same time (and how many). After adding your builder's information to the main buildbot configuration, all that's left is for you to do is to start your builder.


### Starting and stopping your builder


If you installed your builder using apt, then you can start and stop it with:


```
sudo /etc/init.d/buildslave start
sudo /etc/init.d/buildslave stop
```

If you installed your buildslave using pip, then do the following as the buildbot user in their home directory:


```
buildslave start maria-slave
buildslave stop maria-slave
```
