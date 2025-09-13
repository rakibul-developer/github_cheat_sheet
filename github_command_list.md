# 🚀 Git & GitHub Commands Cheat Sheet

## 🔧 Git Configuration
```bash
git config --global user.name "your github name"
git config --global user.email "your github email"
git config --list
```
## 📂 Project Setup in GitHub

```bash 
git init
git add [specific file]        # or git add .
git commit -m "write your comments"
git branch -M main
git remote add origin [your github project repository link]
git push -u origin main
```
## 🔄 Restore Files or Code

### After Staged (before commit)
``` bash
git add .
git restore --staged [your file name]
```
### After Commit
```bash
git log
git log --oneline
git revert [your specific hash code]
```
### After Push
```bash
git reset HEAD~1
# or
git reset --soft HEAD~1
# or
git reset --mixed HEAD~1
# or
git reset --hard HEAD~1
```

## ⚡ Git Aliases
Create Global and Local Git Aliases

```bash
Go to your root directory:

ls -a
nano .gitconfig

Write your shortcuts like this:

[alias]
    st = status
    co = checkout
    cm = commit -m

Save with CTRL + S and CTRL + X.

Or directly via command:

git config alias.[shortcut] "any git command"
git config alias.[shortcut] "any git command" --global
```

## 🌿 GitHub Branch Commands
### Branch Create
```bash
git branch [new-branch-name]
git checkout -b [new-branch-name]
git switch -c [new-branch-name]
```
### Branch Switch
```bash
git checkout [branch-name]
git switch [branch-name]
```
### Branch Delete
```bash
git branch -D [branch-name]
```
### Branch Merge
```bash
git merge [branch-name]
git push -u origin [branch-name]
```
### Change Default Branch
```bash
git branch -M [default-branch-name]
```

## 🛠️ Fix Git Commits
Amend Last Commit
```bash
git commit --amend
# Then ESC + :wq + ENTER

Or directly:

git commit --amend -m "new commit message"
```

## 📥 Git Clone
```bash
git clone [repository HTTPS/SSH link]
git clone [repository HTTPS/SSH link] .
git clone --branch [branch-name] [repository HTTPS/SSH link]
```

## 🔄 Git Pull & Fetch
```bash
git pull origin [branch-name]
git fetch origin
git merge origin/[branch-name]
```

## 👀 Show Code Changes
```bash
git diff
# or
git diff --staged               # after add
# or
git diff origin/[branch-name]   # after commit
# or
git diff [hash-Y] [hash-X]
# or
git diff --name-only
# or
git diff --color-words
```

## ⏭️ Skip Staging Area
```bash
git commit -a -m "your commit message"
# or
git commit ./[file-name] -m "your commit message"
```

## 📦 Git Stash
```bash
git stash
git stash list
git stash apply
# or
git stash apply stash@{[stash-number]}
# or
git stash pop
git stash clear
```
