---
layout: default
title: Branches
nav_order: 4
---

# What is a Branch?
In Git, branches are like alternate timelines in a sci-fi movie.

They allow you to work on different features or fixes without affecting the main project
timeline until you choose to merge the timelines back together. 

# Creating Branches
Creating a new branch:
`git branch <branch-name>`
Switching to a branch:
`git checkout <branch-name>`
Create a switch in a single command:
`git checkout -b <branch-name>`

# Merging Branches
Branching allows for isolated development, and merging brings those developments
back into the main timeline.
Let's say we've been working and committing to an experimental branch and we
want to merge those commits back into main:
`git checkout main`
`git merge experimental`

### Merge Conflicts
Merge conflicts occur when Git can't automatically merge two branches.
When a merge conflict happens, Git will alert you in the terminal and mark the areas of
conflict in the file.

### Git's Markup of Conflicted Files
Git uses special markers to indicate the start and end of the conflicted area:
- `<<<<<<<` HEAD shows the start of the changes in the current branch.
- `=======` separator between the changes in the current and the other branch.
- `>>>>>>>` branch-name shows the end of the changes in the other branch.

### Resolving Merge Conflicts
**To resolve a merge conflict:**
1. Edit the file to fix the conflicting changes. Be sure to remove the conflict markers.
2. Add the file to the staging area with git add .
3. Commit the fix with `git commit`.