# Gym-Git-Exercise-Solutions
# BUNDLE 1
## Exercise 1

```bash

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git init
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

nothing added to commit but untracked files present (use "git add" to track)
fatal: Branch rename failed
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch -m main master
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch -m master main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add .
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git mv index.html exercise.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
No commits yet

  (use "git rm --cached <file>..." to unstage)

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'Renamed a file'
 1 file changed, 14 insertions(+)
 create mode 100644 exercise.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git remote add origin https://github.com/esther921/gitExercise1-Bundle1.git
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch main
nothing to commit, working tree clean
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch -M main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
nothing to commit, working tree clean
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 470 bytes | 235.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
branch 'main' set up to track 'origin/main'.
* main
  remotes/origin/main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch test
nothing to commit, working tree clean
Switched to branch 'test'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout dev
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch --delete test
Deleted branch test (was c4429cc).
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch -a
  main
  remotes/origin/main
No local changes to save
```
## Exercise 2

```bash
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add .
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash
Saved working directory and index state WIP on dev: c4429cc Renamed a file
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
nothing to commit, working tree clean
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add .
Saved working directory and index state WIP on dev: c4429cc Renamed a file
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add .
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash 
Saved working directory and index state WIP on dev: c4429cc Renamed a file
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch dev
nothing to commit, working tree clean
stash@{1}: WIP on dev: c4429cc Renamed a file
stash@{2}: WIP on dev: c4429cc Renamed a file
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash show
 team.html | 14 ++++++++++++++
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash pop 1
On branch dev
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped refs/stash@{1} (e3aacbf13dcc9c2d9e9f37afc825d9abc227911f)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash list
stash@{0}: WIP on dev: c4429cc Renamed a file
stash@{1}: WIP on dev: c4429cc Renamed a file
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash pop 1
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
Dropped refs/stash@{1} (feb86f3090b371c205174568c37091b348ecf2ee)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add .
[dev c2e69e7] Restored with the stash pop index command
 2 files changed, 28 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
On branch dev
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push dev    
fatal: 'dev' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push origin dev
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Writing objects: 100% (4/4), 611 bytes | 305.00 KiB/s, done.
remote:
remote:      https://github.com/esther921/gitExercise1-Bundle1/pull/new/dev
remote:
To https://github.com/esther921/gitExercise1-Bundle1.git
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch main

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    exercise.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout dev
D       exercise.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit 'deleted a folder'
error: pathspec 'deleted a folder' did not match any file(s) known to git
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit 'deleted a folder'
error: pathspec 'deleted a folder' did not match any file(s) known to git
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'deleted a folder'
[dev 15f1e19] deleted a folder
 1 file changed, 14 deletions(-)
 delete mode 100644 exercise.html
fatal: The current branch dev has no upstream branch.


To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
rm 'exercise.html'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'deleted a folder'
[main c7548a9] deleted a folder
 1 file changed, 14 deletions(-)
 delete mode 100644 exercise.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/esther921/gitExercise1-Bundle1.git
   c4429cc..c7548a9  main -> main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout dev
Switched to branch 'dev'
stash@{0}: WIP on dev: c4429cc Renamed a file
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash pop 
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (c97fd0adc40ad1b76d6a6d3cb9089384b166f73a)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add .
error: pathspec 'restored' did not match any file(s) known to git
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'restored'
[dev c139a7d] restored
 1 file changed, 14 insertions(+)
 create mode 100644 team.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push 
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push dev
fatal: 'dev' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push origin dev
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Writing objects: 100% (5/5), 716 bytes | 358.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
To https://github.com/esther921/gitExercise1-Bundle1.git
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git log
commit c139a7d1b542e10fc99ff84c1d5a91cf4ef89330 (HEAD -> dev, origin/dev)
    restored

Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:41:42 2022 +0200

    deleted a folder

commit c2e69e7470733931794ddebb2a798af94f35af71
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:22:27 2022 +0200

    Restored with the stash pop index command

commit c4429ccdb7858d29f12997cd6f41c5faed8fb494
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sat Oct 15 19:05:39 2022 +0200

    Renamed a file
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git reset --soft
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git reset --hard
HEAD is now at c139a7d restored
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
nothing to commit, working tree clean
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git reset HEAD
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git reset HEAD .
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git log 
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:46:07 2022 +0200

    restored
Author: esther921 <estherniyonkuru51@gmail.com>

    deleted a folder

commit c2e69e7470733931794ddebb2a798af94f35af71
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:22:27 2022 +0200

    Restored with the stash pop index command

commit c4429ccdb7858d29f12997cd6f41c5faed8fb494
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sat Oct 15 19:05:39 2022 +0200

    Renamed a file
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git slash list

The most similar command is
        stash
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash list
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git reset --hard
HEAD is now at c139a7d restored
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git slach list
git: 'slach' is not a git command. See 'git --help'.

The most similar command is
        stash
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash list
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash
No local changes to save
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash team.html

   or: git stash drop [-q|--quiet] [<stash>]
   or: git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
   or: git stash branch <branchname> [<stash>]
   or: git stash clear
   or: git stash [push [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [-m|--message <message>]
                 [--pathspec-from-file=<file> [--pathspec-file-nul]]
                 [--] [<pathspec>...]]
   or: git stash save [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [<message>]

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash team     
fatal: unknown subcommand: team

usage: git stash list [<options>]
   or: git stash show [<options>] [<stash>]
   or: git stash drop [-q|--quiet] [<stash>]
   or: git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
   or: git stash branch <branchname> [<stash>]
   or: git stash [push [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [-m|--message <message>]
                 [--pathspec-from-file=<file> [--pathspec-file-nul]]
                 [--] [<pathspec>...]]
   or: git stash save [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [<message>]

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash list
On branch dev
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch dev
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add team.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash
Saved working directory and index state WIP on dev: c139a7d restored
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash list
stash@{0}: WIP on dev: c139a7d restored
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git stash show
 team.html | 1 +
 1 file changed, 1 insertion(+)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git reset --hard
HEAD is now at c139a7d restored
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch dev
nothing to commit, working tree clean
```

# BUNDLE 2
## Exercise 1
```bash 
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch ft/bundle-2
Changes to be committed:

Untracked files:
  (use "git add <file>..." to include in what will be committed)

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout list
error: pathspec 'list' did not match any file(s) known to git
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch
  dev
* ft/bundle-2
  main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout dev
Switched to branch 'dev'
A       exercises.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch --delete 
Deleted branch ft/bundle-2 (was c139a7d).
Switched to a new branch 'ft/bundle-2'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch
* ft/bundle-2
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'First
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 588 bytes | 294.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:     
remote:      https://github.com/esther921/gitExercise1-Bundle1/pull/new/ft/bundle-2
remote:
To https://github.com/esther921/gitExercise1-Bundle1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
```
