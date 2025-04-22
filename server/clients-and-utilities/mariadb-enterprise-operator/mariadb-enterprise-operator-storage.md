
# Storage

This operator gives you flexibility to define the storage that will back the `/var/lib/mysql` data directory mounted by `MariaDB`.


## Table of contents


* [Configuration](#configuration)
* [Volume resize](#volume-resize)
* [Ephemeral storage](#ephemeral-storage)


## Configuration


The simplest way to configure storage for your `MariaDB` is:



```
apiVersion: enterprise.mariadb.com/v1alpha1
kind: MariaDB
metadata:
  name: mariadb-galera
spec:
  ...
  storage:
    size: 1Gi
```



This will make use of the default `StorageClass` available in your cluster, but you can also provide a different one:



```
apiVersion: enterprise.mariadb.com/v1alpha1
kind: MariaDB
metadata:
  name: mariadb-galera
spec:
  ...
  storage:
    size: 1Gi
    storageClassName: gp3
```



Under the scenes, the operator is configuring the `StatefulSet`'s `volumeClaimTemplate` property, which you are also able to provide yourself:



```
apiVersion: enterprise.mariadb.com/v1alpha1
kind: MariaDB
metadata:
  name: mariadb-galera
spec:
  ...
  storage:
    size: 1Gi
    storageClassName: gp3
    volumeClaimTemplate:
      accessModes:
      - ReadWriteOnce
      resources:
        requests:
          storage: 1Gi
      storageClassName: gp3
```



## Volume resize



**WARNING**
The `StorageClass` used for volume resizing must define `allowVolumeExpansion = true`.



It is possible to resize your storage after having provisioned a `MariaDB`. We need to distinguish between:


* PVCs already in use.
* `StatefulSet` storage size, which will be used when provisioning new replicas.


It is important to note that, for the first case, your `StorageClass` must support volume expansion by declaring the `allowVolumeExpansion = true`. In such case, it will be safe to expand the storage by increasing the `size` and setting `resizeInUseVolumes = true`:



```
apiVersion: enterprise.mariadb.com/v1alpha1
kind: MariaDB
metadata:
  name: mariadb-galera
spec:
  ...
  storage:
    size: 2Gi
    resizeInUseVolumes: true
    waitForVolumeResize: true
```



Depending on your storage provider, this operation might take a while, and you can decide to wait for this operation before the `MariaDB` becomes ready by setting `waitForVolumeResize = true`. Operations such as [Galera cluster recovery](mariadb-enterprise-operator-galera-cluster.md#galera-cluster-recovery) and [primary switchover](high-availability.md) will not be performed if the `MariaDB` resource is not ready.


## Ephemeral storage


Provisioning standalone `MariaDB` instances with ephemeral storage can be done by setting `ephemeral = true`:



```
apiVersion: enterprise.mariadb.com/v1alpha1
kind: MariaDB
metadata:
  name: mariadb-galera
spec:
  ...
  storage:
    ephemeral: true
```



This may be useful for multiple use cases, like provisioning ephemeral `MariaDBs` for the integration tests of your CI.
