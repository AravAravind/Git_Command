# Git Stash Command  

## Overview  
The `git stash` command temporarily saves changes that are not yet committed, allowing you to switch branches or work on something else without losing your progress. Stashed changes can be reapplied later.  

## Usage  

### Save uncommitted changes  

```sh
git stash
```  
![1](../Images/Git_stash/1.png)

### Save changes with a custom message  

```sh
git stash push -m "Work in progress on feature X"
```
![2](../Images/Git_stash/2.png)  

### List all stashes  

```sh
git stash list
```  
![3](../Images/Git_stash/3.png)

### Apply the most recent stash  

```sh
git stash apply
``` 
![4](../Images/Git_stash/4.png) 

### Apply a specific stash  

```sh
git stash apply stash@{n}
```  
![9](../Images/Git_stash/9.png)

### Apply and remove the most recent stash  

```sh
git stash pop
```  
![5](../Images/Git_stash/5.png)

### Apply and remove a specific stash  

```sh
git stash pop stash@{n}
```  
![6](../Images/Git_stash/6.png)

### Remove a specific stash  

```sh
git stash drop stash@{n}
```  
![7](../Images/Git_stash/7.png)

### Remove all stashes  

```sh
git stash clear
```  
![10](../Images/Git_stash/10.png)

## Example  

### Stashing Changes  

```sh
git stash
```  

### Switching Branches Without Losing Work  

```sh
git stash
git switch main
```  

### Applying the Last Stash  

```sh
git stash apply
```  

### Applying and Removing a Stash  

```sh
git stash pop
```  

### Viewing Stashed Changes  

```sh
git stash show -p stash@{0}
```  
![8](../Images/Git_stash/8.png)

## Conclusion  

The `git stash` command is useful for temporarily setting aside work, switching contexts, and resuming progress without committing incomplete changes.  
