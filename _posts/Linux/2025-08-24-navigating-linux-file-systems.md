---
layout: post
title: "Navigating Linux File Systems"
date: 2025-08-24
categories: [Linux]
tags: [Linux, Commands]
---

Prior to this, I learned a bit about the history of Linux and different distributions, just glancing over what each offers. For now, I’m focusing on practical command line usage.


From my understanding, the terminal provides access to the system without a GUI. The Bash shell shows a prompt with `$`, the username, and other symbols. At first, it seemed a bit confusing, but now I understand the layout is just the default way the shell shows where you are and what user you’re logged in as.


---


## PWD (Print Working Directory)


`pwd` shows the current directory. I’ve used it to copy paths and paste them into my code to access local files. The root directory is `/`, and my home directory is represented by `~/`. It’s a simple command, but seeing the full path of where I am helps me understand the structure of the filesystem.


---


## CD (Change Directory)


`cd` changes directories. I use it constantly to move around the terminal, often pasting paths I get from `pwd`. Some shortcuts I’ve found helpful include:
- `cd ..` → go back one directory
- `cd -` → go to the previous directory
- `cd` → go to the home directory (same as `cd ~`)


Learning these shortcuts has made moving around much faster, and it’s interesting to see how small commands can save time.


---


## LS (List Directories)


`ls` lists the contents of a directory. I use it to see what’s inside folders since there’s no GUI. Some useful flags include:
- `-a` → show hidden files
- `-l` → show detailed info like permissions, number of links, owner, group, file size, modification date, and filename


A cool thing I discovered is that you can combine flags, like `ls -al`, to show detailed info for all files, including hidden ones. The order of flags doesn’t seem to matter, which I still want to research more, but overall `ls` has been a key tool for navigating the terminal.


---


These commands (`pwd`, `cd`, `ls`) form the foundation of navigating the terminal. I’m still a beginner, but practicing them helps me feel more comfortable moving through directories and understanding the Linux filesystem. It’s simple stuff, but seeing how it all connects makes learning more concrete.