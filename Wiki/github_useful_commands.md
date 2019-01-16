# GitHub

Git is a version control system that tracks changes. Github is a web platform built around Git and has disrupted the software industry. In addition to Github there are other similar platforms such as Bitbucket and GitLab, each of them with a different business model.

## Installing and using Git in Windows machines

* Download Git from <https://git-scm.com/>

## Steps to get started

1. Go to github.com and create an account
2. Create a repository. Make sure to add a **README** file.
3. Go to your computer and open the terminal
4. Navigate to a directory where you want to place the repository
5. Clone the Github repository using: git clone #link#

## Useful git commands

`git clone <repository link>`: Clone repository into your local computer or a remote server. If you work on a server, cloning a repository from a cloud-based platform like Github us much easier than transferring files using the terminal or copy pasting files using a graphical user interface like FileZilla.

`git status`: This command provides the state of the current repository in the local computer (or server) relative to Github's remote repository.

`git add .`: Adds and removes **all** new file additions/deletions from repository. Remember, when you add or remove a new file to a folder in your local computer, it does not get automatically added to your repository. You have to execute the command for this to happen.

`git commit -a -m "<write here a short descriptive message>"`: Send changes to remote repository

`git checkout <branch name>`: Changes scope to any branch, including the master branch.

`git checkout -- .`: Disregard changes.

`git pull`: Updates the entire repository