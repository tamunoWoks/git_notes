## `git remote`
The `git remote` command is used to manage connections to remote repositories. It allows you to view, add, rename, and delete remote repositories, as well as inspect their details. Remote repositories are versions of your project hosted on the internet (e.g., GitHub, GitLab) or another network.
#### Syntax:
```bash
git remote [subcommand] [options] [arguments]
```
### Common Subcommands
#### List Remotes:
To view all configured remote repositories:
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
To add a new remote repository:
```bash
git remote add <name> <url>
```
- Example:
```bash
git remote add origin https://github.com/user/repo.git
```
