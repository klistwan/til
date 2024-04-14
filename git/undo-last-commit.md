# How to undo the last commit

If it's not pushed yet, run `git reset --soft HEAD~`

If it's pushed:

```zsh
git reset --hard HEAD~1
git push -f <remote> <branch>
```
