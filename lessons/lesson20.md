## Lesson 20 - Git and GitHub

GitHub is a code-hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere. At the heart of GitHub is an open-source version control system (VCS) called Git. Git is responsible for everything GitHub-related that happens locally on your computer.

### Understanding the GitHub Flow

GitHub Guides: https://guides.github.com/introduction/flow/

Steps in the GitHub flow:

1. Create a **Branch** -- A branch is a copy of your project where you can try out new features and ideas. Changes won't be merged with the master branch until you are ready and someone else reviews your code. Give your branch a descriptive name.
2. Add **Commits** -- Commits are small milestones that you make after you have added, deleted, or edited files. Every time you make a commit, you provide a short message describing what you have done in that commit, so others can follow your work history. Each commit is a separate unit of change, which can be rolled back if you make a mistake, so they allow for precise version control.
3. Open a **Pull Request** -- A pull request is a request to your collaborators to "pull" your branch into the master branch. It notifies your team that you're making commits to a repository and starts a discussion about your commits. A pull request can be issued at any stage of your edits.
4. Discuss and **Review** your code -- In collaborative projects, after you issue a pull request, one or more people on the project will review your code and offer comments or questions. For example, maybe your code does pass PEP 8 standards or unit tests, or maybe thre's a bug. You have a chance to make additional edits (commits) to your code to improve it until the reviewer is satisfied. Comments are written in Markdown and also support mentions to issues, e.g., "This addresses issue #45".
5. **Deploy** -- If applicable, you can deploy from your branch to test in production, before merging it to master.
6. **Merge** -- Now that your changes have been verified in production, you can merge your code into the master branch. If you fixed an issue, you can close the issue with, e.g., "Closes #45". Then you can delete your branch. Merged Pull Requests are searchable and preserve a record of the historical changes to your code.

Other GitHub terms:

* **Repository** -- A repository, or Git project, encompasses the entire collection of files and folders associated with a project, along with each file’s revision history.
* **Clone** -- A clone is a local copy of a project that already exists remotely. The clone includes all the project’s files, history, and branches.
* **Issues** -- Issues are tasks in the project that need work. Issues start as "Open", and when they are resolved they are changed to "Closed". The author of an issue can assign someone to that issue. Issues support labels, and the text of issues can have "#" mentions to other issues (e.g. "#49"), "@" mentions to other users (e.g. "@cuttlefishh"), or mentions to commit SHA-hashes (e.g., "f36e3c5b3aba23a6c9cf7c01e7485028a23c3811").

### Basic Git Commands

GitHub Guides: https://guides.github.com/introduction/git-handbook/

*This section "Basic Git Commands" is copied from the above site.*

To use Git, developers use specific commands to copy, create, change, and combine code. These commands can be executed directly from the command line or by using an application like [GitHub Desktop](https://desktop.github.com/) or Git Kraken. Here are some common commands for using Git:

* **`git init`** initializes a brand new Git repository and begins tracking an existing directory. It adds a hidden subfolder within the existing directory that houses the internal data structure required for version control.
* **`git clone`** creates a local copy of a project that already exists remotely. The clone includes all the project’s files, history, and branches.
* **`git add`** stages a change. Git tracks changes to a developer’s codebase, but it’s necessary to stage and take a snapshot of the changes to include them in the project’s history. This command performs staging, the first part of that two-step process. Any changes that are staged will become a part of the next snapshot and a part of the project’s history. Staging and committing separately gives developers complete control over the history of their project without changing how they code and work.
* **`git commit`** saves the snapshot to the project history and completes the change-tracking process. In short, a commit functions like taking a photo. Anything that’s been staged with git add will become a part of the snapshot with git commit.
* **`git status`** shows the status of changes as untracked, modified, or staged.
* **`git branch`** shows the branches being worked on locally.
* **`git merge`** merges lines of development together. This command is typically used to combine changes made on two distinct branches. For example, a developer would merge when they want to combine changes from a feature branch into the master branch for deployment.
* **`git pull`** updates the local line of development with updates from its remote counterpart. Developers use this command if a teammate has made commits to a branch on a remote, and they would like to reflect those changes in their local environment.
* **`git push`** updates the remote repository with any commits made locally to a branch.

Learn more from a [full reference guide to Git commands](https://git-scm.com/docs).

### Working on GitHub.com

#### Create a GitHub account

Go to https://github.com and create an account if you don't have one already. Think about what you want your username on GitHub to be because it is difficult to change it later. 

#### Do the GitHub "Hello World" tutorial

You will be prompted to follow this tutorial when you create a new GitHub account, but you can find the tutorial here: https://guides.github.com/activities/hello-world/.

The tutorial has these steps (no coding required!):

1. Create a **repository**.
2. Create a **branch**.
3. Make and **commit** changes.
4. Open a **pull request**.
5. **Merge** your pull request.

### Working with Git on the Command LIne

#### Set up Git

This tutorial will show you how to download and install the latest version of Git, set your username and commit email address in Git, and authenticate a new repository with GitHub. Available online here: https://help.github.com/articles/set-up-git/.

```
# first download and install Git from https://git-scm.com/downloads

# set your Git username for every repository on your computer
git config --global user.name "Mona Lisa"

# confirm that you have set the Git username correctly
git config --global user.name

# set your email address in Git
git config --global user.email "email@example.com"

# confirm that you have set the email address correctly in Git
git config --global user.email
```

#### Set up your working directory

On the command line, go to the place on your computer where you want your repositories to live. I like to have all my repositories in a directory called `git` in my home folder. To make a git directory in your home folder and change to it:

```
mkdir ~/git
cd ~/git
```

#### Example: Contribute to an existing repository

Available online here: https://guides.github.com/introduction/git-handbook/.

```
# download the hello-world repository (that you created above) from your GitHub account 
# to your machine (replace `myusername` with your username)
git clone https://github.com/myusername/hello-world

# change into the `hello-world` directory
cd hello-world

# create a new branch to store any new changes
git branch my-branch

# switch to that branch (line of development)
git checkout my-branch

# make changes: edit `README.md` using a text editor

# create a new file
touch .gitignore

# stage the changed files
git add README.md .gitignore

# commit your changes (a snapshot of the staging area, including anything added)
git commit -m "added .gitignore and edited README.md"

# push changes to github
git push --set-upstream origin my-branch

# now go to GitHub and open a pull request, then merge my-branch into master
```

#### Example: Start a new repository and publish it to GitHub

Available online here: https://guides.github.com/introduction/git-handbook/.

```
# create the repo "my-repo" on your GitHub account

# create a new directory with the same name
cd ~/git
mkdir my-repo

# initialize your repo with git init
git init my-repo

# change into the `my-repo` directory
cd my-repo

# create the first file in the project
echo "# my-repo" >> README.md

# git isn't aware of the file, stage it
git add README.md

# take a snapshot of the staging area
git commit -m "added README to initial commit"

# add the remote location online
# (replace `myusername` with your username)
git remote add origin https://github.com/myusername/my-repo.git

# push changes to github
git push -u origin master

# notice that you don't have to open a pull request because your remote repo is master,
# not a branch off of master
```

#### Example: Contribute to an existing branch on GitHub

Available online here: https://guides.github.com/introduction/git-handbook/.

```
# assumption: a project called `repo` already exists on the machine, and a new branch 
# has been pushed to GitHub.com since the last time changes were made locally

# change into the `repo` directory
cd repo

# update all remote tracking branches, and the currently checked out branch
git pull

# change into the existing branch called `feature-a`
git checkout feature-a

# make changes, for example, edit `file1.md` using the text editor

# stage the changed file
git add file1.md

# take a snapshot of the staging area
git commit -m "edit file1"

# push changes to github
git push
```

#### Example: Fork an existing repository

Modified from Yoshiki Vázquez-Baeza (@ElDeveloper).

```
# on GitHub, go the your favorite repository, such as the repository for this course:
# https://github.com/cuttlefishh/python-for-data-analysis

# click the Fork button, which will create a copy or "fork" of the repository (and 
# a branch, generally master by default)

# create a `python-for-data-analysis` directory in the current directory `~/git` 
# (replace `myusername` with your username)
git clone https://github.com/myusername/python-for-data-analysis
cd python-for-data-analysis

# update your remotes, which allows you to get updates from the master "origin"
# repository (cuttlefishh/python-for-data-analysis, in this case);
# we call this "upstream" as it is upstream of your fork since other people merge to it
git remote add upstream https://github.com/cuttlefishh/python-for-data-analysis

# show your existing remote repositories just to check
git remote -v

# sync just to be sane; we're going to pull down the master branch from upstream
git pull upstream master
 
# sync your fork on github
git push
 
# create a new branch (called "foo") and check it out
git checkout -b foo
 
# time to code ...

# edit or create files, then add them
git add <each file or directory you want to commit>

# rename or delete files (changes will be "added" automatically)
git mv <old file> <new file>
git rm <unwanted file already committed>

# commit changes at a natural milestone (can be offline)
git commit -m "comment about commit"

# ... repeat coding ...
 
# push to origin (your fork) the branch you're working on (must be online)
git push origin foo

# go to your GitHub fork page, select the branch, and click Issue pull request
```

#### Additional Git commands

* `git branch -d foo` deletes local branch `foo`.
* `git push origin --delete foo` deletes remote branch `foo`.
* `git remote -v` shows list of existing remotes with remote url after name.
* `git log` shows log of commits.
* `git stash` stashes changes instead of committing them.
* `git stash pop` re-applies the stashed changes

#### Managing remote repositories

When you fork a GitHub repo at GitHub before cloning that fork locally, you need to set your upstream repo (a location on the internet). This section explains the locations "upstream" and "origin" in the context of the actions "pull"/"fetch" and "push".

* `upstream` generally refers to the original repo that you have forked.
* `origin` is your fork: your own repo on GitHub, a clone of the original repo of GitHub.

From the GitHub page: When a repo is cloned, it has a default remote called `origin` that points to your fork on GitHub, not the original repo it was forked from. To keep track of the original repo, you need to add another remote named `upstream`.

```
git remote add upstream git://github.com/user/repo.git
```

You will use `upstream` to *fetch from the original repo*, in order to keep your local copy in sync with the project you want to contribute to (note: `git fetch` alone would fetch from `origin` by default, which is not what is needed here):

```
git fetch upstream
```

You will use `origin` to *pull and push* since you can contribute to your own repo (again, without parameters, 'origin' is used by default):

```
git pull
gut push
```

You will contribute back to the `upstream` repo by making a *pull request*.

### Command Line Customization

#### Tab completion

You can add tab completion to git so you can tab out commands, branches, etc. This is very handy and can be found at either of these two links:

* https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion
* https://github.com/git/git/blob/master/contrib/completion/git-completion.bash

#### Changing your prompt to show git repo information

The code below creates a nifty bash function `egit` that changes and colors your bash promt to show the current time, your current working directory, and which branch you are working on. Written by Yoshiki Vázquez-Baeza (@ElDeveloper).

Add to your `~/.bash_profile`:

```
function egit (){
    # git specific usage for branching
    function branch_separator () {
        #git name-rev HEAD 2> /dev/null | sed 's#HEAD\ \(.*\)#(git::\1) #'
        if [[ -n $(git rev-parse --abbrev-ref HEAD 2> /dev/null) ]]
        then
        echo "@"
        fi
    }
    function get_git_branch () {
        git rev-parse --abbrev-ref HEAD 2> /dev/null
    }
    export PS1="\[\033[1;32m\]\t \[\033[0m\]\W$(branch_separator)\[\e[m\]\[\e[01;38;5;196m\]$(get_git_branch)\[\e[m\]$ "
}
function dgit (){
    export PS1="\[\033[1;33m\][\u@\h:\w]$\[\033[0m\] "
}
```

*Note: The prompt in dgit should be whichever custom prompt you already defined in your `.bash_profile`; this will make your prompt return to normal when you type `dgit`.*
 
If you have git bash completion installed, or other bash completion scripts, you may need to add this to your `~/.bash_profile`:

	for f in ~/.bash_completion.d/*;
	do
	    source $f;
	done

Enable/disable the git-flavored prompt on the command line:

```
egit
... some git magic ...
dgit
```
