
# STASH - Stash the changes in a dirty working directory away


You can use git stash - if you don’t want to do a commit of half-done work just so you can get back to this point later. 
The answer to this issue is the git stash command.

Stashing takes the dirty state of your working directory — that is, your modified tracked files and staged changes — and saves
it on a stack of unfinished changes that you can reapply at any time.

**example**

create new file

```
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ echo "test45" > awsd
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	awsd

nothing added to commit but untracked files present (use "git add" to track)


Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git add .
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   awsd

```

stash

```
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git stash
Saved working directory and index state WIP on master: 21702d1 Update rebase.md

Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git status
On branch master
nothing to commit, working tree clean


Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git stash list
stash@{0}: WIP on master: 21702d1 Update rebase.md
```

Exit from the stash

```
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git stash apply
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   awsd


Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   awsd

```
