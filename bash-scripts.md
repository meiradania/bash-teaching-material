# Bash Scripts or Shell Scripts

Anything you can run normally on the command line can be put into a script and it will do exactly the same thing. 
Similarly, anything you can put into a script can also be run normally on the command line and it will do exactly the same thing.

It is convention to give files that are bash scripts an extension of .sh 


## Creating the script file
### Shebang  (#!) 
It tells the system which program to use to run the file, and it must be on the very first line of the file (line 2 won't do, even if the first line is blank). 
There must also be no spaces before the # or between the ! and the path to the interpreter.

```
#!/usr/bin/env bash
```

Below that, we can add any commands like the ones we have been running directly at the command line.

Check out more examples on [Chapter 4](https://www.datascienceatthecommandline.com/chapter-4-creating-reusable-command-line-tools.html#converting-one-liners-into-shell-scripts) of the Data Science at the Command Line book.

## Running file / loading a file
Often we will need to change permissions first:
```
$ chmod +x myfile.sh
```

Now can run file without specifying the program
```bash
$ source myfile.sh
```

Or
```bash
$ ./myfile.sh
```

##  Math

For very basic arithmetic:

```

#!/usr/bin/env bash

# File: math.sh

expr 5 + 2

expr 5 - 2

expr 5 \* 2

expr 5 / 2

```

Save `math.sh` and then run this script in your shell:

```{r, engine='bash', eval=FALSE}

$ bash math.sh

```

