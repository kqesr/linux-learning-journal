# Bash Crash After Editing .bashrc

Date: 2026-03-14

## Problem

While creating a command shortcut for ChatGPT, I edited my `~/.bashrc` file.

I accidentally added a line that sourced `.bashrc` from inside itself.

source ~/.bashrc

This caused bash to repeatedly load itself until it crashed.

## Symptoms

The terminal would not open.

Error message:

Program '/usr/bin/bash' crashed  
Signal: 11 (SEGV)

The stack trace showed recursive loading of shell configuration files.

## Fix

I opened the Dolphin file manager and enabled **Show Hidden Files**.

I navigated to:

/home/kqesr

Then edited:

.bashrc

I removed the recursive line.

After saving the file, the terminal opened normally again.

## Lesson Learned

Shell configuration files control the behavior of the entire shell environment.

Shell configuration files control how the terminal starts, so even a single line can break the shell.
