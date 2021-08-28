Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/
$ git clone https://github.com/hassan510-cmd/day2_vcs.git
Cloning into 'day2_vcs'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/
$ cd day2_vcs

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (master)
$ git switch -C Arafa
Switched to a new branch 'Arafa'

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (master)
$ git branch
Arafa

- master

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (master)
$ ssh-add.exe ~/.ssh/id_rsa &>/dev/null

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (master)
$ git config --global credential.helper cache

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (master)
$ eval `ssh-agent.exe -s`
Agent pid 4893

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (master)
$ ssh-add.exe ~/.ssh/\*\_rsa
Enter passphrase for /c/Users/Arfa/.ssh/id_rsa:
Identity added: /c/Users/Arfa/.ssh/id_rsa (bmagpul@gmail.com)

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git branch

- Arafa
  master

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git push -u origin Arafa

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git branch -vv

- Arafa 987ed62 [origin/Arafa] arafa's commit
  master 9b7d872 [origin/master] hassan first commit

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git branch -r | grep -v '\->' | while read remote; do git branch --track "${remote#origin/}" "$remote"; done
fatal: A branch named 'Arafa' already exists.
Branch 'antonbranch' set up to track remote branch 'antonbranch' from 'origin'.
Branch 'hasan_branch' set up to track remote branch 'hasan_branch' from 'origin'.
fatal: A branch named 'master' already exists.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git branch

- Arafa
  antonbranch
  hasan_branch
  master

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ touch script.js app.js source.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ ls
app.js index.html script.js source.py test_hassan.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git status
On branch Arafa
Your branch is up to date with 'origin/Arafa'.

Untracked files:
(use "git add <file>..." to include in what will be committed)
app.js
script.js
source.py

nothing added to commit but untracked files present (use "git add" to track)

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git add .

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git status
On branch Arafa
Your branch is up to date with 'origin/Arafa'.

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: app.js
new file: script.js
new file: source.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git restore --staged app.js

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git status
On branch Arafa
Your branch is up to date with 'origin/Arafa'.

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: script.js
new file: source.py

Untracked files:
(use "git add <file>..." to include in what will be committed)
app.js

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git restore --staged scource.py
error: pathspec 'scource.py' did not match any file(s) known to git

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git status
On branch Arafa
Your branch is up to date with 'origin/Arafa'.

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: script.js
new file: source.py

Untracked files:
(use "git add <file>..." to include in what will be committed)
app.js

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git restore --staged source.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git status
On branch Arafa
Your branch is up to date with 'origin/Arafa'.

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: script.js

Untracked files:
(use "git add <file>..." to include in what will be committed)
app.js
source.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git commit -m "script.js"
[Arafa d932890] script.js
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 script.js

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git add app.js

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git status
On branch Arafa
Your branch is ahead of 'origin/Arafa' by 1 commit.
(use "git push" to publish your local commits)

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: app.js

Untracked files:
(use "git add <file>..." to include in what will be committed)
source.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git commit -m "upload app.js 'Arafa'"
[Arafa 76269f9] upload app.js 'Arafa'
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 app.js

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git status
On branch Arafa
Your branch is ahead of 'origin/Arafa' by 2 commits.
(use "git push" to publish your local commits)

Untracked files:
(use "git add <file>..." to include in what will be committed)
source.py

nothing added to commit but untracked files present (use "git add" to track)

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git add source.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git status
On branch Arafa
Your branch is ahead of 'origin/Arafa' by 2 commits.
(use "git push" to publish your local commits)

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: source.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git commit -m "upload source.py 'Arafa'"
[Arafa a8597fd] upload source.py 'Arafa'
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 source.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git log
commit a8597fd754a10f40800ebeceb03f059304dbd1d0 (HEAD -> Arafa)
Author: bruno-0 <bmagpul@gmail.com>
Date: Sat Aug 28 15:04:31 2021 +0200

    upload source.py 'Arafa'

commit 76269f94c1dc5f750c5f281827cc57ff949a7045
Author: bruno-0 <bmagpul@gmail.com>
Date: Sat Aug 28 15:03:41 2021 +0200

    upload app.js 'Arafa'

commit d932890db8217d0639557b3c2cbb6a06ab1bb188
Author: bruno-0 <bmagpul@gmail.com>
Date: Sat Aug 28 15:02:54 2021 +0200

    script.js

commit 987ed62789dc66768678446a3a81e88a3edd7359 (origin/Arafa)
Author: bruno-0 <bmagpul@gmail.com>
Date: Sat Aug 28 14:32:40 2021 +0200

    arafa's commit

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git push -u origin
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 628 bytes | 125.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To github.com:hassan510-cmd/day2_vcs.git
987ed62..a8597fd Arafa -> Arafa
Branch 'Arafa' set up to track remote branch 'Arafa' from 'origin'.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git revert 76269f94c1dc5f750c5f281827cc57ff949a7045
Removing app.js
[Arafa 10dec3d] Revert "upload app.js 'Arafa'"
1 file changed, 0 insertions(+), 0 deletions(-)
delete mode 100644 app.js

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git push origin Arafa
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 275 bytes | 137.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:hassan510-cmd/day2_vcs.git
a8597fd..10dec3d Arafa -> Arafa

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git merge origin/hasan_branch
Merge made by the 'recursive' strategy.
from_hassan_branch.py | 0
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 from_hassan_branch.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git push
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 517 bytes | 258.00 KiB/s, done.
Total 4 (delta 2), reused 1 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To github.com:hassan510-cmd/day2_vcs.git
10dec3d..93b98cc Arafa -> Arafa

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git merge origin/antonbranch
Merge made by the 'recursive' strategy.
.vs/slnx.sqlite | Bin 0 -> 90112 bytes
indexhtmlanton.html | 0
login.js | 6 ++++++
3 files changed, 6 insertions(+)
create mode 100644 .vs/slnx.sqlite
create mode 100644 indexhtmlanton.html
create mode 100644 login.js

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git push -u
Enumerating objects: 18, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 4 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (16/16), 4.98 KiB | 637.00 KiB/s, done.
Total 16 (delta 4), reused 9 (delta 1), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
To github.com:hassan510-cmd/day2_vcs.git
93b98cc..c6eae68 Arafa -> Arafa
Branch 'Arafa' set up to track remote branch 'Arafa' from 'origin'.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ code .

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git add .

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git commit -m "update to script.js by arafa"
[Arafa 27b79d1] update to script.js by arafa
1 file changed, 1 insertion(+)

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git push -u
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 281 bytes | 140.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:hassan510-cmd/day2_vcs.git
c6eae68..27b79d1 Arafa -> Arafa
Branch 'Arafa' set up to track remote branch 'Arafa' from 'origin'.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git checkout hasan_branch
Switched to branch 'hasan_branch'
Your branch is up to date with 'origin/hasan_branch'.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git pull
remote: Enumerating objects: 27, done.
remote: Counting objects: 100% (27/27), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 24 (delta 12), reused 21 (delta 9), pack-reused 0
Unpacking objects: 100% (24/24), 2.49 KiB | 12.00 KiB/s, done.
From github.com:hassan510-cmd/day2_vcs
268279f..4eb981b hasan_branch -> origin/hasan_branch
47b714a..ac09ab9 antonbranch -> origin/antonbranch
Updating 268279f..4eb981b
Fast-forward
from_hassan_branch.py => 1.py | 0
2.py | 0
3.py | 0
index.html | 0
script.js | 0
some_updates.js | 0
source.py | 0
7 files changed, 0 insertions(+), 0 deletions(-)
rename from_hassan_branch.py => 1.py (100%)
create mode 100644 2.py
create mode 100644 3.py
create mode 100644 index.html
create mode 100644 script.js
create mode 100644 some_updates.js
create mode 100644 source.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git checkout Arafa
Switched to branch 'Arafa'
Your branch is up to date with 'origin/Arafa'.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git log --oneline
27b79d1 (HEAD -> Arafa, origin/Arafa) update to script.js by arafa
c6eae68 Merge remote-tracking branch 'origin/antonbranch' into Arafa
93b98cc Merge remote-tracking branch 'origin/hasan_branch' into Arafa Merge with hassan branch
10dec3d Revert "upload app.js 'Arafa'"
a8597fd upload source.py 'Arafa'
76269f9 upload app.js 'Arafa'
d932890 script.js
47b714a (antonbranch) anton add index html
987ed62 arafa's commit
43e8979 anton samir add function 2login
5ed912e login js anton samir
268279f from hassan_branch
9b7d872 (origin/master, origin/HEAD, master) hassan first commit

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git revert 9b7d872
Removing test_hassan.py
[Arafa cc5cf9f] Revert "hassan first commit"
1 file changed, 0 insertions(+), 0 deletions(-)
delete mode 100644 test_hassan.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 268 bytes | 268.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:hassan510-cmd/day2_vcs.git
88fb8d5..cc5cf9f Arafa -> Arafa

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git log -n 5
commit cc5cf9f6c1634fc51064bf3bfd8b7e1dc6b6706a (HEAD -> Arafa, origin/Arafa)
Author: bruno-0 <bmagpul@gmail.com>
Date: Sat Aug 28 15:42:56 2021 +0200

    Revert "hassan first commit"

    This reverts commit 9b7d87284468456081cda69f6ec6708657ec23b4.

commit 88fb8d5e362a00b697f7e87e77c21040b0a9ba55
Author: bruno-0 <bmagpul@gmail.com>
Date: Sat Aug 28 15:39:43 2021 +0200

    Revert "from hassan_branch"

    This reverts commit 268279fe3f1e6326a1318f7089919ac463cbb492.

commit 27b79d197fdd53fd570480aed7286d0a1fdfed3d
Author: bruno-0 <bmagpul@gmail.com>
Date: Sat Aug 28 15:28:20 2021 +0200

    update to script.js by arafa

commit c6eae68d03732e015e35549ee3414ce030776a5b
Merge: 93b98cc 47b714a
Author: bruno-0 <bmagpul@gmail.com>
Date: Sat Aug 28 15:22:28 2021 +0200

    Merge remote-tracking branch 'origin/antonbranch' into Arafa

commit 93b98cc73954f78eb6f340594eec877636f05098
Merge: 10dec3d 268279f
Author: bruno-0 <bmagpul@gmail.com>
Date: Sat Aug 28 15:18:26 2021 +0200

    Merge remote-tracking branch 'origin/hasan_branch' into Arafa
    Merge with hassan branch

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (Arafa)
$ git checkout hasan_branch
Switched to branch 'hasan_branch'
Your branch is up to date with 'origin/hasan_branch'.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git status
On branch hasan_branch
Your branch is up to date with 'origin/hasan_branch'.

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: 1.py

no changes added to commit (use "git add" and/or "git commit -a")

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git add .

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git commit -m "arafa's conflict commit"
[hasan_branch 366531a] arafa's conflict commit
1 file changed, 1 insertion(+)

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git push
To github.com:hassan510-cmd/day2_vcs.git
! [rejected] hasan_branch -> hasan_branch (fetch first)
error: failed to push some refs to 'github.com:hassan510-cmd/day2_vcs.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git pull
remote: Enumerating objects: 28, done.
remote: Counting objects: 100% (25/25), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 19 (delta 5), reused 17 (delta 3), pack-reused 0
Unpacking objects: 100% (19/19), 4.41 KiB | 2.00 KiB/s, done.
From github.com:hassan510-cmd/day2_vcs
4eb981b..0892d4c hasan_branch -> origin/hasan_branch
ac09ab9..5fc770e antonbranch -> origin/antonbranch

- [new branch] arafa -> origin/arafa
  Removing test_hassan.py
  Auto-merging 1.py
  CONFLICT (content): Merge conflict in 1.py
  Automatic merge failed; fix conflicts and then commit the result.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git pull
error: Pulling is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git push
To github.com:hassan510-cmd/day2_vcs.git
! [rejected] hasan_branch -> hasan_branch (fetch first)
error: failed to push some refs to 'github.com:hassan510-cmd/day2_vcs.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git pull
error: Pulling is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git checkout master
error: you need to resolve your current index first
1.py: needs merge

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git merge master
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git status
On branch hasan_branch
Your branch and 'origin/hasan_branch' have diverged,
and have 1 and 9 different commits each, respectively.
(use "git pull" to merge the remote branch into yours)

You have unmerged paths.
(fix conflicts and run "git commit")
(use "git merge --abort" to abort the merge)

Changes to be committed:
deleted: test_hassan.py

Unmerged paths:
(use "git add <file>..." to mark resolution)
both modified: 1.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git add .

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git commit -m "resolving conflict"
[hasan_branch 1dc0886] resolving conflict

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git push
To github.com:hassan510-cmd/day2_vcs.git
! [rejected] hasan_branch -> hasan_branch (non-fast-forward)
error: failed to push some refs to 'github.com:hassan510-cmd/day2_vcs.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git pull
From github.com:hassan510-cmd/day2_vcs

- [new branch] arafa -> origin/arafa
  Auto-merging 1.py
  CONFLICT (content): Merge conflict in 1.py
  Automatic merge failed; fix conflicts and then commit the result.

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git status
On branch hasan_branch
Your branch and 'origin/hasan_branch' have diverged,
and have 2 and 7 different commits each, respectively.
(use "git pull" to merge the remote branch into yours)

You have unmerged paths.
(fix conflicts and run "git commit")
(use "git merge --abort" to abort the merge)

Changes to be committed:
new file: .idea/.gitignore
new file: .idea/day2_vcs.iml
new file: .idea/modules.xml
new file: .idea/vcs.xml
new file: .vs/VSWorkspaceState.json
new file: .vs/day2_vcs/v16/.suo
new file: .vs/slnx.sqlite
modified: 3.py

Unmerged paths:
(use "git add <file>..." to mark resolution)
both modified: 1.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git add .

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch|MERGING)
$ git commit -m "resolving conflict"
[hasan_branch 94d6bc1] resolving conflict

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git push
Enumerating objects: 15, done.
Counting objects: 100% (15/15), done.
Delta compression using up to 4 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (9/9), 901 bytes | 450.00 KiB/s, done.
Total 9 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
To github.com:hassan510-cmd/day2_vcs.git
9548fff..94d6bc1 hasan_branch -> hasan_branch

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (hasan_branch)
$ git checkout master
Switched to branch 'master'
Your branch is behind 'origin/master' by 4 commits, and can be fast-forwarded.
(use "git pull" to update your local branch)

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (master)
$ ls
test_hassan.py

Arafa@RQ MINGW64 ~/Desktop/ITI PYTHON/Week 03/Day_01_VCS/Lect/lab2/day2_vcs (master)
$ git pull
From github.com:hassan510-cmd/day2_vcs

- [new branch] Arafa -> origin/Arafa
  Updating 9b7d872..665ad01
  Fast-forward
  .idea/workspace.xml | 44 +++
  .vs/slnx.sqlite | Bin 0 -> 90112 bytes
  commands.txt | 630 +++++++++++++++++++++++++++++++++++++++++
  lab 2 anton samir command.docx | Bin 0 -> 64800 bytes
  4 files changed, 674 insertions(+)
  create mode 100644 .idea/workspace.xml
  create mode 100644 .vs/slnx.sqlite
  create mode 100644 commands.txt
  create mode 100644 lab 2 anton samir command.docx
