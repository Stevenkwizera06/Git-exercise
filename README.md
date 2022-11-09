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
```

## Bundle 1
### Exercise 2
```
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
```

## Bundle 2
### Exercise 1
```
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
## Bundle 2
### Exercise 2
```
andelas-MacBook-Pro:Git-exercises andela$ git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 6 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
andelas-MacBook-Pro:Git-exercises andela$ git pull
Updating a341c4b..f2aff36
Fast-forward
 README.md     | 240 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 about.html    |  13 +++++
 home.html     |  13 +++++
 services.html |  13 +++++
 4 files changed, 279 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html
andelas-MacBook-Pro:Git-exercises andela$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch ft/service-redesign
nothing to commit, working tree clean
andelas-MacBook-Pro:Git-exercises andela$ git add services.html
andelas-MacBook-Pro:Git-exercises andela$ git commit "added changes in services.html"
error: pathspec 'added changes in services.html' did not match any file(s) known to git
andelas-MacBook-Pro:Git-exercises andela$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

andelas-MacBook-Pro:Git-exercises andela$ git push --set-upstream origin ft/service-redesign
Total 0 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Stevenkwizera06/Git-exercise/pull/new/ft/service-redesign
remote: 
To https://github.com/Stevenkwizera06/Git-exercise.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
Branch 'ft/service-redesign' set up to track remote branch 'ft/service-redesign' from 'origin'.
andelas-MacBook-Pro:Git-exercises andela$ git add services.html
andelas-MacBook-Pro:Git-exercises andela$ git commit "added changes in services.html"
error: pathspec 'added changes in services.html' did not match any file(s) known to git
andelas-MacBook-Pro:Git-exercises andela$ git push
Everything up-to-date
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   services.html

andelas-MacBook-Pro:Git-exercises andela$ git add .
andelas-MacBook-Pro:Git-exercises andela$ git commit "added changes in services.html"
error: pathspec 'added changes in services.html' did not match any file(s) known to git
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   services.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   services.html

andelas-MacBook-Pro:Git-exercises andela$ git add .
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "added some challenges in services.html"
[ft/service-redesign c0e0f81] added some challenges in services.html
 1 file changed, 5 insertions(+)
andelas-MacBook-Pro:Git-exercises andela$ git pussh
git: 'pussh' is not a git command. See 'git --help'.

The most similar command is
        push
andelas-MacBook-Pro:Git-exercises andela$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 371 bytes | 371.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Stevenkwizera06/Git-exercise.git
   f2aff36..c0e0f81  ft/service-redesign -> ft/service-redesign
andelas-MacBook-Pro:Git-exercises andela$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
andelas-MacBook-Pro:Git-exercises andela$ git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main
andelas-MacBook-Pro:Git-exercises andela$ git add .
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "made some changes in service.html file"
[main b006c5a] made some changes in service.html file
 1 file changed, 1 insertion(+)
andelas-MacBook-Pro:Git-exercises andela$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 338 bytes | 338.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Stevenkwizera06/Git-exercise.git
   f2aff36..b006c5a  main -> main
andelas-MacBook-Pro:Git-exercises andela$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
andelas-MacBook-Pro:Git-exercises andela$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)

        both modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
andelas-MacBook-Pro:Git-exercises andela$ git add .
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "resolved conflicts"
[ft/service-redesign 9f6cc83] resolved conflicts
andelas-MacBook-Pro:Git-exercises andela$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 350 bytes | 350.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Stevenkwizera06/Git-exercise.git
   c0e0f81..9f6cc83  ft/service-redesign -> ft/service-redesign
```