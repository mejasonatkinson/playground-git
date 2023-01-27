# [13 Advanced (but useful) Git Techniques and Shortcuts; Fireship](https://www.youtube.com/watch?v=ecK3EnyGD8o)

Linus Torvalds invented git in 2005.

Adding commits

`git add .` and `git commit -m "hi mom"`

OR

`git commit -am "that was easy!"`

OR

`git config --global alias.ac "commit -am"` to create an alias

`git ac "noice!"` so now you are writing `ac` instead of `commit -am`

Changing the last commit message

`git commit --amend -m "nice!"`

Update the last commit (with files)

`git add .`
`git commit --amend --no-edit`

This only works if you haven't already pushed your code.

To overwrite history on remote, you can run:

`git push origin master --force`

To undo a commit with a new commit run:

`git revert better-days`

Remote work.

On GitHub you can press `.` in any repo to open up a browser based version of vs code. BUT the terminal doesn't work.. you can set up a GitHub Codespace to get this to work.

`git stash` to stash changes you are not ready to commit.

`git stash pop` to add the changes back into your code.

`git stash save lookupname` to stash the changes under a lookup name.

`git stash list` to find the stash AND index.

`git stash apply 0` to add the changes back into the code using the index seen in `git stash list`

In the past the default branch has always been called `master` post 2020 this is no longer the prefered naming structure; instead `main` is prefered.

To change is use `git branch -M main`

`git status` to check the change.

`git log`

`git log --graph --oneline --decorate`

Don't fully understand:

- Bisect
- Fixup
- Squash
- Autosquash
- Hooks
    - Husky

Delete/Reset the code in your local repo to match the remote repo

`git fetch origin`
`git reset --hard origin/master`
`git clean -df`

To remove git completly, you can run:

`rm -rf .git`

To go back to the previous branch you where in, you can run:

`git checkout -`