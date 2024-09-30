# Commands for branches

## Making a new branch
Both ways can be used:
1. ```git checkout -b branchname```
2. ```git switch -c branchname```
   
## The difference between git switch, git restore and git checkout
```git checkout```can  be used in following ways:
1. Changing branches with: ```git checkout branchname```
2. Restoring file from another branch: ```git checkout -- filepath```
   
Both actions are split with ```git switch``` and ```git restore```
1. Changing branches with: ```git switch branchname```
2. Restoring files from another branch with: ```git restore -- filepath```

For a more complete explanation go [here](https://stackoverflow.com/questions/57265785/whats-the-difference-between-git-switch-and-git-checkout-branch).

## Other information
For more information go [here](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging).
