# Notes-Learn git and github

### Current status of git
```
git status
```

***

### Add/stage newly created/modified files
```
git add file_names
git add .
```

***

### Commit changes
* **Commit staged changes**
```
git commit -m "this is message"
```
* **Commit unstaged but tracked changes**
```
git commit -am "this is message"
```
> Major difference between using -am and -m in commit is
> 
> - **When you perform git add for new file, the changes are already staged and you dont need to add -a**
> 
> - **If files are only modified (not added/deleted) then use:** `git commit -am "_msg_"`

***

### Check logs/hostory of commits
```
git log
```

***

### Stash all the uncommited changes tracked changes
- **Stash changes:** `git stash`
- **Get changes from stash:** `git stash pop`
- **Delete changes from stash:** `git stash clear`

***

### Adding remote URLs
- **Check/list remote  urls:** `git remote -v`
- **Add remote URL (as alias origin):** `git remote add origin _link_`

***

### Branches
- **Create branch:** `git branch name`
- **Switch branch:** `git checkout name`
- **Create and switch branch:** `git checkout -b  name`

> - If branch is created using github.com, then upstream is set automatically and can push using `git push` with out specifying branch
> 
> - If branch is created in local using `git checkout -b name`, the upstream needs to be set using `--set-upstream` or need to push with `git push origin _branch_name_`

***

### Fetch vs pull

> - **Fetch:** Fetch metadata but dont get changed files in local
> 
> - **Pull:** Fetch metadata and get changed files in local

- **Fetch from upstream using `git fetch`**
> - **Fetch metadata:** `git fetch --all --prune`
> - **Get changes to local from upstream:**  `git reset --hard upstream/main`
> - **Push changes to origin brnach:** `git push origin branch name`

                                        or

- **Fetch from upstream using `git pull`**
> - **Get changes to local from upstream:** `git pull upstream main`
> - **Push changes to origin branch:** `git push origin branch name`

***

### Interactive rebase or Squash
 - Combine multiple commits into 1 commit
 > - `git rebase -i _commit_id_till_you_want_to_merge_`
 - pick (select) with p and squash (delete) with s
 - Add commit messages by deleting previous commit messages
 - Might have to force push

***

### Reset/Revert
 - Reset reverses the local change and then need to push (delete commit)
 > - `git reset commit_id` 
 - Reset reverses the local change and then need to push (create new commit on top)
 > - `git revert HEAD`

***

### Future scope
 - git cherry-pick
 - git rebase in details
 - git merge
 - git stash in details
 - Merge conflicts

***

### References: 

**[1]** Basic: <https://youtu.be/apGV9Kg7ics> *(Completed)*

**[2]** Professionals: <https://youtu.be/Uszj_k0DGsg> *(Completed)*

**[3]** Advanced: <https://youtu.be/qsTthZi23VE> *(Todo)*

**[4]** Branches: <https://youtu.be/e2IbNHi4uCI> *(Todo)*