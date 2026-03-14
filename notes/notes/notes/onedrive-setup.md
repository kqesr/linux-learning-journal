# OneDrive Setup on Arch Linux

Date: 2026-03-14

## Goal

Set up OneDrive so my Arch Linux desktop can synchronize files with my Microsoft account.

## Problem

Linux does not include built-in OneDrive integration, so I needed to install a command-line client.

## Steps Taken

Installed the OneDrive client.

Command used:

sudo pacman -S onedrive

After installing, I started the configuration process:

onedrive

This opened an authentication process where I logged into my Microsoft account.

## Observations

The login process required copying a link into the browser and then pasting the authentication response back into the terminal.

After authentication, the configuration files were created.

## Solution

After completing authentication, the OneDrive client was able to synchronize files.

The command below can be used to start syncing manually:

onedrive --synchronize

## Lesson Learned

Many cloud services on Linux use command-line tools instead of graphical applications.
