---
id: advanced_git_configuration
title: Advanced Git configuration
---

## Default branch for new repositories

Starting with Git 2.28 you can set the default branch name.
I recommend you use `main` as this is what GitHub will use by default later this year.

To set the default branch name for new repositories do:

```git
$ git config --global init.defaultBranch main
```

## `git pull` rebase/merge strategy

Git 2.27 and newer will complain at you, every pull, until you set the `pull.rebase` variable.

### Use merge strategy when pulling

This is probably what you want Git to do, as it is the default merge strategy.
This strategy will fast-forward if possible, and create merge commits if needed:

```git
$ git config --global pull.rebase "false"
```

### Use rebase strategy when pulling

To rebase when you pull:

```git
$ git config --global pull.rebase "true"
```