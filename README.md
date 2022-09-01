# Main header
Content

# Dos Commands
* dir -> list files and directories under the current path
* cd -> change directory to...
* clear -> clear 

# Git Commands
* repo -> repository

* clone -> bring a repo down from the internet (remote repository like Github) to your local machine

* add -> track your files and changes with Git, "." means track all files or just follow up with file name "index.html"

* commit -> save your changes into Git
 
* push -> push your changes to your remote repo on Github (or another website)
 
* pull -> pull changes down from the remote repo to your local machine
 
* status -> check to see which files are being tracked or need to be commited

* init -> use this command inside of your project to turn it into a Git repository and start using Git with that codebase

* git config –global user.name “[name]” ->sets author name
* git config –global user.email “[email address]” ->sets author email id
* git init [repository name] ->start new repository
* git clone [url] ->obtain a repository from an existing URL.
* git add [file] ->adds a file to the staging area.
* git commit -m “[ Type in the commit message]” ->records or snapshots the file permanently in the version history.
* git commit -a ->commits any files you’ve changed since then.&commits any files you’ve added
* git diff ->shows the file differences which are not yet staged.
* git diff –staged ->differences between the files in the staging area and the latest version present.
* git diff [first branch] [second branch] ->differences between the two branches mentioned.
* git reset [file] ->unstages the file, but it preserves the file contents.
* git reset [commit] ->undoes all the commits after the specified commit and preserves the changes locally. git reset HEAD~x, x is number of how many commits further from the last you undo starting from 0, i.e. second last commit will be HEAD~1.
* git reset –hard [commit] ->discards all history and goes back to the specified commit.
* git status ->command lists all the files that have to be committed.
* git rm [file] ->deletes the file from your working directory and stages the deletion.
* git log ->used to list the version history for the current branch.
* git log –follow[file] ->lists version history for a file, including the renaming of files also.
* git show [commit] ->shows the metadata and content changes of the specified commit.
* git tag [commitID] ->used to give tags to the specified commit.
* git branch ->lists all the local branches in the current repository.
* git branch [branch name] -> creates a new branch.
* git branch -d [branch name] -> deletes the feature branch.
* git checkout [branch name] -> used to switch from one branch to another
* git checkout -b [branch name] ->creates a new branch and also switches to it.
* git merge [branch name] ->merges the specified branch’s history into the current branch.
* git remote add [variable name] [Remote Server Link] ->used to connect your local repository to the remote server.
* git push [variable name] master ->sends the committed changes of master branch to your remote repository.
* git push [variable name] [branch] ->sends the branch commits to your remote repository.
* git push –all [variable name] ->pushes all branches to your remote repository.
* git push [variable name] :[branch name] ->deletes a branch on your remote repository.
* git pull [Repository Link] ->fetches and merges changes on the remote server to your working directory.
* git stash save ->stores all the modified tracked files.
* git stash pop ->restores the most recently stashed files.
* git stash list ->lists all stashed changesets.
* git stash drop ->discards the most recently stashed changeset.
* git checkout -b [name of the branch] -> to create a new branch
* git checkout [name of the branch] -> to navigate into the named branch
* git checkout -d [name of the branch] -> to delete the branch
* git merge [branch name] -> to merge the branch to current branch in working directory

# Generate SSH Key
$ ssh-keygen -t rsa -b 4096 -C "marshal.guo0304@outlook.com"
* "-t" type
* "-b" strength
* "-C" email

$ ls | grep firstKey    -> get ssh keys
firstKey                -> private key, stored on local machine
firstKey.pub            -> public key

$ cat firstKey.pub      -> show ssh key
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCz7B1l+cfNYfISBvHUe1yGkgYo77xWlWs4iN9aXoEV4gAbb6ttJxH5alaBzPTXuVsADE3zuohM0BIlZNnJgXKe4tdozHgYCl+PIHOpifT1cJMQV+t9kqWy5wgocDGqvbZhdL6zUcRyXglj9t5jdHQAg9kvSzy551Dz9SrQyIGUw/UHce3xGF8Txtitrsx4hRsTJShkn1WalkLnkIyIyvsFplXjYDsTKx+Dn6GGqIojh6ndlTuB1qEB4EKkPb1qoeq1QDR0ibEE1xFDuX9bihiiBUSULMjCetqKu8/6dRZGNSmc3E9qfa+atrPR9ZGevoqZnjEL2mGsXluX59cPZqpjYFHuYIz8NXlOPdjkkRO0gNwhin4kH09W9SPWd4Efvlxz4gzBjAA/WDQnJPxSqqrlFCU2VdGaat96zAmWXWoWAw3nHLMzwpQILieNhHktDZwFtiPgrGGGUHb3jflphEptaDw5yXZK3R7LKhfs7PU/Y1h9yzD61EmwGugi6k9LQLs6WYKW/+Rs9QVj8XTViSnTd1/1AgPFrObFUQIY/u0hVsiUFuacN//KkHNpU5ZREXw5PvrymF7aGqERwycu8/iGx3IpjL95zJWIcZK1jTlcNmCeZ9uQWzjWT0nWGJG6iV4DIsHwKACcO61zT4zAFUBB9iZHJTO2RAQaMnAF8H8QHw== marshal.guo0304@outlook.com

$ clip < ~/firstKey.pub -> copy public ssh key to keyboard

# Add ssh key to ssh agent (NOT DONE)

$ eval "$(ssh-agent -s)"    -> start ssh agent in the background
Agent pid 1273

# Push
>> git push origin main
 * origin: original repo location (could be remote) 
 * main: HEAD (older github uses master instead of head)

See if refs/heads/?? is master or main
>> git show-ref









