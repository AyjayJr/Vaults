Misc commands that I've found useful for git
### Reset head to past commit and preserve commit history
```
git reset --hard <commit-hash> 
git reset --soft HEAD@{1}
git commit -m "<message>"
```
### Delete local branch
```
git branch -d <local-branch-name>
```

### Stop tracking a file
```
git rm --cached <file>
```

---
#tools #git 