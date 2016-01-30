# Git common commands

1. For creating a new feature branch:
  
  ```
  git checkout -b feature
  ..... working changes .....
  git checkout master
  git pull
  git checkout feature 
  git rebase master
  git checkout master 
  git merge feature  -s recursive -Xtheirs  
  or git mergetool --tool=diffuse   ##from http://diffuse.sourceforge.net
  git push origin master
  ```
  
2. If you need to reset last commit
  
  ```
  git log ## check a commit VESRION before the last commit
  git reset --hard VERSION
  git push -u origin master -f
  ```
  
3. If you need to add changes to the last commit without editing commit message.
	
  ```
  git add .
  git commit --amend --no-edit
  git push origin master -f  
  ```

4. Stash changes:
  
  ```
  git stash
  .... some changes....  
  git stash list ### list of stash with numbers
  git stash apply stash{number}
  ```
  
5. Init a new git repo with user credentials if you need to work with your repo from not your local machine with another user. It will ask pass for repo.

  ```
  git init 
  git config user.name "username"
  git config user.email "example@gmail.com"
  echo "# Project name" >> README.md
  git add .
  git commit -m "First commit"
  git remote set-url origin https://username@github.com/repo_owner/repo_name
  git push origin master
  ```
  
