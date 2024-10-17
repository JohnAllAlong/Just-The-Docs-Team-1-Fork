---
layout: default
title: Undoing With Git
nav_order: 4
---

# Undoing with git

On this page, you will learn about the various ways you can undo changes in Git, how they work,
and when you should use them!

# Undoing with Checkout
Let's say you made a bunch of changes to your readme.md that you now regret.
If you haven't committed these changes, you can undo them like this:
git checkout readme.md
If you want to revert all folders and files to the most recent commit:
git checkout .
WARNING: Slightly dangerous. The discarded changes cannot be recovered!

# When to Undo with Checkout?
The simplest private undo. Discard uncommitted local changes.
git checkout <path-or-filename>
Works if:
The changes you wish to undo haven't yet been committed. (Dirty files.)
You wish to revert to the most recently committed version of a file or files.

# When to Undo with Reset?
Use git reset to undo one or more commits in our local repository.
WARNING: Dangerous. The rewrites history by changing the HEAD pointer.
A git reset comes in two main flavors:
Hard Reset (Dangerous)
Soft Reset (Weird)

# Hard Reset
Hard reset: Changes your working directory to match a specific commit.
git reset --hard [commit id]
WARNING: Uncommitted changes lost. All files are reset to the specified commit!

# Soft Reset
Soft reset: Keeps your changes in the working directory, but still resets the HEAD.
git reset --soft [commit id]
WEIRD: HEAD and your working directory may differ if you had uncommited
changes.

# Reverting Commits
git revert <commit id>
Creates a new commit that undoes changes from the specified commit.
The Safest Undo Choice!
Reverting maintains history, making it a safe choice for:
Undoing local commits.
Undoing commits pushed to a remote repo.

# When to Use Revert?
Use git revert to run a specific commit in reverse.
Typically used to undo a commit that has been shared with others.
The public undo - it says, 'I made a mistake, but I want to keep a record of it.'

# Reverting Multiple Commits
The git revert command reverts a single commit by default.
We can run it mutiple times to revert multiple commits:
git revert D
git revert C
Or we can revert a sequence of commits: (Each commit is reverted separately!)
git revert C^..D
If you only want a single revert commit: (The -n stands for "no commit".)
git revert -n C^..D
git commit -m "Revert commits C through D inclusively."

# Clean
git clean [-d] [-f] [-i] [-n] [-q] [-e <pattern>] [-x | -X] [--] [<pathspec>…​]

The clean command removes untracked files from the working tree
It does this by recursively removing files that are not under version control, starting from the current directory.
This behaviour can be altered with the following commands:

-d
Normally, when no <pathspec> is specified, git clean will not recurse into untracked directories to avoid removing too much. Specify -d to have it recurse into such directories as well.

-f
If the Git configuration variable clean.requireForce is not set to false, git clean will refuse to delete files or directories unless given -f. 
Git will refuse to modify untracked nested git repositories (directories with a .git subdirectory) unless a second -f is given.

-i
Show what would be done and clean files interactively.

-n
Don’t actually remove anything, just show what would be done.

-q
Be quiet, only report errors, but not the files that are successfully removed.

-e <pattern>
Use the given exclude pattern in addition to the standard ignore rules

-x
Don’t use the standard ignore rules, but still use the ignore rules given with -e options from the command line. This allows removing all untracked files, including build products.

-X
Remove only files ignored by Git. This may be useful to rebuild everything from scratch, but keep manually created files.

# When To Use Clean
Whenever there are unnecessary/untracked files you wish to remove from the repo.