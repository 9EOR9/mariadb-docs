---
icon: check
---

# Contributing Code

_For contributors interested in MariaDB development, explore open projects via_ [_JIRA_](https://jira.mariadb.org) _and check for_ [_beginner-friendly tasks_](https://jira.mariadb.org/issues/?jql=resolution%20%3D%20Unresolved%20AND%20labels%20%3D%20beginner-friendly%20ORDER%20BY%20updated%20DESC)_. Engage with the community on the_ [_maria-developers_](https://lists.mariadb.org/postorius/lists/developers.lists.mariadb.org/) _mailing list,_ [_Slack_](https://r.mariadb.com/join-community-slack) _,_ [_Zulip_](https://mariadb.zulipchat.com)_, or_ [_IRC_](../../../en/irc/) _channel for guidance._

General information about contributing to MariaDB (for developers and\
non-developers) can be found on the [Contributing to the MariaDB Project](contributing-to-the-mariadb-project.md)\
page.

## Finding Development Projects to Work on

There are many open development projects for MariaDB which you can contribute\
to (in addition to any ideas you may have yourself).

* We are using [JIRA](../../development-articles/general-development-information/tools/jira.md) to manage the MariaDB project. Go to[jira.mariadb.org](https://jira.mariadb.org) and click on "Projects" to get to the MariaDB project.\
  Browse around the[unresolved and unassigned](https://jira.mariadb.org/secure/IssueNavigator.jspa?reset=true\&jqlQuery=project+%3D+MDEV+AND+resolution+%3D+Unresolved+AND+assignee+is+EMPTY+ORDER+BY+priority+DESC\&mode=hide)\
  issues to see if there is something that interests you. Some issues have\
  sponsors and you can be paid for doing them!
* A list of [beginner friendly](https://jira.mariadb.org/issues/?jql=resolution%20%3D%20Unresolved%20AND%20labels%20%3D%20beginner-friendly%20ORDER%20BY%20updated%20DESC) tasks is also available.
* Check the [development plans](broken-reference) for the next MariaDB\
  version.
* Join [maria-developers](https://lists.mariadb.org/postorius/lists/developers.lists.mariadb.org/) and ask for suggestions of tasks you could do. Please include your programming experience and your knowledge of the MariaDB source and how much you know about using MySQL/MariaDB with the email so that we know which tasks we can suggest to you.
* If this is your first project, check out the[Suggested Development](project-suggestions.md) page. It lists\
  projects that will make a good start.
* Join MariaDB's Zulip instance at [mariadb.zulipchat.com](https://mariadb.zulipchat.com) and ask for suggestions.
* Join #/maria on[IRC](../../../en/irc/) and ask for suggestions.

If you have your own ideas, please submit them to [JIRA](../../development-articles/general-development-information/tools/jira.md) so other\
MariaDB developers can comment on them and suggest how to implement them. You\
can of course also use the[maria-developers](https://lists.mariadb.org/postorius/lists/developers.lists.mariadb.org/) list for this.

## What to Expect From a MariaDB Server Developer

This section is mainly directed to developers with commit rights to the MariaDB git repository. However, we hope it’s also useful for anyone wanting to contribute code to MariaDB to know what a reviewer will expect from them.

This is not about coding style or if one should prefer C instead of C++. That would be a separate topic that should be created sooner or later.

### The Basics

When coding, try to create code that 'never has to be changed again'. Try to make the code as performant as possible. In general it is acceptable to spend 50% more time to make the code 15% faster than what you originally intended. Take that into account when you plan your time estimates! That said, don't try to add classes or functionality that is not yet used.

The code should be easy to read and follow the coding standards of the project. Patches that are smaller and simpler are often better than complex solutions. Don't make the server depend on new external libraries without first checking with Sergei or Monty!

Add code comments for anything that is not obvious. When possible, use assertions within the code to document expectations of arguments etc. In general, if the code requires complex comments, think if there is a better way to structure the logic. Simpler is often better and with fewer bugs.

### What to Have in a Commit Comment

* Jira issue number and summary ex:[MDEV-23839](https://jira.mariadb.org/browse/MDEV-23839) innodb\_fast\_shutdown=0 hang on change buffer merge
* An empty line
* A short description of the problem
* A description of the solution
* Any extra information needed to understand the patch
* The commit message should be self contained and the reviewer shouldn't preferably have to look at the Jira at all to understand the commit. This doesn’t mean that the commit message should include all background and different design options considered, as the Jira should contain.
* Name of all reviewers and authors should be clear from the commit message. The preferred way would be (one line per person)
  * Reviewed-by: email
  * Co-authored-by: email
  * See [creating-a-commit-with-multiple-authors](https://docs.github.com/en/free-pro-team@latest/github/committing-changes-to-your-project/creating-a-commit-with-multiple-authors) for details
* The default is that all code should be reviewed. Only in really extraordinary cases, like merge (where the original code was already reviewed) then it can be self-reviewed, which should clear from the commit. In this case the code should of course be tested extra carefully both locally and in buildbot before pushing.

### Testing

* All code should have a test case that shows that the new code works or, in case of a bug fix, that the problem is fixed! It should fail with an unpatched server and work with the new version. In the extreme case that a test case is practically impossible to do, there needs to be documentation (in the commit message, optionally also in Jira) how the code was tested.
* The test case should have a reference to the Jira issue, if such one exists.
* Patches related to performance should be tested either by the developer (for simple commits) or by performance testers. The result should be put in Jira with a summary in the commit.
* Complex patches and should be tested by QA in a bb- branch before pushing. The Jira entry should include information that this has been done and what kind of test has been run.
  * Example: `git push --force origin HEAD:bb-11.8-MDEV-1234`
* For anything not trivial, one should run either Valgrind or ASAN/MSAN on the new code. (Buildbot will do this for you if you can’t get valgrind or ASAN to work). At least the test case added should be tested by either. If the developer cannot do that for some reason, he should check the buildbot builders that do this and ensure that at least his test case doesn’t give any warnings about using not initialized memory or other failures.
* For complex code the developer should preferably use gcov or some similar tool to ensure that at least not all not-error branches are executed. “mtr --gcov” or “dgcov.pl” can help you with this.

### Getting Your Code into the Main MariaDB Tree

All code in MariaDB comes from one of the following sources:

* MySQL
* Code developed by people employed by the [MariaDB Foundation](https://mariadb.org).
* Code developed by people employed by [MariaDB Corporation](https://mariadb.com).
* Code shared with the MariaDB Foundation under the [MCA](../company-and-community/legal-documents/mca.md).
* Code with a known origin that is under a permissive license (BSD or public domain).

If you want the code to be part of the main [MariaDB](../../../en/mariadb/) tree, you also have to\
give the MariaDB Foundation a shared copyright to your code. This is needed so\
that the foundation can offer the code to other projects (like MySQL).

You do this by either:

1. Signing the MariaDB Contributor Agreement\
   ([MCA](../company-and-community/legal-documents/mca.md)) and then scanning and sending it to the foundation.
2. Sending an email to[maria-developers](https://launchpad.net/~maria-developers) where you say\
   that your patch and all fixes to it are provided to the MariaDB Foundation under\
   the [MCA](../company-and-community/legal-documents/mca.md).
3. Licensing your code using the[BSD license](https://opensource.org/licenses/bsd-license.html).

We need shared copyright for the following reasons:

1. to defend the copyright or GPL if someone breaks it (this is the same reason\
   why the Free Software Foundation also[requires copyright assignment](https://www.gnu.org/licenses/why-assign.html)\
   for its code)
2. to be able to donate code to MySQL (for example to fix security bugs or new\
   features)
3. to allow people who have a non-free license to the MySQL code to also use\
   MariaDB (the MCA/BSD allows us to give those companies the rights to all\
   changes between MySQL and MariaDB so they can use MariaDB instead of MySQL)

More information about the MCA can be found on the[MCA FAQ](../company-and-community/legal-documents/mariadb-contributor-agreement-faq.md) page.

### Before Pushing Code to a Stable Branch

* Ensure that you have compiled everything for your new code, in a debug server (configured with cmake -DCMAKE\_BUILD\_TYPE=Debug ) including embedded and all plugins that may be affected by your code change..
* Run the mysql-test-run (mtr) test suite locally with your debug server.
* For anything complex the full test suite should be run.
* For something absolutely trivial, at least the main suite must be run.
* Always push first to a bb- branch to test the code. When the bb- branch is green in [buildbot](https://buildbot.mariadb.org/#/grid) you can push to the main branch. Take care of checking that Windows builds compiles (take extra care of checking this as this often fails) and that valgrind and msan builds doesn’t show any problems with your new test cases.
  * You can find your push at the link similar to [grid?branch=your-branch-name](https://buildbot.mariadb.org/#/grid?branch=your-branch-name).
* If you have to do a rebase before pushing, you have to start from the beginning again.
* When porting code from third parties (such as MySQL), make sure to attribute copyright to the right owner, in the header of each modified file.
* For example:\
  Copyright © 2000, 2018, Oracle and/or its affiliates.\
  Copyright © 2009, 2020, MariaDB
* The only exception is that if the changes are trivial and the rebase was trivial and the local mysql-test-run worked, then you can push directly to the main branch. Only do this if you are 99% sure there are no issues! \* Please don't make us regret that we have made this one exception!\
  When we have protected git branches, then the above rule will be enforced automatically as the protection will take care of this.

### Working on a New Project

* First create a Jira entry that explains the problems and the different solutions that can be used to solve the problem. If there is a new syntax include examples of queries and results.
* After getting an agreement of the to-be-used solution, update the Jira entry with the detailed architecture of the suggested solution.
* When the architecture is reviewed, the assigned developer can start coding.
* When the code is ready, the Jira entry should be updated with the reviewer.
* The reviewer checks the code and either approves it to be pushed or gives comments to the developers that should be fixed. In the later case the developer updates the code and gives it back to the reviewer. This continues until the code is approved.
* If the design changes during the project, the design in Jira needs to be updated.

### Working on a Bug Fix

* Ensure that the Jira issue is up to date.
* For complex bugs that require redesign, follow the process in "Working on a new project"
* For simpler bugs, one can skip the listing of different solutions and architecture. However one should still document the reason for the bug and how it's fixed or to-be-fixed, in a JIRA comment.

### Making Things Easier for Reviewers

* Ensure that code compiles, all MTR test works before asking for a review
* Try to split a bigger project into smaller, self-contained change sets.
* Automatic things, like renames of classes, variables, functions etc is better to be done in a separate commit.

### When Reviewing Code

Remember that the stability and security of any project hangs a lot on the reviewers. If there is something wrong with an accepted patch, it's usually the reviewer who is to be blamed for it, as the reviewer was the one who allowed it to go in!

* Ensure that the code is licensed under New BSD or another approved license for MariaDB (basically any open source license not conflicting with GPL) or that the contributor has signed the MCA.
* GPL is only allowed for code from MySQL (as MariaDB is already depending on MySQL code).
* Ensure that commits are not too large. If the code is very large, give suggestions how to split it into smaller pieces. Merge commits, when rebasing is possible, are not allowed, to keep history linear.
* Check that the commits message describes the commit properly. For code that improves performance, ensure that Jira and the commit message contains information about the improvements.
* Check that there are no unexplained changes in old tests.
* Check the quality of the code (no obvious bugs, right algorithms used)
* Check if any code can be simplified or optimized. Using already existing functions, are loops optimal, are mutexes used correctly etc.
* Check that there is an appropriate test case for the code. See ‘testing’ for what is required!
* Ensuring the code follows the coding standard for MariaDB. This document should be created shortly, but in the meantime ask an old MySQL/MariaDB developer if you are unsure.
* Ensuring that the code follows the architecture agreed for in Jira (if it's in Jira).
* Code should be easy to understand (good code comments, good function and\
  variable names etc).
* Ensure you understand every single line of code that is reviewed. If not, ask the developer to add more comments to get things clear or ask help from another reviewer.
* No performance degradations for all common cases.
* Any code that touches any sensitive area (files, communication, login, encryption or security) needs to have another reviewer that is an expert in this area.

## See Also

* [Getting Started For Developers](https://mariadb.org/get-involved/getting-started-for-developers/) (mariadb.org)
* [Get the Code, Build It, Test It](https://mariadb.org/get-involved/getting-started-for-developers/get-code-build-test/) (mariadb.org)
* [Writing Good Test Cases for MariaDB Server](https://mariadb.org/get-involved/getting-started-for-developers/writing-good-test-cases-mariadb-server/) (mariadb.org)
* [Submitting a Pull Request](https://mariadb.org/get-involved/getting-started-for-developers/submitting-pull-request/) (mariadb.org)
* [Contributing to the MariaDB Project](contributing-to-the-mariadb-project.md) (for non-developers)

```
<<nowiki>>
<<style class="redbox centered">>
**The MariaDB source is now hosted on Github:  https://github.com/MariaDB/server. \\See [[using-git|Using Git]]. The information below is outdated and will be rewritten at some point.**
<</style>>

== Prerequisites

You need [[http://bazaar-vcs.org|Bazaar]] for revision control.

= = = bzr Login Setup

* Get a launchpad account at https://launchpad.net/+login
* When logged in, setup your SSH keys
**  Click your name (top right corner)
**  Click Change Details link (upper right)
**  Click SSH Keys button (middle of page)
**  Upload your public SSH key
([[https://help.launchpad.net/YourAccount/CreatingAnSSHKeyPair|How do I get a public key?]])
* Register yourself with launchpad from your local commandline: <<fixed>>bzr launchpad-login [yourloginid]<</fixed>>

=== Getting the MariaDB Code

# First, [[getting-the-mariadb-source-code|get a clean copy of the MariaDB code]]
(for some, the fastest way to get up and running is to follow the
instructions in the "Source Tree Tarball" section).

#decimal.2 Once you have a clean copy of the source, create a working copy for
  your changes:
<<code lang=sh inline=false indent=1>>
cd $maria-repo # ex: ~/repos/maria
bzr branch trunk maria-fix-bugNNNNNN
cd maria-fix-bugNNNNNN
<</code>>

<<style class="bluebox">>
**Tip:** //Use descriptive names such as maria-fix-bugNNNNNN (where NNNNNN is the bug # of course).//
<</style>>

#decimal.3 You should now be ready to [[generic-build-instructions|Compile MariaDB]]. It's
a good idea to compile at this stage to confirm the source tree you are going
to be hacking on works . . . before you make any changes.

The following pages will help you get up and running with the MariaDB source
code:

* [[getting-the-mariadb-source-code|Getting the MariaDB Source Code]]
* Setup your build environment:
** [[build-environment-setup-for-linux|Linux]]
** [[build-environment-setup-for-mac|Mac]]
** [[building-mariadb-on-windows|Windows]]
* [[compiling-mariadb-from-source|Building MariaDB]]

== Setting up tests

The Maria test suite is contained in the <<code>>./mysql-test/<</code>>
subdirectory of the source tree. The mysql-test directory has two
subdirectories of utmost concern to you, the bug fixer: the <<code>>t/<</code>>
directory and the <<code>>r/<</code>> directory (for "tests" and "results"
respectively). Be sure to check and see if your bug already has a test too.

All the tests are found in the <<code>>t/<</code>> directory. Open up the file
that corresponds to the functionality you are changing (or add a new file) and
add the commands that will reproduce the bug or validate the new functionality.

For example, the test below creates a new test table "t1"; shows us the result
of that CREATE TABLE statement; and lastly, we cleanup the test by dropping the
test table:

<<sql>>
#
# Bug #XXXXXX: INET_ATON() returns signed, not unsigned
#
create table t1 select INET_ATON('255.255.0.1') as `a`;
show create table t1;
drop table t1;
<</sql>>

By adding your test first, it will remind you to re-record the test output file
later (and inform future efforts about your expected output, of course). Now
it's time to make your changes.

Examine existing tests to get a better idea of how you should write your test.

We are always on the lookout for better tests, so if you create new test or
improve an existing test, please upload it to the "private" folder on our
[[FTP]] server and then ping us on [[IRC]] or send a note to the
Maria-Developers mailing list to let us know about it.

== Editing and Adding to Your Contribution

With a working version, you can commence making changes in your new branch,
committing code regularly to your local working copy; feel free to commit early
and often as you will formalize your contribution later with a push and
proposal.
 
<<code lang=sh>>
cd $maria-repo/maria-fix-bugNNNNNN
# Make Changes
bzr commit -m "Merge comment"
<</code>>

Prior to publishing your completed work, you need to confirm that your branch
works as expected and update the test runs.

To allow others to see your commits, you should configure
[[setting-up-and-using-bazaar-bzr-with-mariadb|bzr]] to send its commit emails
to
[[http://lists.askmonty.org/cgi-bin/mailman/listinfo/commits|commits 'at' mariadb 'dot' org]]
email list.

== Testing Your Branch

Make sure you have at least libtool 1.5.22
([[http://www.gnu.org/software/libiconv/|found here]]).

First, check to see that all the tests pass (remember the test you set up
earlier? It should fail. That's ok, you will re-record it momentarily):

<<code lang=sh>>
cd $maria-repo/mysql-test
./mysql-test-run
<</code>>

Any that fail will need to be re-recorded (assuming the new result is correct).

<<code lang=sh>>
cd $maria-repo/mysql-test
./mysql-test-run --record $test # where $test is the name of the test that failed 
<</code>>

You are now ready to merge into trunk.

== Merging Recent Changes

It is important to merge any changes from trunk into your branch before pushing
or publishing.

Update your local trunk.

<<code lang=sh>>
cd $maria-repo 
cd trunk
bzr pull   
<</code>>

Updating your local branch.

<<code lang=sh>>
cd $maria-repo
cd maria-fix-bugNNNNNN
bzr merge ../trunk
bzr commit -m "Merged from trunk"
<</code>>

Conflicts can be resolved in bazaar via:

<<code lang=sh>>
bzr resolve $filename
<</code>>

To revert to your last commit on your branch use:

<<code lang=sh>>
bzr revert $filename
<</code>>

(Note you will need to remerge with trunk before pushing)

Verify differences carefully

<<code lang=sh>>
bzr diff
<</code>>

== Publish Your Branch

When all changes are merged and your changes are all consistent you can push
your branch to LaunchPad

<<code lang=sh inline=false>>
cd $maria-repos/$your-branch # where $your-branch is the branch you want to push (ex: maria-bugNNNN)
bzr push lp:~[yourloginid]/maria/$your-branch
<</code>>

If you find that this takes a very long time (eg. >30 minutes), you may want to
try using '<<code>>bzr init-repo --format=1.9<</code>>' to initialize a new
repo and merge your work into it, then push again.

== How to Propose Branch for Merging
 
On your Launchpad Code page
{{{https://code.launchpad.net/~{yourloginid}/maria/{branch-name} }}} click the
**Propose for merging into another branch** link to propose branch to the
maintainers to be merged into the main trunk.

== Fix Branch (if needed)

If fixes are needed on your branch you will need to: make the changes, re-merge
any new changes to trunk, commit and re-push; you do not need to re-propose.
After the push, LaunchPad will pick up the changes automagically.

Please be aware that changes can take a few minutes for LaunchPad to merge your
new changes into your proposal.

== How to Re-Submit a Proposal

At the moment, this is a tricky process, and none of the "Request another
review" links on Launchpad work.

To resubmit a merge proposal, follow these steps:
# On the main page of the merge proposal, the top line will be something like
  "Status: Needs Review". Just to the right of this is a small button; click on
  this to change the status.
# Select "Resubmit" from the drop down menu and click "Change Status".
# The next page should prompt you to resubmit the merge proposal and inform you
  that the new proposal will supersede the old one
# Click "Resubmit" to finish.

A couple of easy ways to get attention to your proposed merge are:

* Join the #maria [[IRC]] channel on [[https://libera.chat/]] ask people to review/discuss your
  merge.
* Subscribe to and send an email to the
  [[http://launchpad.net/~maria-developers|maria-developers]] group on
  Launchpad.
<</nowiki>>
```

CC BY-SA / Gnu FDL
