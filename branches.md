# branches


```
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git checkout
M	ala.txt
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git branch
  develop
* master
```
Create new branch

```
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git branch software
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git branch
  develop
* master
  software
```

Switch to new branch

```
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git  checkout software
M	ala.txt
Switched to branch 'software'

Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git branch
  checkout
  develop
  master
* software

```

Remove branch:

```
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git branch -d software
Deleted branch software (was 182a6d9).

```

Git merge

git-merge - Join two or more development histories together

DESCRIPTION
       Incorporates changes from the named commits (since the time their histories diverged from the
       current branch) into the current branch. This command is used by git pull to incorporate changes
       from another repository and can be used by hand to merge changes from one branch into another.

       Assume the following history exists and the current branch is "master":

                     A---B---C topic
                    /
               D---E---F---G master

       Then "git merge topic" will replay the changes made on the topic branch since it diverged from
       master (i.e., E) until its current commit (C) on top of master, and record the result in a new
       commit along with the names of the two parent commits and a log message from the user describing the
       changes.

                     A---B---C topic
                    /         \
               D---E---F---G---H master

       The second syntax ("git merge --abort") can only be run after the merge has resulted in conflicts.
       git merge --abort will abort the merge process and try to reconstruct the pre-merge state. However,
       if there were uncommitted changes when the merge started (and especially if those changes were
       further modified after the merge was started), git merge --abort will in some cases be unable to
       reconstruct the original (pre-merge) changes. Therefore:

       Warning: Running git merge with non-trivial uncommitted changes is discouraged: while possible, it
       may leave you in a state that is hard to back out of in the case of a conflict.
  

       


  
```
git merge develop
git commit -m "after merge"

```
