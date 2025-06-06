
# Merging New XtraDB Releases (obsolete)

**Note:** This page is obsolete. The information is old, outdated, or otherwise currently incorrect. We are keeping the page for historical reasons only. **Do not** rely on the information in this article.



### Background


Percona used to maintain XtraDB as a patch series against the InnoDB plugin. This affected how we started merging XtraDB in.


Now Percona maintains a normal source repository on launchpad (`lp:percona-server`). But we continue to merge the old way to preserve the history of our changes.


### Merging


There used to be a `lp:percona-xtradb` tree, that we were merging from as:


```
bzr merge lp:percona-xtradb
```

Now we have to maintain our own XtraDB-5.5 repository to merge from. It is `lp:~maria-captains/maria/xtradb-mergetree-5.5`. Follow the procedures as described in [Merging with a merge tree](merging-with-a-merge-tree.md) to merge from it.


CC BY-SA / Gnu FDL

