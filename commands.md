# Git, GitHub and Gitflow Commands





## *Git:*



- ### config

  set username and email

  `git config --global user.name "your name"`

  `git config --global user.email youremail@gmail.com`




------

- ### log and status

  log with first 7 digits of commits hash

  `git log --oneline`

  status of repository

  `git status`




------

- ### initialize of repo

  `git init`




------

- ### adding and commiting

  adding changes from working directory to staging state

  `git add namefile.txt`

  commit of staging state to local repo

  ***atomic commit: each commit is should be about just one topic***

  `git commit -m "message of commit"`

  




------

- ### amending

  if we commiting some files and after that we notice that we want add some other files or same files with some edit after commit to that commit (amending commit): first add files to staging area and after that

  `git commit --amend`





------

- ### git ignore

  to know git ignore some files and folders use `.gitignore` file and in this file

  > `
  >
  > ```
  > file.txt
  > 
  > .env
  > 
  > node_modules/
  > 
  > *.md
  > ```
  >
  > `

  for more information for `.gitignore` file for each framework [gitignore.io](http://gitignore.io/) can very helpfull

  



------

- ### branching

  ***to make each feature we create specific branch and after complete this feature we merge this to main or other branch***

  

  for create branch            

  `git branch branchName`

  

  

  for deleting branch           ***tip: before delete specific branch we must be in other branch***

  delete branch but this branch must merge it to other branch before delete

  `git branch -d branchName`

  

  delete branch when we dont merge this branch to other

  `git branch -D branchName`

  

  switch to other branch              ***tip: before switch to other branch we must commit our last changes or stash it***

  `git switch branchName`

  `git checkout branchName`

  

  create branch and switch it to this branch

  `git switch -c branchName`

  

  rename branch first switch to that branch and

  `git branch -M newName`







------

- ### merging

  to merging branch B to branch A first go switch to branch A and 

  `git merge branchB` 





------

- ### difference between commits or branches or ....

  difference between last commit and unstaged changes in working directory

  `git diff`



​		difference between two commits or two branches

​		`git diff commit1..commit2`

​		`git diff branch1..branch2`





------

- ### stashing

  if we work on some branch like feature1 and we do some changes that not commited and then we decide to back to some commits back or other switch to other branch we must commit it and then go back or switch to another branch.

  in this situation we can do better than commiting we can stashing changes (put all un commited changes to place name stash)  and go back or switch and do something and then back to first place and pop stash area.

  ***tip: stash is list place that we can put our changes to this place and go back or switch and do something and then back and work with that changes***



​	   put all un commited changes from working directory to stash area

​	   `git stash`

​	   pop from stash area to working directory (this command make stash area empty and all that changes moved to working   directory)

​	   `git stash pop`



​		if we want to get copy of changes from stash area and paste it in working directory we use this command

​		`git stash apply` 

​		



​		if we use command    `git stash` each time that we use it we create new instance of stash and all of them is exist in list of stash

​		for that if we want to pop specific stash item

​		`git stash pop stash@{0}`

​		`git stash pop stash@{2}`



​		for dropping one stash instance 

​		`git stash drop stash@{1}`

​		for drop all stash instances

​		`git stash clear`



​		for show list of all stashes

​		`gti stash list`





------

- ### comeback from commit to some previous commit

  to comeback to specific previous commit

  `git checkout 1234567`

  and after comeback if we want to back to last commit 

  `git switch branchName`



​		if after last commit we do some changes and we notice that changes is not correct and we decided to comeback to last commit status of projects

​		`git restore .`



​		if we want to hard deleted some commits 

​		`git reset --hard 1234567`



​		if we want to delete some commits but we want to be that commits be in history of project

​		`git revert 1234567`









------

# GitHub section

# 











