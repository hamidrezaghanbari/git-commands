Git, GitHub and Gitflow Commands





## *Git:*

#### 

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

  if we commit some files and after that we notice that we want to add more file or same files with other changes with that commit, we should use amend commit, for that first we add that files and after that

  `git commit --amend`

  

































