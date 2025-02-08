# git_notes
Git is a distributed version control system that allows developers to track changes in their code, collaborate with others, and manage projects efficiently.  

#### How to Use
- Open your terminal or command-line tool.
- Navigate to the directory you want to initialize as a Git repository.
```bash
cd my_project
```

Below is a list of commonly used Git commands on Windows, along with explanations and examples:
## 1. git init
git init is a command in the Git version control system used to initialize a new Git repository in the current directory. When you run this command, Git creates a hidden folder named .git in the current directory. This folder contains all the metadata and objects for the Git repository.  
Syntax:
```bash
cd my_project
git init
```
After running git init, Git will create a .git folder in the my_project directory. This means my_project is now a Git repository, and you can start using Git to track changes to your files.  

#### Additional Options
- Initializing a Git repository in the specified directory.
```bash
git init <directory>
``` 
- Creating a bare repository, typically used for remote repositories, which does not have a working directory.
```bash
git init --bare
```

#### Notes
- If you run git init in a directory that already contains a .git folder, Git will reinitialize the repository without affecting the existing commit history.
