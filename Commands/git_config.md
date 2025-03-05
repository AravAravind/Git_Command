# Git Config Command  

## Overview  
The `git config` command is used to configure Git settings at different levels: system-wide, user-specific, and repository-specific. It allows users to define preferences such as user identity, editor, default branch, and more.  

## Usage  

### Set User Identity  

#### Set Global Username  

```sh
git config --global user.name "Your Name"
```  

#### Set Global Email  

```sh
git config --global user.email "your.email@example.com"
```  

#### Set Username and Email for a Specific Repository  

```sh
git config user.name "Repo Specific Name"
git config user.email "repo.email@example.com"
```  

### Check Git Configuration  

```sh
git config --list
```  

To check system-wide configuration:  

```sh
git config --system --list
```  

To check global configuration:  

```sh
git config --global --list
```  

To check repository-specific configuration:  

```sh
git config --local --list
```  

### Configure Default Branch Name  

```sh
git config --global init.defaultBranch main
```  

### Set Default Text Editor  

#### Set Nano as the Default Editor  

```sh
git config --global core.editor "nano"
```  

#### Set VS Code as the Default Editor  

```sh
git config --global core.editor "code --wait"
```  

### Enable Color Output  

```sh
git config --global color.ui auto
```  

### Set up Credential Caching  

```sh
git config --global credential.helper cache
```  

### Configure Line Endings  

#### For Windows (Convert LF to CRLF)  

```sh
git config --global core.autocrlf true
```  

## Example  

### Setting User Identity  

```sh
git config --global user.name "John Doe"
git config --global user.email "john.doe@example.com"
```  

### Checking Configurations  

```sh
git config --list
```  

### Setting a Custom Default Branch  

```sh
git config --global init.defaultBranch main
```  

## Conclusion  

The `git config` command is essential for setting up Git preferences and ensuring consistency across repositories. Proper configuration helps streamline workflows and improve efficiency.  
