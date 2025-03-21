## `git commit`
The `git commit` command is used to save the changes you've staged using `git add` to your local repository. Each commit creates a snapshot of your project at that point in time, along with a message describing the changes. This is a key part of the Git workflow, as it allows you to track the history of your project.
#### Syntax:
```bash
git commit -m "Your commit message"
```
- **`-m "Your commit message"`:** Adds a commit message directly in the command. If you omit the -m flag, Git will open your default text editor for you to write a commit message.
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
- Example:
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
### Example Workflow
- Make changes to your files.
- Stage the changes:
```bash
git add file1.txt file2.txt
```
- Commit the changes:
```bash
git commit -m "Update file1.txt and file2.txt"
```
- Push the changes to the remote repository (if needed):
```bash
git push origin main
```
