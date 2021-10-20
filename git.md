# Git cheatsheet

### add and commit:
    git commit -am 'check in comment' ==> new files and folders are not staged.
  OR
    git add . ==> stage all modified, deleted and new files and folders
    git commit -m "check in comment"

### push commited changes to remote/master:
    git push -u origin master


### pull changes from remote/master:
    git pull origin master


### check status and diff:
    git status -u
    git diff  <file>


### create a new branch:
    git checkout -b develop
  This is shorthand for:
    git branch develop
    git checkout develop

  ==> Work on develop and commit changes to the branch. 

### push changes to branch:
    git push -u origin develop


### switch back to master:
    git checkout master

  ==> Work on master and commit changes to the master.

### merge develop to master and push merge changes:
    git merge develop
    git push -u origin master
    git branch -d develop
    git push origin --delete develop

### resolve merge conflicts:
  ==> when you want the file from the branch you are merging in
    git checkout --theirs path/to/confilicted-file  
  ==> when you want the file from current branch
    git checkout --ours path/to/confilicted-file  

### pull git submodules after cloning
git submodule update --init

### add submodule to a repo
    git submodule add https://github.com/gchinna/pyutils.git pyutils
    git commit -m "add pyutils submodule"

### reset git commit author 
    git config --global --edit
    git commit --amend --reset-author --no-edit
