

# GIT LOG



git-log - Show commit logs


```

Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git log
commit c2693c41d012fa2d111e2baf6c80a889479490f9 (HEAD -> master)
Author: Andrzej Hochbaum <a.hochbaum@webellian.com>
Date:   Tue Feb 26 12:19:11 2019 +0100

    rename files

commit af29ebd95251e46cadf929410f4989471afd3f96 (origin/master, origin/HEAD)
Author: Andrzej Hochbaum <a.hochbaum@webellian.com>
Date:   Tue Feb 26 12:17:55 2019 +0100

    ala.txt

commit 57064d4962ded3db1cbef7d32d444533981f9974
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Tue Feb 26 12:15:01 2019 +0100

    Update git-advance.md

commit 633d706145901c4b995d075d7eb14ef9877d479d
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Mon Feb 25 15:44:54 2019 +0100

    Update git-advance.md

commit 87e0b399b83ffd5d3dc321bb38d5a9087ef674d3
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Mon Feb 25 15:43:49 2019 +0100

    Update git-advance.md

commit 4662a89de56646bf4b5864af3b3ef31320f9c976
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Mon Feb 25 15:43:34 2019 +0100

    Update git-advance.md

commit c0419fc6722a734ff284cf9f154a8e9a887d6417
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Mon Feb 25 15:42:15 2019 +0100

    Update git-advance.md

commit 36978f8538916146c75615dbd1d48b7a9ec82e3b
Merge: 334867f da601b1
Author: Andrzej Hochbaum <a.hochbaum@webellian.com>
Date:   Mon Feb 25 15:25:29 2019 +0100

[..]

```

git log --online

```
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git log --oneline
c2693c4 (HEAD -> master) rename files
af29ebd (origin/master, origin/HEAD) ala.txt
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
d350aee (origin/develop, develop) next commit develop - test2
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
```


git log specific file


```
Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git log -- git-advance.md 
commit 57064d4962ded3db1cbef7d32d444533981f9974
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Tue Feb 26 12:15:01 2019 +0100

    Update git-advance.md

commit 633d706145901c4b995d075d7eb14ef9877d479d
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Mon Feb 25 15:44:54 2019 +0100

    Update git-advance.md

commit 87e0b399b83ffd5d3dc321bb38d5a9087ef674d3
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Mon Feb 25 15:43:49 2019 +0100

    Update git-advance.md

commit 4662a89de56646bf4b5864af3b3ef31320f9c976
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Mon Feb 25 15:43:34 2019 +0100

    Update git-advance.md

[..]



$ git log --oneline -- git-advance.md 
57064d4 Update git-advance.md
633d706 Update git-advance.md
87e0b39 Update git-advance.md
4662a89 Update git-advance.md
c0419fc Update git-advance.md
36978f8 Merge branch 'master' of https://github.com/ITAndreHoch/Git
334867f add line to git-advance
da601b1 Update git-advance.md
5b0ed43 Update git-advance.md
68759df Update git-advance.md
ba90ab4 Update git-advance.md
2053dbf Update git-advance.md
9e0249b Update git-advance.md
143fb29 Update git-advance.md
930f81e Update git-advance.md
cfd5e93 Update git-advance.md
3f092de Create git-advance.md

```


comparision two commits:


```
$ git diff 15c3f3b d0908b8
diff --git a/ala.txt b/ala.txt
deleted file mode 100644
index a5bce3f..0000000
--- a/ala.txt
+++ /dev/null
@@ -1 +0,0 @@
-test1

```
