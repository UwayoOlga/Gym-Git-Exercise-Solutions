# Git Exercise 
## Bundle 1
### Exercise 1

``` 
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

```

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
```

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
```

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

