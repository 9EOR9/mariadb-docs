
# Suspend Reconciliation

## Table of contents


* [Suspended state](#suspended-state)
* [Suspend a resource](#suspend-a-resource)


## Suspended state


When a resource is suspended, all operations performed by the operator are disabled, including but not limited to:


* Provisioning
* Upgrades
* Volume resize
* Galera cluster recovery


More specifically, the reconciliation loop of the operator is omitted, anything part of it will not happen while the resource is suspended. This could be useful in **maintenance** scenarios, where manual operations need to be performed, as it helps prevent conflicts with the operator.


## Suspend a resource


Currently, only `MariaDB` and `MaxScale` resources support suspension. You can enable it by setting `suspend=true`:



```
apiVersion: enterprise.mariadb.com/v1alpha1
kind: MariaDB
metadata:
  name: mariadb-galera
spec:
  suspend: true
```



This results in the reconciliation loop being disabled and the status being marked as `Suspended`:



```
kubectl get mariadbs
NAME             READY   STATUS      PRIMARY           UPDATES                   AGE
mariadb-galera   True    Suspended   mariadb-galera-0  ReplicasFirstPrimaryLast  12m
```



To re-enable it, simply remove the `suspend` setting or set it to `suspend=false`.


CC BY-SA / Gnu FDL

