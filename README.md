# git exercises assesiment 

## Bundle 1
### Exercise 1

```
andelas-MacBook-Pro:Git-exercises andela$ git init
Initialized empty Git repository in /Users/andela/Desktop/The-GYM/Git-exercises/.git/
andelas-MacBook-Pro:Git-exercises andela$ git branch
andelas-MacBook-Pro:Git-exercises andela$ git branch -M main
error: refname refs/heads/master not found
fatal: Branch rename failed
andelas-MacBook-Pro:Git-exercises andela$ git add .
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "added a readme file"
[master (root-commit) a341c4b] added a readme file
 1 file changed, 4 insertions(+)
 create mode 100644 README.md
andelas-MacBook-Pro:Git-exercises andela$ git branch -M main
andelas-MacBook-Pro:Git-exercises andela$ git branch
* main
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch main
nothing to commit, working tree clean
andelas-MacBook-Pro:Git-exercises andela$ git remote add origin https://github.com/Stevenkwizera06/Git-exercise.git
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch main
nothing to commit, working tree clean
andelas-MacBook-Pro:Git-exercises andela$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

andelas-MacBook-Pro:Git-exercises andela$  git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 268 bytes | 134.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/Stevenkwizera06/Git-exercise.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
andelas-MacBook-Pro:Git-exercises andela$ git checkout -b dev
Switched to a new branch 'dev'
andelas-MacBook-Pro:Git-exercises andela$ git checkout -b test
Switched to a new branch 'test'
andelas-MacBook-Pro:Git-exercises andela$ git checkout dev
Switched to branch 'dev'
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch dev
nothing to commit, working tree clean
andelas-MacBook-Pro:Git-exercises andela$ git branch -D test
Deleted branch test (was a341c4b).

## Bundle 1
### Exercise 2
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        home.html

nothing added to commit but untracked files present (use "git add" to track)
andelas-MacBook-Pro:Git-exercises andela$ git add home.html
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   home.html

andelas-MacBook-Pro:Git-exercises andela$ git stash
Saved working directory and index state WIP on dev: a341c4b added a readme file
andelas-MacBook-Pro:Git-exercises andela$ git stash list
stash@{0}: WIP on dev: a341c4b added a readme file
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        about.html

nothing added to commit but untracked files present (use "git add" to track)
andelas-MacBook-Pro:Git-exercises andela$ git add about.html
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html

andelas-MacBook-Pro:Git-exercises andela$ git stash
Saved working directory and index state WIP on dev: a341c4b added a readme file
andelas-MacBook-Pro:Git-exercises andela$ git stash list
stash@{0}: WIP on dev: a341c4b added a readme file
stash@{1}: WIP on dev: a341c4b added a readme file
andelas-MacBook-Pro:Git-exercises andela$ git add team.html
andelas-MacBook-Pro:Git-exercises andela$ git git status
git: 'git' is not a git command. See 'git --help'.

The most similar command is
        init
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   team.html

andelas-MacBook-Pro:Git-exercises andela$ git stash
Saved working directory and index state WIP on dev: a341c4b added a readme file
andelas-MacBook-Pro:Git-exercises andela$ git stash list
stash@{0}: WIP on dev: a341c4b added a readme file
stash@{1}: WIP on dev: a341c4b added a readme file
stash@{2}: WIP on dev: a341c4b added a readme file
andelas-MacBook-Pro:Git-exercises andela$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html

Dropped stash@{1} (f7a25f2ae3e1a5d30c2ee8600720667aa1311a37)
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html

andelas-MacBook-Pro:Git-exercises andela$ git stash list
stash@{0}: WIP on dev: a341c4b added a readme file
stash@{1}: WIP on dev: a341c4b added a readme file
andelas-MacBook-Pro:Git-exercises andela$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html
        new file:   home.html

Dropped stash@{1} (5f30c1b0f771683c4ff5e61fd9528e54acbf5f8e)
andelas-MacBook-Pro:Git-exercises andela$ git add .
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "unstashed the stashed pages"
[dev f3689dd] unstashed the stashed pages
 2 files changed, 26 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
andelas-MacBook-Pro:Git-exercises andela$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

andelas-MacBook-Pro:Git-exercises andela$ git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 610 bytes | 610.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Stevenkwizera06/Git-exercise/pull/new/dev
remote: 
To https://github.com/Stevenkwizera06/Git-exercise.git
 * [new branch]      dev -> dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
andelas-MacBook-Pro:Git-exercises andela$ git stash list
stash@{0}: WIP on dev: a341c4b added a readme file
andelas-MacBook-Pro:Git-exercises andela$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   team.html

Dropped stash@{0} (5f78448564e54e1eae7d93461103b78080e95f80)
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   team.html

andelas-MacBook-Pro:Git-exercises andela$ git reset --hard
HEAD is now at f3689dd unstashed the stashed pages
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean

## Bundle 2
### Exercise 1
andelas-MacBook-Pro:Git-exercises andela$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        services.html

nothing added to commit but untracked files present (use "git add" to track)
andelas-MacBook-Pro:Git-exercises andela$ git add services.html
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "added services.html"
[ft/bundle-2 e318cbe] added services.html
 1 file changed, 13 insertions(+)
 create mode 100644 services.html
andelas-MacBook-Pro:Git-exercises andela$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

andelas-MacBook-Pro:Git-exercises andela$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 565 bytes | 565.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Stevenkwizera06/Git-exercise/pull/new/ft/bundle-2
remote: 
To https://github.com/Stevenkwizera06/Git-exercise.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
Branch 'ft/bundle-2' set up to track remote branch 'ft/bundle-2' from 'origin'.
andelas-MacBook-Pro:Git-exercises andela$ 
```