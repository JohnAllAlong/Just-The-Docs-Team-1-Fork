---
layout: default
title: Remote Repositories
nav_order: 4
---

# Remote Repositories

A *remote repository* is a version of your project that is hosted on a remote server.

It can **interact** with **local repositories**, allowing you to push your
changes to others and pull their changes to your local repository.


### Introduction to GitHub

*GitHub* is a hosting platform for Git repositories owned by
Microsoft.

It provides a **web-based interface** to interact with your repositories and adds social and collaboration features.

### Some Remote Repo / GitHub Terminology:
- **Push**: Send your changes to a remote repository.
- **Pull**: Fetch and merge changes from a remote repository into your current branch.
- **Clone**: Make a full copy of a repository at its current state.
- **Fork**: Create a copy of someone else's repository in your own GitHub account.

# Adding and Configuring a Repo to GitHub
To save a local Git repository to your GitHub account, create a new repository by way 
of the "+" button in the top right corner of the GitHub website.

### Linking Your Local Repo to GitHub

Let's say you've created a new repo on GitHub called `My-Lovely-Repo` 
and you've already initialized this project's local git repository.

From the command line (within your project folder) add GitHub as a remote:

`git remote add origin git@github.com:<username>/My-Lovely-Repo.git`

This should be all in one line with <username> replaced by your actual username.
You can also check if a remote has been added to a repo:

`git remote -v`

If you don't have a local copy of a Github repo, you can **clone** it: 

`git clone git@github.com:<username>/<repo-name>.git`

When you want to **push** the latest state of your repo to Github:

`git push origin <branch-name>`

When you want to **pull** the latest commits from Github:

`git pull origin <branch-name>`

