## Week 2

### Advanced Git Interaction

**`git commit -a <file_names>`** : Skips the staging phase and commits the file. This works only when the file is already staged once.

**`git log -p <file_name>`** : Shows log info with patch **(lines added and deleted)** of the file.

**`git show <commit_id>`** : Shows the info of the specified commit_id.

**`git diff`** : Shows all the differnce that has been occured in all the changed files. **--staged** flag shows same info all staged files.

**`git add -p <file_name>`** : Allows to review the patch **(lines added and deleted)** before adding to staged area.

**`git rm <file_name>`** : Removes file from the directory. This operation is also staged.

**`git mv <old_file_name> <new_file_name>`** : Changes the name of the file. This Operartion is also staged.

**`.gitignore`** : This file stores the contents that will be ignored by git for tracking.ss

### Undoing Things

**`git checkout <file_name>`** : Restores the file specified to latest commited version i.e discard all changes of the file in working tree. Works on unstaged area.

**`git reset HEAD <file_name>`** : Removes the file from staged area while maintaining latest snapshot of the tree.

**`git commit --amend`** : It modifies the latest commit. **Should be used for local commits only not public commits**

**`git revert HEAD`** : It removes all the changes of the previous commit and creates a new commit. Use **<commit_id>** inplace of **HEAD** to rollback to the specified commit.

### Branching and Merging

**`git branch`** : Displays all branches of the repo.

**`git branch <new_branch_name>`** : Creates new branch with **<new_branch_name>**. Use **-d** flag to delete the branch which already exists. **-D** deletes the branch forcefully.

**`git checkout <branch_name>`** : Switches to **<branch_name>**.

**`git checkout -b <new_branch_name>`** : Create and switches to new branch **<new_branch_name>**

**`git merge <branch_to_be_merged>`** : It merges the **<branch_to_be_merged>** to the current branch.

**`git merge --abort`** : Aborts the current merging process.

**`git log --graph --oneline`**: shows the log history of the tree in the form of graph.

## Week 3

### Introduction to Github

**`git push`** : Pushes all the snapshots of the project to remote repository.

**`git pull`** : Fetches the latest code of the repo from remote to local.

**`git config --global credential.helper cache`** : Provides a 15 minute where password will be asked only once.

### Using a Remote Repository

**`git remote -v`** : Display info about the remote repo like aliases.

**`git remote show origin`** : Displays detailed info of the origin.

**`git fetch`** : Fetches remote updates to local repo.

#### References
[Common gitignore patterns](https://gist.github.com/octocat/9257657)