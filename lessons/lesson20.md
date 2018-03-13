## Lesson 20 - Git and GitHub

GitHub is a code-hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere. At the heart of GitHub is an open source version control system (VCS) called Git. Git is responsible for everything GitHub-related that happens locally on your computer.

### Working on GitHub (github.com)

#### Create a GitHub account

Go to https://github.com and create an account if you don't have one already. Think about what you want your username on GitHub to be because it is difficult to change it later. 

#### Do the GitHub "Hello World" tutorial

You will be prompted to follow this tutorial when you create a new GitHub account, but you can find the tutorial here: https://guides.github.com/activities/hello-world/.

### Working on Git (command line)

#### Set up Git

This tutorial will show you how to download and install the latest version of Git, set your username and commit email address in Git, and authenticate a new repository with GitHub: https://help.github.com/articles/set-up-git/.

#### Create your own repository

This tutorial shows you how to start a new repository in different ways: http://kbroman.org/github_tutorial/pages/init.html.

#### Fork an existing repository

On GitHub, go the your favorite repository, such as the repository for this course:

https://github.com/cuttlefishh/python-for-data-analysis

Click the **Fork** button, which will create a copy of the forked repository (and branch, generally master by default).

On the command line, go to the place on your computer where you want the repository to live. I like to have all my repositories in a directory called `git` in my home folder. To make a git directory in your home folder and change to it:

    $ mkdir ~/git
    $ cd ~/git

The following will create a `python-for-data-analysis` directory in the current directory `~/git` (replace `myusername` with your username):

	$ git clone https://github.com/myusername/python-for-data-analysis
	$ cd python-for-data-analysis
 
Update your remotes, which allows you to get updates from the master "origin" repository (cuttlefishh/python-for-data-analysis in this case).

We're going to call this upstream as it is upstream of your fork since other people merge to it:

	$ git remote add upstream https://github.com/cuttlefishh/python-for-data-analysis
 
Sync just to be sane; we're going to pull down the master branch from upstream:

	$ git pull upstream master
 
Sync your fork on github:

	$ git push
 
Now we can do some coding.
 
Create a new branch (called "foo") and check it out:

	$ git checkout -b foo
 
Edit files, create files, delete files, etc.:

	$ git add <each file or directory you want to commit>
	$ git mv <old file> <new file>
	$ git commit -m "Comments about commit"
	... repeat ...
 
Push to origin (your fork) the branch you're working on:

	$ git push origin foo

Go to your github fork page, select the branch and click **Issue pull request**.

(Optional) Remove local branch:

	$ git branch -d foo

(Optional) Delete remote branch AND local branch:

    $ git push origin --delete <branch_name>
    $ git branch -d <branch_name>

(Status) Shows list of existing remotes with remote url after name:

	$ git remote -v
	
See log of commits:

	$ git log
	
Stash changes instead of committing them:

    $ git stash
    
...then re-apply the stashed changes:

    $ git stash pop

Download someone else's branch:

	$ git remote add username https://github.com/username/emp.git (use username for sanity)
	$ git checkout -b branchname (use same name as the person issuing PR just for sanity)
	[should be another command to pull their branch]

Note: upstream is a location on the internet, which can have more branches than master in upstream (but not usually).

#### Tab completion

You can add tab completion to git so you can tab out commands, branches, etc. This is very handy and can be found here:
 
https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion

(Alternate link: https://github.com/git/git/blob/master/contrib/completion/git-completion.bash)

#### Changing your prompt to show git repo information

This is a nifty git function that updates your prompt to show what repo you're in (code below). Written by Yoshiki Vázquez-Baeza (@ElDeveloper). 

Add to your `~/.bash_profile` (written originally by Yoshiki Vazquez Baeza):

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
	    export PS1='\[\033[1;32m\]\t \[\033[0m\]\W$(branch_separator)\[\e[m\]\[\e[01;38;5;196m\]$(get_git_branch)\[\e[m\]$ '
	}
	function dgit (){
	    export PS1='\[\033[1;32m\]\t \[\033[0m\]\W$ '
	}
 
Enable/disable git-flavored prompt:

	$ egit
	... some git magic ...
	$ dgit

(Optional) Add this if you have the git bash completion, or other bash completion scripts:

	for f in ~/.bash_completion.d/*;
	do
	    source $f;
	done
	
