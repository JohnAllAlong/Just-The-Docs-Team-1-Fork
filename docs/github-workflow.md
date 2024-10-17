---
layout: default
title: Team Git Workflow
nav_order: 3
---


<!-- prettier-ignore-start -->
# Team Git Workflow
{: .no_toc }

By the end of this page, you will be able to differentiate the different team git workflows, such as 
the centralized workflow, feature branch, and the forking workflow.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->

# What Is a Git Workflow?

**Git workflows** are *methods* or *procedures* that dictate how developers interact with the
Git system to achieve effective team collaboration.

### Some of the Most Popular Git Workflows

1. Centralized Workflow
2. Feature Branch Workflow
3. Forking Workflow



# 1. Centralized Workflow

All developers work directly on a single branch, often main or master.
Simple and similar to Subversion-style workflows.
Not as powerful or flexible as other workflows.
Suitable for small teams and projects.
Merging can be problematic.



### How a Centralized Workflow Operates
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


# 2. Feature Branch Workflow
All feature development or bug fixes are done in dedicated branches. It
isolates new development from the main branch, making it easy to discard experimental changes.
It also facilitates code review through pull requests.

**Note**: *This workflow is sometimes called GitHub Flow.*

### The Distinct Properties of a Feature Branch Workflow
- Branching: New features or fixes are developed locally in a short-lived branch.
- Resolving Conflicts: Remote commits by other developers can be pulled into the
local feature branch, with merge conflicts resolved as required.
- Pushing to Remote: Completed and resolved branches are then pushed.
- Requesting a Remote Merge: A pull request is next initiated on the git hosting
service (example: GitHub).
- Reviewing: One or more team members review the pull request before merging it
into the main remote branch.

**Note**: *Pull requests can be sent back unmerged if rework is deemed necessary.*

# 3. Forking Workflow
Often used for open source projects, in this workflow, each developer gets not only their
local repository, but also a server-side copy of the project.
- Developers push to their server-side repositories.
- Changes are shared via pull requests from their public repository.
- The project maintainer has the final say on what is merged into the official
repository.

### The Forking Workflow Features
- Forking: Each team member creates a fork of the project on the git hosting	
service.
- Cloning: Team members clone their remote fork to a local repo.
- Adding an Upstream: Team members configure a secondary remote called
upstream that points to the official repo.
- Resolving Conflicts: Remote commits from upstream can be pulled into the
local feature branch, with merge conflicts resolved as required.
- Pushing to Remote: Local feature branches are pushed to the forked remote.
- Requesting a Remote Merge: Pull requests are initiated to request merges from
the remote fork to the official upstream repo.

There are more types of git workflows, such as the [pull request workflow], which shares the same goal of
having an effective team collaboration.
For more information about team git workflows, click [here].

----------

[here]: https://www.atlassian.com/git/tutorials/comparing-workflows
[pull request workflow]: https://medium.com/@urna.hybesis/pull-request-workflow-with-git-6-steps-guide-3858e30b5fa4


