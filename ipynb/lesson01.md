## Lesson 1 - Command Line and Bash

* Moving between directories and creating/removing files
* Working with commands and processes
* Investigating text files
* Parsing files
* Working with input and output
* Absolute and relative paths, symbolic links
* Bash variables and commands
* Text editors: nano, vim, emacs, [Sublime Text](https://www.sublimetext.com), [MacDown](http://macdown.uranusjr.com)
* Execute bash scripts and dot-files (e.g., `.bash_profile`)
* Set up your Terminal settings and bash environment

### Basic commands

#### Moving between directories and creating/removing files.

* `pwd` -- print working directory
* `ls` -- list contents of working directory
* `cd DIRECTORY` or `cd` -- change directory, change to home directory
* `mkdir DIRECTORY` -- make directory
* `rmdir DIRECTORY` -- remove empty directory
* `touch FILE` -- create an empty file
* `cat FILE` -- print contents of file
* `cat > FILE` -- write to file
* `cat >> FILE` -- append to file
* `cp FILE1 FILE2` -- copy file
* `mv FILE1 FILE2` -- move file
* `rm FILE` -- remove file
* `exit` -- close the current session

#### Working with commands and processes

* `man COMMAND` -- display manual page of command if it exists
* `which COMMAND` -- show location of command
* `history` -- display past commands
* `top` -- display current processes


### Setting up your bash environment

There are several things you can do to set up your bash environment, which is what you see when you use the terminal (command line). You put these commands in a file called ~/.profile (or ~/.bashrc or ~/.bash_profile). That notation means the file is called .profile (yes, that's a period, and the file is called a dot-file), and it's in your home directory.

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
```

### More commands

#### Other text editors

For serious coding, Sublime Text is great. For small jobs or if you want to stay inside the terminal, there are other useful programs. Note: `cat` is only useful for creating very basic files, or starting files and finishing them in a proper text editor.

* `nano FILE` - nano is the most basic text editor (see Appendix: The Nano Text Editor at end of this lesson)
* `emacs FILE` - emacs is a popular full-featured text editor controlled by keystrokes
* `vim FILE` - vim or vi is a popular competitor to emacs that loads faster 

#### Investigating text files

* `less FILE` -- view a text file
* `head FILE` -- first 10 lines of file
* `tail FILE` -- last 10 lines of file
* `wc FILE` -- count the words and characters in a file
* `open FILE` -- open a file using default program (on a Mac)
* `file FILE` -- get the file type for file(s)
* `grep REGEX FILE` -- search a text file for a string or regular expression

#### Parsing files

* `cut -d "," -f 5- FILE` -- output 5th field through end using comma field delimiter
* `sed 's/FIND/REPLACE/g'` -- replace text in a file
* `perl --e 's/FIND/REPLACE/g'` -- run perl commands in the command line (advanced)

#### Working with input and output

* `|` -- pipe output from one command to another
* `>` -- redirect (write) to file
* `<` -- get output of file (other type of redirect)
* `` `COMMAND` `` -- pass output of a command (e.g., in a for loop)

### Paths and variables

#### Absolute and relative paths, symbolic links

* `.` -- current directory
* `..` -- one directory up
* `../..` -- two directories up
* `/` -- root directory
* `~` -- home directory
* `ln -s FILE LINK` -- make a symbolic link

#### Bash variables and commands

* `A=0` -- assign a variable
* `echo VARIABLE` -- output the value of a variable or expression
* `$PATH` -- your path variable
* `$SHELL` -- your current shell
* `$RANDOM` -- a random number
* `$PPID` -- process ID
* `$HOME` -- your home directory (another name for `~` or `/Users/you`)
* `for VARIABLE in LIST; do COMMANDS; done` -- `for` loop in bash

### Executing bash scripts and dot-files

#### Commands

* `bash SCRIPT.sh` -- run a bash shell script
* `source .DOTFILE` -- run a dot-file like your .profile

#### Bash scripts

Any of the commands we have used from the command line (the bash prompt `$`) can also be typed into a text file and executed by typing `bash SCRIPT.sh` from the command line.

### Assignment for Lesson 1

**Basic commands**

1. Create a working directory for today's class.
2. Within that directory, create a temporary test directory.
3. Create a file using one method I showed you.
4. Create a file using a different method I showed you.
5. Rename one of the files.
6. Copy one of the files.
7. Delete one of the files.
8. Delete the temporary directory.

**Working with commands**

1. Learn more about a command you just learned using a unix command.
2. Learn more about a command you just learned using Google.
3. Find out where the commands `mv` and `cp` are located on your computer.
4. Get a list of the commands you've typed already.
5. See which processes are running on your computer.
6. What happens when you type Tab in the middle of a command?
7. What happens when you type Tab in the middle of a file name or path?

**Setting up your bash environment**

1. Download the text editor [Sublime Text](https://www.sublimetext.com).
2. Customize your terminal by editing `.profile` or `.bashrc` using Sublime Text.
3. Source your bash profile file using `source ~/.profile`.
4. Open a new terminal to make sure it automatically sources your bash profile file. You may have to change the preferences in the Terminal app.

**More commands**

1. Print the first 5 lines of a text file.
2. Print the last 10 commands you entered.
3. View the contents of a file without printing anything to the screen.
4. Open a file in its designated application.
5. Determine the kind/type of a file.
6. Search for a word in a file.
7. Get only the third column of a tab-delimited file.[^1]
8. Using a different method, get the first field of a tab-delimited file and save it as a new file.

[^1]: To insert a Tab character, type Ctrl-V and then Tab.

**Paths and variables**

1. Navigate to root and home directories using absolute paths.
2. Navigate to root and home directories using relative paths.
3. Store an integer as a shell variable then print it.
4. Store a file name as a shell variable.
5. Print your current path variable.
6. Print your home directory.
7. Write a `for` loop to count to 10.

**Executing bash scripts and dot-files**

1. Write a bash script that uses the commands `mkdir`, `cat`, `mv`, `echo`, and a `for` loop.
2. Execute you bash script using the terminal.

### Appendix: The Nano Text Editor

Credit: [SDSU Department of Astronomy](http://mintaka.sdsu.edu/reu/nano.html)

#### Introduction

Nano is a text editor suited to working in UNIX. It is not as powerful as PC window-based editors, as it does not rely on the mouse, but still has many useful features.
Most nano commands are invoked by holding down the `Ctrl` key (that is, the control key), and pressing one of the other keys. In this text, the control key is referred to using `^`. For example, `^X` means "hold down the control key and press the x key". Most of the important commands are listed at the bottom of your screen.

`^G	` nano help

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

