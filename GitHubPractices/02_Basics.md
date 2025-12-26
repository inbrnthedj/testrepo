Some basic things
---
### Github Branches
Creates a copy of the main branch and allows check and verification 
if can be inserted in the main branch. Code is usually branched while 
new features are being developed. Branches can be merged when it has 
been checked and verified. In this case, each branch's code is 
identified as a "Feature Tip"
- **Commit Changes**: used when the developer is convinced that the code can be added to the main branch. Don't end the Commit message with a period (don't know why yet). Description is best to have less than 50 characters
- **Pull Request**: used when we need others to review our proposed changed/commit. The pull request can follow any commits, even if code is unfinished and can target specific users. By default, if you make a change on a branch you do not own, it's considered as a pull request and not a commit. Details of the approval of a pull request will be present in log files.

Note that the Main branch is the only deployed code and changes are not released until:
1. Commited
2. Pull command is issued
3. Code is reviewed and approved
4. Approved code is merged into the main branch

---
### Github Workflow

When *Starting a new project*...
1. **Create a local repository** : initial Git repository inside local pc
2. **Select files to include** : any files related to the new project
3. **Move to staging area** : the staging area is a temporary storage where files are put before commiting changes
4. **Commit to local git repository** : update to local main branch
5. **Push all the project file to the remote repository** : officially create the remote repository for collaboration
6. **Cloning of repository to develop project** : by individual developers to create changes / features
7. ...
8. **Review and approve codes** : the owner of the repository verifies the code and merge the respective branches to the main branch

When *Developing a feature*...
1. **Cloning the remote repository** (into local computer) : creates a complete version history, pull changes when needed
2. **Creating a branch** : create a new isolated branch and work on it without affecting the main branch
3. **Commiting files** : move the files to the staging area (a temporary storage) and then commit (locally) the new feature to the newly created branch
4. **Pushing changes to the remote repository** : push in the remote repository (the new branch) 
5. **Pull request for review** : Pull request and let the main branch manager control the code and verify if it's ready to be merged to the main branch

When *Releasing project*...
1. **Creation of release branch**: lead developer finished all reviews an merged codes to main branch and is now ready to create another branch for release from the main branch in the remote repository
2. **Pull change from remote release branch**: each developer will update their local clones
3. **Perform test and updates**: individual developers will test and makes documentation updates regarding the release
4. **Push commits to remote and create pull request**: each developer will commit the tested and updated code and creates a pull request to finalize project
5. **Approval of pull request and merge changes** : Lead developer will review changes and approve pull requests then proceeds to merging the changes to the release branch 

---
### General Commands

#### Command-Line commands
- **mkdir**: creates new directory (where repositories are stored)
- **cd**: navigate to the directory

#### Git commands:
- **git init**: sets up necessary files and data structures for project's version control
- **git add**: moves changes from the working directory to the staging area / pushes new changes to staging area
  - **git add <"filename.txt">**: to add a specific file (withouth " ")
  - **git add .**: to add all the new or changed files in the current directory
  - **git add -A**: to add all changes in the entire working tree regardless of where you are in the directory
 
- **git reset**: resets changes in the working directory; when used with
  - **git reset --hard HEAD**: (two dashes) discards/deletes all uncommited changes made to the working directory and staging area and resets the repository to the last commit (HEAD). Changes cannot be recovered.
- **git commit - m "text"**: saves changes with a descriptive message "text" (with " ")
- **git log**: enables to browse previous changes to a project
- **git branch**: lists, creates, rename and deletes branches. to delete a branch, first check out the branch using **git checkout** and then run the command
  - **git branch** : lists branches
  - **git branch <'new-branch'>**: creates a new branch (without ' ')
  - **git branch -d <'branch-name'>**: deletes branch (without ' ')
- **git checkout**: allows to switch between existing branches
  - **git checkout main**: switches to the main branch
- **git merge**: merges feature branch to main branch
- **git status**: allows to view the status of all changes
- **git clone**: copies repository from a remote source to your local machine in your currect working directory.
  - *Syntax:* **git clone <'repository URL'>** (without ' ')
- **git pull**: fetches changes from a remote repository and merges into current local branch
  - *Syntax:* **git pull origin main**
- **git push**: uploads local repository content to remote repository
  - *Syntax:* **git push origin <'branch-name'>** (without ' ')
- **git version**: displays current Git version installed
- **git diff**: shows changes between commits, cmmit and working tree. compares branches
  - **git diff**: shows diff between working dir and last commit
  - **git diff HEAD~1 HEAD**: shows diff between last and second-last commits
  - **git diff <'branch-1'> <'branch-2'>**: compares the specified branches
 
- **git revert**: reverts commit by applying a new commit - undoes changes by the last commit
  - *Syntax:* **git revert HEAD**
 
- **git config -global user.email <'YourGitHubE-mail'>**: sets global e-mail config for Git that has to be executed before doing a commit to authenticate the user's email ID. (without ' ')
- **git config -global user.name <'YourGitHubUsername'>**: sets global username config fot Git. execute before commit. (without ' ')

##### Moving directories
- **cd subDirectoryName**: moves to subDirectoryName folder
- **cd ..**: moves one higher directory level
- **cd ../..**: moves two higher directory levels
- **cd ~**: moves to home directory