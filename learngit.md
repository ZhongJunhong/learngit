# Learn How to Use Git

## Install Git on Linux(WSL)

I need to config the environment to tell the Git where to commit or push the data.

```shell
$ git config --global user.name junhong
$ git config --global user.email [My GitHub login in email]
```

## Initialize the Git repo

Create a folder and change dir to it.

```shell
$ mkdir learngit
$ cd learngit
```
Initialize such dir as Git repo.

```shell
$ git init
```
This operation will add a hidden file named ".git" to local dir.

```shell
$ ls -a
. .. .git learngit.md
```

## Git add & commit

To understand `git add` and `git commit` command, it' s necessary to specify the Git workflow:

Step1: Initialize the Git repo, such repo (the work folder actually) is called `master` branch in Git.

Step2: When we change something in repo, the change will not be added to `master` directly, they should be moved to a place that we called `stage` in Git **for temporary**.

Add a changed file to `stage`.

```shell
$ git add [filename]
```

Add all changed files to `stage`.

```shell
$ git add .
```
