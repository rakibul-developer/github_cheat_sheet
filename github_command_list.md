# 🚀 Git & GitHub Commands Cheat Sheet

## 🔧 Git Configuration
```bash
git config --global user.name "your github name"
git config --global user.email "your github email"
git config --list

📂 Project Setup in GitHub

git init
git add [specific file]        # or git add .
git commit -m "write your comments"
git branch -M main
git remote add origin [your github project repository link]
git push -u origin main

🔄 Restore Files or Code
After Staged (before commit)

git add .
git restore --staged [your file name]

After Commit

git log
git log --oneline
git revert [your specific hash code]

After Push

git reset HEAD~1
# or
git reset --soft HEAD~1
# or
git reset --mixed HEAD~1
# or
git reset --hard HEAD~1

⚡ Git Aliases
Create Global and Local Git Aliases

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

🌿 GitHub Branch Commands
Branch Create

git branch [new-branch-name]
git checkout -b [new-branch-name]
git switch -c [new-branch-name]

Branch Switch

git checkout [branch-name]
git switch [branch-name]

Branch Delete

git branch -D [branch-name]

Branch Merge

git merge [branch-name]
git push -u origin [branch-name]

Change Default Branch

git branch -M [default-branch-name]

🛠️ Fix Git Commits
Amend Last Commit

git commit --amend
# Then ESC + :wq + ENTER

Or directly:

git commit --amend -m "new commit message"

📥 Git Clone

git clone [repository HTTPS/SSH link]
git clone [repository HTTPS/SSH link] .
git clone --branch [branch-name] [repository HTTPS/SSH link]

🔄 Git Pull & Fetch

git pull origin [branch-name]
git fetch origin
git merge origin/[branch-name]

👀 Show Code Changes

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

⏭️ Skip Staging Area

git commit -a -m "your commit message"
# or
git commit ./[file-name] -m "your commit message"

📦 Git Stash

git stash
git stash list
git stash apply
# or
git stash apply stash@{[stash-number]}
# or
git stash pop
git stash clear
