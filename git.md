### Git Standards

To develop a feature or fix a bug, just checkout master, pull from server and create a branch to start woking, then commit and push your changes.

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
```
