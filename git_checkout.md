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
