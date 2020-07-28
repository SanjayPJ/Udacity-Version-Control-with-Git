## Workflow

- Workflow
	- Adding or modifying files on the working directory
	- Moving to staging area
	- (commit) Adding to repository
		- When commit is made only files from the staging index moved into the repository
		- When each commit is made git creates and SHA for it

## Config

### First time configuration

```bash
# sets up Git with your name
git config --global user.name "<Your-Full-Name>"

# sets up Git with your email
git config --global user.email "<your-email-address>"

# makes sure that Git output is colored
git config --global color.ui auto

# displays the original state in a conflict
git config --global merge.conflictstyle diff3

git config --list
```

### Sublime Text Setup (used when commiting a code)

```bash
git config --global core.editor "'c:/program files/sublime text 3/subl.exe' -w"
```

## Creating a repo

### Intializing git

```bash
git init
```

### Cloning a repo

```bash
git clone https://github.com/udacity/course-git-blog-project
git clone https://github.com/udacity/course-git-blog-project new-directory-name
git clone https://github.com/udacity/course-git-blog-project .
```

### Finding status of a current repository

```bash
git status
```

## Review a repo's history

### Loging repo's history

```bash
git log
git log fdf5493
git log index.html
```

- Where history of commits useful
	- Whats being stored in a commit
	- How to view it after the commit is made

- More specifically
	- Finding a certain commit by finding SHA
	- Finding a certain commit by finding Message
	- For finding date of the commit
	- Who made the commit

### Show log in one line

```bash
git log --oneline
```

### Show log with stats

- `--stat` used for showing statistics (what changed in a repo)

```bash
git log --stat
```

### Show changed files

- `-p` used to show patches (what changes being made)
- We can use `-p` and `--stat` with `git log`, `git show`, `git diff`

```bash
git log -p
```

- Where its useful
	- displays the files that have been modified
	- displays the location of the lines that have been added/removed
	- displays the actual changes that have been made

### Showing stat and patch

```bash
git log --stat -p
```

### Show details of one commit

```bash 
git log -p fdf5493
git show fdf5493
git show index.html
```

### Show one commit with stat

```bash
git show 8aa6668 --stat
```

## Add commit to a repo

### Add files to staging area

```bash
git add .
git add index.html
git add index.html css/style.css js/app.js
```

### Remove files from staging area

```bash
git rm --cached index.html 
```

### Commiting files

```bash
git commit (set up text editor for this) 
git commit -m "This is a message"
```

- Good Commit Messages
	- (do) be consistent
	- (do) keep the messages short (less than 60 chars)
	- (do) what commit does (not how or why)
	- (dont) explain why or how the commits being made (`git log -p` is for that)
	- (dont) the word `and` break it into multiple commits	

	- (only if you want) (why) Add description using `git commit` 

- Style guide: https://udacity.github.io/git-styleguide/

### Add all and commit (if only the file added to the git before)

```bash
git commit -am "Initial commit"
```

### Git diff

```bash
git diff
```

## Tagging, branching and merging

### Git Tag Command

```bash
git tag -a v1.0
```

### Verify tag

```bash
git tag
```

### Using git to show tags (decorate tag)

```bash
git log
git log --oneline --decorate
```

- `--decorate` is used to show tags
- `--decorate` is default no need to use it

### Deleting a tag

```bash
git tag -d v-10
```

### Adding a tag to a past commit

```bash
git tag v-10 fdf5493
```

### Create a new branch

```bash
git branch sidebar
```

### Checkout a branch

- Workflow
	- remove all files and directories from the Working Directory that Git is tracking
		- (files that Git tracks are stored in the repository, so nothing is lost)
	- go into the repository and pull out all of the files and directories of the commit that the branch points to

```bash
git checkout sidebar
```

### Branches in the log

```bash
git log --oneline --decorate
```

### Find the active branch

```bash
git branch
```

- Look for * before the branch name

### Create a branch and checkout the branch

```bash
git checkout -b sidebar
```

### Create a branch and checkout the branch from another branch or a commit

```bash
git checkout -b sidebar 42a69f
```

### Create a branch from SHA

```bash
git branch alt-sidebar-loc 42a69f
```

### Delete a branch

```bash
git branch -d sidebar
```

### Force delete a branch (without merge)

```bash
git branch -D sidebar
```

### See All Branches At Once

```bash
git log --decorate --oneline --graph --all
```

### Merge branches

- Workflow
	- look at the branches that it's going to merge
	- look back along the branch's history to find a single commit that both branches have in their commit history
	- combine the lines of code that were changed on the separate branches together
	- makes a commit to record the merge

```bash
git merge sidebar
```

## Undoing changes

### Modifying the last commit / Adding new files to the last ccmmit

```bash
git commit --amend
```

### Revert a commit

```bash
git revert 42a69f
```

### Reset a commit

```bash
git reset --hard HEAD^
git reset --soft HEAD^
git reset --mixed HEAD^
```