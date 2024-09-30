# Handy commands using git

## Count lines of code in an entire repo 
```git ls-files | xargs wc -l```
## Pulling changes from remote repository
```git pull```

Disclaimer: Before working on the local repository, make sure to pull from the remote repository (once before you start working on the local repository)
to avoid any conflicts when you're later pushing the new changes to the remote repository. It could be that you unknowingly changed something on the remote 
repository and have forgotten. 
## Commits
### Checking for new changes
```git status```
### Adding new changes
```git add filename``` and if you want to add everything ```git add .```
### Making commits
```git commit -m message```
### Viewing the commit history
```git log```

```git log -p``` to show the changes between the commits as well.

```git log -p -2``` the number limits the amount of commits shown, here that would be 2.

```git log --stat``` shows abbreviated stats per commit.

More options can be found [here](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History).
