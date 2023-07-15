# Git Exercises

## Bundle1

### exercise1

```bash

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git init
Reinitialized existing Git repository in E:/Git exercise/.git/

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   ReadMe.md


EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git commit -m "project init "
[main (root-commit) 827c55f] project init
 1 file changed, 1 insertion(+)
 create mode 100644 ReadMe.md

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git remote add origin git@github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 259 bytes | 86.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0      
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 * [new branch]      main -> main

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git status
On branch main
nothing to commit, working tree clean

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git checkout -b dev
Switched to a new branch 'dev'

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/AdelineA/Gym-Bundle-Exercises-Solutions/pull/new/dev
remote:
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git 
 * [new branch]      dev -> dev

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git checkout -b test
Switched to a new branch 'test'

EDELINE@Mugunga MINGW64 /e/Git exercise (test)
$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/AdelineA/Gym-Bundle-Exercises-Solutions/pull/new/test
remote:
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 * [new branch]      test -> test

EDELINE@Mugunga MINGW64 /e/Git exercise (test)
$ git checkout dev
Switched to branch 'dev'

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git branch -D test
Deleted branch test (was 827c55f).

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git push origin --delete test
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 - [deleted]         test

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$
```
# Bundle 1
## Exercise 2

```bash
EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash list

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git status
On branch dev
nothing to commit, working tree clean

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash list
stash@{0}: WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git status
On branch dev
nothing to commit, working tree clean

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash list
stash@{0}: WIP on dev: 827c55f project init
stash@{1}: WIP on dev: 827c55f project init
stash@{2}: WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (755be2104d9d29aea21b7f988e10ca3aef0716a5)

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash list
stash@{0}: WIP on dev: 827c55f project init
stash@{1}: WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (588a3464b4d28e53805b3829a63b7aa59f08e1b8)

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git commit -m "adding home and about page"
[dev bbd9fe9] adding home and about page
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 557 bytes | 92.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
   827c55f..bbd9fe9  dev -> dev

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash list
stash@{0}: WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (488e3d7648c1f398e350c3ba920b067c6ca48f61)

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git reset --hard
HEAD is now at bbd9fe9 adding home and about page

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$
```