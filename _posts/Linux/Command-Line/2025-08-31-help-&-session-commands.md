---
layout: post
title: "Help and Session Commands"
date: 2025-08-31
categories: [Linux]
tags: [Linux, Commands]
---

These are helpful Linux commands I have learned. They provide guidance directly in the terminal, which makes my workflow faster and reduces how often I need to search online.

---

## history

The `history` command shows the commands I have run in the terminal. My list is currently at 1998 entries, which shows how much I rely on it.

Shortcuts I use with history:
- `Ctrl + R` — reverse-search command history. Start typing to find a previous command that matches.
- Up arrow (`↑`) — cycle through recent commands from this session.
- `!!` — run the last command again.

`Ctrl + R` is the most useful for me when I forget exact syntax.

---

## clear

`clear` wipes the terminal screen so I can focus on the next task. It does not delete command history; it only clears what is displayed.

---

## help

Most commands support a quick help flag:
```bash
command --help
```
This prints a short description and available options. Not every program includes detailed help text, so sometimes it is limited.

---

## man (manual)

`man` opens the full manual page for a command:
```bash
man ls
```
It includes usage, options, and more detail than `--help`. Press `q` to quit the manual page. It can feel long, but it is the most reliable built-in documentation.

---

## whatis

`whatis` gives a one-line summary:
```bash
whatis ls
```
Example output:
```
ls (1) - list directory contents
```
---

## alias

`alias` creates a shortcut for a longer command:
```bash
alias ll='ls -la'
```
Typing `ll` will now run `ls -la`.

Aliases created this way last only for the current session. Remove one with:
```bash
unalias ll
```

To make an alias permanent, add it to `~/.bashrc` using a text editor:
```bash
nano ~/.bashrc
```
Add your alias line, save, then reload:
```bash
source ~/.bashrc
```

An example I use:
```bash
alias clearall='clear && source ~/.bashrc'
```
---
## exit

`exit` (or `logout`) ends the current terminal session. I sometimes still use `Alt + F4` out of habit from Windows, but `exit` is the proper way inside the terminal.

---

These commands may seem basic, but they are some of the most practical tools I use every day. They streamline my workflow, help me troubleshoot without leaving the terminal, and make learning Linux more natural. Having them at hand means I never forget the essentials. This marks the end of the command line section from Linux Journey.