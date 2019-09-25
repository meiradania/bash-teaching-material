# History file
Whenever we close a terminal our recent commands are written to the ~/.bash_history file. 
Let’s a take a look at the beginning of this file:

```bash
$ head -n 5 ~/.bash_history
```

# Configuration file
Your shell is configured using 

`~/.bashrc` (Linux)

`~/.bash_profile` (Mac - but Mac will also have a `bashrc`)

These scripts are run every time you start a new shell.  It is common to add `echo` statements to these files to get used to this idea.

## Aliases
Aliases are like macros. If you often find yourself executing a certain command with the same parameters (or a part of it), you can define an alias for this. 
Aliases are also very useful when you continue to misspell a certain command (see [https://github.com/chrishwiggins/mise/blob/master/sh/aliases-public.sh](https://github.com/chrishwiggins/mise/blob/master/sh/aliases-public.sh) for a long list of useful aliases).

The following command defines such an alias:
```bash
$ alias moer=more
```
Useful aliases

```bash
$ alias ls='ls -aGl'

alias exut='exit'
alias eixt='exit'
alias exot='exit'
alias ext='exit'
alias eit='exit'
alias q='exit'

alias c='clear'
alias cls='clear && ls'
alias ctree='clear && tree'

alias bashrc='vim ~/git/dotfiles/.bashrc'

alias gs='git status'
alias ga='git add -u'
alias gc='git commit -m '
alias gp='git push origin '
alias gls='clear && git status'
