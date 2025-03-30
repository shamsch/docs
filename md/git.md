# Move like Git Gods

Some common git commands I confuse. Don't expect `git add` or `git commit` here. By no means, it's exhaustive, but rather a reference for myself for `concepts` I have had to look up more than once.

## Merge
### FF Merge (Fast-Forward Merge)
- It is when the branch being merged has no new commits since the branch was created.
- No new commit is created; the branch pointer simply moves forward.

### 3-Way Merge
- Used when branches have diverged.
- Creates a new merge commit to combine changes.
- `merge commit`: A commit with two parent commits, representing the merged branches.
   - This commit usually does not have any changes itself, unless there are merge conflicts.
## Rebase
### Interactive Rebase
It allows you to modify your branch's commit. You can:

- `Pick`: Include the commit as-is.
- `Reword`: Edit the commit message.
- `Squash`: Combine multiple commits into one.
- `Drop`: Remove a commit from the history.

Command:
```bash
git rebase -i 
```

Not part of interactive rebase, but somewhat similar:
- `Amend`: Modify the most recent commit (message or changes).
- `Revert`: Undo a commit by creating a new commit.

```bash
git amend # Modify the last commit
git revert <commit-hash> # Undo a commit by creating a new commit
```

### Rebase with main
- Takes commits from the current branch that are not in `main` and starts putting them on top from the last commit in `main` within your current branch.
- Results in a linear history.

Command:
```bash
git rebase main
```

## Reset
- `soft`: Resets the HEAD but keeps changes staged.
- `mixed` (default): Resets the HEAD and unstages changes.
- `hard`: Resets the HEAD, unstages changes, and discards working directory changes.

Command:
```bash
git reset --<mode> <commit>
```

One common use case is undoing the last commit:
```bash
git reset --soft HEAD~1 # Undo the last commit but keep changes staged
# OR
git reset HEAD~1 # Undo the last commit and unstage changes
```
## Stash
- Temporarily shelves changes to switch branches or pull updates.

Commands:
- `git stash`: Stash changes.
- `git stash apply`: Reapply the most recent stash.
- `git stash pop`: Reapply the most recent stash and remove it from the stash list.
- `git stash list`: List all stashes.
- `git stash drop`: Remove a specific stash.
- `git stash clear`: Remove all stashes.
- `git stash branch <branch-name>`: Create a new branch from the stash.
- `git stash show`: Show the changes in the most recent stash.

## Cherry Pick
- Applies a specific commit from one branch to another.
- Can be used to selectively apply changes without merging the entire branch.

Command:
```bash
git cherry-pick <commit-hash>
```

## Other Common commands
- `git log --oneline --graph`: Compact, visual commit history.
- `git branch -d <branch-name>`: Delete a merged branch.
- `git checkout <branch-name>`: Switch branches.
- `git remote -v`: List remote repositories.
- `git pull <remote> <branch>`: Fetch and merge changes from a remote branch.
- `git push -f`: Force push changes to a remote repository. This will overwrite the remote branch with your local changes, so use with caution.
- `git push origin +<commit-hash>:<remote-branch>`: Brings the remote branch to the commit hash you specify. This is a force push, so be careful.
- `git rm -rf --cached .` and `git add .`: When `.gitignore` is not working, this command will remove all files from the index and re-add them, respecting the `.gitignore` file.