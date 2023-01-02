# Learning-Git
Initialize a repository locally
```bash
  git init
```
View the status of modified files
```bash
  git status
```
To add a file to the stage we use the following command
```bash
  git add <name-file>
```
To add to the stage all the files that have been edited, use the following command
```bash
  git add .
```
Perform a commit (code capture) with a message about the changes that were made
```bash
  git commit -m "Message commit"
```
If we want to skip the two previous commands ( _git add_, _git commit -m_ ) we can do the following, it is like watching a shorthand
```bash
  git commit -am "Message commit"
```
It is possible to remove them in several ways, either by deleting the file from the folder, but it may not always be so because maybe that file only added a couple of new lines or that file had to be added in a separate commit, then git makes it easy to remove that file from the staging area with this command:
```bash
  git restore --staged <name-file>
```
Now we will have to create a git repository to be able to add our project
<br>
1.  Click on the "new repository" option
<div align="center">
  <img src="https://github.com/Noriega402/Learning-Git/blob/main/img/init/add-1.PNG">
</div>
2.  A name is required for the repository, so we insert one, GitHub is responsible for seeing if that name we have already used before, if not if it validates the repository name field

__NOTE:__ The repository view option must be public, otherwise no one will be able to see our project
<div align="center">
  <img src="https://github.com/Noriega402/Learning-Git/blob/main/img/init/add-2.png">
 </div>
3.   Click create repository
<div align="center">
  <img src="https://github.com/Noriega402/Learning-Git/blob/main/img/init/add-3.jpg">
 </div>
A space like this will appear:
<img src="https://github.com/Noriega402/Learning-Git/blob/main/img/remote/1.jpg">
