# Git Rebase Command  

## Overview  
The `git rebase` command is used to move or combine a series of commits to a new base commit. It is commonly used to maintain a clean and linear commit history by integrating changes from one branch into another without creating unnecessary merge commits.  

## Usage  

### Rebase the current branch onto another branch  

```sh
git rebase <base_branch>
```  

Example:  

```sh
git checkout feature-branch
git rebase main
```  

This moves the commits from `feature-branch` on top of `main`, making the history linear.  

### Interactive Rebase (Modify Commits)  

```sh
git rebase -i <commit_hash_or_branch>
```  

Example:  

```sh
git rebase -i HEAD~3
```  

This lets you modify the last 3 commits by choosing actions like `pick`, `squash`, `edit`, or `drop`.  

### Abort an Ongoing Rebase  

```sh
git rebase --abort
```  

This cancels the rebase and returns to the previous state.  

### Continue Rebase After Conflict Resolution  

```sh
git rebase --continue
```  

If there are conflicts during rebase, resolve them manually, stage the changes, and continue rebasing.  

### Skip a Conflicting Commit  

```sh
git rebase --skip
```  

This skips the current commit and moves to the next one.  

### Rebase with Autosquash (Automatically Squash Fixup Commits)  

```sh
git rebase --autosquash -i <base_branch>
```  

## Example  

### Basic Rebase  

```sh
git checkout feature-branch
git rebase main
```  

This re-applies `feature-branch` commits on top of `main`.  

### Interactive Rebase to Squash Commits  

```sh
git rebase -i HEAD~3
```  

Then, in the interactive editor, change:  

```
pick abc123 Commit message 1
pick def456 Commit message 2
pick ghi789 Commit message 3
```  

To:  

```
pick abc123 Commit message 1
squash def456 Commit message 2
squash ghi789 Commit message 3
```  

This combines the last 3 commits into one.  

## Difference Between `git rebase` and `git merge`  

- `git rebase` moves commits to a new base and creates a clean linear history.  
- `git merge` integrates changes with a merge commit, preserving the original branch structure.  

## Conclusion  

The `git rebase` command is useful for maintaining a clean commit history. However, **it should not be used on shared branches** to avoid conflicts. When working with public branches, consider using `git merge` instead.  
