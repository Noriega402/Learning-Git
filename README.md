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
- The first box is to connect by https or SSH to our repository, for the moment it will only be by https.
- The second table gives us some of the commands already mentioned above and some new ones that we will mention later.
- The last table is similar to the second with the difference that if the repository already existed there is no need to do more extra steps.

The following command is to create a README file to our project (if necessary) otherwise we can skip this step:
```bash
  echo "# test-repository" >> README.md
```
To create the main branch in our project you need mandatory use of the following command because the __" -M "__ option is to force it to move to the main branch
```bash
  git branch -M main
```
Now we add the path in which our staging area will connect to our remote repository through this command
<pre>FOR EXAMPLE: git remote add origin https://github.com/Noriega402/test-repository.git</pre>
```bash
  git remote add origin [url]
```
Finally we make all changes or new files are uploaded to our repository on GitHub:
```bash
  git push -u origin main
```
Once these steps have been done we can go to our repository on GitHub and refresh the page.

## Other commands
#### git diff
##### diff
It is used to be able to see in console the changes made, either we delete or add new lines of code
```bash
  git diff
```
##### diff <route/file>
We can use it to see the changes made in a single file
```bash
  git diff <route/name-file>
```
##### diff hash-old hash-new
We can use it to see the changes made between one commit and another
```bash
  git diff <hash-commit-old> <hash-commit-new>
```
#### git rm
You have several options which are as follows:
##### -r
- Gives permission to delete recursively within a folder
```bash
  git rm -r
```
##### --cached
- To remove changes added to the stagin area.
```bash
  git rm --cached <name-file>
```
##### -rf
- To forcibly delete a folder
```bash
  git rm -rf <name-folder>
```

#### git log
##### --log
We have many changes or commit in our repository, as the project gets bigger, my project will have more commits, the good thing about this is that each commit has a message to know what changes were made, but how to see the name of those messages and see the hash of each one, we have several ways:
- To view changes in an extended way. By default it displays the following fields
  - Secure Hash Algorithm (SHA).
  - Author.
  - Date.
  - Commit message.
```bash
  git log
```
##### --oneline
- A simple and easy way to read
  -  Displays one commit per line.
  -  the first 7 characters of the hash (SHA).
  -  The commit message.
```bash
  git log --oneline
```
##### --stat
- This option causes the following results:
  - Displays the files that were modified in each commit.
  - View the number of lines added or removed in files.
  - A summary line with the total number of files and lines modified.
```bash
  git log --stat
```
#### --patch
- There is a shorter version instead of writing --patch, you can with -p and this displays the following on the screen:
  - The files you've modified.
  - The location of the lines you've added or removed.
  - Los cambios específicos que ha realizado.
- Extensive version
```bash
  git log --patch
```
- Short version
```bash
  git log -p
```
