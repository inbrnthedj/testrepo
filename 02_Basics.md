Some basic things

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


### Github Workflow

When developing a feature...
1. **Cloning the remote repository** (into local computer) : creates a complete version history
2. **Pushing** (to remote) **and pulling changes** (changes from remote to local)
3. **Implementing the feature** : update files in local repository
4. **Creating a branch** : make changes in a new isolated branch without affecting the main branch - add a feature without affecting the main branch
5. **Commiting files** : move the files to the staging area (a temporary storage) and then commit the new feature to the newly created branch
6. **Pushing changes to the remote repository** : push in the branch 
7. **Reviewing the code** : Pull request and let the main branch manager control the code and verify if it's ready to be merged to the main branch

When Starting a new project...
1. Create a local repository
2. Select files to include
3. Move to staging area
4. Commit to local git repository
5. Push all the project file to the remote repository
6. Cloning of repository to develop project


In other words..
START OF PROJECT
1. Initialize Git Repository (locally)
2. Select and move project files to Staging Area
3. Perform initial commit (to local repository)
4. Push commit to blank remote repository\

5. Clone remote repository (for feature development)
7. Create branches for features needed
8. Commit changes to individual branches
9. Push local branch to remote branch
10. Create a pull request
11. 
 
