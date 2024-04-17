# Git Learning

### What is Version Control?
* A mini file management system where it can see any incremental changes made to the file
* Able to revert changes, which can be good if you want to revert the file to a previous state

## What is Git, and how does it work?
* Not like previous VCS (delta), but Git saves changes as snapshots
* If there were no changes made, Git would link previous file versions instead of storing the new one
* Git allows to view all changes separately, instead having everything as one big change
* Modify, Stage, Commit

## Git Commands:
* **git init** - This initialises the folder as a repository. This creates a new folder, which allows git to manage and track all the changes that occur

![img.png](Images%2Fimg.png)

* **git status** - Shows the status of the folder/repo (There is no harm in using this command).

![img_1.png](Images%2Fimg_1.png)

* **git add** - After modifying files (Git will know the changes), you have the option to move them over to the "**stage**" process, in which the changes can be tracked <br>

![img_2.png](Images%2Fimg_2.png)

* **git commit** - Saves and uploads the changes to the database

![img_3.png](Images%2Fimg_3.png)

## Gitignore
* We use .gitignore for files or folders you don't want to see when making changes, such as .idea or files that have confidential information
* To create a gitignore file, use the command "**nano .gitignore**" which should display a file editor
* type up the files/folders you don't want to display. After that you should press ctrl X to save, Y for yes and then enter

![img_4.png](Images%2Fimg_4.png)

* Now when using the "git status" command, you will not see those files

![img_5.png](Images%2Fimg_5.png)


## What does git log and git diff do?
* git log shows all the previous commits
* git diff shows the difference between 2 changes (example shown below)

![img_6.png](Images%2Fimg_6.png)

# Distributed Version Control

## Diagram:

![img_7.png](Images%2Fimg_7.png)

## What is GitHub?

* Github is a remote repository that can be used as a Version Control System. 
* It allows for collaboration as it is hosted in the cloud

## Competitors:
* GitLab. 
* Bitbucket.
* Azure DevOps
* Bitrise.
* AWS CloudFormation - AWS own services

## How to link a local repo with a remote repo?
To link the local repo to the remote repo, you first need to create locate the local repo folder and then follow these steps:
1) Make sure your email and name matches the email of your remote repo by using this command :
```bash
git config --global user.email "INSERT EMAIL"
git config --global user.name "INSERT NAME"
```
2) Check if there are any files that are staged. All these files should be commited before linking repos:
```bash
git status
git add .
git commit -m "MOVING STAGED FILES TO COMMIT"
```
3) Once everything has been commited. Copy the Remote repo link and type it into this command:
```bash
git remote add origin "LINK OF YOUR REPO STARTING WITH HTTPS://"
```
4) If there are no errors, next step is to follow these commands in order:
```bash
git branch -M main

git push -u origin main
```
5) If you had no errors, it would tell you to login to your Github, in which once you do that, they will be sucessfully linked

## Remote Repo to local repo:
To do this is fairly similar to the previous step. Here is how to link a remote repo to a local repo:

1) First type up these commands to initialise a folder :
```bash
echo #"FOLDER NAME" >> readme.md
git init
git addreadme.md
git commit -m "first commit"
git branch -M main
git remote add origin "LINK YOUR REPO"
git push - u origin main
```


