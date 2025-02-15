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
