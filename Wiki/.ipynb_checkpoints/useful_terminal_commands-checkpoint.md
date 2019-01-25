# Useful Terminal Commands

**General commands** (assuming you are using Mac terminal or Git Bash)

`cd <foldername>` To navigate into a new folder (assuming the folder exists in the directory).

`cd ..` To navigate out of the current directory

`ls` To list the content of the folder


<br/>


**Useful shortcuts**

Use `Tab key` to autocomplete directory and file names

Use `arrow-up` to access the last command

In Macs use `cmd + v` to paste text into the terminal

In Windows machines use `shift + insert` to paste text into Git bash


<br/>


**Set configuration file**

You can run the commands below anywhere, you don't need to be inside any specific directory or repository. These commands will change information in Git's configuration file, so that you don't have to re-type your username and email everytime you make a commit.

`git config --global user.name "andres-patrignani"` In this case my username is: andres-patrignani. The dash in the middle is part of the username.

`git config --global user.email andrespatrignani@ksu.edu` In this case see that I did not include the email between quotation marks as I did with the username.


<br/>


**Common Git commands**

`git clone <repository link>`: Clone repository into your local computer or a remote server. If you work on a server, cloning a repository from a cloud-based platform like Github us much easier than transferring files using the terminal or copy pasting files using a graphical user interface like FileZilla.

`git status`: This command provides the state of the current repository in the local computer (or server) relative to Github's remote repository.

`git add .`: Adds and removes **all** new file additions/deletions from repository. Remember, when you add or remove a new file to a folder in your local computer, it does not get automatically added to your repository. You have to execute the command for this to happen.

`git add <filename>` In case you want to add a single file to your repository. `<filename>` could be `mytextfile.txt`

`git commit -a -m "<write here a short descriptive message>"`: Send changes to remote repository. **Messages are mandatory** and should be short and descriptive. Don't accumulate too many changes before committing, otherwise your message/comment will not be meaningful to all the changes you made.

`git push origin master` Upload changes to master branch in the Github repository. To see changes make sure you refresh the Github webpage.

`git pull origin master`: Downloads updates in the master branch.

`git checkout -- .`: Disregard changes.

`git checkout <branch name>`: Changes scope to any branch, including the master branch. This command assumes that you have a branch.





