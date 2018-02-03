# Git

* [Introduction](#introduction)
* [Documentation and Resources](#documentation-and-resources)
* [Source Code Comments](#source-code-comments)
  * [Line Comment](#line-comment)
* [Git Commands](#git-commands)
  * [Init](#init)
  * [Status](#status)
  * [Add](#add)
  * [Commit](#commit)
  * [Log](#log)
  * [Remote](#remote)
  * [Push](#push)
  * [Pull](#pull)
  * [Diff](#diff)
  * [Reset](#reset)
  * [Checkout](#checkout)
  * [Branch](#branch)
  * [Merge](#merge)
  * [Remove](#remove)

## Introduction

Unlike some of the competition:

1. Git supports simple branching and merging
1. Git is small and fast
1. Git is distributed
1. Git ensures data quality and assurance
1. Git maintains a staging area
1. Git is free and open source

## Documentation and Resources

As we go into details of any programming tool, you'll find that documentation is your best friend for learning and improving your tool skill set:

* [Git Homepage](https://git-scm.com)
* [Git Docs](https://git-scm.com/doc)
* [GitHub Cheat Sheet for Git](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf)
* [SourceTree: Free Git GUI Client](https://www.sourcetreeapp.com)

## Source Code Comments

A comment is a programmer-readable explanation or annotation in the source code of a computer program. Anything within comments will be ignored by a compiler and are just there to help us programmers understand the code better.

You'll use comments for documentation and explanation of your code. Anytime you see comments, just know it's there for clarity.

### Line Comment

Also known as single-line comment, line comment syntax is prepended with `#`

```bash
# Example line comment
```

## Git Commands

### Init

The `init` command will initialize your git repository in the current or specified directory, or reinitialize an existing one:

```bash
# create a new repository
git init
```

### Status

The `status` command will show you the status for the working tree that you're currently in:

```bash
# log the current status
git status
```

### Add

The `add` command adds file contents to the index:

```bash
# add the file by name
git add filename.txt

# add all files within the directory
git add .

# adds every file with the file type: ".txt"
git add '*.txt'
```

### Commit

The `commit` command is used to commit your files to git with a given commit message:

```bash
# commit with the message: "Your Message"
git commit -m "Your Message"
```

### Log

The `log` command does just that; it will show the commit logs:

```bash
# log your commits
git log
```

### Remote

The `remote` command is used to add a remote repository, so that you may successfully push your code:

```bash
# git remote add <name> <url>
git remote add origin https://github.com/your-username/your-repo-name
```

### Push

The `push` command tells git that you're ready to push your local changes. Just tell git where to push:

```bash
# git push <remote-name> <branch-name> [-u: remember these parameters]
git push -u origin master

# If you have already used -u, you can just run `git push`
git push
```

### Pull

The `pull` command tells git that you're wanting to pull any remote changes into your local copy:

```bash
# git pull <remote-name> <branch-name>
git pull origin master

# If you have already used -u to set defaults, you can just run `git pull`
git pull
```

### Diff

The `diff` command allows you to view the differences between commits:

```bash
# `HEAD` will give us the most recent commit
git diff HEAD

# `--staged` will give you the changes you've staged
git diff --staged
```

### Reset

The `reset` command allows you to unstage files that you've staged:

```bash
# unstage file by name
git reset filename.txt

# unstage all staged files
git reset .

# unstage every file with the file type: ".txt"
git reset '*.txt'
```

### Checkout

The `checkout` command allows you to switch branches:

```bash
# Switch to `test-branch` from current branch
git checkout test-branch
```

The `checkout` command also allows you to restore working tree files:

```bash
# git checkout -- <target>
git checkout -- filename.txt
```

### Branch

The `branch` command allows you to list, create, and delete branches:

```bash
# lists branches
git branch

# create a branch with a given name
git branch branch-name

# delete a branch with a given name
git branch -d branch-name
```

### Merge

The `merge` command allows you to join two or more development histories together, such as a branch:

```bash
# merges other-branch into the current branch
git merge other-branch
```

### Remove

The `rm` command (short for remove) allows you to remove files from the working tree and from the index:

```bash
# removes the file by name
git rm filename.txt

# removes every file with the file type: ".txt"
git rm '*.txt'
```
