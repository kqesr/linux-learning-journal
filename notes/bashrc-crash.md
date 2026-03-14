# Bash Crash After Editing .bashrc

Date: 2026-03-14

## Problem

While trying to create a shortcut command for ChatGPT, I edited my `~/.bashrc` file.

I accidentally added a line that caused `.bashrc` to load itself again.

This created a loop and caused bash to crash.

## Symptoms

The terminal would not open normally.

I saw an error saying that `/usr/bin/bash` had crashed.

The crash message included `Signal: 11 (SEGV)`.

## What Caused It

The problem was a line inside `.bashrc` that made bash repeatedly source the same file.

That caused infinite recursion until bash crashed.

## Fix

I opened the file from the file manager and removed the bad line.

After saving the file, the terminal opened normally again.

## Lesson Learned

Shell configuration files are powerful.

A single line in a configuration file can completely change how the terminal behaves.
