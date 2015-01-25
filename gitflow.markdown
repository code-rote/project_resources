# Initial Project Setup
  Step 1. Create repo on [Github](https://github.com)

  Step 2. Copy SSH Url on right-side of Github repo page
   * copy <ssh url>

  Step 3. Go to directory that will hold the repo folder
   ```
    cd /path/to/folder/that/will/hold/repo
   ```

  Step 4. Clone repo to local machine. __Make sure you are in the right directory before cloning.__ It will create a new folder in there to hold the repo.
   ```
    git clone <ssh url>
   ```
  
  Step 5. Go into the cloned directory
  ```
    cd <cloned directory name>
  ```
  
  Step 6. Make the dev branch on your local machine
  ```
    git branch dev
  ```

  Step 5. Switch to the dev branch on your local machine by checking out the dev branch
  ```
   git  checkout dev
  ```

  Step 6. Push the dev branch upstream to GitHub from your local machine. This copies the branch and all its contents that are under version control to the remote branch.
  ```
    git push -u origin dev
  ```
  > __NOTE__: Now you have `master` and `dev` on GitHub



# Working with Existing Repo
  Assumes that the github repo has been successfully created and cloned to your local machine.

## 1. Always make sure your local repo is up-to-date with remote before starting any new work or creating a local branch
  Step 1. Go to the working directory
  Step 2. Check what branches you have by typing:
  ```
    git branch -l
  ```

  Step 3. Make sure you are on the `dev` branch
  ```
    git checkout dev
  ```

  Step 4. Update the dev branch from remote repo
  ```
    git pull
  ```

## 2. Create a New Branch
  Step 1. Create a new local branch. Name it according to the little story/feature you are going to implement.
  ```
    git branch new_branch_name_meaningful_to_task_at_hand
  ```

  Step 2. Switch over to the newly created branch on your local machine
  ```
    git checkout new_branch_name_meaningful_to_task_at_hand
  ```
  
  Step 3. Do some work... Usually on files/folders that already exist. 
  > __DO NOT FORGET TO COMMIT EARLY AND OFTEN__.

most of the time you do not have to add any additional files, you are simply modifying or changing an existing file. Therefore you can simply commit.

FLESH

NOTES ON VIM

if you forget to add the message and press return after `git commit -m` then you will enter your default bash editor (usually VIM). To return to the regular terminal you will press `:q` and `enter`.

#### Adding Files and/or Folders to Version Control.
> Do: add files and/or folder one at a time. Do not use `git add . -A`

  Step 1. See what `untracked files` exist in your local branch
  ```
    git status
  ```

  Step 2. Add files and/or folders one at a time.
  ```
    git add file_1
    git add file_2
    git add /folder1
    git add /folder2
  ```

  Step 3. See what is staged for this commit.
  ```
    git status
  ```

  Step 4. IF AND ONLY IF, you're confident the files and folders are ready to be committed to version control issue the following command:
  ```
    git commit -am "Add meaningful message about the files/folders added or changed."
  ```

  >__Note:__ Make sure that you provide a meaningful commit message. If your commits are small enough (and they should be **SMALL** then a sentence or two should suffice.)

  Step 5. Repeat steps 1-4 of 'Adding Files to Version Control' as you work on the project. Once you have completed the tasks required to fulfill the branch `new_branch_name_meaningful_to_task_at_hand` then you are ready to move on to the next step.



## 3. Push Local branch to Github using `git push -upstream origin <branch_name`>
> Don't: do this step until you are ready to push all changes to GitHub, submit a pull request to merge your work into the Dev branch and delete the local/remote branch that you've been working on.

  Step 1. Push local branch up to Github
  ```
    git push -u origin new_branch_name_meaningful_to_task_at_hand
  ```

  Step 2. Visit Github repo and click Pull Request (a little green button that looks like a recycling logo)

  Step 3. On the next screen, Choose `dev` branch as the `base:` and the `new_branch_name_meaningful_to_task_at_hand` as the `compare:`

  Step 4. Click the `Create pull request` button and write a meaningful comment if your original comment is slacking. It is important to be descriptive so that in case of emergency we can know which commit to revert back to.

  Step 5. Contact the Github lead to have them look at the pull request, pull down your branch and merge it to their local machine in order to test that everything is working merging the request into the `dev` code base. 

  Step 6. Github lead will merge the request, in the process they will also `delete` the remote branch. 

  Step 7. Once the merge has been completed we must cleanup our local machine and rebase the dev branch __before__ starting to work on anything else.



## 4. Cleanup local machine and rebase the dev branch
  Step 1. Check what branches you have by typing:
  ```
    git branch -l
  ```
  __NOTE:__ You should see the branch `new_branch_name_meaningful_to_task_at_hand`

  Step 2: Delete the `new_branch_name_meaningful_to_task_at_hand` from your local git repo to help stay in-sync with Github
  ```
    git branch -d new_branch_name_meaningful_to_task_at_hand
  ```

  Step 3. Verify that your branches are in sync with Github's
  ```
    git branch -l
  ```


## 5. Make sure your `dev` repo is up-to-date with remote
  Step 1. Switch to dev branch
  ```
    git checkout dev
  ```

  Step 2. Update the dev branch from remote repo
  ```
    git pull
  ```
  > __NOTE:__this will now include your merged changes from the successful pull request made in step 3.

  Step 3. Create a new branch locally to start working on another task. That means go back to step `2. Create a New Branch`






<hr>

# Notes from class... will need to cleanup or delete

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

