# Intro to command line
Taking the first steps in interacting with your computer via the terminal instead of using the graphical interface.
Read on to learn how to create, inspect, move, copy, delete and search for files and folders.

## The prompt
The first thing you see on the window when starting the terminal is a dollar sign (**$**). This is called the **prompt**. 
It lets you know that the terminal is ready for you to type in a command.

The commands follow a similar snytax structure. Note that simple commands don't require options nor arguments:
```
[command] [options] [arguments]
```

### Useful to navigate the prompt faster:
-  **clear** command  or `Ctrl+L` will clean up your terminal screen.
-  You can scroll through your command history with the  **Up**  and  **Down**  arrow keys.
- **history** command will print the complete history .
-  Use `TAB` for autocomplete.
- `!python` will rerun last command for the program (python in this example).
- Aliases are also very important for improving speed (see below).
- Use the last argument from your previous command:
```bash
$ echo 'hello world!'
hello world!
$ echo $_
```

## Getting help

```bash
$ man <command>
```


## Inspecting directories

Which directory am I in?
***By default, when you login, this is your home directory.***
```bash
$ pwd
```

What is in this directory?

```bash
$ ls
```
```
Options: 
-a show hidden files
-G colorized
-l long format
-r reverse order 
-t sort by time
```

What is the folder structure deeper in the file system?
```bash
$ tree
```
```
Option:
 -L {num}  max display depth of the directory tree
```
What are the sizes of files in the directory? (the `*` symbol is a wildcard that matches everything)

```bash
$ du -hs *
```
```
Options:
-h prints human readable format 
-s prints summary, that is, only a total for each argument
```
What is my current disk usage?

```bash
$ df -h
```

## Making directories


```bash
$ mkdir practice-dir
```
```
Options: 
-p for parents: no error if existing, make parent directories as needed
```

## Changing directories

Move down into a folder:

```bash
$ cd practice-dir
```

To go one level up:

```bash
$ cd ..
```

Getting to highest level folders by using the absolute path:
```bash
$ cd /etc/
``` 

Going to the home folder:

```bash
$ cd 
$ cd ~
$ cd $HOME
```

Go back to last directory:
```bash
$ cd -
```


## Copying/Moving files and directories

Be careful with `mv` - it will overwrite the file!

```bash
# copy file
$ cp myfile.txt practice-dir/copy.txt

#copy folder
$ cp -r Documents Desktop

# move file or folder
$ mv myfile.txt practice-dir/my-file.txt
```


## Removing files and directories

Be careful with `rm` - there is no trash can for `rm`!

```bash
$ rm <file>

$ rm -rf <directory>
```
```
Options: 
-r recursive, that is, remove directories and their contents
-f force, that is, ignore nonexistent files, never prompt
```


## Find a file in a directory

Using wildcards:

```bash
$ ls *.png
```

Or using `find` command, when searching for an exact file:
```bash
$ find . -name "states.txt"
```


Or using `grep` , one of the UNIX searching tools.

```bash
$ grep -rl MyClass .
```
```
Options: 
-r 
-l
```


## Combining command-line commands

A long command can be broken up with either a backslash (**\\**) or a pipe symbol (**|**). 
By long commands we mean the ones too long to fit on the page. In such cases, you will see the greater-than sign  (**>**) signaling the continuation prompt:
```bash
$ echo 'Hello'\
> ' world' |
> wc
```


```bash
$ pip freeze | grep numpy

$ grep -rl LSTM . | grep -v __pycache__ | grep -v .ipynb_checkpoints

$ ls -lt | grep py | wc -l
```





