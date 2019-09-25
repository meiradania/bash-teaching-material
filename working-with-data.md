# Working with data

Create files from redirecting content, edit, inspect and modify content of a file.

## Making and editing files
Make a file

```bash
$ touch myfile.txt
```

Edit a file

```bash
$ nano myfile.txt
```

## Redirect to file
Generate project structure for use in a readme

```bash
# append
$ tree >> out.txt

# new file
$ tree > out.txt
```

Another common pattern is generating a requirements file for a Python project

```bash
$ pip freeze > requirements.txt
```

You can also put the redirection at the start

```bash
$ > out.txt tree
```
Make a file with a single line `tdd`

```bash
$ echo tdd > newfile.txt
```

## Checking file contents
Using [the states file](http://seankross.com/notes/states.txt) as example:

```bash
#  print all file contents
$ cat states.txt

#  print first n rows
$ head -n 3 states.txt

#  print last n rows
$ tail -n 3 states.txt

#  paging over the file
$ less states.txt

# word count: number of lines, number of words, number of characters of file
$ wc states.txt
```

## Searching file contents
`grep` when using wildcards:
```bash
$ grep "x" states.txt
```

`egrep`when using regular expressions:
```bash
$ egrep "s*as" states.txt
```

Let's create a file to run some more examples:
```bash
$ touch small.txt
$ echo "abcdefghijklmnopqrstuvwxyz" >> small.txt
$ echo "ABCDEFGHIJKLMNOPQRSTUVWXYZ" >> small.txt
$ echo "0123456789" >> small.txt
$ echo "aa bb cc" >> small.txt
$ echo "rhythms" >> small.txt
$ echo "xyz" >> small.txt
$ echo "abc" >> small.txt
$ echo "tragedy + time = humor" >> small.txt
$ echo "http://www.jhsph.edu/" >> small.txt
$ echo "#%&-=***=-&%#" >> small.txt
```

Using our created `small.txt`file as example:
```bash
# list all “word” characters
$ egrep "\w" small.txt

# list all “number” characters
$ egrep "\d" small.txt

# invert match
$ egrep -v "\w" small.txt
```