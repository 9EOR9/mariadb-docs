
# Buildbot Setup for Virtual Machines - Fedora 16


## Base install


```
qemu-img create -f qcow2 /kvm/vms/vm-fedora16-i386-serial.qcow2 10G
qemu-img create -f qcow2 /kvm/vms/vm-fedora16-amd64-serial.qcow2 10G
```

Start each VM booting from the server install iso one at a time and perform
the following install steps:


```
kvm -m 1024 -hda /kvm/vms/vm-fedora16-i386-serial.qcow2 -cdrom /kvm/iso/fedora/Fedora-16-i386-DVD.iso -redir tcp:2263::22 -boot d -smp 2 -cpu qemu32,-nx -net nic,model=virtio -net user
kvm -m 1024 -hda /kvm/vms/vm-fedora16-amd64-serial.qcow2 -cdrom /kvm/iso/fedora/Fedora-16-x86_64-DVD.iso -redir tcp:2264::22 -boot d -smp 2 -cpu qemu64 -net nic,model=virtio -net user
```

Once running you can connect to the VNC server from your local host with:


```
vncviewer -via ${remote-host} localhost
```

Replace ${remote-host} with the host the vm is running on.


**Note:** When you activate the install, vncviewer may disconnect with a complaint about the rect being too large. This is fine. The Fedora installer has just resized the vnc screen. Simply reconnect.


Install, picking default options mostly, with the following notes:


* The Installer will throw up a "Storage Device Warning", choose "Yes, discard any data"
* Set the hostname to fedora16-amd64 (or fedora16-i386)
* Click the "Configure Network" button on the Hostname screen.

  * Edit System eth0 to "connect automatically"
  * Apply and then close the "Network Connections" window
* When partitioning disks, choose "Use All Space"

  * uncheck the "Use LVM" checkbox
  * do not check the "Encrypt system" checkbox
* Minimal install
* Customize Later


When the install is finished, you will be prompted to reboot. Go ahead and do so, but it will fail. Kill the VM (after the reboot fails) and start it up again:


```
kvm -m 1024 -hda /kvm/vms/vm-fedora16-i386-serial.qcow2 -redir tcp:2263::22 -boot c -smp 2 -cpu qemu32,-nx -net nic,model=virtio -net user
kvm -m 1024 -hda /kvm/vms/vm-fedora16-amd64-serial.qcow2 -redir tcp:2264::22 -boot c -smp 2 -cpu qemu64 -net nic,model=virtio -net user
```

Until the extra user is installed you must connect via VNC as before. SSH is preferred, so that's what we'll do first. Login as root.


```
ssh -p 2263 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i ~/.ssh/buildbot.id_dsa root@localhost
ssh -p 2264 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i ~/.ssh/buildbot.id_dsa root@localhost
```

After logging in as root, install proper ssh and then create a local user:


```
/sbin/chkconfig --level 35 network on
ifup eth0
yum install openssh-server openssh-clients
adduser ${username}
usermod -a -G wheel ${username}
passwd ${username}
```

Enable password-less sudo and serial console:


```
visudo
# Uncomment the line "%wheel        ALL=(ALL)       NOPASSWD: ALL"
# Comment out this line:
# Defaults    requiretty
```

Still logged in as root, add to /boot/grub/menu.lst:


Editing /boot/grub/menu.lst:


```
sudo vi /etc/default/grub

# Add/edit these entries:
    GRUB_CMDLINE_LINUX_DEFAULT="console=tty0 console=ttyS0,115200n8"
    GRUB_TERMINAL="serial"
    GRUB_SERIAL_COMMAND="serial --unit=0 --speed=115200 --word=8 --parity=no --stop=1"

grub2-mkconfig -o /boot/grub2/grub.cfg
```

Logout as root, and then, from the VM host server:


Create a .ssh folder:


```
ssh -t -p 2263 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i ~/.ssh/buildbot.id_dsa localhost "mkdir -v .ssh"
ssh -t -p 2264 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i ~/.ssh/buildbot.id_dsa localhost "mkdir -v .ssh"
```

Copy over the authorized keys file:


```
scp -P 2263 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no /kvm/vms/authorized_keys localhost:.ssh/
scp -P 2264 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no /kvm/vms/authorized_keys localhost:.ssh/
```

Set permissions on the .ssh folder correctly:


```
ssh -t -p 2263 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i ~/.ssh/buildbot.id_dsa localhost "chmod -R go-rwx .ssh"
ssh -t -p 2264 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i ~/.ssh/buildbot.id_dsa localhost "chmod -R go-rwx .ssh"
```

Create the buildbot user:


```
ssh -p 2263 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no localhost 'chmod -R go-rwx .ssh; sudo adduser buildbot; sudo usermod -a -G wheel buildbot; sudo mkdir ~buildbot/.ssh; sudo cp -vi .ssh/authorized_keys ~buildbot/.ssh/; sudo chown -vR buildbot:buildbot ~buildbot/.ssh; sudo chmod -vR go-rwx ~buildbot/.ssh'
ssh -p 2264 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no localhost 'chmod -R go-rwx .ssh; sudo adduser buildbot; sudo usermod -a -G wheel buildbot; sudo mkdir ~buildbot/.ssh; sudo cp -vi .ssh/authorized_keys ~buildbot/.ssh/; sudo chown -vR buildbot:buildbot ~buildbot/.ssh; sudo chmod -vR go-rwx ~buildbot/.ssh'
```

su to the local buildbot user and ssh to the vm to put the key in known_hosts:


For i386:


```
sudo su - buildbot
ssh -p 2263 buildbot@localhost
# exit, then exit again
```

For amd64:


```
sudo su - buildbot
ssh -p 2264 buildbot@localhost
# exit, then exit again
```

Upload the ttyS0 file and put it where it goes:


```
scp -P 2263 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no /kvm/vms/ttyS0 buildbot@localhost:
scp -P 2264 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no /kvm/vms/ttyS0 buildbot@localhost:

ssh -p 2263 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no buildbot@localhost 'sudo mv -vi ttyS0 /etc/event.d/;'
ssh -p 2264 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no buildbot@localhost 'sudo mv -vi ttyS0 /etc/event.d/;'
```

Update the VM:


```
ssh -p 2263 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no buildbot@localhost
ssh -p 2264 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no buildbot@localhost
```

Once logged in:


```
sudo yum update
```

After updating, shut down the VM:


```
sudo shutdown -h now
```

## VMs for building .rpms


```
for i in '/kvm/vms/vm-fedora16-amd64-serial.qcow2 2264 qemu64' '/kvm/vms/vm-fedora16-i386-serial.qcow2 2263 qemu64' ; do \
  set $i; \
  runvm --user=buildbot --logfile=kernel_$2.log --base-image=$1 --port=$2 --cpu=$3 "$(echo $1 | sed -e 's/serial/build/')" \
    "sudo yum -y groupinstall 'Development Tools'" \
    "sudo yum -y install wget tree gperf readline-devel ncurses-devel zlib-devel pam-devel libaio-devel openssl-devel perl perl\(DBI\)" \
    "sudo yum -y remove systemtap-sdt-dev" \
    "sudo mkdir -vp /usr/src/redhat/SOURCES /usr/src/redhat/SPECS /usr/src/redhat/RPMS /usr/src/redhat/SRPMS" \
    "wget http://www.cmake.org/files/v2.8/cmake-2.8.8.tar.gz;tar -zxvf cmake-2.8.8.tar.gz;cd cmake-2.8.8;./configure;make;sudo make install"; \
done
```

Also:


* [Installing the Boost library needed for the OQGraph storage engine](../buildbot-setup-for-virtual-machines-additional-steps/installing-the-boost-library-needed-for-the-oqgraph-storage-engine.md)


## VMs for install testing.


`MariaDB.local.repo` points at a local directory on the VM. `MariaDB.repo`
points at the real MariaDB YUM repository.


```
for i in '/kvm/vms/vm-fedora16-amd64-serial.qcow2 2264 qemu64' '/kvm/vms/vm-fedora16-i386-serial.qcow2 2263 qemu64' ; do \
  set $i; \
  runvm --user=buildbot --logfile=kernel_$2.log --base-image=$1 --port=$2 --cpu=$3 "$(echo $1 | sed -e 's/serial/install/')" \
    "sudo yum -y update" \
    "sudo yum -y install libaio perl perl-Time-HiRes perl-DBI" \
    "= scp -P $2 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no /kvm/vms/MariaDB.local.repo buildbot@localhost:/tmp/" \
    "sudo mv -vi /tmp/MariaDB.local.repo /etc/yum.repos.d/"; \
done
```

## VMs for MySQL upgrade testing


```
for i in '/kvm/vms/vm-fedora16-amd64-serial.qcow2 2264 qemu64' '/kvm/vms/vm-fedora16-i386-serial.qcow2 2263 qemu64' ; do \
  set $i; \
  runvm --user=buildbot --logfile=kernel_$2.log --base-image=$1 --port=$2 --cpu=$3 "$(echo $1 | sed -e 's/serial/upgrade/')" \
    "sudo yum -y update" \
    'sudo yum -y install mysql-server' \
    'sudo systemctl enable mysqld.service' \
    'sudo systemctl start mysqld.service' \
    'mysql -uroot -e "create database mytest; use mytest; create table t(a int primary key); insert into t values (1); select * from t"' \
    "= scp -P $2 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no /kvm/vms/MariaDB.local.repo buildbot@localhost:/tmp/" \
    "sudo mv -vi /tmp/MariaDB.local.repo /etc/yum.repos.d/"; \
done
```

The MariaDB upgrade testing VMs were not built. Once we have MariaDB Fedora 16 RPMs, then I will attempt building this VM. For now, the placeholder text below is copied from the [Buildbot Setup for Virtual Machines - CentOS 6.2](buildbot-setup-for-virtual-machines-centos-62.md) page.

## VMs for MariaDB upgrade testing


```
for i in '/kvm/vms/vm-fedora16-amd64-serial.qcow2 2264 qemu64' '/kvm/vms/vm-fedora16-i386-serial.qcow2 2263 qemu64' ; do \
  set $i; \
  runvm --user=buildbot --logfile=kernel_$2.log --base-image=$1 --port=$2 --cpu=$3 "$(echo $1 | sed -e 's/serial/upgrade2/')" \
    'sudo yum -y update' \
    "= scp -P $2 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no /kvm/vms/MariaDB.repo buildbot@localhost:/tmp/" \
    'sudo rpm --verbose --import http://downloads.mariadb.org/repo/RPM-GPG-KEY-MariaDB' \
    'sudo mv -vi /tmp/MariaDB.repo /etc/yum.repos.d/' \
    'sudo yum -y remove mysql-libs' \
    'sudo yum -y install MariaDB-server MariaDB-client MariaDB-test' \
    'sudo yum -y install cronie cronie-anacron crontabs.noarch postfix' \
    'sudo /etc/init.d/mysqld start' \
    'mysql -uroot -prootpass -e "create database mytest; use mytest; create table t(a int primary key); insert into t values (1); select * from t"' \
    'sudo rm -v /etc/yum.repos.d/MariaDB.repo' \
    "= scp -P $2 -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no /kvm/vms/MariaDB.local.repo buildbot@localhost:/tmp/" \
    'sudo mv -vi /tmp/MariaDB.local.repo /etc/yum.repos.d/'; \
done
```



CC BY-SA / Gnu FDL

