# bash
## modules, environment variables and development environments (python)
load a module
`module load <module>`

modify an environment variable, like PATH
`export PATH=$PATH:<path/to/dir>`

activate a development environment
`source <path/to/env>/bin/activate`
here `activate` is a bash file that extends your bash customization, ie development environments like python's `virtual-env` module

## aliases
source bash file containing bash aliases `~/.bash_aliases`
```bash
if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi
```

define an alias
`alias <aliasname>="<command>"`
example:
`alias ll="ls -l"`

common aliases
```bash
alias ..='cd ..'
alias ...='cd ../..'
alias ....='cd ../../..'
alias .4='cd ../../../../'
alias .5='cd ../../../../..'
alias la='ls -a'
alias rm='rm -i' #-i prompts user before deletion
alias cp='cp -i' #-i prompts user before overwriting

# python virtual environments
alias env1="source ~/project1/env/activate"
alias env2="source ~/project2/env/activate"
alias env3="source ~/project3/env/activate"
```

*Note: to switch python environments using these aliases:*
```bash
deactivate # deactivate the currently loaded environment
env2 # activate environment for project3
```

## links
[a quick guide to bashrc](https://www.marquette.edu/high-performance-computing/bashrc.php)

