#  Git Essentials – README

This is a beginner-friendly Git command guide. It covers only the **essential concepts and commands** in a clean and practical format.

---

##  1. Initialization

Create a new Git repository:

```bash
git init

```
## 2. Configuration

Set global username:

```bash
git config --global user.name "YourName"
```

Set global email:
```bash
git config --global user.email "youremail@example.com"
```

## 3. File Operations

Create a new file:

```bash
touch <filename>
```
Remove a file:

```bash
rm <filename>
```

Restore a deleted file:
```bash
git restore <filename>
```

## 4. Staging and Commit

Check the status of the repo:

```bash
git status
```

Add a file to staging:
```bash
git add <filename>

```

Unstage a file:
```bash
git rm --cached <filename>
```
Commit with message:

```bash
git commit -m "your commit message"
```

## 5. Branching

Create and switch to a new branch:

```bash
git checkout -b <branch_name>
```
Switch to another branch:
```bash
git checkout <branch_name>

```

List all branches:
```bash
git branch

```

## 6. Merging

Merge a branch into the current branch:
```bash
git merge <branch_name>

```

## 7. Logs

View full commit history:
```bash
git log

```
View one-line summary of commits:
```bash
git log --oneline
```

##  8. Remote Repositories
Check existing remotes:
```bash
git remote -v
```

Add a remote repository:
```bash
git remote add origin <repo-url>
```

Push to remote (using PAT if required):
```bash
git push origin master
```

Pull from remote:
```bash
git pull origin master
```

## 9. SSH Setup (Optional)

Generate a new SSH key:
```bash
ssh-keygen
```
Show public key:
```bash
cat ~/.ssh/id_rsa.pub
```
    Paste this public key in GitHub:
    GitHub → Settings → SSH and GPG Keys → New SSH Key

Clone a repository using SSH:
```bash
git clone git@github.com:username/repo-name.git
```

## 10. Useful Commands

Show differences in code:
```bash
git diff
```

List all files (including hidden):
```bash
ls -a
```

Clear terminal screen:
```bash
clear
```
Show previous commands:

```bash
history
```

## Author

Omkar Goswami          
Feel free to use, modify, or contribute to this guide.
