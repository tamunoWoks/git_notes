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
#### - Compare Changes in a Specific Commit:
To see changes introduced by a specific commit:
```bash
git diff <commit>^!
```
Example:
```bash
git diff d3b0738^!
```
#### - Compare Changes Between Working Directory and a Specific Commit:
To see differences between your working directory and a specific commit:
```bash
git diff <commit>
```
Example:
```bash
git diff HEAD~3
```
#### - Word Diff:
To see word-level differences instead of line-level:
```bash
git diff --word-diff
```
#### - Summary of Changes:
To see a summary of changes (e.g., which files were modified):
```bash
git diff --stat
```
### Understanding the Output
The output of `git diff` is in **unified diff format**:
- Lines starting with `+` are additions.
- Lines starting with `-` are deletions.
- Lines without a prefix are context lines.

Example:
```diff
diff --git a/README.md b/README.md
index 1234567..890abcd 100644
--- a/README.md
+++ b/README.md
@@ -1,5 +1,5 @@
 Hello, World!
-This is the old text.
+This is the new text.
 Welcome to the project.
```
### Example Workflow
- Check Unstaged Changes:
```bash
git diff
```
- Check Staged Changes:
```bash
git diff --cached
```
- Compare Two Branches:
```bash
git diff main..feature-login
```
- Review Changes in a Specific File:
```bash
git diff README.md
```
- Summarize Changes:
```bash
git diff --stat
```
### Tips
- Use git diff frequently to review changes before committing.
- Combine git diff with git log to understand the history of changes.
- Use git diff --word-diff for more granular comparisons.

