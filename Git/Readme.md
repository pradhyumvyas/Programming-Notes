# GIT

### GIT is a Version Control System:
- it Track files for changes

## Repo Mechanism
   - *git status*
      - Give the tracking status of current directory


   - *git Init*
      - Run one time per project
      - It crate a hidden folder with **.git** name to keep track of all files and sub folders(Go inside this folder its fun to check how git manage this VCS)

   - *Commit*
      - its like check point of directory
      - Write --> Add --> Commit
      - Below are the following commands for Commit
         - git add  (From working Directory to Staging Area)
            - ```git 
                  git add filename
               ```
         - git commit (From Staging Area to local Repository)
            - ```git 
                  git commit -m"commit_message"
               ```
         - git push (From local Repo to to Remote Repository, like Github, BitBucket)
            - ```git 
                  git push
               ```
         - **git log or git log -oneline**
            - Provide you the details of previous commit
      - Make it Atomic Commits
      - Commit tracks the previous commits as well to keep track all the previous commit, every commit had there own unique hash id to categorize unique commit.
      - **.gitignore** file
         - files which should not be tracked or some sensative info which we are not allow to expose over repo so we keep that file inside .gitignore file.
      - For umCommit the changes which are not pushed use below command
           - ```git
             git reset --soft HEAD~1
             ```
   
   - *Branches*
      - Its like an alternaive timeline, always are on some branch
      - Can be used to develop separate featues without touching the production live code or running code 
      - #### Commands
         - To show all available branches ```git branch```
            - **if its "*" as prefix of branch name then its current branch**
         - To create a new branch ```git branch branch_name```
            - It will create a folder inside **.git/refs/heads folder**
         - To point on another branch ```git checkout branch_name``` or ```git switch branch_name```
            - Head is poiniting to current branch can be check inside **.git/refs/HEAD** file
            - Head points to where a branch is currently at...
         - To create a branch and move there ```git checkout -b branch_name``` or ```git switch -c branch_name```
         - To delete the branch ```git branch -d branch_name```

      **Merging the branches**
      - To merge the branch ```git merge branch_name```
      - If conflicts occurs
         - there will be two line top is your current branch code and bottom one in branch which you are mergin into you current branch
         - need to remove manually or conflicts tag and keep the code which you want and save the file

      **Git Diff**
      - git diff compare working with staging it compare the same file with different timeline
      - old commit file its **---** symbol and current file notate from **+++** symbol
      - To check the difference of staged file ``` git diff --staged```    
      - To check the differnct between to commit ```git diff commit_ID commit_ID``` or ```git diff commit_ID..commit_ID``` can be done with branch also ```git diff branch_name..branch_name```

      **Git Stash**
      - Create a repo, work and commit on main branch, Switch to another branch and work
      - Conflicting changes do not allow to switch branch without commits, To solve this stash can be used
      - To stash the changes ```git stash```
      - To bring changes back ```git stash pop```
      - Pop can be done in another branch as well so be cautious
      - There is on more way to back changes using ```git stash apply``` it apply changes & keep then in stash

      **More commands**
      - ```git checkout <Hash>``` (Detach Head): new branch
      - ```git switch main``` Re-attach Head
      - ```git checkout HEAD~2``` Look at 2 commit prior
      - ```git restore filename``` get back to last commit version
      

      **Git Rebase**
      - DON't use in main branch never
      - It should be use with side branch
      - The unnecessary commit message like merge commit will totally gone
      - ```git rebase master```
      - If found any conflicts while running rebase command, just resolve the conflicts and add in staging area after run
      - ```git rebase --continue```
      - NEVER REBASE COMMITS THAT YOU HAVE SHARED PUSHED TO GITHUB --> NEVER REBASE



         
