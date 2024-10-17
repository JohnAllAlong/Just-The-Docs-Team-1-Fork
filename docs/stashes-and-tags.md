---
layout: default
title: Stashes and Tags
nav_order: 5
---

<!-- prettier-ignore-start -->
# Remote Repositories
{: .no_toc }

On this page you'll learn about how to use stashes and tags


## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->


# Stashing
Git stash allows you to put aside changes that
you don't want to commit immediately.

### When to Stash?
- You want to switch branches, but you're in the middle of something and don't want
to commit yet.
- You need to pull changes, but you have uncommitted work.

### Stashing in Action
This command stashes your changes, leaving you with a clean working directory:
`git stash`
**Remember, it's only a temporary storage. Don't forget about your stashed
changes!**

### The Stash Stack
Think of 'git stash' as creating a stack
of saved changes.
You can stash multiple sets of
changes and Git will store them in a
LIFO (Last In, First Out) stack.

### Restoring Stashed Changes
To restore stashed changes use:
`git stash pop` - Re-applies the changes and removes them from the stash.
`git stash apply` - Re-applies the changes but keeps them in the stash.

### Other Helpful Stash Commands
`git stash list` : Review all your stashes before deciding to apply or drop them.
`git stash drop` : Removes the most recent stash from the stack without applying it.
`git stash branch` <branchname> : Creates a new branch based on the popped stash.
`git stash clear` : This command removes all your stashes.
`git stash pop 'stash@{n}'` : Pop a specific stash seen in git stash list .

# Tags
**Tags in Git are like bookmarks for important events or milestones in your project.**
They're often used to mark release points (v1.0.0, v1.1.0, etc.).

### Creating Tags
Creating a new lightweight tag:
`git tag <tag-name>`
`git tag <tag-name> <commit hash>`
This will tag the current or specified commit with the provided name.
Tag names should not include spaces. They should only include characters [a-z], [A-Z],
numbers [0-9] and the dash/hyphen [-].

### Annotated Tags
Annotated tags store additional metadata such as the tagger's name, email, date, and
an optional message.
`git tag -a <tag-name> -m "your message here"`

### Once you've Created a Tag
**Checkout to the tag:** You can treat the tag like a branch/commit, and checkout to the
tag's point in history. For instance: `git checkout <tag-name>`
**List tags:** You can list all the tags in the repository using git tag or git tag -l . To
narrow the list based on a search pattern, you can use: `git tag -l "<search-
pattern>"`
**Show tag information:** If you have annotated tags, you can view the associated
information with: `git show <tag-name>`
**Compare differences:** You can compare the differences between the tagged state of
the code and the current HEAD using: `git diff <tag-name>`