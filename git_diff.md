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
