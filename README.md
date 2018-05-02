### Git Basics
```
git help config
git config --global user.name 'Dibyendu'
git init ( Initialize an empty repository )
git add *.txt
git status ( See your status )
git commit -m "Commit Messages" ( Make a commit to files which are in staging area)
git log ( to see the commit history)
```
### Adding files for staging
```
git add . ( Adds everything )
git add a.txt b.txt ( add files selectively )
git add --all ( Add all files )
git add \*.txt ( Add all *.txt files in current Diretory) 
git add docs/*.txt ( Add all the *.txt files in the docs dirctory
git add "*.txt" Add all *.txt files in the whole project

```
### Staging
```
git diff ( Show unstaged difference since last commit)
git add *.txt
git diff ( No difference after files are staged )
git diff --staged ( View staged difference)
git reset HEAD Somefile ( To remove from a staged area ; HEAD refers to last commit on the timeline)
git checkout -- FileName ( reomove all the changes made to the file since last commit)
git commit -a -m "Change" ( Skip staging and commit direclty. Add changes from all traced files only. Untraced files are not added)
git reset --soft HEAD^ -  (Undoing commit and reset into staging [^ Move one commit before HEAD] )
git add todo.txt
git commit --amend -m "Some message" ( Add to last commit. Overwrite last commit. Whatever has been staged is added to last commit)
git reset --hard HEAD^ ( Undo last commit and all the changes)
git reset --hard HEAD^^ (Undo last 2 commit and all the changes)
```
### Remotes
```
git remote add origin https://github.com/dibsy/git-cheatsheet.git ( Adding a remote )
git remote -v ( List all available remote repository )
git push -u origin master ( Push to origin our master branch )
git pull ( pull changes from remote )
git remote add <name> <address> ( Add remotes) 
git remote rm <name> ( To remove remotes )
git push -u <remote_name> <branch> ( push to remote any branch. Useful in when there are mutliple remotes)
```

### git config --global user.name "Dibsyhex"

### initialize an empty repo
git init

to see the status of the repo
git status

add a file

git add file1.txt

add a file to staging area

git commit -m "My first commit"

git add dir1/

git log

git diff

git diff --stage

git reset HEAD a.txt

Skip staging and add. Add changes from all staged files. Dosent add untraced files
git commit -a -m "commit without staging"

Incase we forgot to add something to the commit and want to ammend to the same comit , add it first

git add

git commit --amend -m "Message" Change the last commit

Undo last commit and put evertything to staging
git reset --soft HEAD^ [ the ^ symbol meand move to one commit before HEAD ]

git reset --hard HEAD^ undo last commit and all changes

to add new remote : git remote add name location
git remote add origin http://xyz.git

to remove remotes
git remote rm "name"

pushing to remote "repo name" , "local branch to push"
git push -u origin master 

clone a repo

git clone git_add

view remotes of current git repo
git remote -v

create new branch
git branch branch_name

checkout to another branch
git checkout branch_name

to merge branches
first move to the master branch
git merge branch_name

delete a branch 
git branch -d branch_name

to creach a brach and checkout in 1 step
git checkout -b branch_name

to fetch or sync our local repository with the remote one
git merge origin/master


Merge conflict

git status
edit the contents
git commit -a

Remote show
git remote show origin 

Removing a remote branch

git push origin :branch_name

List all remote branch
git branch -r

Fetch all remote branches
git fetch

First do git fetch and then git branch -r

To clean up deleted remote branches
state status means deleted 
git remote show origin
git remote prune origin

Tags
git tag -a 2.2 -m "Tag"
git push --tags
git checkout 2.2

Git Rebase 
1. Move all changes to master which are not in origin master or temp area
2. Run all origin/master commit
3. Run all commits in  the temp area one at a time
