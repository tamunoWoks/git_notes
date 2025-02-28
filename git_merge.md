## `git merge`
The `git merge` command is used to combine changes from one branch into another. It integrates the history of two branches, creating a new commit that represents the merged state. This is a key part of Git's branching and merging workflow, allowing you to bring feature branches into the main branch or combine work from multiple contributors.
#### Syntax:
```bash
git merge <branch-name>
```
**`<branch-name>`:** The name of the branch you want to merge into the current branch.
### Common Usage Examples
#### Merge a Branch into the Current Branch:
- To merge a branch (e.g., feature-login) into the current branch (e.g., main):
```bash
git checkout main
git merge feature-login
```
#### Fast-Forward Merge:
If the current branch is directly behind the branch being merged, Git performs a fast-forward merge. This simply moves the current branch pointer forward to match the target branch.
- Example:
```bash
git checkout main
git merge feature-login
```
#### Merge with a Commit Message:
If Git creates a merge commit (e.g., in a non-fast-forward merge), it will open your default text editor for a commit message.  
- You can also provide a message directly:
```bash
git merge -m "Merge feature-login into main" feature-login
```
#### Abort a Merge:
- If you encounter conflicts and want to cancel the merge:
```bash
git merge --abort
```
#### Merge Without Fast-Forward:
- To force Git to create a merge commit even if a fast-forward merge is possible:
```bash
git merge --no-ff <branch-name>
```
#### What Happens When You Merge?
- **Fast-Forward Merge:**
  - If the current branch is directly behind the branch being merged, Git moves the current branch pointer forward to match the target branch.
  - No new commit is created.
- **Three-Way Merge:**
  - If the branches have diverged, Git performs a three-way merge, combining changes from both branches.
  - A new merge commit is created to represent the combined state.
- **Merge Conflicts:**
  - If Git cannot automatically resolve differences between the branches, it pauses the merge and marks the conflicting files.
  - You must manually resolve the conflicts before completing the merge.
### Resolving Merge Conflicts
If a merge results in conflicts, Git will mark the conflicting files and pause the merge. Here's how to resolve conflicts:
#### Check the Status:
```bash
git status
```
Conflicted files will be listed under "Unmerged paths."
#### Open the Conflicting Files:
- Look for conflict markers (<<<<<<<, =======, >>>>>>>).
- Edit the file to resolve the conflict.
Example:
```
<<<<<<< HEAD
This is the change from the current branch.
=======
This is the change from the branch being merged.
>>>>>>> feature-login
```
#### Stage the Resolved Files:
```
git add <file-path>
```
#### Complete the Merge:
```
git commit
```
### Example Workflow
#### Switch to the Target Branch:
```bash
git checkout main
```
#### Merge the Feature Branch:
```bash
git merge feature-login
```
#### Resolve Conflicts (if any):
- Edit the conflicting files.
- Stage the resolved files:
```bash
git add <file-path>
```
- Complete the merge:
```bash
git commit
```
#### Push the Changes:
```bash
git push origin main
```
### Tips
- Always pull the latest changes from the remote repository before merging to avoid conflicts:
```bash
git pull origin main
```
- Use git merge --no-ff to preserve the history of feature branches.
- Regularly delete merged branches to keep your repository clean:
```bash
git branch -d feature-login
```
