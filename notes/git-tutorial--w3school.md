# [Git Tutorial; w3schools](https://www.w3schools.com/git/default.asp)

## [Git and GitHub Introduction](https://www.w3schools.com/git/git_intro.asp?remote=github)

This is also available for: [BitBucket](https://www.w3schools.com/git/git_intro.asp?remote=bitbucket) and [GitLab](https://www.w3schools.com/git/git_intro.asp?remote=gitlab).

## [Git Getting Started](https://www.w3schools.com/git/git_getstarted.asp?remote=github)

You can download Git for free from the following website: https://www.git-scm.com/

To check if Git is properly installed, run the following command in the terminal: `git --version`

If it returns a version (`git version X.Y`) then Git is installed correctly.

It is important to configure git, so it knows who you are. This can be done by running the following commands:

`git config --global user.name "first-name-last-name"`

`git config --global user.email "name@company.com"`

The keyword global is used to set the global values for the name and email for every repo. you can remove the `--global` keyword if you only want to set the values for the name and email address, for the repo you are in.

----

*The following are not Git commands, and are just common terminal commands*

User `mkdir` to make a directory/new folder

`mkdir myproject`

Use `cd` to change directory/move to the new folder

`cd myproject`

----

You can then start/initialize Git by running

`git init`

## [Git New Files](https://www.w3schools.com/git/git_new_files.asp?remote=github)

In side of the directory/folder you can now add files, for example `index.html`

----

*The following is not a Git command, and is just a common terminal command*

Using `ls` can list out all the files with the directory/folder.

----

Runing the command `git status` will show the untracked file, and may also display details around how to add the file or files to a commit.

## [Git Staging Environment](https://www.w3schools.com/git/git_staging_environment.asp?remote=github)

As you are working, you may be adding, editing and removing files. But whenever you hit a milestone or finish a part of the work, you should add the files to a **Staging** Environment.

Staged files are files that are ready to be committed to the repository you are working on.

You can add a file by running the  `git add` followed by the name of the file for example `git add index.html` or to add all the files in the directory/folder that have been edited, you can run `git add .` or `git add --all` or `git add -A`

The `git status` command will now show the tracked changes, which are ready to be commited.

## [Git Commit](https://www.w3schools.com/git/git_commit.asp?remote=github)

Adding commits keep track of our progress and changes as we work. Git considers each commit change point or "save point". It is a point in the project you can go back to if you find a bug, or want to make a change.

When we commit, we should always include a message.

By adding clear messages to each commit, it is easy for yourself (and others) to see what has changed and when.

You make a commit by using the following command: `git commit -m "First commit"` the text within the "quote marks" is the message connected to the commit.

To view the history of commits for a repository, you can use the log command `git log`

## [Git Help](https://www.w3schools.com/git/git_help.asp?remote=github)

There is alot of commands, to help, you can use the help command to see all commands (`git help --all`) or commands relating to a certain command (`git command -help`), for example `git commit -help`

## [Git Branch](https://www.w3schools.com/git/git_branch.asp?remote=github)