- git
	- configuring git

	- creating a repo / cloning a repo
	- checking status of a repo
	- review a repos history (patches, stats)

	- Good commit messages
	- Viewing modifications
	- Ignoring files (using gitignore)

	- Tagging a commit
	- Branching a commit
	- Merging a commit (including fixing merge conflict)

	- Modifying the last commit
	- Reverting a commit
	- Resetting commits

## Main index

- What is version control
	- Two type of version control
	- Version control in daily use
	- Git and version control terminology
	- Mac/Linux configuration
	- Windows setup
	- First time git configuration
	- Sublime text setup
- Creating a git repo
	- Creating a repo from start
	- `.git` directory contents
	- Clone an existing repo
	- Determining a repo's status
- Review a repo's history
	- Display a repo's commits
	- Changing how git log display information
	- Viewing modified files
	- Viewing file changes
	- Viewing a specific commit
- Add commit to a repo
	- Staging files for commit
	- Moving into repository
	- Commit messages
	- Git diff
	- having a .gitignore file
- Tagging, Branching, and Merging
	- Tagging
	- Branching
	- Branching effectively
	- Merging
	- Merge conflict
- Undoing changes
	- Modifying the last commit
	- Reverting a commit
	- Resetting commits


- http://try.github.io/
- https://www.atlassian.com/git/tutorials

- What is version control
	- There are two main types of version control system
		- The centralized model
		- The distributed model
	- Version control in daily use
		- `ctrl+z`
		- Google docs revision control
	- Git and Version Control Terminology
	    - Version Control System / Source Code Manager
	    - Commit
	    - Repository / repo
	    - Working Directory
	    - Checkout
	    - Staging Area / Staging Index / Index
	    - SHA
	    - Branch
	- Mac/Linux configuration
	- Windows setup
	- First time git configuration
	- Sublime Text Setup

	- http://blogs.atlassian.com/2012/02/version-control-centralized-dvcs/
	- https://en.wikipedia.org/wiki/Distributed_version_control

- Creating a git repo
	- Create a repo from scratch
		- Create course directries
		- Git init
		- Git inits effect
		- .git directory contents
			- config file
			- description file
			- hooks directory
			- objects directory
			- refs directory
		- Further research
		- Git init recap

		- https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository#Initializing-a-Repository-in-an-Existing-Directory
		- https://git-scm.com/docs/git-init
		- https://www.atlassian.com/git/tutorials/setting-up-a-repository
	- Clone an existing repo
		- Why clone?
		- Git Clone Output Explanation
		- Clone Project And Use Different Name

		- https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository#Cloning-an-Existing-Repository
		- https://git-scm.com/docs/git-clone
		- https://www.atlassian.com/git/tutorials/setting-up-a-repository
	- Determining a repo's status
		- Git Status Output
		- Git Status Explanation
		- Explanation Of Git Status In A New Repo

		- https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#Checking-the-Status-of-Your-Files
		- https://git-scm.com/docs/git-status
		- https://www.atlassian.com/git/tutorials/inspecting-a-repository/git-status

- Review a repo's history
	- Display a repo's commits
		- Git Status & Opening The Project
		- The Git Log Command
		- Git show command
		- Navigating The Log
		- Git Log Recap
	- Changing How Git Log Displays Information
		- One line log
	- Viewing Modified Files
		- `git log --stat` Intro
		- `git log --stat` Recap
			- displays the file(s) that have been modified
			- displays the number of lines that have been added/removed
			- displays a summary line with the total number of modified files and lines that have been added/removed
	- Viewing File Changes
		- Viewing Changes
		- `git log -p`
		- Annotated `git log -p` Output
		- `git log --stat -p` Output
	- Viewing A Specific Commit
		- Too much scrolling
			- providing the SHA of the commit you want to see to `git log`
			- use a new command `git show`

	- https://www.thegeekstuff.com/2014/04/git-log/

- Add commit to a repo
	- Git add (staging files for commit)
		- Removing files from staging area
	- Git commit (Moving into the repository)
		- Code Editor Commit Message Explanation
		- Bypass The Editor With The `-m` Flag
		- `What to include in a commit`
			- Each commit should make a change to just one aspect of the project.
			- A commit shouldn't include unrelated changes

		- https://help.github.com/articles/associating-text-editors-with-git/
		- https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup
	- Commit messages
		- Good Commit Messages
		- Explain the Why
			- (only if you want) Add description using `git commit` 

		- https://udacity.github.io/git-styleguide/
	- Git diff
		- Why Do We Need This

		- https://git-scm.com/docs/git-diff
	- Having a git ignore files

		- https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#Ignoring-Files
		- https://git-scm.com/docs/gitignore#_pattern_format
		- https://help.github.com/articles/ignoring-files/
		- https://www.gitignore.io/

- Tagging, Branching, and Merging
	- Tagging
		- Git Tag Command (annotated flag)
		- Verify Tag
		- Using git log to show tags (decorate tag)
		- Deleting A Tag
		- Adding A Tag To A Past Commit

		- https://git-scm.com/book/en/v2/Git-Basics-Tagging
		- https://git-scm.com/docs/git-tag
	- Branching
		- The `git branch` command
			- List all branches in a repository
			- Create a new branch
			- Delete branch
		- The `git checkout command`
			- How it works
		- Branches in the log
		- The Active Branch
		- Delete a branch
		- Force delete a branch

		- https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging
		- http://learngitbranching.js.org/
		- https://www.atlassian.com/git/tutorials/using-branches
	- Branching effectively
		- Create a branch from another commit
		- Create a branch from another branch
		- Create and checkout branch on one command
		- Create and checkout branch on one command from another commit or branch
		- See all branches at once
	- Merging
		- The merge command
		- Fast forward merge
		- Perform A Regular Merge
		- Two types of merge
			- Fast forward merge
			- The regular type of merge

		- https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging#Basic-Merging
		- https://git-scm.com/docs/git-merge
		- https://www.atlassian.com/git/tutorials/git-merge
	- Merge conflict
		- Sometimes Merges Fail
		- What Causes A Merge Conflict
		- Forcing A Merge Conflict!
		- Merge Conflict Output Explained
		- Merge Conflict Indicators Explanation
		- Commit Merge Conflict

		- https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging#Basic-Merge-Conflicts
		- https://git-scm.com/docs/git-merge#_how_conflicts_are_presented

- Undoing changes
	- Modifying the last commit
		- Changing The Last Commit
			- `git commit --amend`
		- Add Forgotten Files To Commit
			- Edit and save the files
			- Stage the files
			- run `git commit --amend`
	- Reverting a commit
		- What Is A Revert?
		- https://git-scm.com/docs/git-revert
		- https://www.atlassian.com/git/tutorials/undoing-changes
	- Resetting commits
		- Reset vs Revert
		- Relative Commit References
			- `^` - Indicate the parent commit (when merging there are two parents so `^1` (the branch you ran the merge), `^2`)
			- `~` - Indicate the first parent commit `~1`, `~2`, `~n`
		- Reset commits
			- https://git-scm.com/docs/git-reset
			- https://git-scm.com/book/en/v2/Git-Tools-Reset-Demystified
			- https://git-scm.com/book/en/v2/Git-Tools-Revision-Selection#Ancestry-References
		- Git Reset's Flags
			- `--mixed`: Move into the workign directory
			- `--soft`: move into the staging area
			- `--hard`: move into the trash
		- Backup Branch
			- Create a backup branch before reset
			- If you need it back just merge it into the parent