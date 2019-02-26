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

```
git merge develop
git commit -m "after merge"

```
