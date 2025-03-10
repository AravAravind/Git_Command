# Git Pull Command  

## Overview  
The `git pull` command fetches changes from a remote repository and merges them into the current branch. It is a combination of `git fetch` (to retrieve updates) and `git merge` (to integrate them).  

## Usage  

### Pull changes from the remote repository  

```sh
git pull
```  

### Pull changes from a specific branch  

```sh
git pull origin <branch_name>
```  

### Pull without merging (fetch only)  

```sh
git pull --no-commit
```  

### Pull with rebase instead of merge  

```sh
git pull --rebase
```  

### Pull changes and override local changes (use with caution)  

```sh
git fetch origin
git reset --hard origin/<branch_name>
```  

## Example  

### Basic Pull  

```sh
git pull origin main
```  

This fetches and merges the latest changes from the `main` branch.  

### Pulling with Rebase  

```sh
git pull --rebase origin develop
```  

This applies remote changes on top of local commits, avoiding unnecessary merge commits.  

### Handling Merge Conflicts  

If there are conflicts during `git pull`, resolve them manually, then commit the changes:  

```sh
git add <conflicted_files>
git commit -m "Resolved merge conflicts"
```  

## Conclusion  

The `git pull` command is essential for keeping your local repository up to date with remote changes. Using `--rebase` can help maintain a cleaner commit history.  
