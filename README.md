# configs

##git

```toml
[alias]
    s = status
    co = checkout
    cob = checkout -b
    del = branch -D

    # Checking the status of your git commit
    st = status -sb

    # List all branches
    br = branch --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(contents:subject) %(color:green)((committerdate:relative)) [%(authorname)]' --sort=-committerdate

    # Add all unstaged files
    save = !git add -A && git commit -m

    # Resets the previous commit on this branch
    undo = reset HEAD~1 --mixed

    # Resets all staged changes
    res = !git reset --hard

    # Push changes to upstream
    done = !git push origin HEAD

    # More readable git log
    lg = !git log --pretty=format:\"%C(magenta)%h%Creset -%C(red)%d%Creset %s %C(dim green)(%cr) [%an]\" --abbrev-commit -30

    # Amend last commit
    cam = commit --amend --message

    # Contributors ordered by number of merges
    rank = shortlog -sn --no-merges

    # Remove all merged branches
    bdm = "!git branch --merged | grep -v '*' | xargs -n 1 git branch -d"

    # Fetches a dad joke
    dad = !curl https://icanhazdadjoke.com/ && echo
```