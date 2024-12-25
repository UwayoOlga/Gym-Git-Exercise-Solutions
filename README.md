# Git exercise 
## Bundle1
### Exercise 1
PS C:\Users\HP\git_exercises> git branch     
PS C:\Users\HP\git_exercises> git status     H
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" tttrack)
o track)
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
-a----        12/25/2024   7:25 AM             28 file1. 
                                                  txt    

PS C:\Users\HP\git_exercises> git remote add origin https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git   
PS C:\Users\HP\git_exercises> git status 
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   file1.txt

PS C:\Users\HP\git_exercises> git commit -m "Added file1.txt to repository"
>> 
Author identity unknown
*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

Omit --global to set the identity only in this repository.

fatal: unable to auto-detect egit config --global user.name "UwayoOlga"ne)')
>> git config --global user.email "uwayoolga@gmail.com"
PS C:\Users\HP\git_exercises> git commit -m "Added file1.txt to repository"
>>
[main (root-commit) 2b69a9e] Added file1.txt to repository
 1 file changed, 0 insertions(+), 0 deletions(-)
>> C:\Users\HP\git_exercises>
info: please complete authentication in your browser...
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\HP\git_exercises> 
PS C:\Users\HP\git_exercises> git push -u origin main
>>
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: use 'git pull' before pushing again.
PS C:\Users\HP\git_exercises> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use
    git push --set-upstream origin main
To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\HP\git_exercises>     git push --set-upstream origin main
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git'
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\HP\git_exercises> git push --set-upstream origin main    
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
PS C:\Users\HP\git_exercises> git checkout main
>>
Already on 'main'
PS C:\Users\HP\git_exercises> git pull origin main
From https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
fatal: refusing to merge unrelated histories
PS C:\Users\HP\git_exercises>
PS C:\Users\HP\git_exercises> git push origin main
>>
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
error: failed to push some refs to 'https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\HP\git_exercises> git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>


    git branch --set-upstream-to=origin/<branch> main

PS C:\Users\HP\git_exercises> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use


upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\HP\git_exercises> git push --set-upstream origin main
PS C:\Users\HP\git_exercises> git pull origin main
From https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
PS C:\Users\HP\git_exercises> git add <file_with_conflict>
At line:1 char:9
+ git add <file_with_conflict>
+         ~
The '<' operator is reserved for future use.
    + CategoryInfo          : ParserError: (:) [], ParentContainsErrorRecordException
    + FullyQualifiedErrorId : RedirectionNotSupported
 
>> 
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 254 bytes | 127.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 + 4e04d4e...2b69a9e main -> main (forced update)
PS C:\Users\HP\git_exercises> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\HP\git_exercises> git status
nothing to commit, working tree clean
PS C:\Users\HP\git_exercises> git checkout dev
Already on 'dev'
PS C:\Users\HP\git_exercises> git status
On branch dev
PS C:\Users\HP\git_exercises> git push
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\HP\git_exercises> git push --set-upstream origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/UwayoOlga/Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
PS C:\Users\HP\git_exercises> git push
Everything up-to-date
PS C:\Users\HP\git_exercises> git checkout -b test
>>
Switched to a new branch 'test'
PS C:\Users\HP\git_exercises> git checkout dev
>>
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.
PS C:\Users\HP\git_exercises> git branch -d test
>>
Deleted branch test (was 2b69a9e).
PS C:\Users\HP\git_exercises> git push  
Everything up-to-date
PS C:\Users\HP\git_exercises> 
