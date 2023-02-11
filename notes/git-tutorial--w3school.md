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

In Git, a branch is a new/separate version of the main repository. Switching between branches and work on different projects without them interfering with each other.

To create a new branch you use the command `git branch new-branch` "new-branch" is referring to the name of the branch you are creating.

To confirm that the branch has been created you can run `git branch` which will list out all the branches you have locally. The `*` marker tells you which branch you are currently on.

To switch to the new branch you can use the command `git checkout new-branch` you can check to make sure it has changed by running the `git branch` command again.

You can also combine these commands by running `git checkout -b new-branch` which will create, and move you onto the newly created branch.

After you have made changes and run the commands `git add .` `git commit -m "Branch Changes"` the branch you are working on is different from your main/master branch.

## [Git Branch Merge](https://www.w3schools.com/git/git_branch_merge.asp?remote=github)

When you branch/project is ready you will want to merge it into the main/master branch.

To merge into a branch, you must first be on the branch you wish to merge into.

Running `git checkout master` will move you to the master branch.

Then to merge the branch we had previously been working on run `git merge new-branch`.

Once merged you can run `git branch -d new-branch` to delete the branch locally from your machine.

**Merge conflicts** are caused when there are multiple branches and the same section of code is edited in both branches. When you run the `git merge` command. Use the `git status` command to confirm the conflict and check where the conflict is happening. Open up the file(s) highlighted in the status check to fix the merge conflict.

Use `git status` again to confirm that the merge conflict(s) have been resolved.

Create a commit to confirm the merge. `git commit -m "merged with new-branch after fixing conflicts"`

After this you can then delete the mered branch (`git branch -d new-branch`).

## [Git GitHub Getting Started](https://www.w3schools.com/git/git_remote_getstarted.asp?remote=github)

https://www.github.com/

You can create a new repository on GitHub in accouple of different ways.

On the top right of the nav bar, you can click on the plus '+' and then click 'New repository'

...

This will take you to a details where you can fill in any relevant information about the repository.
The only required fields are the Owner, Repository name and whether it should be a Public or Private repository.

Click 'Create repository' to create the repository.

After this sstep, a Quick setup screen will be displayed. 

There are 3 methods which we can use to link this repo to our local git instance.

1. The GitHub Desktop App
2. HTTPS
3. SSH

**THIS IS WHERE I GET STUCK**

Scenario 1: We already have a local git repo...

`git remote add origin https://github.com/user-name/git-repo-name.git`

`git push --set-upstream origin master`

Go back into GitHub, you will see that the repository has been updated.

## [Git GitHub Edit Code](https://www.w3schools.com/git/git_remote_edit_code.asp?remote=github)

As well as hosting our code, GitHub can also be used to edit the code.

Click the little pencil icon when you have selected a file to be able to edit the file.

After you have made the changes, scoll to the bottom of the page. You will find a Commit changes dialog box, where you can add a commit messsage and commit description, as well as the ability to add the change as a new branch. Clicking Commit changes will commit the change.

## [Git Pull from GitHub](https://www.w3schools.com/git/git_pull_from_remote.asp?remote=github)

The `pull` command is a combination of 2 different commands `fetch` and `merge`.

`fetch` gets all the change history of a tracked branch/repo

If you run `git fetch origin` on your local repo. this will get all the updates which have been made on GitHub.

If you run `git status` you will see what has happened and `git log origin/master` will show you the file(s) which have been updated. 
`git diff origin/master` can show you the differences between the local master and origin/master.

The Merge command can then be run `git merge origin/master`.

To confirm this has been successful, run `git status` again.

To simplify this whole process we can run the `pull` command. `git pull origin`.

## [Git Push to GitHub](https://www.w3schools.com/git/git_push_to_remote.asp?remote=github)

The `push` command pushes the changes to a remote repo such as GitHub.

1. Make a change...
2. Add change to staging `git add .`
3. Commit the change `git commit -m "make another change... example"`
4. Check status `git status`, you will see that your local branch is ahead of 'origin/master'
5. Push the change up to GitHub `git push origin`
6. Check GitHub to confirm that the change has been updated

## [Git GitHub Branch](https://www.w3schools.com/git/git_remote_branch.asp?remote=github)

On the repo on GitHub you can create a new branch by selecting the branch name (below 'code' on the top left). This will open up a dialog box where you can ender a new repo name or see a select of the other branches on the repo, if there is any.

## [Git Pull Branch from GitHub](https://www.w3schools.com/git/git_branch_pull_from_remote.asp?remote=github)

Run `git pull` to make sure our local code base is up-to-date.

Run `git status`

Run `git branch` we do not have the new branch listed on our local Git. But if we run `git branch -a` this will show the remote branchs.

Run `git checkout remote-branch-name` and check to make sure it is up-to-date by running `git pull`

Run `git branch` again and you will now see if on your local machine.

## [Git Push Branch to GitHub](https://www.w3schools.com/git/git_branch_push_to_remote.asp?remote=github)

To do the reverse and push a local branch.

First create and move to a new branch `git checkout -b local-branch-name`

Then update something, in the branch and run `git add .` and `git commit -m "local-branch-name commit message"`

To push the change, run `git push origin local-branch-name`

**NOT SURE IF THIS IS CORRECT? USED TO USING --UPSTREAM**

You will now see this branch on GitHub.

We can now merge the changes on GitHub, this is done by creating pull request. If there is no conflicts it will then ask you to merge pull request, and give you the option to delete the branch.

## [Git GitHub Flow](https://www.w3schools.com/git/git_github_flow.asp?remote=github)

The GitHub flow works like this:

- Create a new Branch
- Make changes and add Commits
- Open a Pull Request
- Review
- Deploy
- Merge

## [Git GitHub Pages](https://www.w3schools.com/git/git_remote_pages.asp?remote=github)

With GitHub pages, GitHub allows you to host a webpage from your repository.

GitHub pages need a special name and setup to work, so we start by creating a new repository.

This repository needs a special name to function as a GitHub page. It needs to be your GitHub username, followed by .github.io: `user-name.github.io`

We add this new repository as a remote for our local repository, we are calling it gh-page (for GitHub Pages).

- `git remote add gh-page https://github.com/user-name/user-name.github.io.git`
- `git push gh-page master`

Check that github has received all the files.

Select Settings from the menu, it should read that Your site is published.

[w3schools GitHub Page](https://w3schools-test.github.io/)

## [Git GitHub Fork](https://www.w3schools.com/git/git_remote_fork.asp?remote=github)

How to add to someone else's Repository?

At the heart of Git is collaboration. However, Git does not allow you to add code to someone else's repository without access rights.

A **fork** is a copy of a repository. This is useful when you want to contribute to someone else's project or start your own project based on theirs.

In the top right below the navigation on a repo there is a 'Fork' button, clicking this will make your own copy of the repo.

## [Git Clone from GitHub](https://www.w3schools.com/git/git_clone.asp?remote=github)

After Forking, you have a git repo on github but no code locally...

The git `clone` command creats a complete copy of the repository.

In the repo on github click the green code button and copy the HTTPS or SSH url.

Then in the terminal navigate to directory you want the repo to live, and run the following command:

`git clone https://github.com/user-name/repo-to-fork.git`

When you check your file system (`ls`) you will see a new directory named after the cloned project.

`cd` into the project: `cd forked-repo` and run `git log` to confirm you have the full repo data.

**THIS IS WHERE I GET STUCK/LOST**

Check how the remotes are set up by running: `git remote -v`

`git remote rename origin upstream`

`git remote -v`

`git remote add origin https://github.com/other-user/forked-repo.git`