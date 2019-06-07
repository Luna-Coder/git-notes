# git-notes

___

## Terminal Basics

* `~` is an alias for `$HOME` directory.

* `.` denotes the current directory.

* `..` denotes the parent directory.

* `*` is the wildcard symbol, selects all files in the working directory.

* Press the `tab` key for auto completion in the command-line.

* `less` is a program that displays the contents of a file.

* `cat` is a program that prints the contents of one of more files to the console.

* `mv` moves or renames a file or directory.

* `cp` copies a file or directory. Similar to `mv`, but `cp` leaves the original in-place. Must use the `-r` flag to recursively copy a directory.

* `rm` removes a file or directory. Use the `-r` recursive flag to remove a directory and its contents.

* `mkdir` creates a new directory. Use the `-p` flag to create nested directories. 

* `touch` creates a new file, but also used to update timestamps on a file.

* `command` **+** `K` to clear the terminal screen.

* `command` **+** `U` clears everything typed in the prompt.



 ___

## Configuration 
 
* `$ git config --global user.name "John Doe"` sets a first and last name.
 
* `$ git config --global user.email "john-doe@gmail.com"` set the user email address.
  
* `$ git config --global color.ui true` turns on code highlighting.
 
* `$ git config --list` shows a list of all the set git configurations.

* `$ git init` initializes a hidden directory called `.git` in the project's root directory and sets up file structure for git.
 
 ___

 ## Add/Remove Files
 
* `$ git add my-new-file.txt`

* `$ git add my-new-file.txt other-file.js`

* `$ git add .` adds all files in the current directory to the staging area.

* `$ git add -all` adds all the files in the root directory and other directories.
 
* `$ git rm --cached my-file-name` the `--cached` option indicats files in the staging area.

* `$ git rm -r folder-name` recursively removes all folders and files from the working directory.

___

 ## Branches
 
* A branch is a version of the repository.
 
* Each branch has its own commit history and current version.
 
* `$ git branch` shows all branches.
 
* `$ git branch my-branch-name` creates a new branch.

* `$ git branch -d some-old-branch` deletes the `some-old-branch` branch.
 
* `$ git checkout my-other-branch` switch to a new branch (checkout to a new branch) .
 
* `$ git checkout -b my-branch-name` is the same as `git branch` and `git checkout` in one step.

* `$ git merge some-branch-name` merges the `some-branch-name` branch with the current working branch.

* Branch Names:
  * All text should be in lower case letters
  * Descriptors should be hyphenated
  * Branch names should start with one of the following:
    * `bug/`name-of-branch
    * `feature/`name-of-branch
    * `refactor/`name-of-branch
    * `style/`name-of-branch

#### Remote 

* `$ git remote add origin https://github.com/Username/some-app.git`

  The `origin` option is the default name for the server on which your remote repository is located.

  Git doesn't care what you name your remote, but its typical to name your main branch `origin`.
 
* `$ git remote -v` the `-v` option lists all the remote repos you've connected to.

#### Push Files

* `$ git push -u origin master` 
  * Pushes your files to a remote repository.
  * We also specify the server our local repo is connected to, `origin`.
  * The branch we are pushing, `master`.
  * The `-u` option remembers the `origin` and `master` parameters and allows us to run `git push` the next time.

___
 
 ## Commit Files
 
* `$ git commit -m "Add three files to project"`

* `$ git commit -am "Do something once more"` the `-a` option auto removes deleted files with the commit.

* `$ git reset my-file-name.js` removes a file form the staging area.

* `$ git reset --soft HEAD^` 
   * `--soft` option means that the commit is cancelled and moved before `HEAD`.
   * You can now add another file to the staging area and commit, or you can amend files and commit them.
   * `HEAD` is just a pointer to a branch.
   * `^` represents the last commit.
   
* Commit Messages:
  * Capitalize the first word
  * Do not end the commit message with a period, `.`
  * Wrap the message content in double quotes, `""`
  * Use imperative mood in the subject line, as if giving a command/instruction

___

## Cloning A Repository

Cloning a repository is very different from pulling from a repository. 

* `$ git clone git@github.com:YourUsername/your-app.git`

If you clone a remote repository, Git will:
- Download the entire project into a specified directory.
-	Create a remote repository called `origin` and point it to the URL you pass.

The last point simply means that you don't need to run `git remote add origin git@github.com:YourUsername/your-app.git` after cloning a repository. 

The `clone` command will add a remote origin automatically, and you can simply run `git push` from the repository.

___

## Pull Changes

* `$ git pull`
  * Pulls changes in the current branch made by other developers.
  * Synchronize your local repository with the remote repository.

  The `pull` command doesn't create a new directory with the project name.

  Git will only pull updates to make sure that your the local repository is up to date.
 
* `$ git pull` shortcut for `git fetch` **+** `git merge origin/master`
 
 ___
 
 ## Fork A Repository
 
 `$ git fork repo-url` creates your own copy of someone else's entire repository (all branches and commit history).

___

 
 
 
 
 
