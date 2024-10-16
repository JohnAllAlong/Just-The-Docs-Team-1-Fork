---
layout: default
title: Undoing With Git
nav_order: 2
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

