
# Using Git


## Just Getting the Source


If you just want to get the latest source and you don't require the ability to push changes to the MariaDB repository, you can use the following command to check out the latest 10.5 branch:


```
git clone -b 10.5 https://github.com/MariaDB/server.git
```

## Setup up git for MariaDB


* Set your name with git


```
git config --global user.name "Ivan Ivanov"
git config --global user.email "ivan@mariadb.com"
```

* Go to [ssh](https://github.com/settings/ssh) and add your public SSH key ([GitHub Help](https://help.github.com/articles/generating-ssh-keys/#step-3-add-your-ssh-key-to-github)).


* Clone the repository


```
git clone git@github.com:MariaDB/server.git
cd server
git checkout 10.5
```

* Config repository pull and alias for fast forward:


```
git config pull.ff only
git config --global alias.ff "merge --ff-only"
```

## Commit comments


In git commit messages are normally formatted as


```
subject

body
more body
...
```

That is, the first line is considered a *subject*, much like email subject. Many git commands and pages on github only show the commit subject, not the complete comment. After the subject goes an empty line, then the detailed description of the comment. Please, structure your commit comments this way, don't forget the empty line.


## Branches


This is an important concept, and git branches do not have equivalents in bzr.


In Bazaar, we all used to have one shared repository, within which there were many branches. This seems to be impossible with git?


In Git, each repository has only one branch that is currently checked out.


```
git branch
```

### List Existing Branches


To see which branches exists locally and remotely:


```
git branch --all
```

### To Move to Work on a Specific Branch


```
git checkout branch-name
```

Note that if the output from `git branch --all` is `remotes/origin/XXX` you should just use `XXX` as branch name.


### Making a Local Copy of a Branch (Like bzr clone)


```
branch clone old_directory new_directory
cd new_directory
git remote set-url origin git@github.com:MariaDB/server.git
git pull
```

### Remove Last Commit From a Branch


```
git reset --hard HEAD^
```

### Fetch a Branch Someone Has Done a Rebase on


If you get the following error on pull:


```
shell>  git pull
X11 forwarding request failed on channel 0
fatal: Not possible to fast-forward, aborting.
```

Instead of removing your copy and then clone, you can do:


```
git reset --hard origin/##branch-name##
```

### Other Things About Branches


* Note: branches whose names start with `bb-` are automatically put into the buildbot.


## Equivalents For Some bzr Commands


CAVEAT UTILITOR. Check the manual before running!


* `bzr status` is `git status`
* `bzr diff` is `git diff`
* `bzr log` is `git log`
* `bzr revert` is `git reset --hard`
* `bzr revert filename` is `git checkout filename`
* `bzr parent` is `git remote -v` (but there are more detailed commands)
* `bzr parent to-default-mariadb-repo ` git remote set-url origin git@github.com:MariaDB/server.git
* `bzr push` is `git push REMOTENAME BRANCHNAME`. REMOTENAME is typically "origin", for example: `git push origin HEAD:10.3-new-feature`. The HEAD: stands for "from current branch".
* `bzr clean-tree --ignored` is `git clean -Xdf` (note the capital X!)
* `bzr root` is `git rev-parse --show-toplevel`
* `bzr missing --mine-only` is `git cherry -v origin` (kind-of).


GUIs


* `bzr gcommit` is `git citool`
* `bzr viz` is `gitk`
* `bzr gannotate` is `git gui blame`


## Commit Emails


In the MariaDB project, it is a good idea (and a long tradition since MySQL Ab) to have all your commits sent to a commits@mariadb.org mailing list. It allows others to follow the progress, comment, etc.


A script and instructions on how to setup commit triggers in Git are here: 
[](https://bazaar.launchpad.net/~maria-captains/mariadb-tools/trunk/files/head:/git_template/) . Jira task for commit trigger was [MDEV-6278](https://jira.mariadb.org/browse/MDEV-6278).


## Attributing Code to Someone Else


If you add code on behalf of someone else, please attribute the code to the original author:


* Run `git citool` and move changed files to staged.
* Don't `commit`, abort instead
* run `git commit --author="Original author name <email_address>"`


The above is needed as `git citool` can't handle the `--author` option.


## Applying a Pull Request


At the end of the pull request page there is a button "Merge pull request" and next to it a link "command line instructions". Click the link, you'll see something like


Step 1: From your project repository, check out a new branch and test the changes.

```
git checkout -b mariadb-server-joeuser-cool-feature 10.3
git pull https://github.com/joeuser/mariadb-server cool-feature
```
Step 2: Merge the changes and update on GitHub.

```
git checkout 10.3
git merge --no-ff mariadb-server-joeuser-cool-feature
git push origin 10.3
```


Note where to pull from — **https:/​/github.com/joeuser/mariadb-server cool-feature**.


Now, checkout the branch you want to merge it to, say, bb-10.3-stage, and do the following


```
git fetch https://github.com/joeuser/mariadb-server cool-feature
git checkout FETCH_HEAD
git rebase @{-1}
```

Now's the time to compile the code, test it, fix, if necessary. Then


```
git checkout @{-1}
git ff @{-1}
```

If you want to do small changes to the pull request, do it in a separate commit, after `git rebase @{-1}` above. If you want to do *big* changes to the pull request, perhaps you shouldn't merge it in the first place, but ask the contributor to fix it?


## Examples


### Diff For Last Commit


```
git show
```

### Applying New Code From Main Tree to a Branch


You are working on a branch (`NEW_FEATURE`) and would like to have into that branch all changes from the main branch (`10.1`).


```
git checkout 10.1
git pull
git checkout NEW_FEATURE
git rebase 10.1
```

### Applying a Bugfix in the Main Branch


You've just fixed and committed a bug in the main 10.1 branch and want to merge it with the latest 10.1. Often a rebase is better in this case. Assuming your current checked out branch is 10.1:


```
git fetch origin
git rebase origin/10.1
```

This will work even if you have done multiple commits in your local 10.1 tree.


### Dealing With Conflicts When One Tries to Push


What to do when you have fixed a bug in the main tree but notices that someone has changed the tree since you pulled last time. This approach ensures that your patch is done in one block and not spread out over several change sets.


```
git clone 10.1  
cd 10.1
< fix a bug here>
git citool
git push
# ^ and the above fails, because someone has pushed to 10.1 in between
git branch tmp
# ^ copy our work to branch named 'tmp'
get checkout 10.1
git reset --hard HEAD^ 
# ^ remove our work from '10.1' local branch'
git pull 
# ^ get changes from remote
git checkout tmp
git rebase 10.1
# ^ switch to 'tmp' and try to rebase 'tmp' branch on top of 10.1 branch.
#   here you will be asked to merge if necessary
git checkout 10.1
git pull --ff . tmp
# ^ switch back to the '10.1' branch, and pull from 'tmp' branch. 
git branch -D tmp
#^ this removes the tmp. branch
git push
```

## Finding in Which MariaDB Version a Commit Exists


```
sh> git tag --contain e65f667bb60244610512efd7491fc77eccceb9db
mariadb-10.0.30
mariadb-10.1.22
mariadb-10.1.23
mariadb-10.2.5
mariadb-10.3.0
mariadb-galera-10.0.30
```

## See Also


* [git-for-bzr-users.pdf](https://agateau.com/talks/2010/git-for-bzr-users_uds-natty/git-for-bzr-users.pdf)
* [Sergei's "Using GIT" presentation. Malaga Meeting, January 2015 "Sergei's "Using GIT" presentation. Malaga Meeting, January 2015"](https://mariadb.com/kb/en/usare-git/+attachment/using-git)

