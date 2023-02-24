# git-lesson
Repo to practice git methods

# Install git
```bash
sudo apt install git -y
```


# Git usage

- Set parameters

```bash
git config --global.user.name "First Last"
git config --global user.email "email@domain.com"
```

- clone a repo
```bash
git clone <url>
```

- New directory will be in terminal working path

## Git Status

- Up to date with origin/main

```bash
git status

cat .git/config
```

# Branch

- Create branch
- Make change
- Merge change

## Optional Install VSCode
- install vscode
  - [Instructions](https://code.visualstudio.com/docs/setup/setup-overview)

- Open folder in vscode
	- `code .`

## Work on Repo

- Add a module similar to moduleP
	- my_module

## Merge

	- git status
		- Shows files that aren't being tracked in red
	- git add filename.py
    - git add -all
	- git status
		- Files will now be displayed
	- git commit -m 'commit message'
	- git status
		- Will now be ahead of main
	- git push
		- Publish local changes
		- If there is changes to main since you made the pull you will get a message to pull changes
		- git pull

## The Lesson from working on Main

Working on the same branch causes issues with syncing changes

- Set global
	- git config pull.rebase false

# Create Branch

- git branch
	- Shows known branches
- git checkout -b branchName
	- Switches to branch
	- Creates the branch if it is new
- git branch
	- Shows new branch
- Make changes to files in branch
	- git add fileName

## Merge changes back to main

- Make sure required files are added
- git commit -m 'commit message'
- If new branch
	- Create new branch origin
	- git push --set-upstream origin branch
- git pull
- git checkout main
- git pull
- git merge --no-ff --no-commit branchName
	- --no-ff no fast forward
	- --no-commit
		- stops before commiting
- git status
- git commit -m 'merged branchName into main'
- git push

# Protecting main

- Setting up protections on main will prevents everyone being able to commit to main without getting it approved first
- Only maintainers of the project can make changes on that branch
