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