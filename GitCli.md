# Clone

Exactly as it sounds.  Clones the specified repository to a workstation

`git clone <repo>`

```
git clone https://github.com/aroeh/cli-commands.git
```

# Pull

> Gets the latest changes from the origin

`git pull`

```
git pull
```

# Branch

> Lists the branches using the specified options if provided
- not providing options will list all local branches
- r will list remote branches
- a will list all branches, local and remote

`git branch <options>`

```
git branch
```
```
git branch -r
```
```
git branch -a
```

## Create New Branch

> Creates a new local branch using another specified local branch as the source

`git branch -m <source-branch> <new-branch>`

```
git branch -m main feature-branch
```

## Unset Branch Origin

> Removes remote branch association from the local branch.  Only use if the branch is based on a different origin branch

`git branch --unset-upstream`

```
git branch --unset-upstream
```

## Delete Local Branch

> Deletes the specified branch from the local workstation

`git branch -D <branch>`

```
git branch -D feature-branch
```

# Checkout

> Switches to the specified branch on the local workstation

`git checkout <branch>`

```
git checkout main
```

# Status

> Lists all files that have changes on the branch.  Also includes information on which changes have been commited

`git status`

```
git status
```

# Add

> Adds the specified files to be included on the next commit.  All changed files can be added or individual files can be added.
- add * will add all files with saved changes

`git add <file>`

```
git add *
```
```
git add README.md
```

# Commit

> Commits files to the current branch and prepares them to be pushed to the remote repository on a server
- m enables specifying a commit comment

`git commit <options>`

```
git commit -m "commit comment"
```

# Push

> Writes the committed files to a remote repository on a server

`git push`

```
git push
```

## Push Local Branch

> Push local branch changes to a specified remote repository.
- Including the branch name will push the local branch to that remote branch

`git push origin HEAD`

```
git push origin HEAD
```

- Excluding the branch will push the local branch to the remote branch with the same name

`git push origin HEAD`

`git push origin HEAD:<branch>`

```
git push origin HEAD:main
```

## Push Branch Origin

> Pushes the changes for the specified branch to the remote server.  If deleting a branch locally, this command will delete teh branch on the remote server

`git push origin :<branch>`

```
git push origin :feature-branch
```

## Push and Set Origin

> Pushes the current local branch to the remote server branch and sets the branch origin to the specified branch name

`git push --set-upstream origin <branch>`

```
git push --set-upstream origin main
```

# Merge

> Merges changes from the specified branch into the branch that is currently checked out

`git merge <branch>`

```
git merge main
```

# Stash

> Save current changes in a temporary commit outside of any branch

`git stash`

```
git stash
```

# Stash Pop

> Retrieves stashed changes and adds them to the current branch

`git stash pop`

```
git stash pop
```

# Config

> Lists global git settings on the PC

`git config --global --list`

```
git config --global --list
```

# Default Branch

> Sets the default branch to the specified name

`git config --global init.defaultbranch <branch>`

```
git config --global init.defaultbranch main
```