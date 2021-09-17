## Bash prompt
Shows username, working directory followed by current branch if applicable in line 1.
Shows current time in AM/PM format in line 2
```
if [ "$color_prompt" = yes ]; then
    PS1='\[\033[01;32m\]\u:\[\033[01;34m\]\w \[\033[01;31m\]$(git branch 2>/dev/null | grep '^*' | colrm 1 2)\n\[\033[01;33m\](\@)\[\033[00m\]\$ '
else
    PS1='\u@\h:\w $(git branch 2>/dev/null | grep '^*' | colrm 1 2)\n(\@)\$ '
fi
```
