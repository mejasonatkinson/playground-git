# [Git It? How to use Git and Github; Fireship](https://www.youtube.com/watch?v=HkdAHXoRtos)

Git is like a history book for your code.

Services such as GitHub make open source software accessible to the world.

To start using git run:
`git init`

To remove git run:
`rm -rf .git` 

Another option is use [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) which is a Visual Studio Code Extension

`.gitignore`

````
/node_modules
````

git will automaticlly look at this file and ignore anything that matches the file path or pattern.

Stage files by running:
`git add .`

Unstage files by running:
`git reset .`

Tip: MAKE MANY small COMMITS.

`git add .`
`git commit -m "first commit"`

*QUESTION:* how do you use emojis in the commit message? 
*QUESTION:* how do you make your commit message multi-line? 

`git branch`

Create and move to the branch by running:
`git checkout -b feature`

`checkout` creates the branch. `-b` moves you on to the branch you have just created.

You don't need to commit code before switching between branches. 
You can also do something called stashing, if you are not ready to commit.
`git stash -u`
`git stash pop`

You can merge a feature into the master by running:
`git checkout master` to move back to the master branch.
`git merge feature` to merge the feature branch into the master branch.

**merge conflict...**

You can squash all the commits you have done on a feature into 1 commite by running: 
`git merge feature --squash`

GitHub
