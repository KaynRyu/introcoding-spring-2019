# Useful git commands

`git clone <repository link>`: Clone repository into your local computer or a remote server. If you work on a server, cloning a repository from a cloud-based platform like Github us much easier than transferring files using the terminal or copy pasting files using a graphical user interface like FileZilla.

`git status`: This command provides the state of the current repository in the local computer (or server) relative to Github's remote repository.

`git add .`: Adds and removes **all** new file additions/deletions from repository. Remember, when you add or remove a new file to a folder in your local computer, it does not get automatically added to your repository. You have to execute the command for this to happen.

`git commit -a -m "<write here a short descriptive message>"`: Send changes to remote repository

`git checkout <branch name>`: Changes scope to any branch, including the master branch.

`git checkout -- .`: Disregard changes.

`git pull`: Updates the entire repository