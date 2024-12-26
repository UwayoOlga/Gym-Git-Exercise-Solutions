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
