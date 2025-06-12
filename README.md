# Git
## What is Git :-
• Git is a version control system.
• Git helps you keep track of code changes.
• Git is used to collaborate on code.
• Git and GitHub are different things.

## What is GitHub :-
Git is not the same as GitHub.
• GitHub makes tools that use Git.
• GitHub is the largest host of source code in the world, and has
been owned by Microsoft since 2018.

## Git Branching :-
In Git, a branch is a new/separate version of the main repository.
Branches allow you to work on different parts of a project without
impacting the main branch. When the work is complete, a branch can be
merged with the main project.
We can even switch between branches and work on different
projects without them interfering with each other.

## Git Reset :-
‘reset’ is the command we use when we want to move the repository
back to a previous commit, discarding any changes made after that commit.
First, get the seven characters of the commit hash from the log for the
commit that you want to go back for. Then we reset our repository back to
that specific commit using ‘git reset commithash’ (commithash being the first
7 characters of the commit hash we found in the log)

**$ git reset <commithash>**


/**/Creating two file**

-rw-r--r-- 1 jbasone 1049089 677 Apr 14 20:17 Day-01-Task.java
-rw-r--r-- 1 jbasone 1049089 677 Apr 14 20:17 Day-02-Task.java

//Setup of the Git 
**$ git init**

//Add both the file
**$ git add Day-01-Task.java**

//Commit both the command

**$ git commit -m "First day task completed"**


**$ git add Day-02-Task.java**
**$ git commit -m "Second day task completed"**

//Check the file are commited
$ git log
commit 3f58bc54eac868e76dd97c7209b92f7d94dbd6fa (HEAD -> master)
Author: Jayant-git-debug <jayantbasone100@yahoo.com>
Date:   Mon Apr 14 20:23:23 2025 +0530

    Second day task completed

commit c8a66b6e8c359b5ff08237a00639810f991c574a
Author: Jayant-git-debug <jayantbasone100@yahoo.com>
Date:   Mon Apr 14 20:21:37 2025 +0530

    First day task completed

 ## //Check any reposrity are added or not 
**$ git remote -v**

## // Add reposritry
$ git remote add origin https://github.com/Jayant-git-debug/Git_JB.git
$ git remote -v
origin  https://github.com/Jayant-git-debug/Git_JB.git (fetch)
origin  https://github.com/Jayant-git-debug/Git_JB.git (push)

## //Now Push the Commited file to git resporitry
** $ git push -u origin main**

## //Branch :  How to create the barnch and how checkout the branch

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (main)
$ ls
Day-01-Task.java  Day-02-Task.java  Git-Traning-Data.txt

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (main)
$ ls
Day-01-Task.java  Day-02-Task.java  Git-Traning-Data.txt


jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (main)
$ ls
Day-01-Task.java  Day-02-Task.java  Git-Traning-Data.txt
$ ls
Day-01-Task.java  Day-02-Task.java  Git-Traning-Data.txt
Day-01-Task.java  Day-02-Task.java  Git-Traning-Data.txt

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (main)
jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (main)
$ git branch
* main

* main


jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (main)
**$ git branch feature**

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (main)
**$ git branch
  feature
* main**

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (main)
**$ git checkout feature**
Switched to branch 'feature'

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (feature)
$

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (feature)
**$ git status**
On branch feature
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Test_python.py


jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (feature)
**$ git add .**

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (feature)
$ git commit -m "This is my python Program"

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (feature)
$ git log --oneline
1689c3c (HEAD -> feature) This is my python Program
d78bdce (origin/main, main) This is for Documention
3f58bc5 Second day task completed
c8a66b6 First day task completed

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (feature)
**$ git remote -v**
origin  https://github.com/Jayant-git-debug/Git_JB.git (fetch)
origin  https://github.com/Jayant-git-debug/Git_JB.git (push) 

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (feature)
**$ git push -u origin feature**
Enumerating objects: 4, done.      
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 342 bytes | 171.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'feature' on GitHub by visiting:
remote:      https://github.com/Jayant-git-debug/Git_JB/pull/new/feature
remote:
To https://github.com/Jayant-git-debug/Git_JB.git
 * [new branch]      feature -> feature
branch 'feature' set up to track 'origin/feature'.

## //How to pull or passing the file one branch to another

Goto -> Pull request->select from which branch to main branch movement->crate the pull request -> review the code

## //If you want to reivew the changes to some one 

Goto -> Pull request->select from which branch to main branch movement->crate the pull request -> review the code -> Assign -> search the name->provide the description->create

## //The peron who you assign he got notification or mail for the approval

## //Shortcut for the git branch :to create the branch as well checkout

jbasone@jbasone-lap MINGW64 ~/Documents/DEVOPS/Radical/Git (main)
$ git checkout -b rise
Switched to a new branch 'rise'

$ git branch
  main
* rise

## //How to fetch details by using of the pull command

jbasone@jbasone-lap MINGW64 /e/Folder/16_04_25
$ git init
Initialized empty Git repository in E:/Folder/16_04_25/.git/

jbasone@jbasone-lap MINGW64 /e/Folder/16_04_25 (master)
$ git remote -v

jbasone@jbasone-lap MINGW64 /e/Folder/16_04_25 (master)
$ git remote add origin https://github.com/Jayant-git-debug/Git_JB.git

jbasone@jbasone-lap MINGW64 /e/Folder/16_04_25 (master)
$ git pull origin main
remote: Enumerating objects: 22, done.
remote: Counting objects: 100% (22/22), done.
remote: Compressing objects: 100% (19/19), done.
remote: Total 22 (delta 9), reused 8 (delta 1), pack-reused 0 (from 0)
Unpacking objects: 100% (22/22), 6.06 KiB | 33.00 KiB/s, done.
From https://github.com/Jayant-git-debug/Git_JB
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> origin/main

## //Merg command use

It’s preferred to change/switch to master branch before any branch
needs to be merged with it.

$ git merge <branch name>
This will merge the specified branch with our master branch.

//









