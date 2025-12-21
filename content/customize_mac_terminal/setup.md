# Setup

There are alot of third-party terminals like oh my zsh, etc that offers great customization but I prefer using the macOS built-in terminal and add subtle but useful features.

## Autosuggestion and Syntax Highlighting
```zsh
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.zsh/zsh-syntax-highlighting
```

## Short Alias to Frequently Used Commands
```zsh
nano ~/.zshrc
```
and then copy-paste the content from below

```zsh
# Python
alias code="open -a 'Visual Studio Code'"
alias p="python"
alias jl="jupyter lab"

# Basic command line operations
alias l="ls"
alias la="ls -a"
alias ll="ls -l"
alias c="clear"
alias o="open"

# Tree
alias t="tree"
alias t1="tree -L1"
alias t2="tree -L2"
alias t3="tree -L3"
alias t4="tree -L4"

# Git
alias gs="git status"
alias ga="git add"
alias gcm="git commit -m"
alias gl="git log"
alias gb="git branch"
alias gba="git branch -a"
alias gf="git fetch"
alias gc="git checkout"
alias gr="git remote"
alias gm="git merge"
alias gp="git push"
alias gpl="git pull"

# Virtual env
sa() {
  if [ -f ".venv/bin/activate" ]; then
    source .venv/bin/activate
  else
    echo "No .venv found in current directory"
  fi
}

alias sd="deactivate"


#---------------------PROMT------------------------
# Function to show virtualenv, defaulting to (base)
virtualenv_name() {
  if [[ -n "$VIRTUAL_ENV" ]]; then
    echo "($(basename $VIRTUAL_ENV))"
  else
    echo "(base)"
  fi
}

# Show current Git branch
parse_git_branch() {
  git rev-parse --abbrev-ref HEAD 2> /dev/null | grep -v 'HEAD' || echo ''
}

# Minimal prompt: (venv) [username] foldername branch %
setopt PROMPT_SUBST
PROMPT=$'%F{cyan}%(1v.%1v .)[%n]%F{white} %F{yellow}%2c%f ${$(parse_git_branch):+"@ %F{white}%F{green}$(parse_git_branch)%F{white}%f"}\n> '

#---------------------PROMT------------------------


# Enable autosuggestions and syntax highlighting (clone the repo first)
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
source ~/.zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
export PATH=$HOME/.npm-global/bin:$PATH
```
and save it with `cmd+x` then `y` then `enter`

After saving the `.zshrc` file, activate it using
```
source ~/.zshrc
```
