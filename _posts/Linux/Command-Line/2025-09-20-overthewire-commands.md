---
layout: post
title: "OverTheWire: Bandit Part 1 (Linux Challenge)"
date: 2025-09-20
categories: [Linux]
tags: [Linux, OverTheWire, CommandLine]
---

I started the [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) challenges to improve my Linux command-line skills. Each level teaches new commands, techniques, or concepts, and this journal documents my experience, thought process, and lessons learned.

---

## [Bandit0](https://overthewire.org/wargames/bandit/bandit0.html)

**Password:** <details>bandit0</details>

**Challenge:** Access a file in the home directory.  

**What I did:** Simple `ls` in the home directory showed `readme`. Using `cat readme` revealed the password.  

**Reflection:** Even the simplest tasks are important to reinforce basic file navigation commands. It's satisfying to see immediate results from `ls` and `cat`.

---

## [Bandit1](https://overthewire.org/wargames/bandit/bandit1.html)

**Password:** <details>ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If</details>

**Challenge:** Read a file named `-`.  

**What I did:** Remembered that files starting with `-` can be tricky. Used `cat ./-` to access it.  

**Reflection:** Learned about how `./` refers to the current directory and how Linux interprets filenames starting with special characters. Small tricks like this save a lot of confusion later.

---

## [Bandit2](https://overthewire.org/wargames/bandit/bandit2.html)

**Password:** <details>263JGJPfgU6LtdEvgfWU1XP5yac29mFx</details>

**Challenge:** Read a file with spaces in the name.  

**What I did:** Initially confusing. I typed the first `-` and pressed tab for auto-completion, then used `cat` to read the file. Learned that spaces in filenames require escaping with `\` or prefixing with `./`.  

**Reflection:** This taught me about filename parsing in Linux. Understanding how the shell treats spaces as argument separators is essential. Tab completion is a lifesaver.

---

## [Bandit3](https://overthewire.org/wargames/bandit/bandit3.html)

**Password:** <details>MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx</details>

**Challenge:** Hidden file inside `inhere` directory.  

**What I did:** `cd inhere` then `ls -a` to list hidden files. `cat` revealed the password.  

**Reflection:** Reinforced the importance of `ls -a` for hidden files and understanding directory structures.

---

## [Bandit4](https://overthewire.org/wargames/bandit/bandit4.html)

**Password:** <details>2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ</details>

**Challenge:** Identify the human-readable file among many.  

**What I did:** Opened files manually until I realized wildcards (`*`) can open multiple files at once with `cat ./-file*`.  

**Reflection:** Learned the power of wildcards in reducing repetitive typing and speeding up workflows.

---

## [Bandit5](https://overthewire.org/wargames/bandit/bandit5.html)

**Password:** <details>4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw</details>

**Challenge:** Find a file of a specific size using `find`.  

**What I did:** Used `find . -type f -size 1033c`. Learned about the `c` flag representing bytes.  

**Reflection:** First hands-on experience with `find` and its flags, which is crucial for more complex searches in Linux.

---

## [Bandit6](https://overthewire.org/wargames/bandit/bandit6.html)

**Password:** <details>HWasnPhtq9AVKe0dmk45nxy20cvUa6EG</details>

**Challenge:** Find a file with a specific user/group ownership and size.  

**What I did:** `find` with `-user`, `-group`, `-size` and ignored errors with `2>/dev/null`.  

**Reflection:** Learned about Linux file ownership, permissions, and error handling. It was challenging but helped me understand the filesystem hierarchy better.

---

## [Bandit7](https://overthewire.org/wargames/bandit/bandit7.html)

**Password:** <details>morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj</details>

**Challenge:** Find a specific string in a file.  

**What I did:** Used `grep "millionth" data.txt`.  

**Reflection:** My first real use of `grep`. Searching text efficiently is fundamental in Linux, and learning this command is going to save time in the future.

---

## [Bandit8](https://overthewire.org/wargames/bandit/bandit8.html)

**Password:** <details>dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc</details>

**Challenge:** Identify unique lines in a file.  

**What I did:** Piped `sort data.txt | uniq -u` to find the unique line.  

**Reflection:** Learned about combining commands with pipes (`|`) to process data efficiently. It’s a practical introduction to Linux text processing.

---

## [Bandit9](https://overthewire.org/wargames/bandit/bandit9.html)

**Password:** <details>4CKMh1JI91bUIZZPXDqGanal4xvAg0JM</details>

**Challenge:** Non-standard filename access.  

**What I did:** Used `cat` with proper path and escaping.  

**Reflection:** Reiterated lessons on filename parsing, path references, and command accuracy.  

---

## Overall Reflection

OverTheWire Bandit has taught me:

- How to navigate directories and handle tricky filenames
- Searching files with `find`, `grep`, and handling permissions
- Piping and text processing commands like `sort` and `uniq`
- The mindset of experimentation and learning through problem-solving

Even small levels build confidence and understanding. Each challenge reinforces Linux fundamentals while introducing new concepts incrementally.  

---