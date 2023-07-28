# Adding only modified files

If you do `git add`, it will stage all modified and new files.

Instead, you can do `git add --update` to add only modified files.

```zsh
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
    modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
    git/add-only-modified-files.md

$ git add --update --verbose
add 'README.md'
```
