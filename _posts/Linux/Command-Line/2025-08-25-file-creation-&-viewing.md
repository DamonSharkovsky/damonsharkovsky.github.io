---
layout: post
title: "File Creation and Viewing"
date: 2025-08-25
categories: [Linux]
tags: [Linux, Commands]
---

Today I learned some commands that help with creating files and viewing them inside the terminal. This is very useful compared to always needing to open the file manager. The shell makes it possible to perform these actions quickly, and it is often more efficient and productive than using a graphical interface.

---

## touch

This command creates a new empty file. For example, `touch notes.txt` will create a text file called `notes.txt`. The extension is not important to Linux itself, but other programs will interpret the extension to decide how to open it. If you run `touch` on a file that already exists, it will not overwrite the contents, but it will update the file’s timestamp. This can be seen with `ls -l`, which shows the detailed file information.

---

## file

The `file` command identifies the type of a file. For example, running `file notes.txt` might output “ASCII text.” This is a simple but useful command for checking what kind of file you are working with.

---

## cat (concatenate)

The `cat` command outputs the contents of a file to the terminal. It is useful for small files or for joining multiple files together. When used on files such as PDFs, the output will appear as unreadable symbols.

---

## less

The `less` command is similar to `cat` but is better suited for larger files. Instead of displaying everything at once, it allows you to scroll through the contents page by page. You can navigate with the arrow keys or the spacebar, and exit by pressing `q`. This makes it much more practical when working with logs or longer text files.

---

These commands make it possible to create and view files directly in the terminal. Combined with the navigation commands learned earlier, they expand the ability to manage files without leaving the shell. This approach is more efficient and contributes to a more smoother workflow.

