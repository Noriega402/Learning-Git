# Learning-Git
Initialize a repository locally
<pre>git init</pre>
View the status of modified files
<pre>git status</pre>
To add a file to the stage we use the following command
<pre>git add <name-file></pre>
To add to the stage all the files that have been edited, use the following command
<pre>git add .</pre>
Perform a commit (code capture) with a message about the changes that were made
<pre>git commit -m "Message description"</pre>
If we want to skip the two previous commands ( _git add_, _git commit -m_ ) we can do the following, it is like watching a shorthand
<pre>git commit -am "Message commit"</pre>
It is possible to remove them in several ways, either by deleting the file from the folder, but it may not always be so because maybe that file only added a couple of new lines or that file had to be added in a separate commit, then git makes it easy to remove that file from the staging area with this command:
<pre>git restore --staged <name-file></pre>
Now we will have to create a git repository to be able to add our project
