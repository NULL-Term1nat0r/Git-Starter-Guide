## Git Staging Guide

Welcome to the Git Staging Guide! This document provides you with the essential information you need to get started with staging files for a potential commit to your Repository

## What is Staging in relation to Git ?

To make Git monitor the alterations you've made to a specific file, you need to include it in the staging area. Git acknowledges file modifications but refrains from actively tracking them unless they are staged. The staging area serves as a protective layer, enabling you to inspect changes before finalizing them.

Being in the staging area is a necessary step for files to eventually become part of a commit, which means they will be integrated into the master branch.

## How to add files to the staging area ?

In order to add files to your staging area you need to run the following command:
```bash
git add <filename>
```
this will add a particular file to your staging area. If you want to add all files to the staging area you can use the following command:
```bash
git add . 
```
This command will add all new created files since your last commit to the staging area (including those in the subdirectories!). Now there is another command to check which files you added to the staging area in case you want change your decision:
```bash
git status
```
There you are going to see which files are currently added to the staging area. Here you have two lists of files. Those you already added to the staging area to commit which you find below "Changes to be commited:" and those files you created since your last commit but haven`t been added yet to the staging are. You will them below "Untracked files:" Let's assume you want to delete a file  or all files which you added to the staging area. For this purpose you can use the following command for selecting them:
```bash
git restore --cached <filename>
```
In case you want to delete only specific files from a folder in the staging area you can use the following command:
```bash
git reset "subdir/*"
```
In case you want to delete all files from the staging area you can use the dot at the end (basically the same logic with git add . if you remember)
```bash
git restore --cached .
```
You can check again with command "git status" if those changes applied to your staging area. 

##Checkout the following video to see how I stage my Tutorial files for committing:

Step 1: check out the stagin area via the "git status" command.

Step 2: adding the folder "Git-Tutorial" to the staging area by using the "git add" command

Step 3: using git status again to check if the change is applied to the staging area

Step 4: deleting the folder "Git-Tutorial" from the commit list via "git restore --staged Git_Tutorial/"

Step 5: using git status again to check if the change is applied to the staging area

Step 6: using the "git add ." command to add all files including those from the subdirectories to the staging area

Step 7: using "git status" again to check for change

Step 8: using "git restore --staged ." to delete all files from the staging area

Step 9: using "git add ." to add all files again to the staging are so they are ready for commit

