# Clone

> Exactly as it sounds.  Clones the specified repository to a workstation

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

# Command Name

> What the command does

`Example syntax or parameterize`

```
Example command for copy and paste
```

# Command Name

> What the command does

`Example syntax or parameterize`

```
Example command for copy and paste
```

# Command Name

> What the command does

`Example syntax or parameterize`

```
Example command for copy and paste
```

# Command Name

> What the command does

`Example syntax or parameterize`

```
Example command for copy and paste
```

# Command Name

> What the command does

`Example syntax or parameterize`

```
Example command for copy and paste
```

# Command Name

> What the command does

`Example syntax or parameterize`

```
Example command for copy and paste
```

# Command Name

> What the command does

`Example syntax or parameterize`

```
Example command for copy and paste
```

# Command Name

> What the command does

`Example syntax or parameterize`

```
Example command for copy and paste
```
