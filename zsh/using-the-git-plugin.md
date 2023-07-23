# Using the git plugin

The zsh `git` plugin comes with several useful functions:

```zsh
function git_main_branch() {
  command git rev-parse --git-dir &>/dev/null || return
  local ref
  for ref in refs/{heads,remotes/{origin,upstream}}/{main,trunk,mainline,default}; do
    if command git show-ref -q --verify $ref; then
      echo ${ref:t}
      return
    fi
  done
  echo master
}
```

It also includes many useful aliases:

```zsh
alias gbl='git blame -b -w'
alias gcm='git checkout $(git_main_branch)'
alias gd='git diff'
alias gl='git pull'
alias gp='git push'
alias grbm='git rebase $(git_main_branch)'
alias gst='git status'
```
