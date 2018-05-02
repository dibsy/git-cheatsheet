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
### Cloning
```

git clone https://github.com/dibsy/git-cheatsheet.git ( Clone a remote repository. Add origin remote pointing to clone URL)
git clone https://github.com/dibsy/git-cheatsheet.git my-repo ( Will be stored in my-repo directory )

```
### Branching
```

git branch new_branch ( Create a new branch )
git checkout new_branch ( Switching to the branch_name )
git checkout master ( Move back to master branch )
git merge new_branch ( Merge the contents of new_branch in master )
git branch -d new_branch ( Delete the branch )
git checkout -b admin ( Fast forward technique. Creates and checksout branch)

```
