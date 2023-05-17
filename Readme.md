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

##Exercise 2

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
