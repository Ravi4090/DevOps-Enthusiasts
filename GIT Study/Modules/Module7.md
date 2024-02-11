
# Module 7 : Understanding Branches

## Concept
Branching in Git allows you to diverge from the main line of development and continue working on features or bug fixes without affecting the main codebase. Each branch represents an independent line of development with its own commit history.

## Example
Suppose you're working on a project. You create a branch named `feature-branch` to add a new feature. While working on this branch, the `main` branch continues to receive other updates. You can switch between branches to work on different features concurrently.

# Creating and Deleting Branches

## Concept
Creating a branch in Git involves making a new line of development, which starts from the current commit. Deleting a branch removes the reference to that branch but doesn't remove the commits or changes.

## Examples

### Creating a Branch
```bash
git branch feature-branch
```
This creates a new branch named `feature-branch` but doesn't switch to it.

### Switching to the New Branch
```bash
git checkout feature-branch
```
Or, in a single command:
```bash
git checkout -b feature-branch
```
This creates and switches to `feature-branch`.

### Deleting a Branch
```bash
git branch -d feature-branch
```
Deletes the local branch.

```bash
git push origin --delete feature-branch
```
Deletes the remote branch.

# Merging Changes

## Concept
Merging combines changes from different branches, integrating them into a single branch. This is typically used to bring changes from a feature branch back into the main branch.

## Example

### Switch to the Target Branch
```bash
git checkout main
```

### Merge the Feature Branch
```bash
git merge feature-branch
```
This combines the changes made in `feature-branch` into `main`.

# Stashing Changes

## Concept
Stashing allows you to save changes without committing them. This is useful when you need to switch branches but don't want to commit incomplete work.

## Example

### Stash Changes
```bash
git stash save "Work in progress"
```
This saves your changes and reverts the working directory to the last commit.

### Apply Stash
```bash
git stash apply
```
Applies the last stash, bringing back your changes.

# Rebasing Commits

## Concept
Rebasing is a way to integrate changes from one branch into another by moving or combining commits. It provides a linear commit history.

## Example

### Switch to the Branch to be Rebased
```bash
git checkout feature-branch
```

### Rebase onto the Target Branch
```bash
git rebase main
```
Moves the changes from `feature-branch` onto `main`.

# Reverting Changes

## Concept
Reverting undoes a commit by creating a new commit that undoes the changes. This keeps a clean history but introduces a new commit.

## Example

### Identify the Commit to Revert
```bash
git log
```

### Revert the Commit
```bash
git revert <commit_hash>
```
Creates a new commit that undoes the changes made in the specified commit.

# Resetting Changes

## Concept
Resetting moves the branch pointer to a different commit, either discarding changes or preserving them in the working directory.

## Examples

### Soft Reset
```bash
git reset --soft HEAD~1
```
Preserves changes, moving the branch pointer to the specified commit.

### Hard Reset
```bash
git reset --hard HEAD~1
```
Discards changes, moving the branch pointer and working directory to the specified commit.

These granular explanations with real-time software development examples showcase how these Git operations are used in everyday scenarios.
