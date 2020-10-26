# git-redate
### Forked from [Potato Labs](http://taterlabs.com)

Change the dates of several git commits with a single command.

# Installation

Linux: 
Save it into your /usr/bin folder
```sudo chmod 755 git-redate```

# Usage

Simply run: `git redate --commits [[number of commits to view]]`.  You'll have to force push in order for your commit history to be rewritten.

To be able to edit all the commits at once add the --all option: `git redate --all`

**Make sure to run this on a clean working directory otherwise it won't work.**

The `--commits` (a.k.a. `-c`) argument is optional, and defaults to 5 if not provided.


# Changing commit messages

Leverage git rebase functionality:

Rebase all commits starting from the first
```git rebase -i --root```

Change from 'pick' to 'reword' for the commits that you want to change
Save and edit your commits one by one

If you want to push you need to
```git push --force example-branch```
to rewrite history 
