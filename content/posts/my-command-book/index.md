+++
date = '2022-09-01T00:00:00-00:00'
draft = false
title = 'MY COMMAND BOOK'
+++

### Git Clear Local Branches
Git Clear All Local Branches Except for Current Branche
```bash
git branch | grep -v "$(git symbolic-ref --short HEAD)" | xargs git branch -D && git tag -l | xargs git tag -d
```

<br>

### Git Fast-Forward Merge
```bash
git merge --no-ff feature-branch
```

<br>

### Windows Creating a Symbolic Link (Like ln -s) in PowerShell

**Syntax (PowerShell 5+ / Windows 10+)**
```powershell
New-Item -ItemType SymbolicLink -Path "C:\link\myshortcut" -Target "C:\original\myfolder"
```


**Example: Link a folder**
Suppose you want to create a symbolic link from:

**Target**: `C:\Projects\RealFolder`
**Link**: `C:\Links\ShortcutToProject`

```powershell
New-Item -ItemType SymbolicLink -Path "C:\Links\ShortcutToProject" -Target "C:\Projects\RealFolder"
```


<br>