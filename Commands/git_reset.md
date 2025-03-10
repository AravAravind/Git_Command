# Git Reset Command  

## Overview  
The `git reset` command is used to undo changes by moving the HEAD pointer to a previous commit. It can modify the staging area and working directory depending on the reset mode used.  

## Usage  

To reset to a previous commit while keeping changes staged:  

```sh
git reset --soft <commit_hash>
```  

To reset to a previous commit and unstage changes:  

```sh
git reset --mixed <commit_hash>
```  

To reset to a previous commit and discard changes permanently:  

```sh
git reset --hard <commit_hash>
```  

To reset only a specific file:  

```sh
git reset <file_name>
```  

## Example  

### Resetting to a Previous Commit  

Find the commit hash using:  

```sh
git log --oneline
```  

Then reset:  

```sh
git reset --soft abc1234
```  

This moves HEAD to `abc1234` but keeps the changes staged.  

### Resetting and Unstaging Changes  

```sh
git reset --mixed HEAD~1
```  

This moves HEAD back one commit and unstages the changes.  

### Resetting and Deleting Changes  

```sh
git reset --hard HEAD~2
```  

This removes the last two commits and deletes all changes permanently.  

### Resetting a Specific File  

```sh
git reset HEAD file.txt
```  

This unstages `file.txt` but keeps the changes in the working directory.  

## Caution When Using `--hard`  

The `--hard` option permanently deletes changes and cannot be undone unless you have a backup or reference to the lost commits (e.g., `git reflog`).  

## Conclusion  

The `git reset` command is a powerful tool for undoing changes at different levels, from unstaging files to permanently discarding commits.  
