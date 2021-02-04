# Git and GitHub

### Commands
- `git show` - check what has been committed, `:q` to quit
- `git diff <filename>` - see what lines have been added, `:q` to quit
- `git log` - history of changes
- `git stash` - removes all code since the last commit
- `git stash pop` - reapplies the last changes that were stashed (if there are multiple stashes, it applies just the last one in the list)
- `git stash save "message here"`to make the stash easier to find later
- `git stash list` - shows all the stashed code, has a number next to the name
- `git stash apply <stash num>` - adds the stashed code associated with that number
- `git show head` - shows the current current commit you are on, with the id number, the commit message, the changes made to the code
- `git config --global user.name "gracehopper"`
- `git config --global user.email gracehopper@example.com`

Check to see if the username and email were set
- `git config --global user.name`
- `git config --global user.email`

### Terminology
`HEAD` - the current commit you are on


### Add Existing Code to a Repo
If you have code on your local machine and you have been making commits
- Create a repo
- Copy the lines from the section `...or push an existing repository from the command line` and paste in terminal
  -  `git remote add origin` - adding a remote connection like GitHub to your repository, 'origin' is the name of the remote, this line only needs to be run once and it is set up for the lifetime of your project
  - `git push -u origin master`


### README
- Text (or mark down) file that sits in the root of your project and explains the project
- It generally talks through the tech on your project, how to get it up and running, general domaine knowledge (If your project needed to be handed off to someone what knowledge transfer would need to happen)
- Never include username, passwords, API keys


### Workflow with Git
- Local environment (your computer)
  - Working directory - all the files in a project
  - Once you are ready to commit, you 'stage' those files and write a message explaining what you did
  - When you commit the files, they are saved to your local repository
- Remote environment
  - You push the file to an online repository (GitHub)

### Fixing Bad Commits
There are several places you can fix a bad commit depending on where you are in the process
**Before you stage your files** - if you have made so many changes it is beyond a 'command-z' fix
- `git status` - what files have been changed
- `git diff <filename>` - what specific changes have been made to the file

To fix:
1) Discard all local changes, but save for re-use later
`git stash`
2) Permanently discard all changes to **one** local file
`git checkout HEAD <filename>` or `git checkout -- <filename>` this takes your code back to the way it was at your last commit
3) Permanently discard all changes to **all** local files
`git reset --hard` removes all code that is not commited

**Unstage a file you haven't committed** - if a file was added but not committed

To fix:
1) `git reset HEAD <filename>` or `git reset` to reset all files
2) The files hasn't changed in the text editor, but the changes are no longer staged
3) Can stash changes or remove permanently with `git reset --hard`

**Committed changes locally but haven't pushed them** - a file was committed but not pushed to GitHub

To fix:
1) Without modifying history - can revert to a specific commit by id, look at the log `git log` to see the commit id (a very long string of numbers, but we only need the first 7 characters) `git revert <commit-id>` `git revert <commit-id> <filename>`
2) Modifying history - drop a commit, `git log` to get the


### Branching
Creating a branch will protect your main branch from code that is in process and allows many people to work on the code base at the same time
1) Checkout a branch `git checkout -b <branch-name>`
2) Editing the name of a branch you are currently on `git branch -m <new-branch-name>`
3) Editing the name of a branch you are not currently on `git branch -m <old-branch-name> <new-branch-name>` (the -m is like "move")

### Merge
To merge code from the command line:
1) Add/commit code or add/commit/push to branch
2) Checkout default branch
3) Merge in the command line `git merge <branch-name>`
4) Delete branch

Check to see which branches have not been merged `git branch --no-merged`
Check to see which branches have been merged `git branch --merged`

### Multiple Branches
Situation: There is a branch that is waiting for approval, but need to start on a new feature.
1) Go back to the default branch and create a new branch, the code on the other branch will not be there
2) Create code, it will not matter which branch gets merged first


### Merge Conflicts
Git generally does a good job of merging our code automatically, but every once in a while there is an issue that git doesn't know how to handle. Usually happens when two people change the same line of code, git doesn't know how to handle that issues so it will flag that line as having a conflict. Before you can make any more changes you have to resolve that issue, but the issues only exists on your machine.


Situation: Two branches change the same line of code
- Merge first branch, no problems
- Merge second branch, merge conflict
- To go back to the way things were: `git merge --abort`
- Open text editor to see changes, remove git notations
- Pick changes to be made manually
- Add and commit changes
