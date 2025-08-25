---
layout: post
title: Tools Setup 2025-26
description: My Journey with Tools Setup and Refresh
permalink: /sprint/1/tools
menu: nav/sprint_1.html
toc: True
comments: True
---

# Tools Setup 2025-26

## Overview

This year’s setup process was smoother because I already had most of my tools configured from last year. I was already familiar with **GitHub, VSCode, and WSL**, and I had previously worked with Linux commands for installing dependencies and managing repositories. The main update was moving to **WSL Ubuntu 24.04** (from 22.04), which went smoothly thanks to my prior experience.  

The most important change in workflow this year was how we connected to the course repository. Instead of using the **OCS repository as a template** like last year, we had to **fork from the upstream OCS repo** and then clone our fork. This ensures that we can pull updates from upstream while still having our own repository for commits and customization. Once I made this adjustment, the GitHub integration with VSCode worked as expected.  

I verified that the setup worked by running the **Makefile**, confirming my environment builds properly and that my site runs both on **localhost** and when deployed to **GitHub Pages**.

<img src="{{ site.baseurl }}/images/00_rg_imgs/sprint1/forked.png" alt="Forked Repository">

<img src="{{ site.baseurl }}/images/00_rg_imgs/sprint1/make.png" alt="Successful Make">

## Easy Access Shell Command Descriptions:

<ul>
  <li><b>wsl</b> – access Windows Subsystem for Linux (Ubuntu 24.04)</li>
  <li><b>cd</b> – change directory</li>
  <li><b>mkdir</b> – create directory</li>
  <li><b>echo</b> – print text</li>
  <li><b>sudo</b> – run commands with elevated privileges</li>
  <li><b>apt</b> – install or manage packages on Linux</li>
  <li><b>git</b> – version control system to manage repositories</li>
  <li><b>code</b> – open VSCode from the terminal</li>
  <li><b>ls</b> – list files and directories</li>
  <li><b>rm</b> – remove files or directories</li>
  <li><b>cp</b> – copy files or directories</li>
  <li><b>mv</b> – move or rename files or directories</li>
  <li><b>find</b> – search for files or directories</li>
  <li><b>grep</b> – search for text patterns inside files</li>
</ul>

## Version Control 

**GitHub and VSCode Setup**
- GitHub is used for remote storage of repositories, while Git tracks version control locally.  
- I forked the **upstream OCS repo**, then cloned my fork into WSL.  
- VSCode with GitLens helps me view commit history, differences, and branches.  

<img src="{{ site.baseurl }}/images/00_rg_imgs/sprint1/gitlens.png" alt="Git Commits">

**Files on Local Machine**
- Cloned repositories are stored inside WSL and can be opened directly in VSCode.  
- Navigation is done with standard Linux shell commands.  

**Updating GitHub**
- *Commit*: Save changes locally.  
- *Push*: Send commits to my fork on GitHub.  
- *Pull*: Sync changes from upstream or my remote fork.  

**Running Makefile**
- Running `make` ensures Ruby, Python, and Jekyll dependencies build correctly.  
- Successfully running the Makefile means the local server (`localhost:4600`) mirrors what will be deployed.

## Localhost vs. Deployed Server and DNS

- **Localhost**: Runs at `http://127.0.0.1:4600/risha_guha_2026`. Only visible to me.  
- **Deployed GitHub Pages**: Runs at `https://blackstar3092.github.io/`. Publicly accessible after pushing commits.  

## Tools Verification

**Installed Versions**
- git: 2.43.0  
- ruby: 3.2.3  
- python: 3.12.3  

When setting up Ruby, I initially ran into a permissions issue. Running the install under a `venv` and with administrator permissions solved the problem.  

## Reflection

This week, I didn’t need to start from scratch because most of my toolchain was already in place. The biggest improvement in my workflow was understanding the difference between **forking from upstream vs. using a template**. Forking allows me to pull updates from the teacher’s repository, which keeps my work synced and prevents me from falling behind.  

I also improved my confidence in verifying the setup by checking GitHub commits, confirming Makefile builds, and testing both localhost and deployed versions of my site. This makes my development process smoother and more professional.
