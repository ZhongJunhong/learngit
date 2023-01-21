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