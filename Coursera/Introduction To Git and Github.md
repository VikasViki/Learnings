## Week 2

### Advanced Git Interaction

`git commit -a <file_names>` : Skips the staging phase and commits the file. This works only when the file is already staged once.

`git log -p <file_name>` : Shows log info with patch **(lines added and deleted)** of the file.

`git show <commit_id>` : Shows the info of the specified commit_id.

`git diff` : Shows all the differnce that has been occured in all the changed files. **--staged** flag shows same info all staged files.

`git add -p <file_name>` : Allows to review the patch **(lines added and deleted)** before adding to staged area.

`git rm <file_name>` : Removes file from the directory. This operation is also staged.

`git mv <old_file_name> <new_file_name>` : Changes the name of the file. This Operartion is also staged.

`.gitignore` : This file stores the contents that will be ignored by git for tracking.ss


#### References
[Common gitignore patterns](https://gist.github.com/octocat/9257657)