# Git Cheatsheet

# Setup & Config

 - To check git version
   
     git --version

 - To set global author on your system
   
   git config --global user.name "Abhijeet"

 - To set global author email on your system
  
    git config --gobal user.email "kale4455@gmail.com"

 - To see a config details on your system

   git config user.name
  
   git config user.email


# Basic Workflow

# Create a Git Repository
  
   - git init
 output :- Initialized empty Git repository

# Check Status

  - git status
  To see status of your repo.

# Add Files

 - git add <File_name>

   To add untracked files to stagging

 - To unstage 

   git rm --cached <File_name>

# Commit Changes

 - Add file stagging to tracked

   git commit -m "message"

 - To remove from tracked
  
   git rm --cached <file_name>

# TO Restore file

   git restore <file_name>

# Check History
     
    -  git log

      To see commit log

    - to see commit history in  oneline

     git log --oneline


# Branch 

- A branch is an independent line of development.

   . master/main = Original project
   . dev = A copy where you can work safely
- Whatever you do in the dev branch does not affect the master branch until you merge the changes.

- Create a New Branch

  - git branch <New_branch_name>

- Check the branches

  - git branch

- To create a branch & checkout to that branch

   - git checkout -b <New_branch_name>

- To switch/Checkout to branch 

  - git switch <branch_name>
  - git switch  <branch_name>

- To rename branch (master->main)

  - git switch master
  - git branch -m main

- To delete branch 

   - git branch -d <branch_name>


# Remote Repo

- A remote repository is an online copy of your Git repository, stored on a server like GitHub, so you can back up your code, share it with others, and collaborate.

- Simple Example :- 
  > Local repository → On your computer 💻
  > Remote repository → On GitHub ☁️

- Show all remote repositories with their fetch and push URLs

 - git remote -v

- To add remote repository yo your origin 

  - git remote add origin <repository-url>
  - git remote add origin <git@github.com:abhijeetkale4455/my-first-repo.git>
  
  - Remove the remote repository named origin

     - git remote remove origin

- Change the URL of the origin remote

  - git remote set-url origin <new-url>

- Rename a remote repository.

 - git remote rename origin github.

# Push/Pull from local/remote repo

- Push (Local → Remote) 
   - Push means uploading your local commits from your computer to the remote repository (GitHub).

- Pull (Remote → Local)

   - Pull means downloading the latest changes from the remote repository (GitHub) to your local repository.
 
- There are three ways to pull push from local to remote

 1. Using ssh keys

  - generate ssh keys first in ~/.ssh direcory 
   
   ssh-keygen

 - add public key to your github account
 
   setting>>SSH and GPG key >> New SSH key 
    
- check your origin & set your origin to ssh url 
   
   git remote -v 

git  set-url origin <git@github.com:abhijeetkale4455/my-first-repo.git>

- Then you can push or pull from /to remote


     



    



     

