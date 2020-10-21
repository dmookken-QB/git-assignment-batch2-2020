# GIT Commands
##### Basic GIT Commands
* git config
* git init
* git clone
* git add
* git commit
* git diff
* git reset
* git status

Working with **Git** on the command line can be daunting. To help with that, we’ve put together a list of common Git commands, what each one means, and how to use them. Our hope is that this makes Git easier to use on a daily basis.

![Image of Yaktocat](https://miro.medium.com/max/700/1*y7D5jICmjzvxZP6z-5EtDg.png)

## Working with local repositories
#### git init
This command turns a directory into an empty Git repository. This is the first step in creating a repository. After running git init, adding and committing files/directories is possible.
Usage:
```sh
# change directory to codebase
$ cd /file/path/to/code

# make directory a git repository
$ git init
```

#### git add
Adds files in the to the staging area for Git. Before a file is available to commit to a repository, the file needs to be added to the Git index (staging area). There are a few different ways to use git add, by adding entire directories, specific files, or all unstaged files.
Usage:
```sh
# To add all files not staged:
$ git add .

# To stage a specific file:
$ git add index.html

# To stage an entire directory:
$ git add css
```
#### git commit
Record the changes made to the files to a local repository. For easy reference, each commit has a unique ID.

It’s best practice to include a message with each commit explaining the changes made in a commit. Adding a commit message helps to find a particular change or understanding the changes.
Usage:
```sh
$ git commit -m "My first commit message"
[SecretTesting 0254c3d] My first commit message
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 homepage/index.html
```
#### git status
This command returns the current state of the repository.

git status will return the current working branch. If a file is in the staging area, but not committed, it shows with git status. Or, if there are no changes it’ll return nothing to commit, working directory clean.
Usage:
```sh
# Message when files have not been staged (git add)
$ git status
On branch SecretTesting
Untracked files:
  (use "git add <file>..." to include in what will be committed)

  	homepage/index.html

# Message when files have been not been committed (git commit)
$ git status
On branch SecretTesting
Your branch is up-to-date with 'origin/SecretTesting'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   homepage/index.html

# Message when all files have been staged and committed 
$ git status
On branch SecretTesting
nothing to commit, working directory clean
```

#### git config

With Git, there are many configurations and settings possible. git config is how to assign these settings. Two important settings are user user.name and user.email. These values set what email address and name commits will be from on a local computer. With git config, a --global flag is used to write the settings to all repositories on a computer. Without a --global flag settings will only apply to the current repository that you are currently in.

There are many other variables available to edit in git config. From editing color outputs to changing the behavior of git status. Learn about git config settings in the official [Git documentation](https://git-scm.com/docs/git-config).

Usage:

```sh
# Running git config globally
$ git config --global user.email "my@emailaddress.com"
$ git config --global user.name "Brian Kerr"

# Running git config on the current repository settings
$ git config user.email "my@emailaddress.com"
$ git config user.name "Brian Kerr"
```

#### git branch

To determine what branch the local repository is on, add a new branch, or delete a branch.

Usage:

```sh
# Create a new branch
$ git branch new_feature

# List branches
$ git branch -a
* SecretTesting
  new_feature
  remotes/origin/stable
  remotes/origin/staging
  remotes/origin/master -> origin/SecretTesting
  
# Delete a branch
$ git branch -d new_feature
Deleted branch new_feature (was 0254c3d).
```

#### git checkout

To start working in a different branch, use git checkout to switch branches.

Usage:

```sh
# Switching to branch 'new_feature'
$ git checkout new_feature
Switched to branch 'new_feature'

# Creating and switching to branch 'staging'
$ git checkout -b staging
Switched to a new branch 'staging'
```

# Summary  

| Command | Description |
| ------ | ------ |
| git config | Turns a directory into an empty Git repository.] |
| git add | Adds files in the to the staging area |
| git commit | Record the changes made to the files to a local repository. |
| git status | Returns the current state of the repository. |
| git config | Assign the config detail. Two important settings are user user.name and user.email. |
| git branch | Determine what branch the local repository is on |
| git checkout | To start working in a different branch, use git checkout to switch branches. |


