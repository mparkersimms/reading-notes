# Notes on Git Tutorial

#### Back to README Home Page
* [README](../README.md)

* reference [Git Tutorial](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/) by Jenni Choi


## Version Control 
* *Version Control system (VCS)*
* a system that allows you to revisit various versions of a file or set of filess by recording changes
* you can revert a file to a previous version
* track modifications and the people that made the modifications
* compare changes

### Local Version Control
* entails one database on your hard disk that stores changes to files

### Centralized Version Control System (CVCS)

* single server, accessed by all clients
* streamlined by eliminating the need for all local databases

### Distributed Version Control System (DVCS)
* addresses major vulnerability of the CVS (the server as a single point of failure) 
  * if a CVS goes down, noone can do any work
    * with the absense of backups, all the work will be lost
* allows clients to create mirrored repositories
  * can be placed on the server to replace any lost information
  * allows various simultaneous workflows

### Using git 
  * to check settings use
    * 'git config -- list' command 
  * getting help 
    * 'git help command' 
  
#### Setting up a repository
  * $ cd test (cd = change directory)
  * $ git init
  * to start tracking these repositories type the following 
    * $ git add *.c
    * $ git add LICENSE
    * $ git commit -m “any message here”

#### cloning 
  * *this is what we did to clone github to vscode* 
  * $ git clone https://github.com/test -- etc.. 

### Workflow

#### Local REpository Structure
  * three components 
    * Working directory
      * where the actual files lives
    * Index
      * used for staging
    * Head 
      * the most recent commit

#### Saving Changes
  * all files are either tracked or untracked
  * tracked 
    * can be modified, unmodified or staged
    * part of the most recent file snapshot
  * Untracked
    * not in the last snapshot and do not live in the staging area

#### The life cycle of a file status
  * once a file is edited, git flags it because of the changes made
  * stage the modified file
  * commit the staged changes

#### check file status
  * use '$ git status' command 

#### Tracking and staging a new file
  * sigle file
    * git add filename
  * all files 
    * $ git add *

#### Committing a File
  * git commit -m "made change x, y, z" 

#### Commiting all changes
  * git commit -a

#### Pushing Changes 
  * git push origin master
    * this command pushes changes form the local "master" branch to the remoter repositry named "origin" 

#### Stashing Changes 
  * when your not ready to commit changes, but dont want to lose them 
    * 'git stash' command temporarily removes changes and hides them giving a clean working directory
    * 'git stash apply' to retrieve hidden changes

### Remote Repositories 

#### cloned repositories
  * git will automatically give the name "origin" to the server from which you cloned and the name "master" to your local branch

#### seeing your remotes 
  * run 'git remote' command you can view the hsort names such as "origin" of all specified remote handles
  * by using 'git remote -v' you can view all the remote URKLs next to their names 

#### Adding Remotes
  * to create  a new remote Git repository with a short name 
    * git remote add shortname url

#### Fetching
  * pulling data from a remote project
  * git fetch [remote name]
  * for cloned repositories use : 'git fetch origin'

#### Pushing 
  * to push changes upstream for sharing 
  * 'git push [remote-name][branch-name]
  * example : git push origin master
  
#### Renaming / Removing Remotes 
  * git remote rename [old-name][new-name]
  * git remote rm [name] 

### Undoing Actions

#### Commit mistakes
  * 'git commit --amend'
