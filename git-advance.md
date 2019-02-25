
# GitHub 

* Github is repository hosting service 
* Github is a Central Repository
* Github is Code Hosting Platform


# 

workflow

<img src="images/git3.png " alt="drawing" width="600"/>


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

