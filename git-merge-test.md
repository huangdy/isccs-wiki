Test your merge with
```
git merge --no-commit --no-ff <branch name>
```  
If you don't like the results, roll it back with
```
git merge --abort
```
Or just commit it.  
```
git commit -a -m "Your commit message here."
```  
**Example**:  
```
git merge --no-commit --no-ff development
```
