# GIT

- [Mathieu Nebra tips](https://openclassrooms.com/fr/courses/1233741-gerez-vos-codes-source-avec-git)

### Basic

- git clone [link] [repo_name]
1. clone a repository

- git status
1. show file status

- git add [repo/file]
1. add the repo/file - you can put as many as you want

- git commit
1. commit the changes
2. -m: add a message
3. --amend: modify the last commit message

- git push
1. push the changes

- git pull
1. get the latest version of file uploaded to git

### Move 

- git checkout
1. move the pointer to another location
2. [repo/file]: discard changes to the repo/file (stay as it was in the last commit)
3. [commit id]: go back to the version of the commit
4. [branch]: go to that branch

- git reset [flag] [commit]
1. alone: git reset will roll back modifications in the server
2. --hard: git reset will roll back modifications in the server and the local 

```sh
1. HEAD: last commit (n)
2. HEAD^: previous commit (n - 1)
3. HEAD^^: previous commit (n - 2)
4. HEAD~x: previous commit (n - x)
5. COMMIT_NUMBER: corresponding commit
```

### Information

- git log
1. show logs
2. -p: to see more details

- git diff
1. show differences

- git remote --v
1. show the url of the repo host

### Branches

- git branch [flag] [name]
1. alone: show all branchs
2. [name]: create a branch with the corresponding name
3. -d [name]: delete the branch

- git stash [branch]
1. alone it saves changes
2. if we go back to another branch, changes will be lost if not push
3. git stash will "save" them so we can checkout elsewhere and then come back
4. it's used when you don't want to commit on branch test but need to go elsewhere
5. with branch name, it recover changes

- git merge
1. go in the branch where you merge (git checkout master)
2. merge the branch you want to (git merge test)

### Submodules

- git submodule init [link]
1. add a link to a submodule

- git submodule update
1. clone or update the submodule

### Delete

- git rm
1. remove a file from the server

- git revert [commit]
1. revert a commit by adding the opposite modifs 