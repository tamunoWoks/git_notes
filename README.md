# git_notes
Git is a distributed version control system that allows developers to track changes in their code, collaborate with others, and manage projects efficiently.  
#### How to Use:
- Open your terminal or command-line tool.
- Navigate to the directory you want to initialize as a Git repository.
```bash
cd my_project
```

Below is a list of commonly used Git commands on Windows, along with explanations and examples:
## 1. git init
The git init is a command in the Git version control system used to initialize a new Git repository in the current directory. When you run this command, Git creates a hidden folder named .git in the current directory. This folder contains all the metadata and objects for the Git repository.  
#### Syntax:
```bash
cd my_project
git init
```
After running git init, Git will create a .git folder in the my_project directory. This means my_project is now a Git repository, and you can start using Git to track changes to your files.  
#### Additional Options:
- Initializing a Git repository in the specified directory.
```bash
git init <directory>
``` 
- Creating a bare repository, typically used for remote repositories, which does not have a working directory.
```bash
git init --bare
```
#### Notes:
- If you run git init in a directory that already contains a .git folder, Git will reinitialize the repository without affecting the existing commit history.

## 2. git clone
The git clone command is used to create a copy of a remote Git repository on your local machine. This is one of the most common commands when working with Git, as it allows you to download an entire repository, including its history and all branches.
#### Syntax:
```bash
git clone <repository-url> [destination-directory]
```
- **repository-url:** The URL of the remote repository you want to clone.
- **destination-directory:** (Optional) The name of the directory where the repository will be cloned. If not provided, Git will use the repository's name as the directory name.
####  Clone a repository:
To clone a repository, simply provide the repository's URL:
```bash
git clone https://github.com/user/repo.git
```
This will create a directory named repo (the name of the repository) in your current working directory and download all the files and commit history into it.  
#### Clone into a Specific Directory:
If you want to clone the repository into a specific directory, provide the directory name as the second argument:
```bash
git clone https://github.com/user/repo.git my-project
```
This will clone the repository into a directory named my-project.
#### Clone a Specific Branch:
To clone a specific branch of a repository, use the -b flag followed by the branch name:
```bash
git clone -b branch-name https://github.com/user/repo.git
```
#### Clone with SSH:
If you have SSH access to the repository, you can use the SSH URL instead of HTTPS:
```bash
git clone git@github.com:user/repo.git
```
#### Shallow Clone (Limited History):
If you only need the latest version of the repository and not the entire commit history, you can perform a shallow clone using the --depth flag:
```bash
git clone --depth 1 https://github.com/user/repo.git
```
This will clone only the most recent commit, saving time and disk space.
#### What Happens When You Clone?
When you run git clone, Git performs the following steps:
- Downloads the entire repository (files, branches, and commit history) from the remote server.
- Creates a .git directory in the local repository to store metadata and version control information.
- Checks out the default branch (usually main or master) into your working directory.
#### Common Use Cases
- Downloading a project from GitHub, GitLab, Bitbucket, or any other Git hosting service.
- Starting work on an existing project.
- Creating a local copy of a repository for development or testing.

## 3. git add
The git add command is used to stage changes in your working directory for the next commit. It tells Git which files or changes you want to include in the next snapshot (commit). This is a crucial step in the Git workflow, as it allows you to selectively choose what gets committed.
#### Syntax:
```bash
git add<file-or-directory>
```
- **file-or-directory:** The file or directory you want to stage. You can specify individual files, directories, or use wildcards.
#### Stage a Specific File:
To stage a single file for the next commit:
```bash
git add filename.txt
```
#### Stage All Changes in a Directory:
To stage all changes in a specific directory:
```bash
git add dirname/
```
#### Stage All Changes in the Working Directory:
To stage all changes (new, modified, and deleted files) in the entire working directory:
```bash
git add .
```
#### Stage All Changes (Including Untracked Files):
To stage all changes, including untracked files (new files that Git hasn't been tracking yet):
```bash
git add -A
```
or
```bash
git add --all
```
#### Stage Only Modified or Deleted Files (Exclude Untracked Files):
To stage only modified or deleted files, but not untracked files:
```bash
git add -u
```
#### Stage Specific File Types:
To stage all files of a specific type (e.g., all .txt files):
```bash
git add *.txt
```
#### What Happens When You Run git add?
- Git takes a snapshot of the changes you've staged and prepares them for the next commit.
- The changes are added to the staging area (also called the index), which is a temporary area where Git stores changes before they are committed.

## 4. git commit
The git commit command is used to save the changes you've staged using `git add` to your local repository. Each commit creates a snapshot of your project at that point in time, along with a message describing the changes. This is a key part of the Git workflow, as it allows you to track the history of your project.
#### Syntax:
```bash
git commit -m "Your commit message"
```
- **-m "Your commit message":** Adds a commit message directly in the command. If you omit the -m flag, Git will open your default text editor for you to write a commit message.
#### Commit Staged Changes:
After staging changes with git add, you can commit them with:
```bash
git commit -m "Add new feature"
```
#### Commit All Tracked Changes (Skip git add):
If you want to commit all tracked files (modified or deleted) without explicitly running git add, use the -a flag:
```bash
git commit -a -m "Update existing files"
```
- **Note:** This does not include untracked files (new files)
#### Amend the Previous Commit:
If you want to modify the most recent commit (e.g., to add forgotten changes or fix the commit message), use:
```bash
git commit --amend
```
This opens your default text editor to update the commit message. To add changes to the previous commit:
```bash
git add forgotten-file.txt
git commit --amend
```
#### Commit with a Multi-line Message:
If you want to write a detailed commit message, omit the -m flag:
```bash
git commit
```
This will open your default text editor (e.g., Vim, Nano, or VS Code) for you to write a multi-line message.
#### What Happens When You Commit?
- Git takes the changes you've staged (with git add) and creates a new commit.
- The commit is saved to your local repository with a unique SHA-1 hash (e.g., d3b07384d113edec49eaa6238ad5ff00).
- The commit includes:
  - A snapshot of the changes.
  - Your commit message.
  - Your name and email (from your Git configuration).
  - A timestamp.
#### Writing Good Commit Messages:
A good commit message clearly describes the changes made. Here’s a common format:
```bash
<type>: <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```
**Example:**
```
feat: Add user authentication

- Add login and registration functionality
- Implement password hashing

Fixes #123
```
- **Type:** Describes the kind of change (e.g., feat, fix, docs, style, refactor, test, chore).
- **Subject:** A concise summary of the changes (50 characters or less).
- **Body:** A detailed description of the changes (optional but recommended for larger commits).
- **Footer:** Reference issues or pull requests (e.g., Fixes #123).
#### Tips:
- Keep commits small and focused. Each commit should represent a single logical change.
- Use meaningful commit messages that explain why the change was made, not just what was changed.
- If you forget to include a file in your commit, use git commit --amend to fix it.

## 5. git status
The git status command is one of the most frequently used Git commands. It provides a summary of the current state of your working directory and staging area. This includes information about which files are staged, unstaged, untracked, or have conflicts. It’s a great way to see what changes Git is tracking and what actions you might need to take next.
#### Syntax:
```bash
git status
```
#### What Does git status Show?
When you run git status, Git provides the following information:
- **Current Branch:** Tells you which branch you're currently on.
- **Changes to be Committed (Staged Changes):** Lists files that have been staged (added to the index) using git add and are ready to be committed.
- **Changes not staged for Commit (Unstaged Changes):** Lists files that have been modified but not yet staged for commit.
- **Untracked Files:** Lists files that are in your working directory but not yet tracked by Git.
- **Branch Status:** If your branch is ahead or behind the remote branch, Git will notify you.
- **Merge or Rebase Status:** If you're in the middle of a merge or rebase, git status will show the current state and any conflicts that need to be resolved.
#### Example Output:
Here’s an example of what git status might display:
```bash
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   script.js

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        styles.css
```
### Common Scenarios and What to Do
#### Staged Changes:
If you see files under "Changes to be committed," you can proceed to commit them:
```bash
git commit -m "Your commit message"
```
#### Unstaged Changes:
If you see files under "Changes not staged for commit," you need to stage them first:
```bash
git add <file>
```
#### Untracked Files:
If you see files under "Untracked files," you can start tracking them by staging them:
```bash
git add <file>
```
#### Branch Status:
If your branch is ahead of the remote, you can push your changes:
```bash
git push origin <branch-name>
```
If your branch is behind, you can pull the latest changes:
```bash
git pull origin <branch-name>
```
#### Merge Conflicts:
If you’re in the middle of a merge and have conflicts, git status will list the conflicting files. Resolve the conflicts, stage the files, and complete the merge:
```bash
git add <resolved-file>
git commit
```
#### Short Status:
For a more concise summary, you can use the -s or --short flag:
```bash
git status -s
```
Example output:
```
 M README.md
A  script.js
M  index.html
?? styles.css
```
- **M:** Modified file (staged or unstaged).
- **A:** Added file (staged).
- **??:** Untracked file.
#### Tips
- Run git status frequently to stay aware of the state of your working directory.
- Use git status before committing to ensure you’re including all the changes you intend to.
- If you’re unsure what to do next, git status often provides helpful hints in its output.

## git push
The git push command is used to upload your local repository's commits to a remote repository. This is how you share your changes with others or back them up on a remote server (e.g., GitHub, GitLab, Bitbucket). After committing your changes locally, you use `git push` to synchronize your work with the remote repository.
