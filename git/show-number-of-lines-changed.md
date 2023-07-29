# Showing the number of lines added and removed

For untracked changes:

```zsh
$ git diff --shortstat
5 files changed, 97 insertions(+), 78 deletions(-)
````

For staged changes:

```zsh
$ git diff --shortstat --cached
5 files changed, 97 insertions(+), 78 deletions(-)
````
