Working with Git
=================
## Git Basic Commands

To clone a project

  ```git clone git@github.com:<projectname>.git```

**Note:** Project url can be obtained from https://github.com/<projectname>

Create a new feature branch  

  ```git branch feature-login```

Switch to the new branch

  ```git checkout feature-login```

Do the necessary changes on the files, add the files

  ```git add -A```

Commit the changes

  ```git commit -m "Implemented the login feature"```

Pull the changes from the server ( not applicable for the first push )

  ```git pull origin feature-login```

Push the changes to server for the first time

  ```git push origin feature-login```

Once the feature is complete, merge the changes to the develop branch ( the team lead does this )

  ```git checkout develop```

  ```git merge feature-login```

Make sure you pull the changes from the required repo and keep your branch updated. 

![Screen-shot-2009-12-24-at-11.32.03](http://<projectname>/branch/code-review-guide/uploads/cf9608832446cedbe82c107fe33eec3f/Screen-shot-2009-12-24-at-11.32.03.png)

The central repository holds two main branches with an infinite lifetime:
  - master
  - develop

origin/master is the main branch where the source code of HEAD always reflects a production-ready state.
origin/develop is the main branch where the source code of HEAD always reflects a state with the latest delivered development changes for the next release

## Supporting branches
  - Feature branches
  - Release branches
  - Hotfix branches

## Feature Branch
  - May branch off from: ```develop```
  - Must merge back into: ```develop```
  - Branch naming convention: anything except ```master```, ```develop```, ```release-*```, or ```hotfix-*```
  - Branches should be prefixed with ```feature-```
  - They should be in small letter casing with multiple words separated by ```-```

Eg: feature-signup, feature-taskid123
## Bugfix Branch
  - May branch off from: ```develop```
  - Must merge back into: ```develop```
  - Branch naming convention: ```bugfix-*```
  - Branches should be prefixed with ```bugfix-*```
  - They should be in small letter casing with multiple words separated by ```-```

## Release Branch
  - May branch off from: ```develop```
  - Must merge back into: ```develop```
  - Branch naming convention: anything except ```master```, ```develop```, ```release-*```, or ```hotfix-*```
  - Branches should be prefixed with ```release-*```
  - They should be in small letter casing with multiple words separated by ```-```

Eg: release-v1.1

## Hotfix Branch
  - May branch off from: ```master```
  - Must merge back into: ```develop``` and ```master```
  - Branch naming convention: ```hotfix-*```
  - Branches should be prefixed with ```hotfix-*```
  - They should be in small letter casing with multiple words separated by ```-```

Eg: hotfix-signup-failure, hotfix-taskid123

## Simultaneous Multiple Versions

If your project has multiple versions which are live simultaneously, you would need multiple master and develop branches for them .

For example, If your project has a lite and a standard version. Suppose the light version has reduced feature set than the standard version. In that case, you would need to create two master branches and two develop branches individually for them
- master-lite
- master-standard
- develop-lite
- develop-standard



## Further References
  - http://www.gitimmerssion.com
  - http://git-scm.com/

## Basic Git Commands

## Why Git?
Git is a distributed version-control system for tracking changes in source code during software development.
It is designed for coordinating work among programmers, but it can be used to track changes — in any set of files.
Its goals include speed, data integrity, and support for distributed, non-linear workflows.

  No	Git commands	Description
 * 1	git config — global user.name “name”	  Configure user name globally
 * 2	git config — global user.email “email id”	  Configure user email id * globally
 * 3	git config — global — list	  List global user
 * 4	git config — global — help.autocorrect 1	Autocorrect the spelling mistake in git command
 * 5	git config —unset option	Remove from git config
 * 6	git add	Adds a file to the staging area
 * 7	git commit -m “”	Records the file permanently in the version history
 * 8	git status	Lists all the files that have to be committed
 * 9	git log	List the version history for the current branch.
 * 10	git diff	Shows the file differences which are not yet staged
 * 11	git diff [first branch] [second branch]	Differences between the two branches mentioned
 * 12	git reset [file]	Unstages the file, but it preserves the file contents
 * 13	git reset –hard [commit]	Discards all history and goes back to the specified commit
 * 14	git rm [file]	Deletes the file from your working directory and stages the deletion
 * 15	git show [commit]	Shows the metadata and content changes of the specified commit
 * 16	git branch	Lists all the local branches in the current repository
 * 17	git branch [branch name]	Creates a new branch
 * 18	git branch -d [branch name]	Deletes the feature branch
 * 19	git checkout [branch name]	Switch from one branch to another
 * 20	git checkout -b [branch name]	Creates a new branch and also switches to it
 * 21	git merge [branch name]	Merges the specified branch’s history into the current branch
 * 22	git branch -r	Show remove branches
 * 23	git push [variable name] master	Sends the committed changes of master branch to your remote repository
 * 24	git push [variable name] :[branch name]	Deletes a branch on your remote repository
 * 25	git pull [Repository Link]	Fetches and merges changes on the remote server to your working directory
 * 26	git stash save	Temporarily stores all the modified tracked files
 * 27	git stash pop	Restores the most recently stashed files
 * 28	git stash list	Lists all stashed changesets
 * 29	git stash drop	Discards the most recently stashed changeset
 * 30	git stash	Takes your uncommitted changes and saves them away for later use
 * 31	git stash show	View a summary of a stash
 * 32	git clean -f	Clean untracked files
 * 33	git clean -f -d	Remove directories
 * 34	git clean -f -X	Remove ignored files
 * 35	git clean -f -x	Remove ignored as well as non-ignored files
 * 36	git clone [url]	Download all the history of the project
 * 37	git log —online | wc -1	Total commit count
 * 38	git shortlog	Log history with author details also show number of commits for each of them
 * 39	git fetch	Download contents from a remote repository
 * 40	git rebase	Feature branch on to master
 * 41	git merge	Merging adds a new commit to your history
 * 42	git cherry-pick commit-name	Picking a commit from a branch and applying it to another
