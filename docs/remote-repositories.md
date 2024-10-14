---
layout: default
title: Remote Repositories
nav_order: 4
---

<!-- prettier-ignore-start -->
# Remote Repositories
{: .no_toc }

On this page, you will learn about remote repositories and how you can use them for your projects.
You will also learn how to use GitHub commands for your remote repo, as well as using SSH keys 
for authentication.


## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->

# What Is a Remote Repository?

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





### SSH Keys for Authentication (Optional)

- Generate a *public/private* key pair, from the *Git Bash* terminal:

`ssh-keygen -t ed25519 -C "your_email@example.com"`

- Press `Enter` to accept the default save path, and make note of this path.

**Note**: *It's good practice to secure your keys with a passphrase. Just don't forget it.*

- Navigate to the save path, open the `id_ed25519.pub` file and copy-paste its
contents here.


- Test your from the terminal: `ssh -T git@github.com` (Type `yes` when
prompted.)