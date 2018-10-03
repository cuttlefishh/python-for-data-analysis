## Lesson 2 - Command Line Part I

#### A note about operating systems

This tutorial works best if you are using the Bash shell. Linux and macOS come standard with Bash, which you can access in the Terminal application. Windows PowerShell uses the .NET framework, which is not Bash. For Windows users, you have several options:

1. Best option: Install [Git Bash](https://gitforwindows.org) and use the Bash shell that comes with it. This is fast.
2. Next best option: Install a Linux virtual machine like [VirtualBox](https://www.virtualbox.org) and use the Terminal that comes with it. This takes more time but gives you access to a virtual Linux machine on your PC.
3. Last resort: Use Windows PowerShell. This has some functionality, as you saw in Appendix A of Shaw. But many of the commands below will not work, including `cd` (by itself), `cd -`, `touch`, `cat` (try `type` or a text editor), `head`, `tail`, and others.

### Overview of today's lesson

#### Setup

* Open a shell in Terminal (Mac/Linux) or GitBash (Windows)
* Create a working directory for the course, and a lessons directory inside that
* Copy the day's lesson from GitHub to your lessons folder

#### Basic commands and skills

* Moving between directories
* Absolute and relative paths
* Creating, moving, and removing files and directories
* Investigating text files
* Working with commands and processes
* Tab-completion of commands and paths
* GUI and command-line text editors

#### Customization

* Customize your Finder window (or similar on non-Mac)
* Customize up your Bash environment

### Basic commands

#### Moving between directories

* `pwd` — print working directory
* `ls` — list contents of working directory
* `cd DIRECTORY` — change to directory
* `cd ~` or `cd` — change to home directory
* `cd -` — change to previous directory

#### Absolute and relative paths

* `.` — current directory
* `..` — one directory up
* `../..` — two directories up
* `/` — root directory
* `~` — home directory

#### Creating, moving, and removing files and directories

* `mkdir DIRECTORY` — make directory
* `rmdir DIRECTORY` — remove empty directory
* `touch FILE` — create an empty file or change file modification time
* `cat FILE` — print contents of file
* `cat FILE1 FILE2 > FILE3` — combine two files into third file
* `cat > FILE` — write to file
* `cat >> FILE` — append to file
* `cp FILE1 FILE2` — copy file
* `mv FILE1 FILE2` — move file
* `rm FILE` — remove file
* `ln -s FILE LINK` — make a symbolic link

#### Investigating text files

* `less FILE` — view a text file
* `head FILE` — first 10 lines of file
* `tail FILE` — last 10 lines of file
* `wc FILE` — count the words and characters in a file
* `open FILE` — open a file using default program (on a Mac)
* `file FILE` — get the file type for file(s)
* `grep REGEX FILE` — search a text file for a string or regular expression

#### Working with commands and processes

* `man COMMAND` — display manual page of command if it exists
* `help COMMAND` — display help description of command if it exists
* `which COMMAND` — show location of command
* `history` — display past commands
* `top` — display current processes
* `exit` — close the current session

### Text editors

#### GUI text editors

Popular text editors for writing code are [Atom](https://atom.io) and [Sublime Text](https://www.sublimetext.com). Download and install one of them if you haven't already.

A great way to document your work is using Markdown, a simple markup style. It is used widely in Jupyter notebooks and GitHub. Many text editors support Markdown, but I like the Mac program [MacDown](http://macdown.uranusjr.com). I use it as a virtual lab notebook for my bioinformatics research.

#### Command-line text editors

For small jobs or if you want to stay inside the terminal, there are other useful programs. Note: `cat` is only useful for creating very basic files, or starting files and finishing them in a proper text editor.

* `nano FILE` — nano is the most basic text editor (see Appendix: The Nano Text Editor at end of this lesson)
* `emacs FILE` — emacs is a popular full-featured text editor controlled by keystrokes
* `vim FILE` — vim or vi is a popular competitor to emacs that loads faster 

### Setting up your bash environment

There are several things you can do to set up your bash environment, which is what you see when you use the terminal (command line). You put these commands in a file called ~/.bash_profile (or ~/.bashrc or ~/.profile). That notation means the file is called .bash_profile (yes, that's a period, and the file is called a dot-file), and it's in your home directory.

```	
# customize prompt with color and pwd
PS1="\[\033[1;33m\][\u@\h:\w]$\[\033[0m\] "
	
# customize terminal window title to display pwd
PROMPT_COMMAND='echo -ne "\033]0; ${PWD##*/}\007"'
	
# autocomplete history with up arrow
bind '"\e[A": history-search-backward'
bind '"\e[B": history-search-forward'

# grep coloring
export GREP_OPTIONS='--color=auto' 
export GREP_COLOR='01;38;5;226'

# command aliases (shortcuts)
alias cd..='cd ..'
alias cd...='cd ../..'
alias cd....='cd ../../..'
alias du='du -sh'
alias excel='open -a /Applications/Microsoft\ Office\ 2011/Microsoft\ Excel.app'
alias l='ls -p'
alias la='ls -ap'
alias lal='ls -alhp'
alias ll='ls -lhp'
alias m2u="tr '\015' '\012'"
alias u2m="tr '\012' '\015'"
alias rm='rm -i'
alias taill='ls -lrt | tail'

# history settings
export HISTCONTROL=ignoredups:erasedups  # no duplicate entries
export HISTSIZE=100000                   # big big history
export HISTFILESIZE=100000               # big big history
shopt -s histappend                      # append to history, don't overwrite it

# save and reload the history after each command finishes
export PROMPT_COMMAND="history -a; history -c; history -r; $PROMPT_COMMAND"
```

### Appendix: The Nano Text Editor

Credit: [SDSU Department of Astronomy](http://mintaka.sdsu.edu/reu/nano.html)

#### Introduction

Nano is a text editor suited to working in UNIX. It is not as powerful as PC window-based editors, as it does not rely on the mouse, but still has many useful features.
Most nano commands are invoked by holding down the `Ctrl` key (that is, the control key), and pressing one of the other keys. In this text, the control key is referred to using `^`. For example, `^X` means "hold down the control key and press the x key". Most of the important commands are listed at the bottom of your screen.

* `^G	` nano help

#### Starting nano

To edit a file called filename, type nano filename.
In nano, you can insert another file:

* `^R`	read an existing file into nano (inserted at the current cursor position)
* `^T`	opens a browser that allows you to select a file name from a list of files and directories

#### Navigation

The usual mouse-based point-and-click method is not supported by nano. Use the arrow keys to move around the page in nano.

Other navigation commands:

* `^A`	move to beginning of line
* `^E`	move to end of line
* `^Y`	move down a page
* `^V`	move up a page
* `^_`	move to a specific line (`^_^V` moves to the top of the file, `^_^Y` to the bottom)
* `^C`	find out what line the cursor is currently on
* `^W`	search for some text.

When searching, you will be prompted for the text to search for. It searches from the current cursor position, wrapping back up to the top if necessary.

#### Editing

Insert new text at the current cursor position just by typing the text in.

Delete commands:

* `^D`	delete character currently under the cursor
* `Backspace`	delete character currently in front of the cursor
* `^K`	delete entire line
* `^\`	search for (and replace) a string of characters

Cut and paste:

* `^K` does not delete lines permanently; the most recent set of deletions are stored in a buffer. These lines may be re-inserted at the current cursor location using `^U`. This may be used to simulate cut and paste:
	* Repeatedly use `^K` until all of the text you want to move has been deleted.
	* Move to the line that you want to insert the text at, and use `^U`.
* Note that pressing `^U` more than once will cause multiple copies to be inserted. This is particularly useful if you want to copy text:
	* Repeatedly use `^K` until all of the text you want to copy has been deleted.
	* Press `^U` immediately to put a copy back in its original location.
	* Move to the line that you want to copy the text to, and use `^U`.

#### Saving and Exiting

* `^O`	save contents without exiting (you will be prompted for a file to save to)
* `^X`	exit nano (you will be prompted to save your file if you haven't)
* `^T`	when saving a file, opens a browser that allows you to select a file name from a list of files and directories
