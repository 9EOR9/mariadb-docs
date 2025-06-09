
# Buildbot Setup for Virtual Machines - Debian 6 amd64

Create the VM:


```
cd /kvm/vms
qemu-img create -f qcow2 vm-debian6-amd64-serial.qcow2 8G
kvm -m 2047 -hda /kvm/vms/vm-debian6-amd64-serial.qcow2 -cdrom /kvm/debian-6a1-amd64-netinst.iso -redir 'tcp:2244::22' -boot d -smp 2 -cpu qemu64 -net nic,model=virtio -net user
```

## Serial console and account setup


From base install, setup for serial port, and setup accounts for passwordless
ssh login and sudo:


```
kvm -m 2047 -hda /kvm/vms/vm-debian6-amd64-serial.qcow2 -redir 'tcp:2244::22' -boot c -smp 2 -cpu qemu64 -net nic,model=virtio -net user

su
apt-get install sudo openssh-server
visudo

# Add: %sudo ALL=NOPASSWD: ALL
# add user account to group sudo `addgroup <USER> sudo`.
# Copy in public ssh key.

# Add in /etc/inittab:
S0:2345:respawn:/sbin/getty -L ttyS0 19200 vt100
```

Editing /etc/default/grub:


```
sudo vi /etc/default/grub
# Add/edit these entries:
    GRUB_CMDLINE_LINUX_DEFAULT="console=tty0 console=ttyS0,115200n8"
    GRUB_TERMINAL="serial"
    GRUB_SERIAL_COMMAND="serial --unit=0 --speed=115200 --word=8 --parity=no --stop=1"

sudo update-grub
```

Add user buildbot, with disabled password. Add as sudo, and add ssh key.


```
sudo adduser --disabled-password buildbot
sudo adduser buildbot sudo
sudo su - buildbot
mkdir .ssh
# Add all necessary keys.
cat >.ssh/authorized_keys
chmod -R go-rwx .ssh
```

## VM for building .deb


```
qemu-img create -b vm-debian6-amd64-serial.qcow2 -f qcow2 vm-debian6-amd64-build.qcow2
kvm -m 2047 -hda /kvm/vms/vm-debian6-amd64-build.qcow2 -redir 'tcp:2244::22' -boot c -smp 2 -cpu qemu64 -net nic,model=virtio -net user -nographic

sudo apt-get build-dep mysql-server-5.1
sudo apt-get install devscripts hardening-wrapper doxygen texlive-latex-base ghostscript libevent-dev libssl-dev zlib1g-dev libreadline-dev
```

## VM for install testing


```
qemu-img create -b vm-debian6-amd64-serial.qcow2 -f qcow2 vm-debian6-amd64-install.qcow2
kvm -m 2047 -hda /kvm/vms/vm-debian6-amd64-install.qcow2 -redir 'tcp:2244::22' -boot c -smp 2 -cpu qemu64 -net nic,model=virtio -net user -nographic
```

See the [General Principles](../buildbot-setup-for-virtual-machines-general-principles.md) 
article for how to make the '`my.seed`' file.


```
# No packages mostly!
sudo apt-get install debconf-utils

cat >>/etc/apt/sources.list <<END
deb file:///home/buildbot/buildbot/debs binary/
deb-src file:///home/buildbot/buildbot/debs source/
END

sudo debconf-set-selections /tmp/my.seed
```

## VM for upgrade testing


```
qemu-img create -b vm-debian6-amd64-install.qcow2 -f qcow2 vm-debian6-amd64-upgrade.qcow2
kvm -m 2047 -hda /kvm/vms/vm-debian6-amd64-upgrade.qcow2 -redir 'tcp:2244::22' -boot c -smp 2 -cpu qemu64 -net nic,model=virtio -net user -nographic

sudo apt-get install mysql-server-5.1
mysql -uroot -prootpass -e "create database mytest; use mytest; create table t(a int primary key); insert into t values (1); select * from t"
```


CC BY-SA / Gnu FDL


{% @marketo/form formId="4316" %}
