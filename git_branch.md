## `git branch`
The `git branch` command is used to manage branches in a Git repository. Branches allow you to work on different versions of your project simultaneously. You can create, list, rename, and delete branches using this command.
#### Syntax:
```bash
git branch [options] [branch-name]
```
**`[branch-name]`:** The name of the branch you want to create, delete, or rename.  
**`[options]`:** Additional flags to modify the behavior of the command.
### Common Usage Examples
#### List All Branches:
- To see a list of all branches in your repository:
```bash
git branch
```
The current branch will be highlighted with an asterisk (*).
- To see remote branches as well:
```bash
git branch -a
```
#### Create a New Branch:
- To create a new branch:
```bash
git branch <branch-name>
```
Example:
```bash
git branch feature-login
```
#### Switch to a Branch:
- To switch to an existing branch, use git checkout or git switch:
``` bash
git checkout <branch-name>
```
- or (Git 2.23+):
```bash
git switch <branch-name>
```
#### Create and Switch to a New Branch:
- To create a new branch and switch to it in one command:
```bash
git checkout -b <branch-name>
```
- or (Git 2.23+):
```bash
git switch -c <branch-name>
```
#### Delete a Branch:
- To delete a branch:
```bash
git branch -d <branch-name>
```
Example:
```bash
git branch -d feature-login
```
- If the branch has unmerged changes, Git will refuse to delete it. To force deletion:
```bash
git branch -D <branch-name>
```
#### Rename a Branch:
- To rename the current branch:
```bash
git branch -m <new-branch-name>
```
- To rename a different branch:
```bash
git branch -m <old-branch-name> <new-branch-name>
```
#### List Merged Branches:
- To see which branches have been merged into the current branch:
```bash
git branch --merged
```
- To see branches that haven’t been merged:
```bash
git branch --no-merged
```
#### Set Upstream Branch:
- To set the upstream (tracking) branch for the current branch:
```bash
git branch --set-upstream-to=origin/<branch-name>
```
#### What Happens When You Create a Branch?
- Git creates a new pointer to the current commit.
- The new branch is independent of other branches until you merge them.
#### Tips:
- Use descriptive branch names to make it clear what the branch is for (e.g., feature-login, bugfix-header, hotfix-security).
- Regularly delete branches that are no longer needed to keep your repository clean.
- Use git branch -a to see both local and remote branches.
### Example Workflow:
- Create a New Branch:
```bash
git branch feature-login
```
- Switch to the New Branch:
```bash
git checkout feature-login
```
- Make Changes and Commit:
```bash
git add .
git commit -m "Add login feature"
```
- Push the Branch to Remote:
```bash
git push -u origin feature-login
```
- Merge the Branch into Main:  
Switch back to the main branch and merge:
```bash
git checkout main
git merge feature-login
```
- Delete the Branch (optional):  
After merging, you can delete the branch:
```bash
git branch -d feature-login
```
