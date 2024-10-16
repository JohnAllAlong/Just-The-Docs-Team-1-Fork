---
layout: default
title: REMEMBER TO CHANGE THIS LATER
nav_order: 4
---

<!-- prettier-ignore-start -->
# Remote Repositories
{: .no_toc }

This page will cover an abundance of git topics such as branches, resolving merge conflicts, stashing, tags and more. After covering all of the material you will have a better understanding on how to properly use them to the best of your ability.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->

# What is a Branch?


# Creating Branches


# Merging Branches


# Resolving Merge Conflicts
If Git can't automatically merge two branches a merge conflict will occur. It will notify you in the terminal and mark the areas of conflict in the file.

# Resolving Merge Conflicts


# Stashing

### Introduction to Stashing
Stashing is a way to temporarily save your modified changes in a project. You can choose to stash your uncommited work if:
- You want to switch branches.
- You have changes to pull.

You can have multiple stashes and they will be stored in a Last In, First Out fashion.

This command will stash your changes and give you a clean work directory:
`git stash`
Note: The storage is only temporary so do not forget about your stashes!

To re-apply the modifications and remove them from the stash.
`git stash pop`
To re-apply the modifications and keep them in the stash.
`git stash apply`

### More Stash Commands
These commands may be useful to know.

To see a log of all your current stashes:
`git stash list`
If you want to remove and delete the modifications of your most recent stash:
`git stash drop`
?
`git stash branch <branchname>`
Remove all your stashes:
`git stash clear`
?
`git stash pop 'stash@{n}'`

# Tags




# Other Interesting/Useful Git Topics