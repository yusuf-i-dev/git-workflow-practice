# git-workflow-practice

Scratch repo where I practice the day-to-day Git flow: branch, PR, merge, pull.

## How I work in this repo

`main` only changes through a pull request. Branches are named `<type>/<short-description>`, for example `docs/branch-pr-workflow`. After a merge I delete the branch and pull `main`.

```
git switch -c docs/branch-pr-workflow
git add README.md
git commit -m "docs: document branch and PR workflow"
git push -u origin docs/branch-pr-workflow
# open the PR on GitHub, review, merge
git switch main
git pull
git branch -d docs/branch-pr-workflow
git fetch --prune
```

## Windows note

Point Git at the built-in OpenSSH so it uses the Windows ssh-agent:
```
git config --global core.sshCommand "C:/Windows/System32/OpenSSH/ssh.exe"
```
