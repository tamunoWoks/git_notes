## `git diff`
The git diff command is used to show differences between various states of your repository. It can compare changes between:
- The working directory and the staging area (index).
- The staging area and the latest commit.
- Two commits or branches.
- Specific files or directories.  

This command is incredibly useful for reviewing changes before committing or merging.
### Syntax
```bash
git diff [options] [commit1] [commit2] [--] [path]
```
- **``[options]``:** Additional flags to customize the output.
- **``[commit1]``** and **``[commit2]``:** Commits, branches, or tags to compare.
- **``[--]``:** Separates options from file paths.
- **``[path]``:** Specific file or directory to compare.
### Common Usage Examples
#### - Compare Working Directory and Staging Area:
To see changes in your working directory that are not yet staged:
```bash
git diff
```
#### - Compare Staging Area and Latest Commit:
To see changes that are staged but not yet committed:
```bash
git diff --cached
```
or:
```bash
git diff --staged
```
#### - Compare Working Directory and Latest Commit:
To see all changes in your working directory (both staged and unstaged):
```bash
git diff HEAD
```
#### - Compare Two Commits:
To see differences between two commits:
```bash
git diff <commit1> <commit2>
```
Example:
```bash
git diff d3b0738 a1b2c3d
```
#### - Compare Two Branches:
To see differences between two branches:
```bash
git diff <branch1>..<branch2>
```
Example:
```bash
git diff main..feature-login
```
#### - Compare Specific File:
To see changes in a specific file:
```bash
git diff <file-path>
```
Example:
```bash
git diff README.md
```
