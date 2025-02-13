## git push
The git push command is used to upload your local repository's commits to a remote repository. This is how you share your changes with others or back them up on a remote server (e.g., GitHub, GitLab, Bitbucket). After committing your changes locally, you use `git push` to synchronize your work with the remote repository.
#### Syntax:
```bash
git push <remote-name> <branch-name>
```
- **`<remote-name>`:** The name of the remote repository (usually `origin` by default).
- **`<branch-name>`:** The name of the branch you want to push.
### Common Usage Examples
#### Push to the Default Remote and Branch:
If you're working on the `main` branch and want to push to the default remote (`origin`):
```bash
git push origin main
```
#### Push to the Current Branch:
If you're already on the branch you want to push, you can use:
```bash
git push
```
This assumes the local branch is tracking a remote branch. If not, you may need to set the upstream branch (see below).
#### Push All Branches:
To push all local branches to the remote:
```bash
git push --all origin
```
#### Push Tags:
To push tags (e.g., `v1.0`) to the remote:
```bash
git push origin <tag-name>
```
Or push all tags:
```bash
git push --tags origin
```
#### Force Push (Use with Caution):
If you need to overwrite the remote branch with your local branch (e.g., after rewriting history with `git rebase` or `git commit --amend`), use:
```bash
git push --force origin <branch-name>
```
- **Warning:** Force pushing can overwrite others' work, so use it carefully!
#### Set Upstream Branch:
If your local branch isn't tracking a remote branch yet, you can set the upstream branch and push in one command:
```bash
git push -u origin <branch-name>
```
The `-u` flag sets the upstream branch, so future pushes can simply use git push.
#### What Happens When You Push?
- Git uploads your local commits to the remote repository.
- The remote repository updates its branch to include your changes.
- If the remote branch has new commits that you don't have locally, Git will reject the push (to avoid overwriting work). You'll need to pull and merge those changes first.
### Common Scenarios and Solutions
#### Rejected Push (Remote Has New Changes):
If the remote branch has changes that you don't have locally, you'll see an error like:
```
! [rejected] main -> main (non-fast-forward)
```
**To fix this:**
- Pull the latest changes:
```bash
git pull origin main
```
- Resolve any merge conflicts.
- Push again:
```bash
git push origin main
```
#### Local Branch Not Tracking Remote Branch:
If you see:
```
fatal: The current branch <branch-name> has no upstream branch.
```
Set the upstream branch:
```bash
git push -u origin <branch-name>
```
#### Force Push After Rewriting History:
If you've rewritten history (e.g., with `git rebase` or `git commit --amend`), you may need to force push:
```bash
git push --force origin <branch-name>
```
Caution: Only force push if you're sure it won't overwrite others' work.
#### Tips:
- Always check `git status` and `git log` before pushing to ensure you're pushing the correct changes.
- Use `git pull` before pushing to avoid conflicts with the remote branch.
- Avoid force pushing (`--force`) unless absolutely necessary, as it can overwrite others' work.

