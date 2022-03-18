# Notes-Learn git and github

### Current status of git

```
git status
```

### add/stage newly created files to git to track
```
git add file_names
git add .
```
### Commit changes to local
#### commit staged changes
```
git commit -m "this is message"

```
#### commit unstaged but tracked changes 
```
git commit -am "this is message"

```
> Major difference between using -am and -m in commit is
> 
> 1. When you perform git add for new file, the changes are already staged and you dont need to add -a
> 
> 1. When you change the file you can directly use `git commit -am`

### check logs of commits/ history of commits
```
git log
```
### stash all the uncommited changes tracked changes
stash changes - `git stash`
get stash back `git pop`
cleared stashed changes `git stash clear`
```

git restore/reset?
