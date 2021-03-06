# bashrc
## Bash prompt
Shows username, working directory followed by current branch if applicable in line 1.
Shows current time in AM/PM format in line 2
```sh
if [ "$color_prompt" = yes ]; then
  PS1="\[\033[01;32m\]\u:\[\033[01;34m\]\w \[\033[01;31m\]$(git branch 2>/dev/null | grep '^*' | colrm 1 2)\n\[\033[01;33m\](\$(TZ='Asia/Kolkata' date '+%I:%M %p'))\[\033[00m\]\$ "
else
    PS1="\u@\h:\w $(git branch 2>/dev/null | grep '^*' | colrm 1 2)\n(\$(TZ='Asia/Kolkata' date '+%I:%M %p'))\$ "
fi
```

## git aliases
```sh
# git aliases
alias gst="git status"
alias gcb="git checkout -b"
alias gcm="git checkout master"
alias gd="git diff"
alias gds="git diff --staged"
alias gp="git push"
alias ga="git add"
alias gc="git commit"
alias gcm="git commit -m"
```

## miscellaneous aliases
```sh
# miscellaneous aliases
alias ..="cd .."
```
# inputrc

## reverse search on up key
```
# Respect default shortcuts.
$include /etc/inputrc

## arrow up
"\e[A":history-search-backward
## arrow down
"\e[B":history-search-forward
```
