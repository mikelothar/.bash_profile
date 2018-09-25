# Bash


## .bash_profile
```bash
export PATH="$HOME/.yarn/bin:$PATH"
export PATH="$HOME/AppData/Roaming/npm:$PATH"
source ~/.bash_aliases
```

## .bash_aliases
```bash
gitFetchAndCheckoutBranch() {
  git fetch
  git checkout $1
}

alias ..='cd ..'
alias ...='cd ../..'
alias br='source ~/.bash_profile ; source ~/.bash_aliases ; echo --- reloaded'
alias c='clear'
alias deletealldockerimages='docker rmi $(docker images -q)'
alias fetchout='gitFetchAndCheckoutBranch'
alias gitfix='git gc --prune=now'
alias gitup='git fetch origin ; git branch -v -a'
alias gw='gulp && gulp watch'
alias killnode='taskkill -F -IM node.exe'
alias ll='ls -lhF --color --group-directories-first'
alias ls='ls -hF --color --group-directories-first'
alias myremotebranches='git for-each-ref --format=" %09 %(authordate:short) %09 %(authorname) %09 %(refname)" --sort=-authordate | grep Michael | grep refs/remotes | grep -n " " | sed "s@refs/remotes/origin/@@g" | sed "s@Lothar@L@g"'
alias npmglob='npm list -g --depth=0'
alias uniqhistory='cat ~/.bash_history | sort | uniq > ~/.bash_history.uniq'
alias vial='vi ~/.bash_aliases'
alias vibr='vi ~/.bash_profile'
```
