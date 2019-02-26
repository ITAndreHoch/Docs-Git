
# tagging




```

Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git tag -a v1.0 -m 'my version 1.0'
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git tag
v1.0
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git show v1.0
tag v1.0
Tagger: Andrzej Hochbaum <a.hochbaum@webellian.com>
Date:   Tue Feb 26 17:26:42 2019 +0100

my version 1.0

commit b61fce43d6576ecc4fa721f2a1af66eca4813ac7 (HEAD -> master, tag: v1.0, origin/master)
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Tue Feb 26 17:22:19 2019 +0100

    Create git-stash.md

diff --git a/git-stash.md b/git-stash.md
new file mode 100644
index 0000000..a13ce1f
--- /dev/null
+++ b/git-stash.md
@@ -0,0 +1,73 @@
+
+# STASH - Stash the changes in a dirty working directory away
+
+
+You can use git stash - if you don<E2><80><99>t want to do a commit of half-done work just so you can get back to this point later. 
+The answer to this issue is the git stash command.
+
+Stashing takes the dirty state of your working directory <E2><80><94> that is, your modified tracked files and staged changes <E2><80><94> and saves
+it on a stack of unfinished changes that you can reapply at any time.
+
+**example**
+
+create new file
+
+```
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ echo "test45" > awsd
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git status
+On branch master
+Untracked files:
+  (use "git add <file>..." to include in what will be committed)
+
+       awsd
+
+nothing added to commit but untracked files present (use "git add" to track)
+
+
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git add .
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git status
+On branch master
+Changes to be committed:
+  (use "git reset HEAD <file>..." to unstage)
+
+       new file:   awsd
+
+```
+
+stash
+
+```
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git stash
+Saved working directory and index state WIP on master: 21702d1 Update rebase.md
+
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git status
+On branch master
+nothing to commit, working tree clean
+
+
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git stash list
+stash@{0}: WIP on master: 21702d1 Update rebase.md
+```
+
+Exit from the stash
+
+```
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git stash apply
+On branch master
+Changes to be committed:
+  (use "git reset HEAD <file>..." to unstage)
+
+       new file:   awsd
+
+
+Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git status
+On branch master
+Changes to be committed:
+  (use "git reset HEAD <file>..." to unstage)
+
+       new file:   awsd
+
+```
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git log --oneline
b61fce4 (HEAD -> master, tag: v1.0, origin/master) Create git-stash.md
21702d1 Update rebase.md
d69f67d Add files via upload
4cf4a72 Update rebase.md
fbbd65d Update rebase.md
2cfe1ee Delete git7.png
b202aae Add files via upload
dde9571 Add files via upload
9647d87 Update rebase.md
01c18cd Update branches.md
23b56b6 Update branches.md
677ea46 Update branches.md
9b36aa2 Create rebase.md
4991fd3 Update branches.md
a134ca4 Rename branches to branches.md
45c06d9 Create branches
5c71f3a Update gitlog.md
f7e4cbe Delete test2
fc7466a Update and rename ala.txt to testignore.txt
1ce25ea Update exclude-files.md
bdf9220 Update exclude-files.md
a89c786 Create exclude-files.md
a38a333 test
6d9148f gitignore
e5c3208 next
ad132a5 gitignore
15c3f3b next ala
d0908b8 next one
a20e8c1 Merge branch 'master' of https://github.com/ITAndreHoch/Git
f7f30c4 Create alias.md
3ebe2fd Update gitlog.md
cab3fd0 Create gitlog.md
392bc38 Update git-advance.md
c2693c4 rename files
af29ebd ala.txt
57064d4 Update git-advance.md
633d706 Update git-advance.md
87e0b39 Update git-advance.md
4662a89 Update git-advance.md
c0419fc Update git-advance.md
36978f8 Merge branch 'master' of https://github.com/ITAndreHoch/Git
334867f add line to git-advance
da601b1 Update git-advance.md
5b0ed43 Update git-advance.md
c132882 delete files
ac526a9 Merge branch 'master' of https://github.com/ITAndreHoch/Git
90711a7 Merge pull request #2 from ITAndreHoch/develop
355a99b Merge branch 'develop'
d350aee next commit develop - test2
e737562 Merge pull request #1 from ITAndreHoch/develop
68759df Update git-advance.md
ac12ae9 Merge branch 'develop'
ba90ab4 Update git-advance.md
2053dbf Update git-advance.md
9e0249b Update git-advance.md
3012b89 branch develop update
143fb29 Update git-advance.md
930f81e Update git-advance.md
cfd5e93 Update git-advance.md
b8e88a5 Update README.md
a63da4e Add files via upload
3f092de Create git-advance.md
ac90247 next commit
5225f51 second commit
7883bd4 first commit
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git tag -a v0.4 -m 'my version 0.4' 4662a89
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git tag
v0.4
v1.0
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ 
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git show v0.4
tag v0.4
Tagger: Andrzej Hochbaum <a.hochbaum@webellian.com>
Date:   Tue Feb 26 17:28:50 2019 +0100

my version 0.4

commit 4662a89de56646bf4b5864af3b3ef31320f9c976 (tag: v0.4)
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Mon Feb 25 15:43:34 2019 +0100

    Update git-advance.md

diff --git a/git-advance.md b/git-advance.md
index 3426f6c..b077a41 100644
--- a/git-advance.md
+++ b/git-advance.md
@@ -237,6 +237,10 @@ Date:   Mon Feb 25 15:15:41 2019 +0100
     
 ```
 
+
+ **git reset: git-reset - Reset current HEAD to the specified state**
+ 
+ ```
 $ git reset --hard 36978f8538916146c75615dbd1d48b7a9ec82e3b
 HEAD is now at 36978f8 Merge branch 'master' of https://github.com/ITAndreHoch/Git
 
@@ -246,7 +250,7 @@ Total 0 (delta 0), reused 0 (delta 0)
 To https://github.com/ITAndreHoch/Git.git
  + e322ced...36978f8 master -> master (forced update)
 
-
+```
 
 
```
