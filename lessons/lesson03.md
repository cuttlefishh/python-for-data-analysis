## Lesson 03 - Command Line Part II

Skills you will learn in this lesson:

* Parsing files
* Working with input and output
* Wildcards
* Brace expansion
* Control keys
* Bash variables and commands
* Executing bash scripts and dot-files
 
### More commands

#### Parsing files

* `cut -d "," -f 5- FILE` -- output 5th field through end using comma field delimiter
* `sed 's/FIND/REPLACE/g'` -- replace text in a file
* `perl --e 's/FIND/REPLACE/g'` -- run perl commands in the command line (advanced)

#### Working with input and output

* `|` -- pipe output from one command to another
* `>` -- redirect (write) to file
* `<` -- get output of file (other type of redirect)
* `` `COMMAND` `` -- pass output of a command (e.g., in a for loop)

#### Wildcards

* `?` -- match any single character
* `*` -- match any string of characters
* `[set]` -- match any character in set
* `[!set]` -- match any character *not* in set

#### Brace expansion

* `{start..end}` -- expand a range; e.g., `b{ed,olt,ar}s`, `{2..5}`, `{d..h}`

#### Control keys

* `CTRL-C` -- stop current command
* `CTRL-D` -- end of input
* `CTRL-Z` -- suspend current command

### Variables, bash scripts, and dot-files

#### Bash variables and commands

* `A=0` -- assign a variable
* `echo VARIABLE` -- output the value of a variable or expression
* `$PATH` -- your path variable
* `$SHELL` -- your current shell
* `$RANDOM` -- a random number
* `$PPID` -- process ID
* `$HOME` -- your home directory (another name for `~` or `/Users/you`)
* `for VARIABLE in LIST; do COMMANDS; done` -- `for` loop in bash

#### Executing bash scripts and dot-files

* `bash SCRIPT.sh` -- run a bash shell script
* `source .DOTFILE` -- run a dot-file like your .bash_profile

Any of the commands we have used from the command line (the bash prompt `$`) can also be typed into a text file and executed by typing `bash SCRIPT.sh` from the command line.
