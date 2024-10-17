---
layout: default
title: The Git Life Cycle
nav_order: 2
---


<!-- prettier-ignore-start -->

# The Git Life Cycle
{: .no_toc }
This page serves as a high-level overview of the git life cycle. 
For a detailed step-by step instruction of how to direct files within your project, refer to the Git Fundamentals page.

![image of life cycle](https://git-scm.com/book/en/v2/images/lifecycle.png)

(Image Source: [https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository]())

## Breakdown
If you are working locally to start, you will have already initialized your local repository. Otherwise, you must clone the desired remote Git repository to make a local working copy. 

When using Git, each file in your working directory can be in one of either two states: untracked or tracked. After initializing your repository, all files will be in a tracked state.
- Untracked files are ones that Git does not know about, if they weren't part of your last commit and have not yet been staged. This includes any newly created or added files.
- Tracked files are everything else - files that were in the last commit, or have been staged. They can be modified, unmodified, or staged.
