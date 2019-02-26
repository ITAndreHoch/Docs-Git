
# GitHub 

* Github is repository hosting service 
* Github is a Central Repository
* Github is Code Hosting Platform


# 

workflow

<img src="images/git3.png " alt="drawing" width="400"/>


# git-clone - Clone a repository into a new directory

```
$ git clone https://github.com/ITAndreHoch/Git.git
Cloning into 'Git'...
remote: Enumerating objects: 30, done.
remote: Counting objects: 100% (30/30), done.
remote: Compressing objects: 100% (28/28), done.
remote: Total 30 (delta 7), reused 9 (delta 1), pack-reused 0
Unpacking objects: 100% (30/30), done.


```

# git-push - Update remote refs along with associated objects

```
$ git add .
$ git commit -m "branch develop update"
[develop 3012b89] branch develop update
 1 file changed, 1 insertion(+)
 create mode 100644 test1

$ git push origin develop
Counting objects: 3, done.
Delta compression using up to 12 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 284 bytes | 284.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/ITAndreHoch/Git/pull/new/develop
remote: 
To https://github.com/ITAndreHoch/Git.git
 * [new branch]      develop -> develop

```

# git-pull - Fetch from and integrate with another repository or a local branch

```

$ git pull origin master
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/ITAndreHoch/Git
 * branch            master     -> FETCH_HEAD
   143fb29..9e0249b  master     -> origin/master
Updating 143fb29..9e0249b
Fast-forward
 git-advance.md | 68 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 1 file changed, 67 insertions(+), 1 deletion(-)
 ```
 



# 

**Branches**

```

$ git branch develop

$ git branch
  develop
* master

$ git checkout develop
Switched to branch 'develop'

$ git branch
* develop
  master

$ ls -la
total 16
drwxr-xr-x   6 andrzejhochbaum  staff   192 Feb 25 14:33 .
drwxr-xr-x   4 andrzejhochbaum  staff   128 Feb 25 14:33 ..
drwxr-xr-x  12 andrzejhochbaum  staff   384 Feb 25 14:34 .git
-rw-r--r--   1 andrzejhochbaum  staff  4090 Feb 25 14:33 README.md
-rw-r--r--   1 andrzejhochbaum  staff   201 Feb 25 14:33 git-advance.md
drwxr-xr-x   5 andrzejhochbaum  staff   160 Feb 25 14:33 images

$ touch test1
$ echo "Test1" > test1 

$ ls -la
total 24
drwxr-xr-x   7 andrzejhochbaum  staff   224 Feb 25 14:35 .
drwxr-xr-x   4 andrzejhochbaum  staff   128 Feb 25 14:33 ..
drwxr-xr-x  12 andrzejhochbaum  staff   384 Feb 25 14:34 .git
-rw-r--r--   1 andrzejhochbaum  staff  4090 Feb 25 14:33 README.md
-rw-r--r--   1 andrzejhochbaum  staff   201 Feb 25 14:33 git-advance.md
drwxr-xr-x   5 andrzejhochbaum  staff   160 Feb 25 14:33 images
-rw-r--r--   1 andrzejhochbaum  staff     6 Feb 25 14:36 test1

$ git add .

$ git commit -m "branch develop update"
[develop 3012b89] branch develop update
 1 file changed, 1 insertion(+)
 create mode 100644 test1

$ git push origin develop
Counting objects: 3, done.
Delta compression using up to 12 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 284 bytes | 284.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/ITAndreHoch/Git/pull/new/develop
remote: 
To https://github.com/ITAndreHoch/Git.git
 * [new branch]      develop -> develop

$ git branch
* develop
  master

```

# Git Merge

* Branch Develop has one file more than master: test1


We need to mergge develop branch to master:


```
$ git branch
* develop
  master

$ git merge develop
Already up to date.

$ ls -la           
total 24
drwxr-xr-x   7 andrzejhochbaum  staff   224 Feb 25 14:51 .
drwxr-xr-x   4 andrzejhochbaum  staff   128 Feb 25 14:33 ..
drwxr-xr-x  15 andrzejhochbaum  staff   480 Feb 25 14:52 .git
-rw-r--r--   1 andrzejhochbaum  staff  4090 Feb 25 14:33 README.md
-rw-r--r--   1 andrzejhochbaum  staff   201 Feb 25 14:51 git-advance.md
drwxr-xr-x   5 andrzejhochbaum  staff   160 Feb 25 14:33 images
-rw-r--r--   1 andrzejhochbaum  staff     6 Feb 25 14:51 test1

$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

$ git branch
  develop
* master

```

Merge

```
$ git merge develop
Merge made by the 'recursive' strategy.
 test1 | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 test1

$ ls -la
total 24
drwxr-xr-x   7 andrzejhochbaum  staff   224 Feb 25 14:52 .
drwxr-xr-x   4 andrzejhochbaum  staff   128 Feb 25 14:33 ..
drwxr-xr-x  15 andrzejhochbaum  staff   480 Feb 25 14:53 .git
-rw-r--r--   1 andrzejhochbaum  staff  4090 Feb 25 14:33 README.md
-rw-r--r--   1 andrzejhochbaum  staff  1990 Feb 25 14:52 git-advance.md
drwxr-xr-x   5 andrzejhochbaum  staff   160 Feb 25 14:33 images
-rw-r--r--   1 andrzejhochbaum  staff     6 Feb 25 14:52 test


```
**Acknowledge merge request**

<img src="images/git4.png " alt="drawing" width="600"/>


<img src="images/git5.png " alt="drawing" width="600"/>

# GIT ROLLBACK

```
$ git log
commit e322ced72aa981c76fc85ccaf1ddcf182c4b47e1 (HEAD -> master, origin/master, origin/HEAD)
Author: Andrzej Hochbaum <a.hochbaum@webellian.com>
Date:   Mon Feb 25 15:29:49 2019 +0100

    2222222

commit 36978f8538916146c75615dbd1d48b7a9ec82e3b
Merge: 334867f da601b1
Author: Andrzej Hochbaum <a.hochbaum@webellian.com>
Date:   Mon Feb 25 15:25:29 2019 +0100

    Merge branch 'master' of https://github.com/ITAndreHoch/Git

commit 334867f7af57e1715fd6eb762fadc711fc414005
Author: Andrzej Hochbaum <a.hochbaum@webellian.com>
Date:   Mon Feb 25 15:24:14 2019 +0100

    add line to git-advance

commit da601b19dbb76bceaa7c086342a1c6ee1fe7615f
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Mon Feb 25 15:15:41 2019 +0100

    Update git-advance.md
    
```


 **git reset: git-reset - Reset current HEAD to the specified state**
 
 HEAD is a reference to the last commit in the currently check-out branch. You can think of the HEAD as the "current branch". When you switch branches with git checkout, the HEAD revision changes to point to the tip of the new branch. You can see what HEAD points to by doing: cat .git/HEAD.
 
 
 ```
$ git reset --hard 36978f8538916146c75615dbd1d48b7a9ec82e3b
HEAD is now at 36978f8 Merge branch 'master' of https://github.com/ITAndreHoch/Git


$ git push origin master -f
Total 0 (delta 0), reused 0 (delta 0)
To https://github.com/ITAndreHoch/Git.git
 + e322ced...36978f8 master -> master (forced update)

```

**Second example: Rollback:

1. Modyfing one file:

```
cat git-advance.md | more
# test1
# GitHub 

[..]

```

vi git-advance.md

```
cat git-advance.md | more
# test2
# GitHub 
[..]

```

2. check status:

```
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   git-advance.md

no changes added to commit (use "git add" and/or "git commit -a")
```

3. Reset. git-reset - Reset current HEAD to the specified state

```
$ git reset HEAD git-advance.md 
Unstaged changes after reset:
M	git-advance.md
```
4. checkout. git-checkout - Switch branches or restore working tree files

```
$ git checkout -- git-advance.md 

$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

$ more git-advance.md 
# test1
# GitHub 

[..]

```

**GIT MV. git-mv - Move or rename a file, a directory, or a symlink**

```

Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git mv ala.txt bartek.txt

Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	renamed:    ala.txt -> bartek.txt

Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git add .
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git commit -m "rename files"
[master c2693c4] rename files
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename ala.txt => bartek.txt (100%)


$ ls -la
total 32
drwxr-xr-x   7 andrzejhochbaum  staff   224 Feb 26 12:18 .
drwxr-xr-x   4 andrzejhochbaum  staff   128 Feb 25 14:33 ..
drwxr-xr-x  15 andrzejhochbaum  staff   480 Feb 26 12:19 .git
-rw-r--r--   1 andrzejhochbaum  staff  4090 Feb 25 14:33 README.md
-rw-r--r--   1 andrzejhochbaum  staff    12 Feb 26 12:17 bartek.txt
-rw-r--r--   1 andrzejhochbaum  staff  7855 Feb 26 12:17 git-advance.md
drwxr-xr-x   7 andrzejhochbaum  staff   224 Feb 25 15:12 images
```







