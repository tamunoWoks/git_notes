## `git log`
The git log command is used to display the commit history of a repository. It shows a detailed list of commits, including the commit hash, author, date, and commit message. This is incredibly useful for understanding the history of a project, tracking changes, and debugging issues.
#### Syntax:
```bash
git log [options]
```
- **`[options]`:** Additional flags to customize the output.
### Common Usage Examples
#### View the Commit History:
- To display the full commit history:
```bash
git log
```
- Example output:
```
commit d3b07384d113edec49eaa6238ad5ff00
Author: John Doe <john.doe@example.com>
Date:   Mon Oct 2 12:00:00 2023 -0400

    Add login feature

commit a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6
Author: Jane Smith <jane.smith@example.com>
Date:   Sun Oct 1 10:00:00 2023 -0400

    Update README.md
```
#### Limit the Number of Commits:
- To show only the last n commits:
```bash
git log -n <number>
```
- Example (show the last 3 commits):
```bash
git log -n 3
```
#### Show a Summary of Changes:
- To display a condensed summary of each commit:
```bash
git log --oneline
```
- Example output:
```
d3b0738 Add login feature
a1b2c3d Update README.md
```
#### Filter by Author:
- To show commits by a specific author:
```bash
git log --author="John Doe"
```
