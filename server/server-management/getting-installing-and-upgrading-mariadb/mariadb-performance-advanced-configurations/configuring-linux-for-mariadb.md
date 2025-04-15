# Configuring Linux for MariaDB

#

# Linux kernel settings

#

## IO scheduler

For optimal IO performance running a database on modern hardware we recommend using the *none* (previously called *noop*) scheduler.

Recommended schedulers are *none*, for SSDs and NVMes, and *mq-deadline* (previously called *deadline*) for hard disks.

You can check your scheduler setting with:

```
cat /sys/block/${DEVICE}/queue/scheduler
```

For instance, it should look like this output:

```
cat /sys/block/vdb/queue/scheduler
[none] mq-deadline kyber bfq
```

Older kernels may look like:

```
cat /sys/block/sda/queue/scheduler
[noop] deadline cfq
```

Writing the new scheduler name to the same /sys node will change the scheduler:

```
echo noop > /sys/block/vdb/queue/scheduler
```

The impact of schedulers depend significantly on workload and hardware. You can measure the IO-latency using the [biolatency](https://github.com/iovisor/bcc/blob/master/tools/biolatency_example.txt) bcc-tools script with an aim to keep the mean as low as possible.

#

# Resource Limits

#

## Configuring the Open Files Limit

By default, the system limits how many open file descriptors a process can have open at one time. It has both a soft and hard limit. On many systems, both the soft and hard limit default to 1024. On an active database server, it is very easy to exceed 1024 open file descriptors. Therefore, you may need to increase the soft and hard limits. There are a few ways to do so.

If you are using `[mysqld_safe or mariadbd-safe](../starting-and-stopping-mariadb/mariadbd-safe.md)` to start `mysqld`, then see the instructions at [mariadbd-safe: Configuring the Open Files Limit](../starting-and-stopping-mariadb/mariadbd-safe.md#configuring-the-open-files-limit).

If you are using `[systemd](../starting-and-stopping-mariadb/systemd.md)` to start `mysqld`, then see the instructions at [systemd: Configuring the Open Files Limit](../starting-and-stopping-mariadb/systemd.md#configuring-the-open-files-limit).

Otherwise, you can set the soft and hard limits for the `mysql` user account by adding the following lines to `[/etc/security/limits.conf](https://linux.die.net/man/5/limits.conf)`:

```
mysql soft nofile 65535
mysql hard nofile 65535
```

After the system is rebooted, the `mysql` user should use the new limits, and the user's `ulimit` output should look like the following:

```
$ ulimit -Sn
65535
$ ulimit -Hn
65535
```

#

## Configuring the Core File Size

By default, the system limits the size of core files that could be created. It has both a soft and hard limit. On many systems, the soft limit defaults to 0. If you want to [enable core dumps](https://app.gitbook.com/s/iJPrPCGi329TSR8WIXJW/learning-and-training/training-and-tutorials/advanced-mariadb-articles/development-articles/debugging-mariadb/enabling-core-dumps), then you may need to increase this. Therefore, you may need to increase the soft and hard limits. There are a few ways to do so.

If you are using `[mysqld_safe or mariadbd-safe](../starting-and-stopping-mariadb/mariadbd-safe.md)` to start `mysqld`, then see the instructions at [mariadb-safe: Configuring the Core File Size](../starting-and-stopping-mariadb/mariadbd-safe.md#configuring-the-core-file-size).

If you are using `[systemd](../starting-and-stopping-mariadb/systemd.md)` to start `mysqld`, then see the instructions at [systemd: Configuring the Core File Size](../starting-and-stopping-mariadb/systemd.md#configuring-the-core-file-size).

Otherwise, you can set the soft and hard limits for the `mysql` user account by adding the following lines to `[/etc/security/limits.conf](https://linux.die.net/man/5/limits.conf)`:

```
mysql soft core unlimited
mysql hard core unlimited
```

After the system is rebooted, the `mysql` user should use the new limits, and the user's `ulimit` output should look like the following:

```
$ ulimit -Sc
unlimited
$ ulimit -Hc
unlimited
```

#

# Swappiness

See [configuring swappiness](configuring-swappiness.md).