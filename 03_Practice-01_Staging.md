## Description
This is a documentation of my git practice using Git Bash following w3schools course on Git
- **Argument**: Staging
- **Source**: w3schools.com
- **Date**: 26/12/2025

---


Following the lectures in w3schools.com, I followed the codes used to create, add and remove files to/from the staging environment.

git -- version
- showed version of git bash

mkdir PythonProject
- created a repository (folder)
- I named it PythonProject because I'm going to create a repository locally for my Python Practices

cd PythonProject
- moved to PythonProject directory (folder)

git init
- made the folder a git repository

ls
- listed all the items stored

git status
- said the repository had no commits yet
- it listed the untracked files: only one in this case
  - index.html is an html file w3schools provided to be saved in the directory created.
- it said that there's nothing to commit but untracked fiels are present

git add --all
- puts all the file (just index.html in this case) in the staging environment

git status
- said the repository had no commits yet
- has a list of all changes to be commited, indicating that a new file is found: index.html
  - index.html is successfully put into the staged environment

git restore --staged index.html
- is supposed to remove index.html but didn't work

git reset HEAD index.html
- another solution in w3schools but didn't work

git rm --cached index.html
- a solution I realized that was written everytime I entered git status

---
others:
- **git add -A** : another way to add all files to staging area
- **git commit -m** : commit staged changes with message
- **git commit -a -m**: commit all tracked changes with message, skipping staging (-a)
  - DOES NOT WORK FOR NEW/UNTRACKED FILES
  - new/untracked files need to go to staging area (use **git add filename**)

- **git commit** (without -m): commit staged changes with multiline message - a text editor will open
- **git commit --allow-empty -m "Start project"**: create empty commit
- **git commit --no-edit** : use previous commit message
- **git commit --amend --no-edit** : quickly add staged message to previous commit, same message
- **git log**: lists all commits
  - **git log --oneline**: shorter view
  - **git log --stat**: see which files changed in each commit
