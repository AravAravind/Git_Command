# Git Fetch Command  

## Overview  
The `git fetch` command retrieves updates from a remote repository without merging them into your local branch. It allows you to check for changes before integrating them.  

## Usage  

### Fetch updates from the remote repository  

```sh
git fetch
```  

### Fetch updates from a specific remote branch  

```sh
git fetch origin <branch_name>
```  

### Fetch all branches from the remote repository  

```sh
git fetch --all
```  

### Fetch and prune deleted remote branches  

```sh
git fetch --prune
```  

### Fetch without updating remote tracking references  

```sh
git fetch --no-tags
```  

## Example  

### Basic Fetch  

```sh
git fetch origin
```  

This retrieves changes from the remote repository but does not merge them.  

### Checking for New Changes  

After fetching, you can check for updates using:  

```sh
git log origin/main --oneline
```  

### Fetching and Cleaning Up Deleted Remote Branches  

```sh
git fetch --prune
```  

This removes references to deleted remote branches.  

### Applying Fetched Changes  

To merge the fetched changes into your local branch:  

```sh
git merge origin/main
```  

To rebase instead of merging:  

```sh
git rebase origin/main
```  

## Difference Between `git fetch` and `git pull`  

- `git fetch` only downloads updates without merging them.  
- `git pull` fetches updates and merges them into the current branch.  

## Conclusion  

The `git fetch` command is useful for checking remote updates before merging them, allowing for better control over the integration process.  
