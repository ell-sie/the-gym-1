# Bundle 1

## Exercise 1
```
Lenovo@DESKTOP-6LCGN4B MINGW64 ~ (main)
$ cd git
git-exercises/

Lenovo@DESKTOP-6LCGN4B MINGW64 ~ (main)
$ cd git-exercises/

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git init
Initialized empty Git repository in C:/Users/Lenovo/git-exercises/.git/

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (master)
$ git branch -m main

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ touch bundle-1

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ mv bundle-1 Bundle-1

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ vi Bundle-1

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git add .
warning: LF will be replaced by CRLF in Bundle-1.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git commit -m 'added files'
[main (root-commit) 04aba68] added files
 1 file changed, 1 insertion(+)
 create mode 100644 Bundle-1

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git remote add origin https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git push -u origin
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main


Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 222 bytes | 222.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout -b dev
Switched to a new branch 'dev'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git checkout -b test
Switched to a new branch 'test'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (test)
$ git checkout dev
Switched to branch 'dev'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git branch -D test
Deleted branch test (was 04aba68).

```

## Exercise 2

```

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ touch home.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ vi home.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git add .
warning: LF will be replaced by CRLF in home.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git stash save "home"
Saved working directory and index state On dev: home

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ touch about.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ vi about.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git add .
warning: LF will be replaced by CRLF in about.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git stash save "about"
Saved working directory and index state On dev: about

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ touch team.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ vi team.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git add .
warning: LF will be replaced by CRLF in team.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git stash save "team"
Saved working directory and index state On dev: team

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git stash list
stash@{0}: On dev: team
stash@{1}: On dev: about
stash@{2}: On dev: home
stash@{3}: On dev: changes made to home

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (e83018504509d751540864d0015b6aa499086169)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git stash pop stash@{2}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    about.html

Dropped stash@{2} (1437c8a355b013cbe059b34733a689a36d33df06)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git commit -m 'html files'
[dev 79a3813] html files
 1 file changed, 16 insertions(+)
 create mode 100644 home.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ gut stash list
bash: gut: command not found

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git stash list
stash@{0}: On dev: team
stash@{1}: On dev: home

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is ahead of 'origin/dev' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (f4c5332402f2ba52e76535516244262ca48d6e69)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (dev)
$ git reset --hard HEAD
HEAD is now at 79a3813 html files
```

#Bundle 2

##Exercise 1

```

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/bundle-2)
$ vi services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/bundle-2)
$ git add .
warning: LF will be replaced by CRLF in services.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/bundle-2)
$ git commit -m 'services page'
[ft/bundle-2 6a93753] services page
 1 file changed, 16 insertions(+)
 create mode 100644 services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 533 bytes | 266.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/ell-sie/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
```
## Exercise 2

```
Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ ls
Bundle-1  Readme.md

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ ls
Bundle-1  Readme.md

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git pull
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), 754 bytes | 75.00 KiB/s, done.
From https://github.com/ell-sie/Gym-Git-Exercise-Solutions
   6783228..f1f0d91  main       -> origin/main
Updating 6783228..f1f0d91
Fast-forward
 services.html | 16 ++++++++++++++++
 1 file changed, 16 insertions(+)
 create mode 100644 services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ ls
Bundle-1  Readme.md  services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ vi services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ ls
Bundle-1  Readme.md  services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/
ft/bundle-2            ft/services-redesign

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/service-redesign
error: pathspec 'ft/service-redesign' did not match any file(s) known to git

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/service-redesign
error: pathspec 'ft/service-redesign' did not match any file(s) known to git

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft
error: pathspec 'ft' did not match any file(s) known to git

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout -b ft/services-redesign
fatal: a branch named 'ft/services-redesign' already exists

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ ls
Bundle-1  Readme.md  services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/services-redesign
Switched to branch 'ft/services-redesign'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ ls
Bundle-1  Readme.md

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> ft/services-redesign


Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git push
Everything up-to-date

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git commit -m 'pulled services'
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/services-redesign
Switched to branch 'ft/services-redesign'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ ls
Bundle-1  Readme.md

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git commit -m 'b and r'
On branch ft/services-redesign
nothing to commit, working tree clean

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git branch -d ft/services-redesign
Deleted branch ft/services-redesign (was 6783228).

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout -b ft/services-redesign
Switched to a new branch 'ft/services-redesign'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ ls
Bundle-1  Readme.md  services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ vi services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git commit -m 'added changes to services'
[ft/services-redesign 4fb0b17] added changes to services
 1 file changed, 3 insertions(+), 5 deletions(-)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git push orgin ft/services-redesign
fatal: 'orgin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git push
fatal: The current branch ft/services-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/services-redesign


Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ ^C

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$  git push --set-upstream origin ft/services-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 329 bytes | 329.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/services-redesign' on GitHub by visiting:
remote:      https://github.com/ell-sie/Gym-Git-Exercise-Solutions/pull/new/ft/services-redesign
remote:
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/services-redesign -> ft/services-redesign
branch 'ft/services-redesign' set up to track 'origin/ft/services-redesign'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ vi services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git commit -m 'Add conflicting changes to services.html'
[main d98ebbd] Add conflicting changes to services.html
 1 file changed, 3 insertions(+), 5 deletions(-)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 358 bytes | 358.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
   f1f0d91..d98ebbd  main -> main

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/services-redesign
Switched to branch 'ft/services-redesign'
Your branch is up to date with 'origin/ft/services-redesign'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git diff main
diff --git a/services.html b/services.html
index 20a8fa0..474ce62 100644
--- a/services.html
+++ b/services.html
@@ -8,7 +8,7 @@
 </head>
 <body>
     <h1>
-      second change is the service page
-    <h1>
+       sercvices page
+    </h1>
 </body>
 </html>

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign|MERGING)
$ git commit -m 'merge main branch into ft/services-redesign'
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign|MERGING)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign|MERGING)
$ git commit -m 'merge main branch into ft/services-redesign'
[ft/services-redesign e7c9d6d] merge main branch into ft/services-redesign

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 391 bytes | 130.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
   4fb0b17..e7c9d6d  ft/services-redesign -> ft/services-redesign
```
# Bundle 3

## Exercise 1
```
Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/contact-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/team-page)
$ git log
commit ebd739cbc60979b342e1acc7a96cb632a3817d0e (HEAD -> ft/team-page, origin/ft/team-page)
Author: ll-sie <e.ndiramiye@alustudent.com>
Date:   Fri May 19 23:50:49 2023 +0200

    team page

commit b733dadcc7a7ce2c2d568aee7087ad16a8846616 (origin/main, main, ft/contact-page)
Merge: 77fe50a 1ed2269
Author: ll-sie <e.ndiramiye@alustudent.com>
Date:   Fri May 19 20:28:05 2023 +0200

    Merge branch 'main' of https://github.com/ell-sie/Gym-Git-Exercise-Solutions

commit 77fe50a3fde1717f346a9462e60d2b65a2ae7432
Author: ll-sie <e.ndiramiye@alustudent.com>
Date:   Fri May 19 20:27:25 2023 +0200

    bundle exercise2

commit 1ed2269e46d64df46bf0a4ba35a9d3fc87753eff
Merge: d98ebbd e7c9d6d
:
commit ebd739cbc60979b342e1acc7a96cb632a3817d0e (HEAD -> ft/team-page, origin/ft/team-page)
Author: ll-sie <e.ndiramiye@alustudent.com>
Date:   Fri May 19 23:50:49 2023 +0200

    team page

commit b733dadcc7a7ce2c2d568aee7087ad16a8846616 (origin/main, main, ft/contact-page)
Merge: 77fe50a 1ed2269
Author: ll-sie <e.ndiramiye@alustudent.com>
Date:   Fri May 19 20:28:05 2023 +0200

    Merge branch 'main' of https://github.com/ell-sie/Gym-Git-Exercise-Solutions

commit 77fe50a3fde1717f346a9462e60d2b65a2ae7432
Author: ll-sie <e.ndiramiye@alustudent.com>
Date:   Fri May 19 20:27:25 2023 +0200

    bundle exercise2

commit 1ed2269e46d64df46bf0a4ba35a9d3fc87753eff
Merge: d98ebbd e7c9d6d

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/contact-page)
$ git cherry-pick ebd739cbc60979b342e1acc7a96cb632a3817d0e
[ft/contact-page 325a132] team page
 Date: Fri May 19 23:50:49 2023 +0200
 1 file changed, 16 insertions(+)
 create mode 100644 team.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/contact-page)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/contact-page)
$ git commit -m 'contact page'
On branch ft/contact-page
nothing to commit, working tree clean

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/contact-page)
$  git push --set-upstream origin ft/contact-page

Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 494 bytes | 494.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/ell-sie/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/contact-page)
$

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/faq-page)
$ vi faq.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/faq-page)
$ git add .
warning: LF will be replaced by CRLF in faq.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/faq-page)
$ git commit -m 'contact page'
[ft/faq-page aabb138] contact page
OA 1 file changed, 16 insertions(+)
 create mode 100644 faq.html

OALenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/faq-page)
$  git push --set-upstream origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 231 bytes | 115.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/ell-sie/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/faq-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/team-page)
$ git revert ebd739cbc60979b342e1acc7a96cb632a3817d0e
[ft/team-page ec946e3] Revert "team page"
 1 file changed, 16 deletions(-)
 delete mode 100644 team.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/team-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 248 bytes | 248.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
   ebd739c..ec946e3  ft/team-page -> ft/team-page

```
# Bundle 4
## Exercise 1
```

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git remote add git-copy https://github.com/ell-sie/the-gym-1.git

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ ls
Bundle-1  Readme.md  faq.html  home.html  services.html  team.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ vi home.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git commit -m 'work'
[main 8008797] work
 1 file changed, 1 insertion(+)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 297 bytes | 297.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
   562cba7..8008797  main -> main

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git push git-copy main
Enumerating objects: 66, done.
Counting objects: 100% (66/66), done.
Delta compression using up to 8 threads
Compressing objects: 100% (32/32), done.
Writing objects: 100% (65/65), 13.52 KiB | 4.51 MiB/s, done.
Total 65 (delta 35), reused 57 (delta 31), pack-reused 0
remote: Resolving deltas: 100% (35/35), done.
To https://github.com/ell-sie/the-gym-1.git
   87beef1..6b31a42  main -> main
```
