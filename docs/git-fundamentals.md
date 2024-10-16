---
layout: default
title: Git Fundamentals
nav_order: 1
---

<!-- prettier-ignore-start -->
# Git Fundamentals
{: .no_toc }




## Table of Contents
{: .no_toc }

1. TOC
{:toc}

# Configuring Git

After installing git, you can configure the name and email address that will be associated with your commits.
To do so, use the following commands:

`git config --global user.name "Your Name"`
`git config --global user.email "your.email.example.com"`

# Initializing a Repo

To create a new git repository in the [Current Working Directory], use the initialization command:

`git init`

Git defaults to using the word "master" (as in "master copy" or "master recording") for
the main branch, but we can change this:

`git branch -m main`

{: .note }
Creating a git repository adds an invisible `.git` folder. To see it, be sure to show hidden items in your file explorer.

### Checking Your Repo's Status

The status command will display the current status of the repository. This is helpful for checking if you are up to date with the changes present on a remote repository, or if you have modified files to stage/commit. The status command is simply:

`git status`

# Staging and Committing Files

# Log and Diff

# Using a Git Ignore File

<!-- prettier-ignore-end -->

[Current Working Directory]: https://hpc.nmsu.edu/onboarding/linux/commands/cd/#:~:text=The%20current%20working%20directory%20is,stands%20for%20Print%20Working%20Directory.&text=The%20name%20of%20the%20current,directory%20in%20the%20absolute%20path.