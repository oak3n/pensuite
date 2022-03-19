# xclip
## install
`sudo apt-get install xclip`

## links
- [a quick guide to .bashrc](https://www.marquette.edu/high-performance-computing/bashrc.php)

## use

### optional: alias in `~/.bashrc`
`~/.bashrc` stores your users bash profile.
1. backup `~/.bashrc`
```bash
mkdir backup
cp ~/.bashrc backup/bashrc.b
```
2. edit `~/.bashrc`
`nano ~/.bashrc`
append the following:
```bash
# xclip alias shortcuts
alias "cc=xclip -selection clipboard"
alias "ct=xclip"
alias "v=xclip -o"
```

*Note: you will need to reload your bash profile. (Restart terminal ez)* 
