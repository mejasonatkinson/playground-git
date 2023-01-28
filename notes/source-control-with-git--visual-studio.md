# [Source Control with Git; Visual Studio](https://code.visualstudio.com/docs/sourcecontrol/overview)


Visual Studio Code has integrated **source control management (SCM)** and includes Git support out-of-the-box. Many other source control providers are available through extensions on the VS Code Marketplace.

## [Using Git with Visual Studio Code (Official Beginner Tutorial)](https://www.youtube.com/watch?v=i_23KUAEtUM)

Reynald Adolphe | Senior Cloud Advocate

Git: is a program for managing source code.
GitHub: hosts a copy of the source code, or repository online.

Visual Studio Code, makes the process of using Git and GitHub easier.

You first need to install git. Then when you open up a folder, you will be given the option to 'Intialize Repository' on the Source Control panel.

The bottom left hand corned, will tell you the name of the branch you are on.

`Ctrl+Shift+P` or `Cmd+Shift+P` can be used to open the command palette, and access different git commands.

'Git: Rename Branch...' being one of these options.

A file with a 'U' next to it, means the file is untracked.

The '+' Icon can be pressed to stage the file.

The file will then have a 'A' next to it, this means a new file has been added to the repoitory.

To commit, Just add a message in the dialog box above the staged changes, and hit enter or the checkmark icon.

In the command palette search: 'Git: Create Brnach...' to create a new branch and move to the new branch.

When new lines of code are added. The gutter on the left hand side will show this by adding a **green line**.

When a line is changed. The gutter on the left hand side will show this by adding a **blue line**.

When a line is removed. the guter on the left hand side will show this by adding a **red arrow**.

On the Source Control panel along side the '+' Icon is a Discard icon, which will discard all the changes in the file. These 2 icons also appear at the top of the list of changes, so it is possible to Add or Discard ALL changes.

Visual Studio Code, can also run a diff check. To do this you just click on the file in the source control panel.

This will show the changes next to each other, however this can also be done inline. If you select the 3 dots at the top right '...' and select 'Inline View'

In the command palette you can search for branch names, to switch branches.

On the Source Control panel click the 3 dots '...' and select branch > merge branch; It will then ask you from where.

On the Source Control panel click 'Publish Branch', and it will walk you through all the steps to get set up.

In the command palette search: 'Git: Clone' to clone a repo from your GitHub, via url.


### GIT SCM

- [Documentation](https://git-scm.com/documentation)
- [Book](https://git-scm.com/book)
- [Video](https://git-scm.com/video/what-is-git)
- [Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)

VS Code will use your machine's Git installation, so you need to [install Git](https://git-scm.com/download) first before you get these features.

The Source Control icon in the Activity Bar on the left will always indicate an overview of how many changes you currently have in your repository. Selecting the icon will show you the details of your current repository.

Clicking each item will show you in detail the textual changes within each file.

You can also access all git commands from the Command Palette by pressing `Ctrl+Shift+P`.

## [Git: Commits in Visual Studio Code](https://www.youtube.com/watch?v=E6ADS2k8oNQ)

*... notes needed for video*

In order to use git features, you can open a folder containing a git repository or clone from a URL, using the Clone Repository button.

For a GitHub repository, you would find the URL from the GitHub Code dialog.

## [Git: branches in Visual Studio Code](https://www.youtube.com/watch?v=b9LTz6joMf8)

*... notes needed for video*

*... to be continued*