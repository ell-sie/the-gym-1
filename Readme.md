Exercise 1
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

