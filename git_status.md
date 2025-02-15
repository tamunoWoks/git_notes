## git status
The git status command is one of the most frequently used Git commands. It provides a summary of the current state of your working directory and staging area. This includes information about which files are staged, unstaged, untracked, or have conflicts. It’s a great way to see what changes Git is tracking and what actions you might need to take next.
#### Syntax:
```bash
git status
```
#### What Does git status Show?
When you run git status, Git provides the following information:
- **Current Branch:** Tells you which branch you're currently on.
- **Changes to be Committed (Staged Changes):** Lists files that have been staged (added to the index) using git add and are ready to be committed.
- **Changes not staged for Commit (Unstaged Changes):** Lists files that have been modified but not yet staged for commit.
- **Untracked Files:** Lists files that are in your working directory but not yet tracked by Git.
- **Branch Status:** If your branch is ahead or behind the remote branch, Git will notify you.
- **Merge or Rebase Status:** If you're in the middle of a merge or rebase, git status will show the current state and any conflicts that need to be resolved.
### Example Output:
Here’s an example of what git status might display:
```bash
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   script.js

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        styles.css
```
### Common Scenarios and What to Do
#### Staged Changes:
If you see files under "Changes to be committed," you can proceed to commit them:
```bash
git commit -m "Your commit message"
```
#### Unstaged Changes:
If you see files under "Changes not staged for commit," you need to stage them first:
```bash
git add <file>
```
#### Untracked Files:
If you see files under "Untracked files," you can start tracking them by staging them:
```bash
git add <file>
```
#### Branch Status:
If your branch is ahead of the remote, you can push your changes:
```bash
git push origin <branch-name>
```
If your branch is behind, you can pull the latest changes:
```bash
git pull origin <branch-name>
```
#### Merge Conflicts:
If you’re in the middle of a merge and have conflicts, git status will list the conflicting files. Resolve the conflicts, stage the files, and complete the merge:
```bash
git add <resolved-file>
git commit
```
#### Short Status:
For a more concise summary, you can use the -s or --short flag:
```bash
git status -s
```
Example output:
```
 M README.md
A  script.js
M  index.html
?? styles.css
```
- **M:** Modified file (staged or unstaged).
- **A:** Added file (staged).
- **??:** Untracked file.
#### Tips
- Run git status frequently to stay aware of the state of your working directory.
- Use git status before committing to ensure you’re including all the changes you intend to.
- If you’re unsure what to do next, git status often provides helpful hints in its output.
