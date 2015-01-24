# here is the README
git add README.md
git commit -m "Angelo"

git pull latest dev branch
git branch "NEW_FEATURE BRANCH"

do some work, commit along the way
git add "file name"
git commit -m "message"
git push -u origin "new_FEATURE_BRANCH"


before merge (do the manual steps from another machine to make sure that it works...)

<!-- pull the pull request to local machine -->
git checkout -b add_boilerplate origin/add_boilerplate
  <!-- test locally, make sure everything is still working... run test suite -->
  <!-- then confirm merge online.  -->
confirm merge
delete branch

<!-- do another pull request from dev into master -->
once merged, update Heroku

<!-- starting up -->
git checkout master
git pull
git checkout working
git pull
  <!-- always branch off of working -->

git checkout branch my_story1
  <!-- do work -->
  git add filename
  git add filename
  ...
  git commit -m "message"

<!-- once you are satisfied its working on your local branch, push it up to GitHub with -u -->
git push -u origin my_story1 

<!-- go on github and click on pull request (make sure you select working NOT master) -->

