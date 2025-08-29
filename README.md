# Git Training Repository by Jayant

This repository serves as a learning and reference guide for using Git and GitHub effectively. It includes basic Git operations, branching strategies, reset commands, working with remote repositories, and pull request workflows.

## 📌 What is Git?

- Git is a **version control system**.
- It helps track changes in source code over time.
- Git is used for **collaboration** in teams and managing code history.
- **Note:** Git and GitHub are not the same.

## 📌 What is GitHub?

- GitHub is a **cloud-based platform** that uses Git for version control.
- It allows developers to **host**, **manage**, and **review** code.
- GitHub is the **largest host of source code** and is owned by **Microsoft (since 2018)**.

## 📌 What is the difference between `git fetch` and `git pull`?

- `git fetch`: Downloads changes from the remote repository without merging them.
- `git pull`: Fetches and merges changes from the remote repository into your current branch.

## 🔀 Git Branching

- Branching creates an **isolated version** of the project for development.
- Use branches to work on features or fixes **without affecting the main branch**.
- After completion, branches can be **merged back** to the main branch.
- Switching between branches allows working on multiple versions in parallel.

### Commands:
```bash
$ git branch feature # Create branch
$ git checkout feature # Switch to branch
$ git checkout -b rise # Create and switch in one command
$ git branch # List branches
$ git merge <branch-name> # Merge into current branch
```


## ♻️ Git Reset

Use `reset` to revert your repo to a previous commit and discard newer changes.

### Steps:
```bash
$ git log # Get commit hash (7 chars)
$ git reset <commithash> # Reset to that commit
```

## 📁 File Creation & Commit Example

### Files Created:
Day-01-Task.java
Day-02-Task.java


### Git Setup & Commit:
```bash
$ git init
$ git add Day-01-Task.java
$ git commit -m "First day task completed"

$ git add Day-02-Task.java
$ git commit -m "Second day task completed"


### Git Log Output:
$ git log
commit 3f58bc5 - Second day task completed
commit c8a66b6 - First day task completed
```
## 🌐 Connecting to GitHub
```bash
$ git remote -v # Check remotes
$ git remote add origin https://github.com/Jayant-git-debug/Git_JB.git
$ git push -u origin main # Push to GitHub
```

## 🚀 Working with Feature Branch

```bash
$ git branch feature
$ git checkout feature
```
## Add and commit file in feature branch
```bash
$ git add Test_python.py
$ git commit -m "This is my python Program"
$ git push -u origin feature
```


## 🔁 Pull Requests & Code Review

1. Go to GitHub → **Pull Requests**.
2. Click **New Pull Request**.
3. Choose **source branch** (e.g., `feature`) and **target branch** (e.g., `main`).
4. Add description, assign reviewer, and click **Create**.
5. Assigned reviewer gets a **notification/email** to review and approve.

## ⬇️ Git Pull to Clone Repository
```bash
$ git init
$ git remote add origin https://github.com/Jayant-git-debug/Git_JB.git
$ git pull origin main
```
## 🌿 Git Branch List Example
```bash
$ git branch
feature
* main
```
## How to change git to push remote master branch to main branch on github
```bash
git push -u origin master:main
```


## 🎨 Git Branch Naming Convention (Blue-Green Deployment)
Used in deployment strategies for staging and production environments.

| Branch | Purpose                    |
|--------|----------------------------|
| blue   | Staging / UAT environment  |
| green  | Production / Live version  |

> In **Blue-Green Deployment**:
> - `blue` = current live system
> - `green` = new candidate version  
> Switch traffic between environments for **zero-downtime deployment**.

## ✅ Common Git Commands Summary
| Command | Description |
|---------|-------------|
| `git init` | Initialize a local repo |
| `git add <file>` | Stage file |
| `git commit -m ""` | Commit changes |
| `git log` | View commit history |
| `git branch` | Show all branches |
| `git checkout <branch>` | Switch branch |
| `git checkout -b <branch>` | Create and switch to new branch |
| `git merge <branch>` | Merge into current branch |
| `git remote -v` | Show remote links |
| `git remote add origin <url>` | Connect to remote |
| `git push -u origin <branch>` | Push to remote |
| `git pull origin <branch>` | Pull from remote |





