---
layout: default
title: Git Fundamentals
nav_order: 1
---

<!-- prettier-ignore-start -->
# Git Fundamentals
{: .no_toc }

By the end of this page, you will be able to set up git to associate your work with your name and email address, create new repositories and add files to them. You will also be able to see the history of your project and compare it to its current state.

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

As we make changes to our code we commit the changes to our git repo.
Before we can commit we must add new or changed files to a staging area.

Let's assume we have a file named `information.txt`.
We can **stage** it with the following command:

`git add information.txt`

We can also add all changed files with:

`git add .`

The add command also accepts sub-folders:

`git add docs/information.txt`

Lastly, if we want to add all files of a certain type, we can do that using a **wildcard** character.

`git add docs/*.txt`
*This will add all text files in the docs folder.*

### Committing Staged Files

We commit our staged changes with a commit message:

`git commit -m "Your explanation of the changes goes here."`

For complex changes, we can include a short title, followed by a long explaination:
`git commit -m "Title" -m "Long description goes here .........."`

# Log and Diff

We can review all previous commits with:

`git log`

Each entry in the log shows:
- The commit hash.
- Who made the commit.
- When it was made.
- The commit message.

We can compare the differences between the current files and the last commit with:

`git diff`

We can compare the differences with specific files too:

`git diff information.txt`

We can also compare specific folders:

`git diff ./docs`

# Using a Git Ignore File

Often when working on a project, there will be files you *don't* want to have saved in your repository. Some examples of these files are:
- Files that include secrets like passwords or API keys.
- Temporary files and folders.
- Build files and folders.
- Hidden OS files like .DS_Store (Mac) or Thumbs.db (Windows) files.

For situations like these, you will need a `.gitignore` file.
These files describe a list of "rules" to decide which files to skip over when staging and committing files.
An example .gitignore might look like this:

```
# Ignore specific files. (Note that comments start with: #)
Thumbs.db
# Wildcards: Ignore all .exe files.
*.exe
# Exception to wildcards: Do track the special.exe file.
!special.exe
# Ignore all files in any folder called build.
build/
# Ignore all .pdf files in the doc/ folder and any of its sub-folders.
doc/**/*.pdf
```

{: .note }
A helpful list of common .gitignore templates for many languages and programs can be found [here].

<!-- prettier-ignore-end -->

[Current Working Directory]: https://hpc.nmsu.edu/onboarding/linux/commands/cd/#:~:text=The%20current%20working%20directory%20is,stands%20for%20Print%20Working%20Directory.&text=The%20name%20of%20the%20current,directory%20in%20the%20absolute%20path.
[here]: https://github.com/github/gitignore