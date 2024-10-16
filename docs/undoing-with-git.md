---
layout: default
title: Undoing With Git
nav_order: 2
---

Undoing with Checkout
Let's say you made a bunch of changes to your readme.md that you now regret.
If you haven't committed these changes, you can undo them like this:
git checkout readme.md
If you want to revert all folders and files to the most recent commit:
git checkout .
WARNING: Slightly dangerous. The discarded changes cannot be recovered!

When to Undo with Checkout?
The simplest private undo. Discard uncommitted local changes.
git checkout <path-or-filename>
Works if:
The changes you wish to undo haven't yet been committed. (Dirty files.)
You wish to revert to the most recently committed version of a file or files.

