---
published: true
tags: git
---
### Add to Staging
```
git add .
```

### Create a branch
```
git checkout -b <branch-name>
```

### Commit changes to local
``` 
git commit -m <comments> 
```

### Commit changes to server
```
git push origin/<branch-name>
```

### Get a branch from server
```
git checkout <branch-name>
```

### List current branch
```
git branch
```

### List branches local and remote
```
git branch -a
```

### Get code from the server for the current branch
```
git pull
```

### Get metadata/information about repository
This is useful for determining how out of alignment your local is with the server
```
git fetch
git diff
git status
```

### Clone a repository
```
git clone <repository path>
```

### Merge master into a local branch
```
git checkout master
git pull
git checkout <branch-name>
git merge master
```

### Unstage changes (ie: undo a `git add .`)
```powershell
git reset 
```

### Revert uncommitted local changes
```
git checkout .
```
