## `git fetch`

The git fetch command is used to download changes from a remote repository to your local repository. Unlike git pull, which automatically merges the changes into your working directory, git fetch only updates your local copy of the remote repository. This allows you to review changes before integrating them into your work.
#### Syntax
```bash
git fetch <remote-name> [branch-name]
```
- **`<remote-name>`:** The name of the remote repository (usually origin by default).
- **`[branch-name]`:** (Optional) The specific branch you want to fetch. If omitted, Git fetches all branches from the remote.
### Common Usage Examples
