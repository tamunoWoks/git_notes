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
#### Pull from the Current Branch:
If you're already on the branch you want to pull, you can use:
```bash
git pull
```
This assumes the local branch is tracking a remote branch. If not, you may need to set the upstream branch (see below).
#### Pull and Rebase Instead of Merge:
If you want to avoid creating a merge commit and instead rebase your local changes on top of the remote changes, use:
```bash
git pull --rebase
```
#### Set Upstream Branch:
If your local branch isn't tracking a remote branch yet, you can set the upstream branch and pull in one command:
```bash
git pull -u origin <branch-name>
```
