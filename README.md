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
alias gphs='git push --set-upstream origin $(git branch --show-current)'

## adds and commits
## gac <optional_commit_message_with_no_quotes>
function gac {
  if [[ $# -eq 0 ]]
    then git add . && git commit
  else
    git add . && git commit -m "$*"
  fi
}

## adds, commits and pushes
## gacp <optional_commit_message_with_no_quotes>
function gacp {
  if [[ $# -eq 0 ]]
    then git add . && git commit && git push
  else
    git add . && git commit -m "$*" && git push
  fi
}

## adds, commits and pushes with setting upstream (useful for first commit)
## first_commit <optional_commit_message_with_no_quotes>
function first_commit {
  if [[ $# -eq 0 ]]
    then git add . && git commit && git push --set-upstream origin $(git branch --show-current)
  else
    git add . && git commit -m "$*" && git push --set-upstream origin $(git branch --show-current)
  fi
}

## checkout to develop, pull develop from origin, checkout back to current branch and merge it with develop
function merge_develop {
curr_branch=$(git branch --show-current)
echo current branch is $curr_branch
echo "=======START==========="
echo checkout to develop
git checkout develop
echo "=================="
echo pulling develop from origin
git pull origin develop
echo "=================="
echo checkout to $curr_branch
git checkout $curr_branch
echo "=================="
echo merging develop to $curr_branch
git merge develop
echo "=======FINISH==========="
}
```
