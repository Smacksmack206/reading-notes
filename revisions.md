# Initial Customization
After making sure Git has been installed, you should perform some customization steps, which should only need to be completed once on any machine. To change settings, you can repeat these steps.

## Configuration of Variables

An inherent Git tool called git config allows the setting of configuration variables that control aspects of Git’s operation and look.

## Identity Setting

After installing Git, users should immediately set the user name and email address, which will be used for every Git commit.

Type the following into Terminal or Command Line:

`git config --global user.name "Jane Smith"`

`git config --global user.email "example@email.com"`
To confirm that you have the correct settings, enter the following command:

`git config --global user.name` (should return Jane Smith)

git config --global user.email (should return example@email.com)
*By using the –global option, these Git settings apply to anything on the system. To use different identity settings for a specific project, change the working directory to the desired local Git repository and repeat the steps above without using –global.

## Default Text Editor
Without configuration of a default text editor, Git will use the system’s default editor–most likely Vim. To configure a different text editor, such as Emacs, type the following into your Terminal or Command Line:

$ git config --global core.editor emacs

Note: For some editors, you may need to find specific instructions for default configuration.

Check Settings
To check settings, use the git config --list command.

Example:

`$ git config --list`

`user.name=Jane Smith`

`user.email=example@email.com`

`color.status=auto`

`color.branch=auto`

`color.interactive=auto`

...

## Getting Help
There are three ways to get more information on a particular command, by accessing the manual:

git help command

git command --help

`man git-command`

# Setting up a Git Repository
Importing
To import an existing project or directory into Git, follow these steps using the Terminal or Command Line:

Switch to the target project’s directory
Example:

$ `cd test` (cd = change directory)
Use the `git init` command
$ `git init`
Note: At this stage, you have created a new subdirectory named .git that has the repository files. Tracking has not commenced.

To start tracking these repository files, perform an initial commit by typing the following:
$ `git add *.c`
$ `git add LICENSE`
$ `git commit -m “any message here”`
Now, your files are tracked and there’s an initial commit. We will discuss the particular commands in detail soon.

## Cloning
You can also create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:

$ git clone https://github.com/test
By cloning the file, you have copied all versions of all files for a project. This command leads to the creation of a directory called “test,” with an initialized .git directory inside it, which has copies of all versions of all files for the specified project. The command also automatically checks out — or retrieves for editing — a copy of the newest version of the project.

To clone a repository into a directory with another name of your choosing, use the following command format:

$ git clone https://github.com/test mydirectory
The command above makes a copy of the target repository in a directory named “mydirectory.”

## Workflow
Local Repository Structure
The local Git repository has three components:

Working Directory: The actual files reside here.
Index: The area used for staging
Head: Points to the most recent commit
image03

## Saving Changes
All files in a checked out (or working) copy of a project file are either in a tracked or untracked state.

## Tracked
Tracked files can be modified, unmodified, or staged; they were part of the most recent file snapshot.

## Untracked
Untracked files were not in the last snapshot and do not currently reside in the staging area.

*After cloning a repository, files have tracked status and are unmodified because they have been checked out but not edited.

## The Life Cycle of File Status
After you edit a file, Git flags it as modified because of changes made after the previous commit.
You stage the modified file.
Then, you commit staged changes.
image00

## Check File Status
To determine the state of files, utilize the git status command:

$ git status
On branch master

nothing to commit, working directory clean

*This information indicates which branch you’re on (we will cover branches in a later section) and states “working directory clean,” which means that files have tracked or modified status at the moment. Also, no untracked files are present because Git has not listed any.

Tracking and Staging a New File
Single File

Track one file only by using the following format:

`git add filename`
All Files

Track all files in a repository by using the following command:

$ `git add *`
*After using these commands, files are tracked and staged for committing.

After adding a new file called EXAMPLE, you would see information regarding changes to be committed when using the git status command:

$ `git status`

On branch master

Changes to be committed:

  (use "git reset HEAD ..." to unstage)
new file: EXAMPLE
This information tells us that there are changes to be committed and that the file has been staged.

Committing a File
After staging one or multiple files, you should commit the changes and record what you did within the commit message:

$ git commit -m “made change x,y,z”
*This step has committed changes for the file or files (you can have one commit message for multiple files, if applicable) to the HEAD.

## Committing All Changes
$ git commit -a
*This command commits a snapshot of all modifications to tracked files in the working directory.

## Pushing Changes
Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.

Example:

$ `git push origin master`
*This command pushes changes from the local “master” branch to the remote repository named “origin”.

*For cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local repository. However, these names can be changed by the user.

## Stashing Changes
When you are not ready to commit changes but do not want to lose them either, git stash is a great option. This command temporarily removes changes and hides them, giving you a clean working directory. When you are ready to continue working on the changes, simply use the git stash apply command to retrieve the hidden changes.

## Remote Repositories
In order to collaborate on Git projects, you must interact with remote repositories, versions of a project residing online or on a network. You can work with multiple repositories, for which you can have read/write or read-only privileges. Teams can use remote repositories to push information to and pull data from.

## Cloned Repositories
As mentioned earlier, for cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local branch.

## Seeing Your Remotes
By running the git remote command, you can view the short names, such as “origin,” of all specified remote handles.

By using git remote -v, you can view all the remote URLs next to their corresponding short names.

$ `cd example`

$ `git remote -v`

remote1 https://github.com/remote1/example (fetch)

remote1 https://github.com/remote1/example (push)

remote2 https://github.com/remote2/example (fetch)

remote2 https://github.com/remote2/example (push)

remote3 https://github.com/remote3/example (fetch)

remote3 https://github.com/remote3/example (push)