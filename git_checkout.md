## git checkout
The git checkout command is one of the most versatile commands in Git. It is primarily used to switch between branches, restore files, or create new branches. It allows you to navigate through different versions of your project and work on different branches.
#### Syntax:
```bash
git checkout [options] <branch-or-commit>
```
**`<branch-or-commit>`:** The name of the branch or the commit hash you want to switch to.  
**`[options]`:** Additional flags to modify the behavior of the command.
### Common Usage Examples
#### Switch to an Existing Branch:
- To switch to an existing branch:
```bash
git checkout <branch-name>
```
Example:
```bash
git checkout main
```
#### Create and Switch to a New Branch:
- To create a new branch and switch to it in one command:
```bash
git checkout -b <new-branch-name>
```
Example:
```bash
git checkout -b feature-login
```
#### Switch to a Specific Commit:
- To switch to a specific commit (detached HEAD state):
```bash
git checkout <commit-hash>
```
Example:
```bash
git checkout d3b07384d113edec49eaa6238ad5ff00
```
#### Restore a File from a Specific Commit:
- To restore a file to its state in a specific commit:
```bash
git checkout <commit-hash> -- <file-path>
```
Example:
```bash
git checkout d3b07384d113edec49eaa6238ad5ff00 -- README.md
```
#### Discard Changes in a File:
- To discard changes in a file and restore it to the state in the last commit:
```bash
git checkout -- <file-path>
```
Example:
```bash
git checkout -- README.md
```
