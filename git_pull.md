## git pull
The git pull command is used to fetch changes from a remote repository and integrate them into your local branch. It’s essentially a combination of two commands: git fetch (to download changes) and git merge (to integrate them into your local branch). This is how you keep your local repository up to date with the remote repository.
#### Syntax:
```bash
git pull <remote-name> <branch-name>
```
**`<remote-name>`:** The name of the remote repository (usually origin by default).  
**`<branch-name>`:** The name of the branch you want to pull from.
#### Common Usage Examples
#### Pull from the Default Remote and Branch:
If you're working on the main branch and want to pull from the default remote (origin):
```bash
git pull origin main
```
