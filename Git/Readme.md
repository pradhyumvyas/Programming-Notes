# GIT

### GIT is a Version Control System:
- it Track files for changes

1. Repo Mechanism
   - *git status*
      - Give the tracking status of current directory


   - *git Init*
      - Run one time per project
      - It crate a hidden folder with **.git** name to keep track of all files and sub folders

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