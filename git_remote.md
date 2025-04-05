## `git remote`
The `git remote` command is used to manage connections to remote repositories. It allows you to view, add, rename, and delete remote repositories, as well as inspect their details. Remote repositories are versions of your project hosted on the internet (e.g., GitHub, GitLab) or another network.
#### Syntax:
```bash
git remote [subcommand] [options] [arguments]
```
### Common Subcommands
#### List Remotes:
- To view all configured remote repositories:
```bash
git remote
```
- For more details (including URLs):
```bash
git remote -v
```
- Example output:
```
origin  https://github.com/user/repo.git (fetch)
origin  https://github.com/user/repo.git (push)
```
#### Add a Remote:
- To add a new remote repository:
```bash
git remote add <name> <url>
```
- Example:
```bash
git remote add origin https://github.com/user/repo.git
```
#### Rename a Remote:
- To rename an existing remote:
```bash
git remote rename <old-name> <new-name>
```
- Example:
```bash
git remote rename origin upstream
```
#### Remove a Remote:
- To delete a remote:
```bash
git remote remove <name>
```
or:
```bash
git remote rm <name>
```
- Example:
```bash
git remote remove origin
```
#### Show Remote Details:
- To inspect a specific remote (URL, fetch/push info):
```bash
git remote show <name>
```
- Example:
```bash
git remote show origin
```
#### Update Remote URL:
- To change the URL of an existing remote:
```bash
git remote set-url <name> <new-url>
```
- Example (switch from HTTPS to SSH):
```bash
git remote set-url origin git@github.com:user/repo.git
```
### Key Use Cases
#### Cloning a Repository:
- When you clone a repo, Git automatically adds a remote named origin:
```bash
git clone https://github.com/user/repo.git
```
#### Working with Multiple Remotes:
- Add a second remote (e.g., for a fork):
```bash
git remote add upstream https://github.com/original/repo.git
```
#### Switching Protocols:
- Update the remote URL from HTTPS to SSH:
```bash
git remote set-url origin git@github.com:user/repo.git
```
### Example Workflow
- List existing remotes:
```bash
git remote -v
```
- Add a new remote (e.g., for a fork):
```bash
git remote add myfork https://github.com/your-username/repo.git
```
- Fetch changes from a remote:
```bash
git fetch upstream
```
- Rename a remote:
```bash
git remote rename myfork fork
```
