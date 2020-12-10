# Git cheatsheet

## Common commands
**add and commit** 
Usage: 
``` 
git add <file>
```
Commonly, you `add` all the changes you've made already, so it's easier to do 
```
git add .
``` 

After staging (adding) your changes, commit them, so they're tracked: 
```
git commit -m '[branch name] A brief/good description of these changes'
```

**pull and push**
Pull any changes from the remote repository (github, bitbucket, ...). Do this after using `commit`.

```
git pull
``` 

To push your commit to the remote repository, use `push` (after your commit)
```
git push
```

## Not so common commands
```
git log --graph --decorate --pretty=oneline --abbrev-commit
```

**branch**
List all branches (with the one you're on highlighted)
```
git branch -a 
```
Create a new branch `branchName`
```
git checkout -b branchName
```
Create a new branch `branchName`, linked to remote branch `branchName`.
```
git checkout -b branchName --track origin/branchName
```
Delete branch `branchName` (use `-D` instead of `-d` to force deletion)
```
git branch -d brachName
```
Change to branch `otherBranch`
```
git checkout otherBranch
```

**merge**
Merge branch `featureBranch` into `mainBranch` 
```
git checkout mainBranch
git merge featureBranch
```
