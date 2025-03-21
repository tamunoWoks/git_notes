## `git reset`
The `git reset` command is used to undo changes in your repository. It can modify the state of your working directory, staging area (index), and commit history. This command is powerful and should be used with caution, as it can overwrite or discard changes.
#### Syntax:
```bash
git reset [mode] [commit]
```
- **`[mode]`:** Determines how the reset is performed. Common modes are `--soft`, `--mixed`, and `--hard`.
- **`[commit]`:** The commit to reset to (default is `HEAD`).
### Common Usage Examples
#### Unstage Changes (Mixed Reset):
To unstage changes but keep them in your working directory:
```bash
git reset
```
or:
```bash
git reset --mixed
```
#### Reset to a Specific Commit:
To reset the current branch to a specific commit:
```bash
git reset <commit>
```
- Example:
```bash
git reset d3b0738
```
#### Soft Reset:
To reset the branch pointer to a specific commit but keep changes in the staging area and working directory:
```bash
git reset --soft <commit>
```
- Example:
```bash
git reset --soft HEAD~1
```
#### Hard Reset:
To reset the branch pointer, staging area, and working directory to a specific commit (discarding all changes):
```bash
git reset --hard <commit>
```
- Example:
```bash
git reset --hard HEAD~1
```
#### Reset a Specific File:
To reset a specific file to its state in a specific commit:
```bash
git reset <commit> -- <file-path>
```
- Example:
```bash
git reset HEAD -- README.md
```
#### Undo the Last Commit:
To undo the last commit but keep the changes in your working directory:
```bash
git reset --soft HEAD~1
```
#### Undo the Last Commit and Discard Changes:
To undo the last commit and discard all changes:
```bash
git reset --hard HEAD~1
```
### Modes of `git reset`
| Mode | Effect |
|------|--------|
| `--soft` |	Resets the branch pointer but keeps changes in the staging area and working directory. |
| `--mixed` |	Resets the branch pointer and staging area but keeps changes in the working directory (default mode). |
| `--hard` |	Resets the branch pointer, staging area, and working directory (discards all changes). |
### Common Scenarios and Solutions
#### Unstage Changes:
If you accidentally staged changes and want to unstage them:
```bash
git reset
```
