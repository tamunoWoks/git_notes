## `git fetch`

The git fetch command is used to download changes from a remote repository to your local repository. Unlike git pull, which automatically merges the changes into your working directory, git fetch only updates your local copy of the remote repository. This allows you to review changes before integrating them into your work.
#### Syntax
```bash
git fetch <remote-name> [branch-name]
```
- **`<remote-name>`:** The name of the remote repository (usually origin by default).
- **`[branch-name]`:** (Optional) The specific branch you want to fetch. If omitted, Git fetches all branches from the remote.
### Common Usage Examples
#### Fetch All Branches from the Remote:
- To fetch all branches and updates from the remote repository:
```bash
git fetch origin
```
#### Fetch a Specific Branch:
- To fetch updates for a specific branch (e.g., main):
```bash
git fetch origin main
```
#### Fetch and Prune Deleted Branches:
- To remove local references to branches that have been deleted on the remote:
```bash
git fetch --prune
```
#### Fetch Tags:
- To fetch all tags from the remote repository:
```bash
git fetch --tags
```
#### Fetch and Display Changes:
- To fetch changes and display what’s new:
```bash
git fetch origin
git log origin/main..main
```
#### What Happens When You Fetch?
- Git downloads the latest changes (commits, branches, and tags) from the remote repository.
- These changes are stored in your local repository but not merged into your working directory.
- You can review the changes using commands like `git log`, `git diff`, or `git status`.
#### Key Differences Between git fetch and git pull:
| Command | Behavior |
|-----------|-------------|
| `git fetch` | Downloads changes from the remote repository but does not merge them. |
| `git pull` | Downloads changes from the remote repository and merges them into your branch. |
### Common Scenarios and Solutions
