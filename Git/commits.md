# Using commits in git
## Checking for new changes
```git status```
## Adding new changes
```git add filename``` and if you want to add everything ```git add .```
## Making commits
```git commit -m message```
## Viewing the commit history
```git log```

```git log -p``` to show the changes between the commits as well.

```git log -p -2``` the number limits the amount of commits shown, here that would be 2.

```git log --stat``` shows abbreviated stats per commit.

```git log --oneline``` shows one line.
## Going back to a previous commit
In this example, you are going back to the third commit (the last two commits are being removed).
If you want to go to the third commit, (DISCLAIMER: DOING THIS WILL REMOVE ALL THE COMMITS BEFORE THE COMMIT YOU ARE GOING BACK TO AND
ALL UNCOMMITED CHANGES ARE DELETED) you can use :

```git reset --hard HEAD~2```

- ~2 stands for the last two commits that are being deleted. You can edit the number to your situation.

- --hard removes all uncommited changes.

## Stash changes instead of committing
If you don't want to commit yet but rather want to stash the changes away temporarily until you decide what to do with them, use:

```git stash```

To get back to the usual status with uncommited changes, use: 

```git stash pop```

This can be used in the following example: You are working on a branch and suddenly want to check something in another branch. 
Instead of commiting the current changes in order to switch to the other branch, you can simply stash away the changes until you
get back from the other branch, and then unstash them when you're back on the first branch and want to commit the changes or 
work on them further.


More options can be found [here](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History).
