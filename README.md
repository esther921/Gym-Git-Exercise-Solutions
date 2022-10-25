# BUNDLE 1
## EXERCISE 1

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
## EXERCISE 2

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
## Exercise 2
```bash
  To https://github.com/esther921/gitExercise1-Bundle1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git pull
Already up to date.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git pull --help     
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add services.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'Added a file'
[ft/service-redesign 421d0f6] Added a file
 1 file changed, 17 insertions(+)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push originft/service-redesign
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 513 bytes | 171.00 KiB/s, done.
                                                    s> git push origin ft/s
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/esther921/gitExercise1-Bundle1/pull/new/ft/service-redesign
remote:                                             s, done.
To https://github.com/esther921/gitExercise1-Bundle1.git
 * [new branch]      ft/service-redesign -> ft/servign' on GitHub by visitice-redesign
s> git checkout main                                e1-Bundle1/pull/new/ft/
Switched to branch 'main'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add .                                        .git
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutionce-redesigns> git commit -m 'Added services.html to main'      s> git checkout main   
[main 9fcfd3a] Added services.html to main
 1 file changed, 17 insertions(+)
 create mode 100644 services.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push origin main

Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 505 bytes | 252.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0To https://github.com/esther921/gitExercise1-Bundle1.git
   c7548a9..9fcfd3a  main -> main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git merge main      
CONFLICT (add/add): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
PS ^C  sers\TheGym\Desktop\Gym Git Exercise Solutions>
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git merge main      
hint: Fix them up in the work tree, and then use 'git add/rm <file>'       
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git merge main      
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add services.htmfatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'ResolPS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git merge main      
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add services.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'Merged'
On branch ft/service-redesign
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 225 bytes | 225.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/esther921/gitExercise1-Bundle1.git
   421d0f6..785b0fe  ft/service-redesign -> ft/service-redesign
 ```
# BUNDLE 3

## Exercise 1
```bash 
 dev
  ft/service-redesign
* ft/team-page
  main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout -d ft/team-page
HEAD is now at 66c30d2 Merge pull request #2 from esther921/ft/bundle-2    
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch
  dev
  ft/bundle-2
  ft/service-redesign
  ft/team-page
  main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git reset --hard    
HEAD is now at 66c30d2 Merge pull request #2 from esther921/ft/bundle-2    
* (HEAD detached at refs/heads/ft/team-page)
  dev
  ft/bundle-2
  ft/service-redesign
  ft/team-page
  main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git reset
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch
* (HEAD detached at refs/heads/ft/team-page)
  dev
  ft/bundle-2
  ft/service-redesign
  ft/team-page
  main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch delete ftPS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch
* (HEAD detached at refs/heads/ft/team-page)
  delete
  dev
  ft/bundle-2
  ft/service-redesign
  ft/team-page
  main
history (in this case the commit previous to HEAD, i.e. HEAD^).
>> You only need to checkout the branch you were on, e.g.
>>
>> git checkout master
At line:3 char:3
+ If you want to delete your changes associated with the detached HEAD     
+   ~
Missing '(' after 'If' in if statement.
    + CategoryInfo          : ParserError: (:) [], ParentContainsErrorRec  
   ordException
    + FullyQualifiedErrorId : MissingOpenParenthesisInIfStatement
 
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout ft/team-page
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout --     
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch
  main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutionerror: The branch 'ft/team-page' is not fully mergedut at 'C:/Users/TheGym/If you are sure you want to delete it, run 'git branch -D ft/team-page'.                                s> git checkout dev    
PS C:\Users\TheGym\Desktop\Gym Git Exercise SolutionDeleted branch ft/team-page (was 66c30d2).          s> git branch -d ft/tea
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout -b ft/team-page                     .
Switched to a new branch 'ft/team-page'             ch -D ft/team-page'.   
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch -D ft/teas> git add team.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add team.html                                s> git checkout -b ft/t
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add team.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add team.html   s> git commit -m 'Added team.html'                  s> 
[ft/team-page 909ae88] Added team.html
 1 file changed, 2 insertions(+), 2 deletions(-)    
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push origin ft/team-page
To https://github.com/esther921/gitExercise1-Bundle1.git
 ! [rejected]        ft/team-page -> ft/team-page (non-fast-forward)       
error: failed to push some refs to 'https://github.com/esther921/gitExercise1-Bundle1.git'
hint: Updates were rejected because the tip of your current branch is behinhint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details. 
PS git pull\TheGym\Desktop\Gym Git Exercise Solutions>
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> ft/team-page

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch --set-upstream-to=origin/<branch> ft/team-page
fatal: the requested upstream branch 'origin/<branch>' does not exist
hint: 
hint: If you are planning on basing your work on an upstream
hint: branch that already exists at the remote, you may need to
hint: run "git fetch" to retrieve it.
hint: 
hint: "git push -u" to set the upstream config as you push.
hint: Disable this message with "git config advice.setUpstreamFailure false"
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> ft/team-page
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git pull ft/team-page
fatal: 'ft/team-page' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git pull Gym Git Exercises Solutions  ft/team-page
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push origin ft/team-page
To https://github.com/esther921/gitExercise1-Bundle1.git
 ! [rejected]        ft/team-page -> ft/team-page (non-fast-forward)       
error: failed to push some refs to 'https://github.com/esther921/gitExercise1-Bundle1.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
usage: git remote add [<options>] <name> <url>

    --tags                import all tags and associated objects when fetch
                          or do not fetch any tag at all (--no-tags)
    -t, --track <branch>  branch(es) to track
    -m, --master <branch>
                          master branch
    --mirror[=(push|fetch)]
                          set up remote as a mirror to push to or fetch fro

Switched to branch 'dev'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch -d ft/tea
error: The branch 'ft/team-page' is not fully merged.
If you are sure you want to delete it, run 'git branch -D ft/team-page'.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch -D ft/tea
Deleted branch ft/team-page (was 909ae88).
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout -b ft/t
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add team.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'Added
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        exercise.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add team.html
[ft/team-page 23112c1] Added the team.html page
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push


To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push --set-upstr
To https://github.com/esther921/gitExercise1-Bundle1.git
 ! [rejected]        ft/team-page -> ft/team-page (non-fast-forward)
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> [D
At line:1 char:3
+ [D
+   ~
Missing ] at end of attribute or type literal.
    + CategoryInfo          : ParserError: (:) [], ParentContainsErrorRecor
    + FullyQualifiedErrorId : EndSquareBracketExpectedAtEndOfAttribute

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions>
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch -D ft/tea
error: Cannot delete branch 'ft/team-page' checked out at 'C:/Users/TheGym/
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout dev
Switched to branch 'dev'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch -D ft/tea
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push --set-upstream origin ft/team-page
Enumerating objects: 5, done.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 322 bytes | 161.00 KiB/s, done.
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.      
remote:
remote:      https://github.com/esther921/gitExercise1-Bundle1/pull/new/ft/team-page
remote:
To https://github.com/esther921/gitExercise1-Bundle1.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout main   
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch
  delete
  dev
  ft/bundle-2
  ft/service-redesign
  ft/team-page
* main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout ft/contact-page
error: pathspec 'ft/contact-page' did not match any file(s) known to git   
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git log

    Added the team.html page

commit c139a7d1b542e10fc99ff84c1d5a91cf4ef89330 (origin/dev, dev)
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:46:07 2022 +0200

    restored

commit 15f1e19f3c0b8f8e4c90ef3682058c7472cc660a
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:41:42 2022 +0200


commit c2e69e7470733931794ddebb2a798af94f35af71
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:22:27 2022 +0200

    Restored with the stash pop index command
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions>
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions>
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions>
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git cherry pick Checkout again ft/contact-page using git cherry-pick get th:wq
script file, or operable program. Check the spelling of the name, or if a  
path was included, verify that the path is correct and try again.
At line:1 char:1
+ :wq
+ ~~~
   FoundException
    + FullyQualifiedErrorId : CommandNotFoundException
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git cherry-pick c139a7d1b542e10fc99ff84c1d5a91cf4ef89330
Auto-merging team.html
CONFLICT (add/add): Merge conflict in team.html
error: could not apply c139a7d... restored
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git cherry-pick --continue".
hint: You can instead skip this commit with "git cherry-pick --skip".      
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git ft/contact-page 
git: 'ft/contact-page' is not a git command. See 'git --help'.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout ft/contact-page
error: you need to resolve your current index first
team.html: needs merge
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git reset --hard    
HEAD is now at 432ba8a Added the team.html page
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout ft/contrestored
Switched to branch 'ft/contact-page'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git cherry-pick c139The previous cherry-pick is now empty, possibly due to conflict resolution.If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
On branch ft/contact-page
You are currently cherry-picking commit c139a7d.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)      

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        exercise.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions>  git commit --allow-empty
[ft/contact-page a3b4d6c] restored
 Date: Sun Oct 16 11:46:07 2022 +0200
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git log
commit a3b4d6cb19d02953b2a296b9466c4b218cecfef7 (HEAD -> ft/contact-page)
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:46:07 2022 +0200

    restored

commit 66c30d2cf19270898891ee0adc739476d72db7ab (origin/main, main, delete)Merge: 9fcfd3a 09cb37c
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Wed Oct 19 20:27:57 2022 +0200

    Merge pull request #2 from esther921/ft/bundle-2

    Ft/bundle 2

commit 9fcfd3aad02cf0fe2470379521a9c591f23c3725
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Wed Oct 19 10:50:18 2022 +0200

    Added services.html to main

commit 09cb37c0499c1275cca3d627b1230c878b154b72 (origin/ft/bundle-2, ft/bundle-2)
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Wed Oct 19 07:55:00 2022 +0200

    First file

commit c139a7d1b542e10fc99ff84c1d5a91cf4ef89330 (origin/dev, dev)
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:46:07 2022 +0200

    restored
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Wed Oct 19 20:27:57 2022 +0200

    Merge pull request #2 from esther921/ft/bundle-2

    Ft/bundle 2

commit 9fcfd3aad02cf0fe2470379521a9c591f23c3725
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Wed Oct 19 10:50:18 2022 +0200

    Added services.html to main

commit 09cb37c0499c1275cca3d627b1230c878b154b72 (origin/ft/bundle-2, ft/bundle-2)
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Wed Oct 19 07:55:00 2022 +0200

    First file

commit c139a7d1b542e10fc99ff84c1d5a91cf4ef89330 (origin/dev, dev)
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:46:07 2022 +0200

    restored

Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Try the new cross-platform PowerShell https://aka.ms/pscore6

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch
  delete
  dev
  ft/bundle-2
* ft/contact-page
  ft/service-redesign
  ft/team-page
  main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout ft/team
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.  
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git log
commit 432ba8af1f6676264d9adcb991fd551950c9001f (HEAD -> ft/team-page, orig
Date:   Sun Oct 23 18:52:04 2022 +0200

    Added the team.html page

commit c139a7d1b542e10fc99ff84c1d5a91cf4ef89330 (origin/dev, dev)
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:46:07 2022 +0200

    restored

commit 15f1e19f3c0b8f8e4c90ef3682058c7472cc660a
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:41:42 2022 +0200

    deleted a folder

commit c2e69e7470733931794ddebb2a798af94f35af71
Author: esther921 <estherniyonkuru51@gmail.com>
Date:   Sun Oct 16 11:22:27 2022 +0200

The previous cherry-pick is now empty, possibly due to conflict resolution.

If you wish to commit it anyway, use:
    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)      

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        exercise.html

nothing added to commit but untracked files present (use "git add" to track)

                                                       :
: : The term ':' is not recognized as the name of a cmdlet, function,      
path was included, verify that the path is correct and try again.
At line:1 char:1
+ :
+ ~
   undException
    + FullyQualifiedErrorId : CommandNotFoundException

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add contact.html

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git






PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'Added contact page'
[ft/contact-page e14499b] Added contact page
 1 file changed, 14 insertions(+)
 create mode 100644 contact.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git puch
git: 'puch' is not a git command. See 'git --help'.

The most similar command is
        push
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push
fatal: The current branch ft/contact-page has no upstream branch.
    git push --set-upstream origin ft/contact-page
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.      
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting: 
contact-page
remote:
To https://github.com/esther921/gitExercise1-Bundle1.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions>







PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add faq.html    
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'Added the faq page'
[ft/faq-page 0c1936c] Added the faq page
 1 file changed, 14 insertions(+)
 create mode 100644 faq.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 502 bytes | 251.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.       
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:     
remote:      https://github.com/esther921/gitExercise1-Bundle1/pull/new/ft/faq-page
remote:
To https://github.com/esther921/gitExercise1-Bundle1.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
   or: git revert <subcommand>

Revert "Added the team.html page"
    --continue            resume revert or cherry-pick sequence
    --abort               cancel revert or cherry-pick sequence
    --cleanup <mode>      how to strip spaces and #comments from message   
    -n, --no-commit       don't automatically commit
    -e, --edit            edit the commit message
    -s, --signoff         add a Signed-off-by trailer
    -m, --mainline <parent-number>
                          select mainline parent
    --rerere-autoupdate   update the index with reused conflict resolution 
if possible
    --strategy <strategy>
    -X, --strategy-option <option>
                          option for merge strategy
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit
    --reference           use the 'reference' format to refer to commits   

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git revert cherry-pick 432ba8af1f6676264d9adcb991fd551950c9001f 
fatal: bad revision 'cherry-pick'
f6676264d9adcb991fd551950c9001f
[ft/faq-page 5ba2a1d] Revert "Added the team.html page"
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push

```
## Exercise 2
```bash 

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push

remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/esther921/gitExercise1-Bundle1.git                                                s, done.
   0c1936c..5ba2a1d  ft/faq-page -> ft/faq-page     
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solution 2 local objects.      s> git branch                                       .git
  delete
  dev                                               s> git branch
  ft/contact-page
* ft/faq-page
  ft/service-redesign
  ft/team-page
  main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'    
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout -b ft/hs> git checkout main   Switched to branch 'main'    
Your branch is up to date with 'origin/main'.       
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout main     delete
  dev
  ft/bundle-2                                       s>
  ft/contact-page
  ft/faq-page
  ft/home-page-redesign
  ft/service-redesign
  ft/team-page
* main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git status
On branch main

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        exercise.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'Added something'
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        exercise.html

nothing added to commit but untracked files present (use "git add" to trackPS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push
Everything up-to-date
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git rebase
There is no tracking information for the current branch.
Please specify which branch you want to rebase against.
See git-rebase(1) for details.


                                                    nch you can do so with:
s> git rebase main
Current branch ft/home-page-redesign is up to date. t/home-page-redesign   
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add home.html                                s> git rebase main     
s> git commit -m 'Added changes to the home page'   
[ft/home-page-redesign 5637807] Added changes to thes>  home page
 1 file changed, 1 insertion(+)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push
fatal: The current branch ft/home-page-redesign has 
no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS    git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 333 bytes | 333.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/esther921/gitExercise1-Bundle1/pull/new/ft/home-page-redesign
remote:
To https://github.com/esther921/gitExercise1-Bundle1.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

```
# BUNDLE 4 
## Exercise 1
```bash  

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git branch
  dev
  ft/bundle-2
  ft/contact-page
  ft/faq-page
* ft/home-page-redesign
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        exercise.html

nothing added to commit but untracked files present (use "git add" to track) 
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git remote
git-copy
origin
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git remote -v
git-copy        https://github.com/esther921/git-exercise-bundle4.git (fetch)

git-copy        https://github.com/esther921/git-exercise-bundle4.git (push) 
origin  https://github.com/esther921/gitExercise1-Bundle1.git (fetch)        
origin  https://github.com/esther921/gitExercise1-Bundle1.git (push)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions>








                                                       git
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]   
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]      
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one  

work on the current change (see also: git help everyday)
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect    Use binary search to find the commit that introduced a bug      
   grep      Print lines matching a pattern
   log       Show commit logs
   show      Show various types of objects
   status    Show the working tree status
   commit    Record changes to the repository
   merge     Join two or more development histories together
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG     

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects
'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
See 'git help git' for an overview of the system.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add 
Nothing specified, nothing added.
hint: Maybe you wanted to say 'git add .'?
hint: Turn this message off by running
hint: "git config advice.addEmptyPathspec false"
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add home.html     
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'Added changes to the home page'hanges to the home page'
[main c1a630c] Added changes to the home page
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 328 bytes | 328.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.        
To https://github.com/esther921/gitExercise1-Bundle1.git
   66c30d2..c1a630c  main -> main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push git-copy     
Enumerating objects: 25, done.
Counting objects: 100% (25/25), done.
Delta compression using up to 4 threads
Compressing objects: 100% (22/22), done.
Writing objects: 100% (25/25), 2.88 KiB | 268.00 KiB/s, done.
Total 25 (delta 11), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (11/11), done.
To https://github.com/esther921/git-exercise-bundle4.git
 * [new branch]      main -> main
```
## Exercises 2

```bash
 PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions>, done. git branch

  delete                                              it
  dev
  ft/bundle-2                                          git branch
  ft/contact-page
  ft/faq-page
  ft/home-page-redesign
  ft/service-redesign
  ft/team-page
* main
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout -b ft/footer
Switched to a new branch 'ft/footer'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions>
                                                       git checkout -b ft/foo
 git add footer.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git add Footer.html                                   
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 
Oops, something went wrong.  Please report this bug with the details below.
Report on GitHub: https://github.com/lzybkr/PSReadLine/issues/new
-----------------------------------------------------------------------
Last 200 Keys:
 A d d e d Space c h s n g e d Backspace Backspace Backspace Backspace Backspace Backspace Backspace c h a n g e s Space t o Space t h e Space h o m e Space p a g e ' Enter
 g i t Space p u s h Enter
 g i t Space p u s h Space c o p y - Backspace Backspace Backspace Backspace Backspace g i t - c o p y Enter g i t Backspace Backspace Backspace Backspace g i t Space b r a n c h Enter
 g i t Space c h e c k o y t \ Backspace Backspace Backspace u t Space f t / t Backspace f o o t e r LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow Space - b Enter g i t Space a d d Space f o o t e r . h t m l Enter  
 g i t Space UpArrow UpArrow DownArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow LeftArrow Backspace F Enter      
 g i t Space c o m m i t Space - m Space '

Exception:
System.ArgumentOutOfRangeException: The value must be 
greater than or equal to zero and less than the console's buffer size in that dimension.
Parameter name: left
Actual value was -1.
   at System.Console.SetCursorPosition(Int32 left, Int32 top)
   at Microsoft.PowerShell.Internal.VirtualTerminal.set_CursorLeft(Int32 value)
   at Microsoft.PowerShell.PSConsoleReadLine.ReallyRender(RenderData renderData, String defaultColor)
   at Microsoft.PowerShell.PSConsoleReadLine.ForceRender()
   at Microsoft.PowerShell.PSConsoleReadLine.Insert(Char c)
   at Microsoft.PowerShell.PSConsoleReadLine.SelfInsert(Nullable`1 key, Objec   at Microsoft.PowerShell.PSConsoleReadLine.InputLoop()
   at Microsoft.PowerShell.PSConsoleReadLine.ReadLine(Runspace runspace, EngineIntrinsics engineIntrinsics)






 :wq
:wq : The term ':wq' is not recognized as the name of a cmdlet, function,    
script file, or operable program. Check the spelling of the name, or if a    
path was included, verify that the path is correct and try again.
At line:1 char:1
+ :wq
+ ~~~
    + CategoryInfo          : ObjectNotFound: (:wq:String) [], CommandNotFo  
[ft/footer 6a3b838] Added the footer
 1 file changed, 14 insertions(+)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push origin ft/footer
Enumerating objects: 4, done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 508 bytes | 254.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/esther921/gitExercise1-Bundle1/pull/new/ft/footer
To https://github.com/esther921/gitExercise1-Bundle1.git
 * [new branch]      ft/footer -> ft/footer
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions>


                                                       git add Footer.html   
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'Applied some changes the footer'
[ft/footer e70dbb6] Applied some changes the footer
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push origin ft/fooEnumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Writing objects: 100% (3/3), 375 bytes | 375.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.        
To https://github.com/esther921/gitExercise1-Bundle1.git
   6a3b838..e70dbb6  ft/footer -> ft/footer
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout main     
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git checkout -b ft/squSwitched to a new branch 'ft/squashing'
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git merge --squash ft/footer
Updating c1a630c..e70dbb6
Fast-forward
Squash commit -- not updating HEAD
 Footer.html | 14 ++++++++++++++
 1 file changed, 14 insertions(+)
 create mode 100644 Footer.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git commit -m 'footer 
changes squashing'
[ft/squashing ad9d147] footer changes squashing
 1 file changed, 14 insertions(+)
 create mode 100644 Footer.html
PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push
fatal: The current branch ft/squashing has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/squashing

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\TheGym\Desktop\Gym Git Exercise Solutions> git push --set-upstream origin ft/squashing
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 538 bytes | 179.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:      
remote:      https://github.com/esther921/gitExercise1-Bundle1/pull/new/ft/squashing
remote:
To https://github.com/esther921/gitExercise1-Bundle1.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.
```

# BUNDLE 5
## Exercises 1


## Exercises 2
```bash


Try the new cross-platform PowerShell https://aka.ms/pscore6

PS C:\Users\TheGym\Desktop\git-cafe-exercise> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git restore <file>..." to discard changes in working directory)

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\TheGym\Desktop\git-cafe-exercise> git branch
* main
git: 'addd' is not a git command. See 'git --help'.
The most similar command is
        add
PS C:\Users\TheGym\Desktop\git-cafe-exercise> git commit 'Made a small change to index file only'
error: pathspec 'Made a small change to index file only' did not match any file(s) known to git
PS C:\Users\TheGym\Desktop\git-cafe-exercise> git commit -m 'Made a small change to index file only'
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

The most similar command is
PS C:\Users\TheGym\Desktop\git-cafe-exercise> git add .
PS C:\Users\TheGym\Desktop\git-cafe-exercise> git commit -m 'Made a small change to index file only'
[main e30023a] Made a small change to index file only
 1 file changed, 3 insertions(+), 3 deletions(-)
PS C:\Users\TheGym\Desktop\git-cafe-exercise> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/esther921/git-cafe-exercise.git
PS C:\Users\TheGym\Desktop\git-cafe-exercise> git add .
PS C:\Users\TheGym\Desktop\git-cafe-exercise> git commit -m 'Made a small change to index file only'
[main 0216f10] Made a small change to index file only
 1 file changed, 2 insertions(+), 2 deletions(-)
PS C:\Users\TheGym\Desktop\git-cafe-exercise> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 365 bytes | 365.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/esther921/git-cafe-exercise.git
   e30023a..0216f10  main -> main
PS C:\Users\TheGym\Desktop\git-cafe-exercise> 
```
