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

