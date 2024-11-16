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
### When the commits HAVE NOT been pushed to remote yet
Using following example, you have made four commits, A, B, C and D (with D being the last commit that was done). You would now like to remove 
the three last commits (so B, C and D).
(DISCLAIMER: DOING THIS WILL REMOVE ALL THE COMMITS BEFORE THE COMMIT YOU ARE GOING BACK TO AND ALL UNCOMMITED CHANGES ARE DELETED) 
Only when you haven't pushed the commits to the remote repository yet, you can use:

```git reset --hard HEAD~3```

- ~2 stands for the last two commits that are being deleted. You can edit the number to your situation.

- --hard removes all uncommited changes.

If you do this when you have already pushed the commits, there will be a conflict when pushing the new commit. Following images show this problem. The first image shows the four commits initially, the second image shows the local repository situation, where the the last three commits have been removed and a new commit has been added (for example when you unknowingly already started working on top of the removal of the commits). This new commit is now called E. Putting both of these situations together, it is clear that pushing the local A-E commits will conflict with the A-B-C-D commits in the remote repository. 

![initial commits](/images/init.png)![local commits](/images/local.png) 

(credits to [@mai-soup](https://github.com/mai-soup) for these images and the explanation)

The given error when trying to push will look something like this:
```
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'github.com:britthubs/project.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
### When the commits HAVE been pushed to remote
If you've already pushed the commits, there is a way to remove the commits safely so no conflicts appear when trying push again after removing the commits. 
Using the same example, you can, instead of removing commits, make a commit that's the inverse of the commits you want to remove. Visually this would look something like:

![solution](/images/solution.png)

(credits to [@mai-soup](https://github.com/mai-soup) for this images and the explanation)

It is important you are committing the inverse of the latest commit first, in this case that would be D, followed by C and then B. In general, to commit an inverse of a commit, the following command can be used:
```git revert --no-commit hashcodeofcommit``` Where hashcodeofcommit needs to be replaced with the hash code of the commit that should be inverted. This code can be found in the log of the commits. If the log (using ```git log --oneline``` looks like this:

```
3dfba4f Custom message for commit D
1cfdcb7 Custom message for commit C
8e0e4d0 Custom message for commit B
4d453e3 Custom message for commit A
```

The hash code is the code at the beginning of the line, so for the last commit (commit D) that would be '3dfba4f'.
Putting this information together, for this particular example the commands would look like this:

```
git revert --no-commit 3dfba4f
git revert --no-commit 1cfdcb7
git revert --no-commit 8e0e4d0
```
Finally, don't forget to commit this:

```
git commit -m "Undo changes"
```

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
