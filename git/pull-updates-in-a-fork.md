# How to pull updates in a forked repository from upstream

First, set your upstream to the repository you forked from: `git remote add upstream ORIGINAL_REPOSITORY_URL`.

To pull updates:

```zsh
git fetch upstream
git merge upstream/main
```
