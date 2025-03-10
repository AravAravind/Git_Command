# Git Revert Command  

## Overview  
The `git revert` command is used to undo a specific commit by creating a new commit that reverses the changes. Unlike `git reset`, it does not alter the commit history, making it a safer way to undo changes in a shared repository.  

## Usage  

To revert a specific commit:  

```sh
git revert <commit_hash>
```  

To revert the last commit:  

```sh
git revert HEAD
```  

To revert multiple commits:  

```sh
git revert HEAD~2..HEAD
```  

To revert a commit without opening the default editor for a commit message:  

```sh
git revert --no-edit <commit_hash>
```  

## Example  

### Reverting a Specific Commit  

Find the commit hash using:  

```sh
git log --oneline
```  

Then revert it:  

```sh
git revert abc1234
```  

This creates a new commit that negates the changes made by commit `abc1234`.  

### Reverting the Last Commit  

```sh
git revert HEAD
```  

### Reverting Multiple Commits  

To undo the last two commits:  

```sh
git revert HEAD~1 HEAD
```  

## Handling Merge Conflicts  

If reverting causes conflicts, Git will prompt you to resolve them manually before completing the revert. After resolving conflicts, run:  

```sh
git revert --continue
```  

To abort the revert process:  

```sh
git revert --abort
```  

## Conclusion  

The `git revert` command is a safe way to undo specific commits without rewriting history, making it ideal for collaborative projects.  
