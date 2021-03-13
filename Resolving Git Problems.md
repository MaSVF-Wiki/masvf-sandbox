(a page to start collecting how-to-fix tips.  not yet friendly enough for most people.)

## Pull failed error: Your local changes to the following files would be overwritten by merge

This happens when you have changed files on your computer and you do a pull.

### Strategies for fixing

1. Undo all local changes.
	1. command-line: `git checkout .`

2. Save ("stash") your changes to a temporary location.
	1. command-line:
		1. `git stash`
		2. `git pull`
		3. (deal with any merge conflicts)
		4. `git stash pull`
		5. (continue with your edits and/or do another pull+push)

3. Save your changes to a new branch.
	1. command-line:
		1. `git checkout -b pk-name-of-new-branch-20210313`
		2. `git switch main`
		3. `git pull`
		4. (deal with any merge conflicts)
		5. `git switch -`
		6. `git merge main`
		7. (continue working on your new branch; later, follow a strategy about merging branches back into main)