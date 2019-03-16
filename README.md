# GIT

- [Mathieu Nebra tips](https://openclassrooms.com/fr/courses/1233741-gerez-vos-codes-source-avec-git)

### Basic

- clone a repository
```sh
git clone [link] [repo_name]
```

- show file status
```sh
git status
```
- add the repo/file - you can put as many as you want
```sh
git add [repo/file]
```

- commit the changes
```sh
git commit
-m: add a message
--amend: modify the last commit message
```

- push the changes
```sh
git push
```

- get the latest version of file uploaded to git
```sh
git pull
```

### Move 

- move the pointer to another location
```sh
git checkout
[repo/file]: discard changes to the repo/file (stay as it was in the last commit)
[commit id]: go back to the version of the commit
[branch]: go to that branch
```

git reset will roll back modifications in the server
```sh
git reset [flag] [commit]
2. --hard: git reset will also roll back modif on local
```

```sh
1. HEAD: last commit (n)
2. HEAD^: previous commit (n - 1)
3. HEAD^^: previous commit (n - 2)
4. HEAD~x: previous commit (n - x)
5. COMMIT_NUMBER: corresponding commit
```

### Information

- show logs
```sh
git log
-p: to see more details
```

- show differences
```sh
git diff
```

- show the url of the repo host
```sh
git remote --v
```

### Branches

- list branchs
```sh
git branch [flag] [name]
[name]: create a branch with the corresponding name
-d [name]: delete the branch
```

- saves changes on branch
```sh
git stash [branch]
if we go back to another branch, changes will be lost if not push
git stash will "save" them so we can checkout elsewhere and then come back
it's used when you don't want to commit on branch test but need to go elsewhere
with branch name, it recover changes
```

- merge branchs
```sh
git merge
go in the branch where you merge (git checkout master)
merge the branch you want to (git merge test)
```

### Submodules

- add a link to a submodule
```sh
git submodule init [link]
```

- clone or update the submodule
```sh
git submodule update
```

### Delete

- remove a file from the server
```sh
git rm
```

- revert a commit by adding the opposite modifs 
```sh
git revert [commit]
```