# Git Exercise 
## Bundle 1
### Exercise 1

```bash
PS C:\Users\HP\git_exercises> git branch     
PS C:\Users\HP\git_exercises> git status     
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

PS C:\Users\HP\git_exercises> git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\HP\git_exercises> echo "Hello, Git!" > file1.txt
PS C:\Users\HP\git_exercises> git add file1.txt 
PS C:\Users\HP\git_exercises> ls

    Directory: C:\Users\HP\git_exercises

Mode                 LastWriteTime         Length Name   
----                 -------------         ------ ----   
-a----        12/25/2024   7:25 AM             28 file1.txt    
PS C:\Users\HP\git_exercises> git remote add origin https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git   
PS C:\Users\HP\git_exercises> git status 
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   file1.txt
PS C:\Users\HP\git_exercises> git commit -m "Added file1.txt to repository"
PS C:\Users\HP\git_exercises> git push
Everything up-to-date
PS C:\Users\HP\git_exercises> git checkout -b test
PS C:\Users\HP\git_exercises> git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.
PS C:\Users\HP\git_exercises> git branch -d test
Deleted branch test (was 2b69a9e).
PS C:\Users\HP\git_exercises> git push  
Everything up-to-date

```
### Exercise 2

```bash

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ touch home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ echo "<html><body><h1>Welcome to Olga's Home Page</h1></body></html>" > home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git add home.html
warning: in the working copy of 'home.html', LF will be replaced by CRLF the nex
t time Git touches it

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash save "Stashing the home.html"
Saved working directory and index state On dev: Stashing the home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash list
stash@{0}: On dev: Stashing the home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ touch about.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ echo "<h1>About me </h1>" > about.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git add about.html
warning: in the working copy of 'about.html', LF will be replaced by CRLF the ne
xt time Git touches it

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash save "Stashing the about.html"
Saved working directory and index state On dev: Stashing the about.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ touch team.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ echo "<h1>My Team </h1>" > team.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash save "Stashing the team.html"
No local changes to save

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git add team.html
warning: in the working copy of 'team.html', LF will be replaced by CRLF the nex
t time Git touches it

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash save "Stashing the team.html"
Saved working directory and index state On dev: Stashing the team.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash list
stash@{0}: On dev: Stashing the team.html
stash@{1}: On dev: Stashing the about.html
stash@{2}: On dev: Stashing the home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (393f330f76dc18642df23bc960745d148ecf399c)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash list
stash@{0}: On dev: Stashing the team.html
stash@{1}: On dev: Stashing the home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash pop stash@{2}
fatal: log for 'stash' only has 2 entries

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash list
stash@{0}: On dev: Stashing the team.html
stash@{1}: On dev: Stashing the home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ ^C

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (6427019534f2d68d7a2709dcf7d52cabbc4e27e9)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git add home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git add about.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git commit -m "Restoring the home.html and about.html changes"
[dev 597bbb6] Restoring the home.html and about.html changes
 2 files changed, 2 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash list
stash@{0}: On dev: Stashing the team.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is ahead of 'origin/dev' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (ef8840f7d852744b88469fdd6b11b50c271a6143)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git reset

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git restore team.html
error: pathspec 'team.html' did not match any file(s) known to git

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git status
On branch dev
Your branch is ahead of 'origin/dev' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git reset --hard
HEAD is now at 597bbb6 Restoring the home.html and about.html changes

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$
git push origin dev
```
## Bundle 2
### Exercise 1
```bash

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/bundle-2)
$ echo "<html>
<head><title>Services</title></head>
<body>
<h1>My Services</h1>
<p>swe.</p>
</body>
</html>" > services.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/bundle-2)
$ git add services.html
warning: in the working copy of 'services.html', LF will be replaced by CRLF the
 next time Git touches it

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/bundle-2)
$ git commit -m "Added services.html page"
[ft/bundle-2 f334c77] Added services.html page
 1 file changed, 7 insertions(+)
 create mode 100644 services.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 357 bytes | 357.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions/pull/new/ft
/bundle-2
remote:
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/bundle-2)
$
```
### Exercise 2
```bash

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git pull origin main
From https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Already up to date.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git add service.html
fatal: pathspec 'service.html' did not match any files

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ ls
README.md  about.html  file1.txt  home.html  services.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git add --all

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git status
On branch ft/service-redesign
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   services.html


HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git commit -m "Add service.html page"
[ft/service-redesign d6b1e39] Add service.html page
 1 file changed, 17 insertions(+)
 create mode 100644 services.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 518 bytes | 518.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions/pull/new/ft
/service-redesign
remote:
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (add/add): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign|MERGING)
$ git diff main..ft/service-redesign
diff --git a/services.html b/services.html
index a524df9..a8cf865 100644
--- a/services.html
+++ b/services.html
@@ -7,7 +7,7 @@
 </head>
 <body>
     <h1>Our Services</h1>
-    <p>Welcome to my services page. Here are the services i offer:</p>
+    <p>Welcome to my services page i offer:</p>
     <ul>
         <li>Web Development</li>
         <li>App Development</li>

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign|MERGING)
$ git pull origin main
error: You have not concluded your merge (MERGE_HEAD exists).
hint: Please, commit your changes before merging.
fatal: Exiting because of unfinished merge.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign|MERGING)
$ git pull origin main
From https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Already up to date.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git merge main
Already up to date.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git push -u origin ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
Everything up-to-date

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git add service.html
git commit -m "changes in main"
fatal: pathspec 'service.html' did not match any files
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git add service.html
fatal: pathspec 'service.html' did not match any files

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git add --all

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git commit -m "changes in main"
On branch main
nothing to commit, working tree clean

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git add --all

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git commit -m "changes in main"
[main b235995] changes in main
 1 file changed, 1 insertion(+), 1 deletion(-)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git push origin main
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/UwayoOlga/Gym-Git-Exercis
e-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git pull origin main
From https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main|MERGING)
$ git diff main..ft/service-redesign
diff --git a/services.html b/services.html
index 1b39903..a8cf865 100644
--- a/services.html
+++ b/services.html
@@ -7,7 +7,7 @@
 </head>
 <body>
     <h1>Our Services</h1>
-    <p>Welcome to my services page. Here are the services i offer:(changes in m
ain branch )</p>
+    <p>Welcome to my services page i offer:</p>
     <ul>
         <li>Web Development</li>
         <li>App Development</li>

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main|MERGING)
$ git commit -m "Resolved merge conflicts for main"
[main cf75932] Resolved merge conflicts for main

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git merge
fatal: No remote for the current branch.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git merge main
Already up to date.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git merge main
Updating c94cb18..cf75932
Fast-forward
 services.html | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git add service.html
fatal: pathspec 'service.html' did not match any files

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 4 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (8/8), 819 bytes | 409.00 KiB/s, done.
Total 8 (delta 6), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (6/6), completed with 2 local objects.
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
   c94cb18..cf75932  ft/service-redesign -> ft/service-redesign

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$
```
## Bundle 3
### Exercise 1
```bash

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/service-redesign)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
 
HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$ touch team.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$ echo "<\!DOCTYPE html><html><head><title>Team</title></head><body><h1>My Team</h1></body></html>" > team.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$ git add team.html
git commit -m "Add team.html with initial content"
git push origin ft/team-page
warning: in the working copy of 'team.html', LF will be replaced by CRLF the nex
t time Git touches it
[ft/team-page 3753b47] Add team.html with initial content
 1 file changed, 1 insertion(+)
 create mode 100644 team.html
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 351 bytes | 351.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions/pull/new/ft
/team-page
remote:
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$ git checkout main
Switched to branch 'main'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$ git log -1
commit 3753b479c91ee15502b88dc2ec840791ce0e5280 (HEAD -> ft/team-page, origin/ft
/team-page)
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Mon Dec 30 09:18:41 2024 +1300

    Add team.html with initial content

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/contact-page)
$ git cherry-pick 3753b479c91ee15502b88dc2ec840791ce0e5280
[ft/contact-page 85811e9] Add team.html with initial content
 Date: Mon Dec 30 09:18:41 2024 +1300
 1 file changed, 1 insertion(+)
 create mode 100644 team.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/contact-page)
$ touch contact.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/contact-page)
$ echo "<!DOCTYPE html><html><head><title>Contact</title></head><body><h1>My Contacts</h1></body></html>" > contact.html
bash: !DOCTYPE: event not found

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/contact-page)
$ echo "<\!DOCTYPE html><html><head><title>Contact</title></head><body><h1>My Contacts</h1></body></html>" > contact.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/contact-page)
$ git add contact.html
git commit -m "Add contact.html with initial content"
git push origin ft/contact-page
warning: in the working copy of 'contact.html', LF will be replaced by CRLF the
next time Git touches it
[ft/contact-page e02e0eb] Add contact.html with initial content
 1 file changed, 1 insertion(+)
 create mode 100644 contact.html
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 663 bytes | 331.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions/pull/new/ft
/contact-page
remote:
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page

Revert "Add team.html with initial content"




[ft/team-page 7d4205e] Revert "Add team.html with initial content"
 1 file changed, 1 deletion(-)
 delete mode 100644 team.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$ git log
commit 7d4205eb97b1fba9c4a382f4b5a765564688e0d5 (HEAD -> ft/team-page)
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Mon Dec 30 09:38:24 2024 +1300

    Revert "Add team.html with initial content"

    This reverts commit 3753b479c91ee15502b88dc2ec840791ce0e5280.

commit 3753b479c91ee15502b88dc2ec840791ce0e5280 (origin/ft/team-page)
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Mon Dec 30 09:18:41 2024 +1300

    Add team.html with initial content

commit cf759322b0f64c777e34d3838caed2d9cc6f4a24 (origin/ft/service-redesign, main, ft/service-
redesign)
Merge: b235995 b49d51f
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 20:16:41 2024 +1300

    Resolved merge conflicts for main

commit b49d51fe21ab779180c979e815a75d0f3c47aeb1
Merge: 3e83cfd c94cb18
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sun Dec 29 08:06:44 2024 +1300

    Merge pull request #7 from UwayoOlga/ft/service-redesign

    Add service.html page

commit 3e83cfddc368e106e3c1e08809032b520cb32e9b
Merge: 759be23 46cb621
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sun Dec 29 07:41:46 2024 +1300

    Merge pull request #6 from UwayoOlga/ft/bundle-2

    Add services.html page with basic content

commit 759be2310874c48457e6b9c859875af8c5d5170d
Merge: 66b7d78 e18ce52
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sun Dec 29 06:40:51 2024 +1300

    Merge pull request #4 from UwayoOlga/ft/bundle-2

    Ft/bundle 2

commit b235995ca059969966360660933947da1640bcff
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 20:11:57 2024 +1300

    changes in main

commit 0abf72aa6bb50a542f1f09e1226e47b748518515
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 20:09:27 2024 +1300

    changes in main

commit 964f75cdea4b5292e497caf98d961aa2b943ce24
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 20:08:59 2024 +1300

    changes in main

commit c94cb184efc6a44747d430b29534b5fc4b6cb741
Merge: d6b1e39 3e83cfd
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 20:05:16 2024 +1300

    Merge branch 'main' into ft/service-redesign

commit d6b1e396c4cb099cac2d24835bb6c25fb2b64b20
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 19:57:36 2024 +1300

    Add service.html page

commit 46cb621f5200c7db64645a681bc5fa9d9818bcbe (origin/ft/bundle-2, ft/bundle-2)
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 19:38:05 2024 +1300

    Add services.html page with basic content

commit e18ce52e27557b9dc981363ae80f3595cb761e51
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 18:35:44 2024 +1300

    Restored services.html that was deleted

commit 799010f9df1b5c5395ce70303847b1a74630522e
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 18:24:09 2024 +1300

    Remove services.html

commit 66b7d78cb3cd53d95b2c45d8b6bc469bd6f5e1e4
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 18:20:06 2024 +1300

    Remove services.html

commit 9b97d1cb67e9e673cf18112484fe208d1a0c794d
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 17:10:30 2024 +1300

    Delete team.html from main branch

commit 337e186d31f5a91b6408d5dc20141778bedbfb8c
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 13:03:57 2024 +1300

    Updated services.html in main branch

commit 41cb4f55ebc175837b8d9d723dbfcd4e61f33516
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 12:56:30 2024 +1300

    Remove services.html from main branch

commit eea675329c5ef04208cbfdfa6b1010242c223d99
Merge: ecd3a84 d9318d5
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 12:48:35 2024 +1300

    Merge branch 'main' of https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions

commit d9318d58c3ee2360fe81546764ea64f534142bc8
Merge: c9f4f36 22e771b
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sun Dec 29 00:40:59 2024 +1300

    Merge pull request #3 from UwayoOlga/ft/service-redesign

    Updated services.html in ft/service-redesign

commit c9f4f36985e4f06385872f10669d6719d2f02cfe
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sun Dec 29 00:13:20 2024 +1300

    Bundle 2, exercise1

commit abac280604b3a11210d3aee11cc07ec7c44e2c51
Merge: 869f8a2 f334c77
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sun Dec 29 00:06:06 2024 +1300

    Merge pull request #2 from UwayoOlga/ft/bundle-2

    Ft/bundle 2

commit ecd3a84a91d4f9b38a8f01bdac91dc7e3ea4bbde
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 12:42:34 2024 +1300
Date:   Sat Dec 28 11:36:18 2024 +1300

    Added services.html page

commit 869f8a26a79f588d5a9a03085f94737b4ce2e480
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 02:10:41 2024 +1300

    exercise2

commit 44d572f8e6293ac7e485d8bd47b45c8995871a12
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Sat Dec 28 02:06:44 2024 +1300

    Update README.md

commit 597bbb6c204839180be518272d8b538fb755d715 (origin/dev, dev)
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Fri Dec 27 13:46:09 2024 +1300

    Restoring the home.html and about.html changes

commit 0e0199300f99f7b1282704592db8bb80aec9a1f9
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Fri Dec 27 06:28:51 2024 +1300

    Update README.md

commit b4e7ab9dbb6986899a5f092ab4e5fe34aa5ec1cc
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Thu Dec 26 07:08:33 2024 +1300

    Create README.md

    Bundle1: Exercise 1

commit 2b69a9e35326c19c52a944e760c158a258086ee7
Author: UwayoOlga <uwayoolga@gmail.com>
Date:   Wed Dec 25 07:42:24 2024 +1300

    Added file1.txt to repository
~
~
~

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 263 bytes | 263.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
   3753b47..7d4205e  ft/team-page -> ft/team-page

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$

```
## Bundle 3
### Exercise 2
```bash

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/team-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ code .

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git add home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git commit -m "changes in main for bundle 3"
[main f614eb5] changes in main for bundle 3
 1 file changed, 38 insertions(+), 1 deletion(-)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git push origin main
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/UwayoOlga/Gym-Git-Exercis
e-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/home-page-redesign)
$ git add home.html

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/home-page-redesign)
$ git commit -m "changes the home page redesign"
[ft/home-page-redesign a4c0a88] changes the home page redesign
 1 file changed, 1 insertion(+)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 17, done.
Counting objects: 100% (17/17), done.
Delta compression using up to 4 threads
Compressing objects: 100% (15/15), done.
Writing objects: 100% (15/15), 1.96 KiB | 334.00 KiB/s, done.
Total 15 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), done.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting
remote:      https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions/pull/new/ft
/home-page-redesign
remote:
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/home-page-redesign)
$


```
## Bundle 4
### Exercise 1
```bash


HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git remote add git-copy https://github.com/UwayoOlga/git-copy

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git remote -v
git-copy        https://github.com/UwayoOlga/git-copy (fetch)
git-copy        https://github.com/UwayoOlga/git-copy (push)
origin  https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git (fetch)
origin  https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git (push)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ code .

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git add .
git commit -m "Updated the home page with new repo"
warning: adding embedded git repository: websiteclonning-
hint: You've added another git repository inside your current repository.
hint: Clones of the outer repository will not contain the contents of
hint: the embedded repository and will not know how to obtain it.
hint: If you meant to add a submodule, use:
hint:
hint:   git submodule add <url> websiteclonning-
hint:
hint: If you added this path by mistake, you can remove it from the
hint: index with:
hint:
hint:   git rm --cached websiteclonning-
hint:
hint: See "git help submodule" for more information.
hint: Disable this message with "git config advice.addEmbeddedRepo false"
[main 9c7bd36] Updated the home page with new repo
 2 files changed, 2 insertions(+), 1 deletion(-)
 create mode 160000 websiteclonning-

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git push origin main
git push git-copy main
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/UwayoOlga/Gym-Git-Exercis
e-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
Enumerating objects: 71, done.
Counting objects: 100% (71/71), done.
Delta compression using up to 4 threads
Compressing objects: 100% (67/67), done.
Writing objects: 100% (71/71), 18.01 KiB | 542.00 KiB/s, done.
Total 71 (delta 24), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (24/24), done.
To https://github.com/UwayoOlga/git-copy
 * [new branch]      main -> main

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git pull origin main
From https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Auto-merging home.html
CONFLICT (content): Merge conflict in home.html
Automatic merge failed; fix conflicts and then commit the result.

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main|MERGING)
$ git add .
git commit -m "Resolved merge conflicts"
[main 1aad256] Resolved merge conflicts

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git push origin main
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 776 bytes | 258.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
   a626b09..1aad256  main -> main
 

```
## Bundle 4
### Exercise 2
```bash

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/footer)
$ git add .
git commit -m "Adding the changes to the new branch"
On branch ft/footer
nothing to commit, working tree clean

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/footer)
$ git add .

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/footer)
$ git commit -m "Adding the changes to the new branch"
[ft/footer 10d8da9] Adding the changes to the new branch
 1 file changed, 23 insertions(+), 1 deletion(-)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/footer)
$ git add .

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/footer)
$ git commit -m "Adding the additional changes to the new branch"
[ft/footer cbbc8c9] Adding the additional changes to the new branch
 1 file changed, 1 insertion(+), 1 deletion(-)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/footer)
$ git push origin ft/footer
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 952 bytes | 317.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions/pull/new/ft
/footer
remote:
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/footer -> ft/footer

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/footer)
$ git checkout main
Switched to branch 'main'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/squashing)
$ git merge --squash ft/footer
Updating b24b0d9..cbbc8c9
Fast-forward
Squash commit -- not updating HEAD
 about.html   | 24 +++++++++++++++++++++++-
 contact.html |  2 +-
 2 files changed, 24 insertions(+), 2 deletions(-)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/squashing)
$ git commit -m "Footer changes squashing"
[ft/squashing 2b78e8c] Footer changes squashing
 2 files changed, 24 insertions(+), 2 deletions(-)

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/squashing)
$ git push origin ft/squashing
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 709 bytes | 236.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions/pull/new/ft
/squashing
remote:
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/squashing -> ft/squashing

HP@DESKTOP-514LIR9 MINGW64 ~/git_exercises (ft/squashing)
$
```
## Bundle 5
### Exercise 2
```bash

HP@DESKTOP-514LIR9 MINGW64 ~
$ git clone https://github.com/UwayoOlga/git-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (15/15), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 107 (delta 5), reused 4 (delta 4), pack-reused 92 (from 1)
Receiving objects: 100% (107/107), 1.95 MiB | 1.82 MiB/s, done.
Resolving deltas: 100% (5/5), done.

HP@DESKTOP-514LIR9 MINGW64 ~
$ cd git-cafe-exercise

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ code .

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git add index.html

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git commit -m "Changed text to 'Welcome to our restaurant'"
[main 4db2549] Changed text to 'Welcome to our restaurant'
 1 file changed, 1 insertion(+), 1 deletion(-)

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 339 bytes | 339.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/UwayoOlga/git-cafe-exercise.git
   d1d3f9c..4db2549  main -> main

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$
```
## Bundle 6
### Exercise 1
```bash
HP@DESKTOP-514LIR9 MINGW64 ~
$ git clone https://github.com/UwayoOlga/git-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (15/15), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 107 (delta 5), reused 4 (delta 4), pack-reused 92 (from 1)
Receiving objects: 100% (107/107), 1.95 MiB | 1.82 MiB/s, done.
Resolving deltas: 100% (5/5), done.

HP@DESKTOP-514LIR9 MINGW64 ~
$ cd git-cafe-exercise

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ code .

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git add index.html

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git commit -m "Changed text to 'Welcome to our restaurant'"
[main 4db2549] Changed text to 'Welcome to our restaurant'
 1 file changed, 1 insertion(+), 1 deletion(-)

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 339 bytes | 339.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/UwayoOlga/git-cafe-exercise.git
   d1d3f9c..4db2549  main -> main

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ cd git-cafe-exercise
bash: cd: git-cafe-exercise: No such file or directory

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ pwd
/c/Users/HP/git-cafe-exercise

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ ls
README.md  css/     index-1.html  index-3.html  index.html
bat/       images/  index-2.html  index-4.html  js/

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git checkout -b ft/menu-page
Switched to a new branch 'ft/menu-page'

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (ft/menu-page)
$ touch menu.html

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (ft/menu-page)
$ git add menu.html

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (ft/menu-page)
$ git commit -m "Added menu.html page"
[ft/menu-page 58ca7ed] Added menu.html page
 1 file changed, 96 insertions(+)
 create mode 100644 menu.html

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (ft/menu-page)
$ git push origin ft/menu-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.03 KiB | 1.03 MiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/menu-page' on GitHub by visiting:
remote:      https://github.com/UwayoOlga/git-cafe-exercise/pull/new/ft/menu-pag
e
remote:
To https://github.com/UwayoOlga/git-cafe-exercise.git
 * [new branch]      ft/menu-page -> ft/menu-page

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (ft/menu-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git pull origin main
From https://github.com/UwayoOlga/git-cafe-exercise
 * branch            main       -> FETCH_HEAD
Already up to date.

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ gh pr create --base main --head ft/menu-page --title "Added menu.html page" --body "This PR adds the menu.html page."
bash: gh: command not found

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git checkout ft/menu-page
Switched to branch 'ft/menu-page'

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (ft/menu-page)
$ git add menu.html

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (ft/menu-page)
$ git commit -m "Added menu.html page"
[ft/menu-page 7f1b537] Added menu.html page
 1 file changed, 4 insertions(+), 4 deletions(-)

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (ft/menu-page)
$ git push origin ft/menu-page
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 318 bytes | 318.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/UwayoOlga/git-cafe-exercise.git
   58ca7ed..7f1b537  ft/menu-page -> ft/menu-page

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (ft/menu-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git pull origin main
From https://github.com/UwayoOlga/git-cafe-exercise
 * branch            main       -> FETCH_HEAD
Already up to date.

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git merge ft/menu-page
Updating 4db2549..7f1b537
Fast-forward
 menu.html | 96 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 96 insertions(+)
 create mode 100644 menu.html

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git push origin main
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/UwayoOlga/git-cafe-exercise.git
   4db2549..7f1b537  main -> main
 
``` 
## Bundle 6
### Exercise 2
```bash
HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (main)
$ git checkout -b bugfix
Switched to a new branch 'bugfix'

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (bugfix)
$ git add index-4.html

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (bugfix)
$ git commit -m "Update title of index-4.html to 'Contact'"
[bugfix 077aa92] Update title of index-4.html to 'Contact'
 1 file changed, 1 insertion(+), 1 deletion(-)


HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (bugfix)
$ git push origin bugfix
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 323 bytes | 323.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'bugfix' on GitHub by visiting:
remote:      https://github.com/UwayoOlga/git-cafe-exercise/pull/new/bugfix
remote:
To https://github.com/UwayoOlga/git-cafe-exercise.git
 * [new branch]      bugfix -> bugfix

HP@DESKTOP-514LIR9 MINGW64 ~/git-cafe-exercise (bugfix)
$

 
