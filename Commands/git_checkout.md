# Git Checkout Command  

## Overview  
The `git checkout` command is used to switch between branches or restore files in a Git repository. It allows you to navigate to a different branch or reset files to a previous state.  

## Usage  

### Switch to an existing branch  

```sh
git checkout <branch_name>
```  

### Create and switch to a new branch  

```sh
git checkout -b <branch_name>
```  

### Restore a file to its last committed state  

```sh
git checkout -- <file_name>
```  

### Restore a file from a specific commit  

```sh
git checkout <commit_hash> -- <file_name>
```  

## Example  

### Switching to a Different Branch  

```sh
git checkout develop
```  

### Creating and Switching to a New Branch  

```sh
git checkout -b feature-branch
```  

### Restoring a Modified File  

If you made changes to `index.html` and want to discard them:  

```sh
git checkout -- index.html
```  

### Restoring a File from an Older Commit  

```sh
git checkout abc1234 -- style.css
```  

## Checking Out a Specific Commit  

If you want to temporarily switch to a past commit (detached HEAD state):  

```sh
git checkout abc1234
```  

To return to the latest commit:  

```sh
git checkout main
```  

## Conclusion  

The `git checkout` command is useful for switching branches and restoring files to previous states. However, it has been partially replaced by `git switch` (for branch switching) and `git restore` (for file restoration) in newer Git versions.  
