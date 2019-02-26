
# tagging

git-tag - Create, list, delete or verify a tag object signed with GPG


Add tag:

```

Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git tag -a v1.0 -m 'my version 1.0'


Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git tag
v1.0


Andrzejs-MacBook-Pro:Git andrzejhochbaum$ git show v1.0
tag v1.0
Tagger: Andrzej Hochbaum <a.hochbaum@webellian.com>
Date:   Tue Feb 26 17:26:42 2019 +0100

my version 1.0

commit b61fce43d6576ecc4fa721f2a1af66eca4813ac7 (HEAD -> master, tag: v1.0, origin/master)
Author: AndreHoch <39279226+ITAndreHoch@users.noreply.github.com>
Date:   Tue Feb 26 17:22:19 2019 +0100

    Create git-stash.md

[..]

```

Add tag from commit history
```
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
[..]
```

Add next tag

```
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

[..]
 
```
