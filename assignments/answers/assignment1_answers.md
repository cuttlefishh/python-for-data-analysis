### Answers for Assignment 1 - Basic Shell Commands

Execute these commands in your terminal. Copy and paste the commands and output (i.e., your terminal session) to a text file, then save and submit this text file as your completed assignment. You may use plain text (.txt) or Markdown (.md) format. Please name your file `1_first_last.txt` or `1_first_last.md` (substitute your first and last name).

**Basic commands**

1. Navigate to your working directory for the class.
2. Within that directory, create a temporary test directory.
3. Create a file using one method I showed you.
4. Create a file using a different method I showed you.
5. Rename one of the files.
6. Copy one of the files.
7. Delete one of the files.
8. Delete the temporary directory.

```
$ cd ~/sio209
$ mkdir test
$ cd test
$ cat > file1
I am creating a file using cat.
^C
$ touch file2
$ nano file2
(add text using nano)
$ mv file2 file3
$ cp file1 file2
$ rm file1
$ cd ..
$ rm -r test
```

**Working with commands**

1. Learn more about a command from class using a Unix command.
2. Learn more about a command from class using a Google search.
3. Find out where the commands `mv` and `cp` are located on your computer.
4. Get a list of the commands you've typed already.
5. See which processes are running on your computer.
6. What happens when you type `Tab` in the middle of typing a command?
7. What happens when you type `Tab` in the middle of typing a file name or path?

```
$ man cd
$ help cd
(google "unix cd command")
$ which mv
$ which cp
$ history
$ top
$ hist<Tab> -> history
$ cd ~/sio<Tab> -> cd ~/sio209
```

**Setting up your bash environment**

1. Download a text editor such as []() or [Sublime Text](https://www.sublimetext.com) if you haven't already.
2. Using your text editor, customize your terminal by editing the file `.bash_profile` in your home directory.
3. Source your bash profile file with the command `source ~/.bash_profile`.
4. Open a new terminal to make sure it automatically sources your bash profile file. You may have to change the preferences in the Terminal app.

```
$ nano ~/.bash_profile
$ source ~/.bash_profile
$ exit
```

**More commands**

1. Print the first 5 lines of a text file.
2. Print the last 10 commands you entered.
3. View the contents of a file without printing anything to the screen.
4. Open a file in its designated application.
5. Determine the kind/type of a file.
6. Search for a word in a file.
7. Get only the third column of a tab-delimited file. (To insert a tab character, type `Ctrl-V` and then `Tab`.)
8. Using a different method, get the first field of a tab-delimited file and save it as a new file.

```
$ head -n 5 FILE
$ history | tail
$ less FILE
$ open FILE
$ file FILE
$ grep WORD FILE
$ cut -d '    ' -f 3 FILE
$ cat FILE | awk '{FS="\t"}; {print $3}' > NEWFILE
$ cat FILE | perl -alne 'print $F[2]' > NEWFILE
```

**Paths and variables**

1. Navigate to root and home directories using absolute paths.
2. Navigate to root and home directories using relative paths.
3. Store an integer as a shell variable then print it.
4. Store a file name as a shell variable.
5. Print your current path variable.
6. Print your home directory.
7. Write a `for` loop to count to 10.

```
$ cd /
$ cd /Users/luke
$ cd ../..
$ cd ~
$ A=5
$ echo $A
$ B='myfile.txt'
$ echo $PATH
$ echo $HOME
$ for i in {1..10}; do echo $i; done
```

**Executing bash scripts and dot-files**

1. Write a bash script that uses the commands `mkdir`, `cat`, `mv`, `echo`, and a `for` loop.
2. Execute you bash script using the terminal.

```
# myscript.sh
mkdir mytempdir
cd mytempdir
echo "some text" > myfile
cat myfile
mv myfile myfile2
for i in line1 line2 line3
do
    echo $i >> myfile2
done
cat myfile2
```

```
$ bash myscript.sh
```
