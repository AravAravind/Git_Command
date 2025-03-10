# Git Merge Command  

## Overview  
The `git merge` command is used to combine two branches into one. It integrates changes from a source branch into the current branch by creating a merge commit.  

## Usage  

### Merge a Branch into the Current Branch  

```sh
git merge <branch_name>
```  

Example:  

```sh
git checkout main
git merge feature-branch
```  

This merges `feature-branch` into `main`.  

### Merge Without Fast-Forward  

```sh
git merge --no-ff <branch_name>
```  

This creates a merge commit even if the history is linear, preserving the record of the merge.  

### Abort an Ongoing Merge  

```sh
git merge --abort
```  

This cancels the merge and restores the previous state.  

### Resolve Merge Conflicts  

If there are conflicts during a merge, Git will pause and show conflicted files. Follow these steps:  

1. **Check the status**  

   ```sh
   git status
   ```  

2. **Manually resolve conflicts in the listed files.**  

3. **Stage the resolved files**  

   ```sh
   git add <file_name>
   ```  

4. **Complete the merge**  

   ```sh
   git commit
   ```  

### Merge with a Specific Commit Message  

```sh
git merge -m "Merging feature-branch into main" feature-branch
```  

## Example  

### Fast-Forward Merge (Default Behavior)  

```sh
git checkout main
git merge feature-branch
```  

If `main` has no new commits, Git will move the branch pointer forward instead of creating a merge commit.  

### Merge with a Commit History  

```sh
git merge --no-ff feature-branch
```  

This ensures that the merge is recorded in the commit history.  

## Difference Between `git merge` and `git rebase`  

| Feature  | `git merge` | `git rebase` |
|----------|------------|--------------|
| Commit history | Retains original history with a merge commit | Creates a linear history |
| Conflict resolution | Happens once during the merge | Must be resolved at each commit |
| Used for | Preserving a clear history of merges | Keeping a clean, linear history |

## Conclusion  

The `git merge` command is useful for combining branches while preserving commit history. It is ideal for integrating completed features into the main branch in a structured way.  
