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

Initialize the Git repo, such repo (the work folder actually) is called `master` branch in Git.

When we change something in repo, the change will not be added to `master` directly, they should be moved to a place that we called `stage` in Git **for temporary**.

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

And we will see the respon from Git:

```shell
1 file changed, 2 insertions(+), 1 deletion(-)
```

## Check Git status

To check Git status by command:

Respond showed below mean something has been changed but not commit.

```shell
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   learngit.md

no changes added to commit (use "git add" and/or "git commit -a")
```

After `git add`:

```shell
$ git add .
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   learngit.md
```

After `git commit`:

```shell
$ git commit -m "test"
[master 78da7cf] test
 1 file changed, 9 insertions(+)
$ git status
On branch master
nothing to commit, working tree clean
```

## Connect to GitHub

Create local personal public and privace ssh key.

```shell
$ cd # Change to user home dir.
$ ssh-keygen -t rsa -C [GitHub login email address] # Generate personal public ssh key and private ssh key.
$ cd .ssh
$ ls
id_rsa id_rsa.pub # id_rsa stored the private ssh key that can not be share. The other is the public ssh key.
$ vim id_rsa.pub # open the public ssh key, and copy all content in it.
```

Add ssh key to GitHub account. Just turn on the personal account setting, and direct to ssh setting, create a new ssh key and name it what you like. Here 's no detail cause I need to protect my privacy.

**ssh key is used for GitHub to identify the permission of who commits to the repo.**

*More detail about differencies between privace and public ssh key please search on Google, this is really a good way instead of identification by username and password.*

Create a GitHub repo. Here I create a repo named learngit for example.

Connect to GitHub repo.

```shell
$ git remote add origin git@github.com:junhong/learngit.git
```