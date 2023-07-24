# Using the fixup command during an interactive rebase

The example below is from [thoughtbot](https://thoughtbot.com/blog/git-interactive-rebase-squash-amend-rewriting-history):

```zsh
$ git rebase -i HEAD~4
pick 07c5abd Introduce OpenPGP and teach basic usage
pick de9b1eb Fix PostChecker::Post#urls
pick 3e7ee36 Hey kids, stop all the highlighting
pick fa20af3 git interactive rebase, squash, amend

# Rebase 8db7e8b..fa20af3 onto 8db7e8b
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
# Note that empty commits are commented out
```

If you're squashing many commits, if you use `squash`, you still have to manually discard each commit message.

Instead, you can use `f` or `fixup` to squash these commits and discard their messages.
