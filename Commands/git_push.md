# Git Push Command  

## Overview  
The `git push` command uploads local commits to a remote repository. It allows team members to share updates and collaborate effectively.  

## Usage  

### Push changes to the remote repository  

```sh
git push
```  

### Push changes to a specific branch  

```sh
git push origin <branch_name>
```  

### Push and set upstream (track the remote branch)  

```sh
git push --set-upstream origin <branch_name>
```  

or  

```sh
git push -u origin <branch_name>
```  

### Force push (overwrite remote changes with local changes)  

```sh
git push --force
```  

⚠ **Warning:** Use `--force` carefully, as it can overwrite commits and cause data loss.  

### Push all branches  

```sh
git push --all origin
```  

### Push tags  

```sh
git push --tags
```  

### Delete a remote branch  

```sh
git push origin --delete <branch_name>
```  

## Example  

### Pushing Changes to the Main Branch  

```sh
git push origin main
```  

### Pushing a New Branch and Setting Upstream  

```sh
git push -u origin feature-branch
```  

This command pushes the `feature-branch` to the remote repository and sets it as the upstream branch.  

### Force Pushing After Rewriting History  

```sh
git push --force
```  

⚠ **Use this with caution, as it overwrites remote history.**  

## Common Issues  

### 1. **Error: "fatal: The current branch has no upstream branch"**  

If you see this error, set the upstream branch using:  

```sh
git push --set-upstream origin <branch_name>
```  

### 2. **Rejected Push Due to Non-Fast-Forward**  

If your push is rejected, pull the latest changes first:  

```sh
git pull --rebase origin <branch_name>
git push origin <branch_name>
```  

## Conclusion  

The `git push` command is essential for sharing work with a remote repository. It allows users to keep remote branches updated and collaborate efficiently.  
