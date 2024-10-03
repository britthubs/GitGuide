# Useful commands using git

## Count lines of code in an entire repo 
```git ls-files | xargs wc -l```
## Pulling changes from remote repository
```git pull```

Disclaimer: Before working on the local repository, make sure to pull from the remote repository (once before you start working on the local repository)
to avoid any conflicts when you're later pushing the new changes to the remote repository. It could be that you unknowingly changed something on the remote 
repository and have forgotten. 
