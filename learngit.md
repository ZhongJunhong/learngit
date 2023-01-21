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

Or add all changed files to `stage`.

```shell
$ git add .
```

Step3: All change added to `stage` need to be moved to `master` branch.

```shell
$ git commit -m "first commit"
```

**Commit comment could not be skip. It 's necessary to specify what have been changed in every commit time.**

Every commit is to specify a version of such repo. It 's the key for Git to achieve **version control**. 

And we will see the respon from Git

```shell
1 file changed, 2 insertions(+), 1 deletion(-)
```

