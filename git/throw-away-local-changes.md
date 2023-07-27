# How to throw away local changes to tracked files

If you want to throw away your local changes, git stash is one option.

```zsh
$ git status
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
    modified:   README.md

$ git stash
Saved working directory and index state WIP on main: 8eb5625 Add how to activate virtualenv in a Makefile

$ git status
On branch main
Your branch is up to date with 'origin/main'.
```

However, these get stored in your dirty working directory (you can get them back by using `git stash pop`).

If you don't need any of these changes, use `git checkout --force` or `gco -f` if you're using `zsh`'s git plugin.

```zsh
$ gco -f
Your branch is up to date with 'origin/main'.
```
