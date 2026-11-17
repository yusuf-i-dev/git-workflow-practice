# git-workflow-practice

Practice repo for core Git workflow: branch, PR, merge.

## Workflow
- `main` only changes through pull requests
- Branch off `main` using `<type>/<short-description>`, e.g. `docs/branch-pr-workflow`
- Open a PR into `main`, review the diff, merge, then delete the branch
- Pull `main` locally after every merge

## Commands
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
