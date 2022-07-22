# git_learn
MY GIT ALIAS

```
## ALIAS ##
alias cdap="cd /Users/harshitbolt/admin-panel"
alias cds="cd /Users/harshitbolt/repos/taxify/server"
alias gcd="git checkout develop && git pull origin develop"
alias gph='git push'
alias gcm='git commit -m'
alias gst='git status'
alias gb='git branch'
alias gco='git checkout'
alias gcob='git checkout -b'
alias glg='git log'

## FUNCTION
function gac {
  if [[ $# -eq 0 ]]
    then git add . && git commit
  else
    git add . && git commit -m "$*"
  fi
}
# USAGE
gac <optional_commit_message_without_quotes>

```
