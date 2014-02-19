### Git Standards

To develop a feature or fix a bug, just checkout master, pull from server and create a branch to start woking, then commit and push your changes.


### Case 1: If you're working on a branch, we recommend you constantly pull changes from `master`

```bash

# Before start working, pull changes from server
$ git pull origin master

# Hack...

# Add and commit you changes
$ git add .
$ git status
$ git commit -m "Component: commit description. Closes #10"
$ git push origin current-branch

# Start agin...
```

### Case 2: Workflow when creating a new branch.

When you create a new branch, we recommend you create it from `master`, so that it reflects the latest state in the project and can be easily merged.

```bash
# Move to master and pull new changes
$ git checkout master
$ git pull origin master
$ git checkout -b new-feature

# Hack...

# Add and commit your changes
$ git add .
$ git commit -m "Commit description. Closes #10"
$ git push origin new-feature

# Start again...
```


## Useful git commands

**Create a new branch and switch to it**
```bash
$ git checkout -b my-branch
```

**Reset changes that are not added.**
```bash
$ git reset --hard
```

**Delete the last commit**
```bash
$ git reset --soft HEAD^~1
```

### Git command within Sublime

**Show the history of the current file**
```
# Open command palette
ctrl + shift + p

# Show file history
git show current file
```
