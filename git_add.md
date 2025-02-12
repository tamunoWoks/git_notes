## git add
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
