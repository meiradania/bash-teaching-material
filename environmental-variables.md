# Setting environment variables

The terminal is a stateful system - it has a whole bunch of variables.  
You can see these using `env` (the equivalent of `dir()` in Python)

We can set a variable using:
```bash
$ zz=1
```

If you want to see what value this variable is holding (note the `$` - this is always used):

```bash
$ echo $zz
```

But these variables will not be inherited by sub processes - to get this we need to use `export`.  You will always see `export` used in the shell config scripts (i.e. `.bash_rc`), and the simpler variable assignment in shell scripts.

```bash
$ export zz=2
```

# PATH

Locations the shell checks when you type a command.  You can think of adding a location to your `PATH` as installing a program.

`echo $PATH | tr ":" "\n"`

`export PATH=$PATH:$SPARK_HOME/bin`

A common pattern you will see in install scripts

`echo 'export PATH=$PATH:$SPARK_HOME/bin' >> ~/.bashrc`
