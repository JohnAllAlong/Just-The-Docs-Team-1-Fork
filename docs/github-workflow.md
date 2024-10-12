---
layout: default
title: Team Git Workflow
nav_order: 3
---

# Team Git Workflow

Git workflows are methods or procedures that dictate how developers interact with the
Git system to achieve effective team collaboration.

Some of the popular workflows used by teams are:
- Centralized Workflow
- Feature Branch Workflow
- Forking Workflow



# Centralized Workflow

All developers work directly on a single branch, often main or master .
Simple and similar to Subversion-style workflows.
Not as powerful or flexible as other workflows.
Suitable for small teams and projects.
Merging can be problematic.



# How a Centralized Workflow Works
1. Initialization: One team member creates the repository with an online remote.
2. Cloning: Each team member creates a local copy by "cloning" the remote.
3. Working Locally: Developers work on the project, committing to their local repo.
4. Resolving Conflicts: When a developer is ready to share their changes, they
must pull outstanding changes from the remote, and resolve merge conflicts as
required.
5. Pushing to Remote: The developer can now push their changes to the central
repo.
6. Synchronizing Team: Others can now pull from the central repo to locally
incorporate the latest changes.
