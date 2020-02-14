# Collection of Shell Aliases

##### BE CAREFUL WHEN USING ALIASES

**## ##Use Sudo with Aliases**

```
alias sudo='sudo '
```

**## Colorize the ls output**
```
alias ls='ls --color=auto'
```

**## Use a long listing format with most recently updated files at the bottom.**
```
alias ll='ls -Flrt'
##-F append indicator (one of */=>@|) to entries
```

**## Show hidden files**
```
alias l.='ls -dlrt .* --color=auto'
```

**## Search for a process**
```
alias psg='ps aux | grep -v grep | grep -i -e VSZ -e'
```

**## Keep forgetting the flags to extract a tarball?**
```
alias untar='tar -zxvf'
```

**## List the processes using the most CPU time**
```
alias hogs='ps uxga | sort --key=3.1 -n'
```

**## List files in order of ascending their size**
```
function lsdu() { ls -l $* | sort --key=5.1 -n; };
```

**## Count the number of files in current directory**
```
alias lsc='ls -l | wc -l' **
```

**## Find files in the current/root directory by name**
```
alias ff='find . -name $1'
alias fr='find / -name $1'
```

**## Reopen file last edit in vi, in edit mode in vi again**
```
!vi
**## Technically not an alias, just a short-cut
```
**## Search history**
```
alias hg='history | grep -i'
```
**## Grabs the disk usage in the current directory**
```
alias usage='du -ch | grep total'
```

**## Gets the total disk usage on your machine**
```
alias totalusage='df -hl --total | grep total'
```

**## Gives you what is using the most space. Top 10**
```
alias most='du -hsx * | sort -rh | head -10'
```

**## Resume wget by default**
```
 alias wget='wget -c'
```

**## See memory information**
```
alias meminfo='free -m -l -t'
```
 
**## Get top process eating memory**
```
alias psmem='ps auxf | sort -nr -k 4'
alias psmem10='ps auxf | sort -nr -k 4 | head -10'
```
 
**## Get top process eating cpu**
```
alias pscpu='ps auxf | sort -nr -k 3'
alias pscpu10='ps auxf | sort -nr -k 3 | head -10'
```
 
**## Get server cpu info**
```
alias cpuinfo='lscpu'
```
**## Stop after sending count ECHO_REQUEST packets**
 ```
 alias ping='ping -c 5'
 ```
**## Do not wait interval 1 second, go fast**
```
alias fastping='ping -c 100 -s.2'
```
**## All of our servers eth1 is connected to the Internets via vlan / router etc**
```
alias dnstop='dnstop -l 5  eth1'
alias vnstat='vnstat -i eth1'
alias iftop='iftop -i eth1'
alias tcpdump='tcpdump -i eth1'
alias ethtool='ethtool eth1'
```

**## Create shortcut commands**
```
alias path='echo -e ${PATH//:/\\n}'
alias nowtime='date +"%T"'
alias nowdate='date +"%d-%m-%Y"'
```

**## Get local ip**
```
alias ipi='ipconfig getifaddr en0'
```

**## System Updates**
```
alias apt='sudo apt-get'
alias update='sudo apt-get update && sudo apt-get upgrade'
##Debian / Ubuntu 
```

**## Git related**
```
alias g='git'
alias gr='git rm -rf'
alias gs='git status'
alias ga='g add'
alias gc='git commit -m'
alias gp='git push origin master'
alias gl='git pull origin master'
```