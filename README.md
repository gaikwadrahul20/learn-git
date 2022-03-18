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

### Adding remote URLs
check/list remote  urls `git remote -v`
add remote URL to as alias origin `git remote add origin link`


### Branches
Create branch: `git branch name`
Switch branch: `git checkout name`
Create and switch branch `git checkout -b  name`

> If you create branch in github it will automatically push to that branch using `git push`
> 
> If branch is created in local using `git checkout -b name`, the uptream is not setand need to push with `git push origin branch`


### Fetch vs pull
> Fetch: fetch metadata but dont get changed files in local
> 
> Fetch: fetch metadata and get changed files in local


### Fetch from upstream
Fetch metadata: `git fetch --all --prune`
Get changes to local from upstream:  `git reset --hard upstream/main`
Push changes to origin brnach: `git push origin branch name`

or 

Get changes to local from upstream:: `git pull upstream main`
Push changes to origin branch: `git push origin branch name`

### Squash
 - Combine multiple commits into 1 commit
 - `git rebase -i commit_id_till_you_want_to_merge`
 - pick with p and squash with s
 - Add commit messages by deleting previous commit messages
 - Might have to force push

### Reset/Revert
 - Reset reverses the local change and then need to push
 - `git reset commit_id` 
 - Reset reverses the local change and then need to push
 - `git revert commit_id`