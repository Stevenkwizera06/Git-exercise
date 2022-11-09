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
### Exercise 2
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

## Bundle 3
### Exercise 1
```
andelas-MacBook-Pro:Git-exercises andela$ git checkout -b ft/team-page
M       README.md
Switched to a new branch 'ft/team-page'
andelas-MacBook-Pro:Git-exercises andela$ git checkout -b ft/team-page
fatal: A branch named 'ft/team-page' already exists.
andelas-MacBook-Pro:Git-exercises andela$ git add team.html
andelas-MacBook-Pro:Git-exercises andela$ git statuss
git: 'statuss' is not a git command. See 'git --help'.

The most similar command is
        status
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch ft/team-page
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   team.html

andelas-MacBook-Pro:Git-exercises andela$ git commit -m "added team.html file"
[ft/team-page 81acaf4] added team.html file
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
andelas-MacBook-Pro:Git-exercises andela$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 470 bytes | 470.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Stevenkwizera06/Git-exercise/pull/new/ft/team-page
remote: 
To https://github.com/Stevenkwizera06/Git-exercise.git
 * [new branch]      ft/team-page -> ft/team-page
andelas-MacBook-Pro:Git-exercises andela$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
andelas-MacBook-Pro:Git-exercises andela$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
andelas-MacBook-Pro:Git-exercises andela$ git checkout ft/team-page
Switched to branch 'ft/team-page'
andelas-MacBook-Pro:Git-exercises andela$ git log
commit 81acaf40a53b4d0c7ce2b805a9c215aa79373222 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:35:16 2022 +0200

    added team.html file

commit 45ef9be1944372904416ae07ca82f318ba75ed0d (origin/ft/service-redesign, ft/service-redesign)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:30:30 2022 +0200

    added Readme

commit 9f6cc8397220fc2af2f86a4bc61d1f6b14548ba6
Merge: c0e0f81 b006c5a
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:24:44 2022 +0200

    resolved conflicts

commit b006c5a26700beb4030da9478d15146e365ef94e (origin/main, main, ft/contact-page)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:16:39 2022 +0200

    made some changes in service.html file

commit c0e0f81a0df00f8fe5bcacfce8dea1bc336745a2
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:13:31 2022 +0200

    added some challenges in services.html

commit f2aff365762b09e4660eaa3cf1d13b4ca4704824
Merge: a341c4b 4f9737f
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Wed Nov 9 12:08:56 2022 +0200

    Merge pull request #1 from Stevenkwizera06/ft/bundle-2
    
    new pages were added

commit 4f9737fbfd822add155c3bf8f5acd325e6dfe4d1 (origin/ft/bundle-2, ft/bundle-2)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:39:34 2022 +0200

    added services.html

commit c47c028207bd7d35d302b6c6e5c4e0215cf0143f
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:36:46 2022 +0200

    added services.html

commit ef4a8b1dd5808d71e0727dcbcb26aaa2e4893edd
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:25:31 2022 +0200

    
    new pages were added

commit 4f9737fbfd822add155c3bf8f5acd325e6dfe4d1 (origin/ft/bundle-2, ft/bundle-2)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:39:34 2022 +0200

    added services.html

commit c47c028207bd7d35d302b6c6e5c4e0215cf0143f
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:36:46 2022 +0200

    added services.html

commit ef4a8b1dd5808d71e0727dcbcb26aaa2e4893edd
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:25:31 2022 +0200

    added services.html

commit e318cbe746d1c0c9d5bc56a09dd5457519a3343a
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:12:56 2022 +0200

    added services.html

commit f3689ddc74410b1ab7b0b09facbf099aefe99a7a (origin/dev, dev)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:06:05 2022 +0200

    unstashed the stashed pages

commit a341c4b6de18d1e43d3e0b20751118b51129934f
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 10:28:22 2022 +0200

    added a readme file

andelas-MacBook-Pro:Git-exercises andela$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'
andelas-MacBook-Pro:Git-exercises andela$ git cherry-pick 81acaf40a53b4d0c7ce2b805a9c215aa79373222
[ft/contact-page f4498ec] added team.html file
 Date: Wed Nov 9 14:35:16 2022 +0200
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch ft/contact-page
nothing to commit, working tree clean
andelas-MacBook-Pro:Git-exercises andela$ git log
commit f4498ecca38c9401d46b6173319a59d2276ff696 (HEAD -> ft/contact-page)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:35:16 2022 +0200

    added team.html file

commit b006c5a26700beb4030da9478d15146e365ef94e (origin/main, main)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:16:39 2022 +0200

    made some changes in service.html file

commit f2aff365762b09e4660eaa3cf1d13b4ca4704824
Merge: a341c4b 4f9737f
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Wed Nov 9 12:08:56 2022 +0200

    Merge pull request #1 from Stevenkwizera06/ft/bundle-2
    
andelas-MacBook-Pro:Git-exercises andela$ git add .
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "added new contact page"
[ft/contact-page fdea58c] added new contact page
 1 file changed, 12 insertions(+)
 create mode 100644 contact.html
andelas-MacBook-Pro:Git-exercises andela$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

andelas-MacBook-Pro:Git-exercises andela$ git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 745 bytes | 745.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Stevenkwizera06/Git-exercise/pull/new/ft/contact-page
remote: 
To https://github.com/Stevenkwizera06/Git-exercise.git
 * [new branch]      ft/contact-page -> ft/contact-page
Branch 'ft/contact-page' set up to track remote branch 'ft/contact-page' from 'origin'.
andelas-MacBook-Pro:Git-exercises andela$ git checkout ft/faq-page
error: pathspec 'ft/faq-page' did not match any file(s) known to git
andelas-MacBook-Pro:Git-exercises andela$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
andelas-MacBook-Pro:Git-exercises andela$ git add .
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "added faq page "
[ft/faq-page 51b82b7] added faq page
 1 file changed, 15 insertions(+)
 create mode 100644 faq.html
andelas-MacBook-Pro:Git-exercises andela$ git push 
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

andelas-MacBook-Pro:Git-exercises andela$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 478 bytes | 478.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Stevenkwizera06/Git-exercise/pull/new/ft/faq-page
remote: 
To https://github.com/Stevenkwizera06/Git-exercise.git
 * [new branch]      ft/faq-page -> ft/faq-page
Branch 'ft/faq-page' set up to track remote branch 'ft/faq-page' from 'origin'.
andelas-MacBook-Pro:Git-exercises andela$ git log
commit 51b82b7a84b74c79dbeb600cb8512a608d61b486 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:53:21 2022 +0200

    added faq page

commit fdea58cf656a963bb97d49b61c60c7be97e62ba4 (origin/ft/contact-page, ft/contact-page)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:48:19 2022 +0200

    added new contact page

commit f4498ecca38c9401d46b6173319a59d2276ff696
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:35:16 2022 +0200

    added team.html file

commit b006c5a26700beb4030da9478d15146e365ef94e (origin/main, main)
andelas-MacBook-Pro:Git-exercises andela$ git revert f4498ecca38c9401d46b6173319a59d2276ff696
[ft/faq-page 20cc689] Revert "added team.html file"
 1 file changed, 12 deletions(-)
 delete mode 100644 team.html
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "reverted the changes of the last commit"
On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
andelas-MacBook-Pro:Git-exercises andela$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 277 bytes | 277.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Stevenkwizera06/Git-exercise.git
   51b82b7..20cc689  ft/faq-page -> ft/faq-page
```

## Bundle 3
### Exercise 2
```
andelas-MacBook-Pro:Git-exercises andela$ git checkout -b ft/home-page-redesign
M       README.md
Switched to a new branch 'ft/home-page-redesign'
andelas-MacBook-Pro:Git-exercises andela$ git checkout main
M       README.md
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
andelas-MacBook-Pro:Git-exercises andela$ git add .
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "added changes on main branch "
[main ad2c4d0] added changes on main branch
 2 files changed, 272 insertions(+), 1 deletion(-)
andelas-MacBook-Pro:Git-exercises andela$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 3.43 KiB | 3.43 MiB/s, done.
Total 4 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Stevenkwizera06/Git-exercise.git
   b006c5a..ad2c4d0  main -> main
andelas-MacBook-Pro:Git-exercises andela$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
andelas-MacBook-Pro:Git-exercises andela$ git rebase main
First, rewinding head to replay your work on top of it...
Applying: added team.html file
Applying: added new contact page
Applying: added faq page
Applying: Revert "added team.html file"
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch ft/home-page-redesign
nothing to commit, working tree clean
andelas-MacBook-Pro:Git-exercises andela$ git log
commit e52226f17371dc5cc6635aa85282ad50423ece2c (HEAD -> ft/home-page-redesign)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 15:03:26 2022 +0200

    Revert "added team.html file"
    
    This reverts commit f4498ecca38c9401d46b6173319a59d2276ff696.

commit 2c61553ac31f671084acab75546719a6d7364792
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:53:21 2022 +0200

    added faq page

commit fe654060d6539ea494bad06519d337e6abdebd94
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:48:19 2022 +0200

    added new contact page

commit 11ec588992ad283a2ec9edc7b9e014500d4c5066
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:35:16 2022 +0200

    added team.html file

commit ad2c4d0f1c724b8d9e6ebaa3dbec25714b9a01e7 (origin/main, main)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 15:14:16 2022 +0200

    added changes on main branch

commit b006c5a26700beb4030da9478d15146e365ef94e
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 14:16:39 2022 +0200

    made some changes in service.html file

commit f2aff365762b09e4660eaa3cf1d13b4ca4704824
Merge: a341c4b 4f9737f
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Wed Nov 9 12:08:56 2022 +0200

    Merge pull request #1 from Stevenkwizera06/ft/bundle-2
    
    new pages were added

commit 4f9737fbfd822add155c3bf8f5acd325e6dfe4d1 (origin/ft/bundle-2, ft/bundle-2)
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:39:34 2022 +0200

    added services.html

commit c47c028207bd7d35d302b6c6e5c4e0215cf0143f
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:36:46 2022 +0200

    added services.html

commit ef4a8b1dd5808d71e0727dcbcb26aaa2e4893edd
Author: Stevenkwizera06 <kwiste06@gmail.com>
Date:   Wed Nov 9 11:25:31 2022 +0200

    added services.html

commit e318cbe746d1c0c9d5bc56a09dd5457519a3343a
Author: Stevenkwizera06 <kwiste06@gmail.com>
andelas-MacBook-Pro:Git-exercises andela$ git add .
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "added changes in home page"
[ft/home-page-redesign 3c0ad45] added changes in home page
 1 file changed, 1 insertion(+)
andelas-MacBook-Pro:Git-exercises andela$ git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

andelas-MacBook-Pro:Git-exercises andela$ git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 4 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.62 KiB | 276.00 KiB/s, done.
Total 14 (delta 7), reused 0 (delta 0)
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/Stevenkwizera06/Git-exercise/pull/new/ft/home-page-redesign
remote: 
To https://github.com/Stevenkwizera06/Git-exercise.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
Branch 'ft/home-page-redesign' set up to track remote branch 'ft/home-page-redesign' from 'origin'.
```

## Bundle 4
### Exercise 1
```
andelas-MacBook-Pro:Git-exercises andela$ git checkout main
M       README.md
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
andelas-MacBook-Pro:Git-exercises andela$ git remote add git-copy https://github.com/Stevenkwizera06/git-exercise-2.git
andelas-MacBook-Pro:Git-exercises andela$ git remote
git-copy
origin
andelas-MacBook-Pro:Git-exercises andela$ git add home.html
andelas-MacBook-Pro:Git-exercises andela$ git commit -m "added new changes in home page"
[main bf7e1c4] added new changes in home page
 1 file changed, 1 insertion(+)
andelas-MacBook-Pro:Git-exercises andela$ git push origin
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 352 bytes | 352.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Stevenkwizera06/Git-exercise.git
   ad2c4d0..bf7e1c4  main -> main
andelas-MacBook-Pro:Git-exercises andela$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
andelas-MacBook-Pro:Git-exercises andela$ git push git-copy
Enumerating objects: 30, done.
Counting objects: 100% (30/30), done.
Delta compression using up to 4 threads
Compressing objects: 100% (29/29), done.
Writing objects: 100% (30/30), 6.85 KiB | 2.28 MiB/s, done.
Total 30 (delta 10), reused 0 (delta 0)
remote: Resolving deltas: 100% (10/10), done.
To https://github.com/Stevenkwizera06/git-exercise-2.git
 * [new branch]      main -> main
```