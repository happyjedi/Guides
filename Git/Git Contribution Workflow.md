# Git Contribution Workflow

1. Fork repositary github.com/user1/project, and you'll get github.com/you/project
2. Clone repo to your local machine:
  
  ```
  git clone git@github.com:/you/project project
  ```
  
3. Create a link to parent repository, for example - upstream
  
  ```
  git remote add upstream git@github.com:/user1/project
  ```
  
4. Create new branch for feature
  
  ```
  git checkout -b feature
  ```
  
5. Working on feature.... If you need to get update from parent repository:
  
  ```
  git checkout master
  git pull upstream master
  git checkout feature
  git merge master ### but better to use - git rebase master
  ```
  
6. When job is done, push it to your repository:
  
  ```
  git push origin feature
  ```
  
7. Then go to your github repository github.com/you/project and press button «Pull request».
8. Choose a branch to merge on the left side of panel and choose a changes from the your repo on the right side.
Important: find a README file in a contribution repository and check in what branch you need to add changes.
9. Fill the fieldes and press button «Send Pull Request».
10. [Here](https://github.com/phonegap/phonegap/wiki/Git-Contributor-Workflow) is more additional information about this.
