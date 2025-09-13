***All GitHub Config List***
    git config --global user.name "your github name"
    git config --global user.email "your github email"
    git config --list

***Command Of Project Setup In GitHub***
    git init
    git add [specific file] or git add .
    git commit -m "write your comments"
    git branch -M main
    git remote add origin [your github project repository link]
    git push -u origin main
	
***Command Of Files Or Code Restore***
    **AFTER STATE MOOD**
    git add .
    git restore --staged [your file name]
    
    **AFTER COMMITE MOOD**
    git log or git log --oneline
    git revert [your specific hash code]

    **AFTER PUSH MOOD**
    git reset HEAD~1
    or
    git reset --soft HEAD~1
    or
    git reset --mixed HEAD~1
    or
    git reset --hard HEAD~1

***Create Global and Local Git Aliases***
    go to your root directory
    ls -a
    nano .gitconfig
    now write your shortcut like this
        [alias]
            [your shortcut] = any git command
    enter CTRL + S and CTRL + Y
    

    or

    git config alias.[your shortcut] any git command
    or
    git config alias.[your shortcut] any git command --global

***Command Of GitHub Branches***
    **BRANCE CREATE**
    git branch [your new branch name]
    git checkout -b [your new branch name]
    git switch -c [your new branch name]

    **BRANCE SWITCH**
    git checkout [your branch name]
    git switch [your branch name]

    **BRANCE DELETE**
    git branch -D [your branch name]

    **BRANCE MERGE**
    git merge [your branch name]
    git push -u origin [your branch name]

    **DEFAULT BRANCE CHANGE**
    git branch -M [your default branch name]

***Fix Git Commits***
    git commit --amend
    ESC and wq and ENTER
    
    or

    git commit --amend -m "[write your commit]"

***Git Clone Command***
    git clone [repository HTTPS/SSH link]
    or
    git clone [repository HTTPS/SSH link] .
    or
    git clone --branch [specific branch name] [repository HTTPS/SSH link]

***Git Pull and Git Fetch***
    git pull origin [specific branch name]
    git fetch origin
    git merge origin/[specific branch name]

***Show Changes Of Code***
    git diff
    or
    git diff --staged //after add
    or
    git diff origin/[your branch name] //after commit
    or
    git diff [github hash code Y] [github hash code X]
    or
    git diff --name-only
    or
    or git diff --color-words

***Skip Git Staging Area***
    git commit -a -m "[your commit message]"
    or
    git commit ./[specific file name] -m "[your commit message]"

***Git Stash Command***
    git stash
    git stash list
    git stash apply
    or
    git stash apply stash@{[specific commit number of stash mood]}
    or
    git stash pop
    git stash clear




    
