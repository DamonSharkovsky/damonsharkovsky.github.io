---
layout: post
title: "File Management"
date: 2025-08-29
categories: [Linux]
tags: [Linux, Commands]
---

Today I explored file management commands in Linux from learning how to create, delete, and manage files directly from the shell. This approach saves time and feels much more efficient than relying solely on graphical tools.

## Wildcards

Wildcards are special characters that simplify working with multiple files:

- `*` matches zero or more characters (e.g., `*.txt` matches all `.txt` files).  
- `?` matches a single character (e.g., `file?.txt` matches `file1.txt`, `fileA.txt`, but not `file10.txt`).  
- `[ ]` matches a range or set of characters (e.g., `file[1-3].txt` matches `file1.txt`, `file2.txt`, and `file3.txt`).  

They become especially useful when combined with commands such as `cp`, `mv`, and `rm`.

## cp (Copy)

The `cp` command is more versatile than I initially thought. Beyond simply duplicating a file, it includes options for safer and more controlled copying:

- `-i`: Prompt for confirmation before overwriting.  
- `-p`: Preserve file attributes (timestamps, permissions).  
- `-r`: Copy directories recursively.  

Using wildcards with `cp` makes it easy to copy groups of files at once.

## mv (Move / Rename)

In the terminal, renaming a file is just moving it to the same directory under a new name.  
Example:  
```bash
mv oldname.txt newname.txt
```  

Useful options:  
- `-i`: Prompt before overwriting.  
- `-b`: Create a backup before overwriting.  
- `-r`: Move directories recursively.  

## mkdir (Make Directory)

`mkdir` creates directories. Multiple directories can be made in one command:  
```bash
mkdir dir1 dir2 dir3
```  

The `-p` flag allows nested directory creation:  
```bash
mkdir -p books/hemingway
```  

## rm (Remove)

`rm` deletes files and directories permanently. There is no “trash bin,” so caution is required.

Options include:  
- `-i`: Prompt before deleting.  
- `-r`: Remove directories recursively.  
- `-f`: Force deletion without confirmation.  

Be careful: combining `-i` and `-f` defaults to force deletion, bypassing prompts.  

The infamous command:  

![rm](assets/img/linux/4e22zVJ5Kz9J6yxy3oRksfH8uOANfXaScoSlMY75YrM.jpg)


```bash
sudo rm -rf ./*
```
- `sudo`: Run as superuser.  
- `rm`: Remove command.  
- `-rf`: Recursive, forced deletion.  
- `./*`: Everything in the current directory (including hidden files).  

It is fast, powerful, and dangerous.

## find

The `find` command locates files and directories:

- `-name`: Search by filename (supports wildcards).  
- `-type`: Search by type (e.g., `f` for files, `d` for directories).  

It is a flexible tool that pairs well with other commands.

## wc (Word Count)

`wc` counts lines, words, or bytes.

- `-l`: Count lines.  

It is often used with pipelines (`|`) to process command output. Example:  
```bash
find . -name "*.txt" | wc -l
```
This counts the number of `.txt` files in the current directory and its subdirectories.

## Final Thoughts

Learning these commands has completely changed how I work in Linux. From renaming and copying files to managing directories, everything feels faster and more precise. The combination of wildcards, flags, and pipelines makes the command line a powerful environment one I am starting to rely on more every day.