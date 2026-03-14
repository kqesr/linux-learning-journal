# OneDrive Setup on Arch Linux

Date: 2026-03-14

## Goal

Configure OneDrive on my Arch Linux workstation so I could synchronize files with my Microsoft account.

## Problem

Linux does not include native OneDrive integration by default, so I needed a command-line client to connect and sync my files.

## Steps Taken

Installed a OneDrive client from the Arch repositories.

Command used:

sudo pacman -S onedrive

After installation, I ran the initial configuration command:

onedrive

This opened a login process where I authenticated with my Microsoft account.

## Observations

The setup required copying a login URL into the browser and pasting the authentication response back into the terminal.

After authentication, the OneDrive client created a configuration directory.

## Solution

After completing authentication, the OneDrive client successfully synchronized my files.

The command below can be used to start syncing manually:

onedrive --synchronize

## Lesson Learned

Many cloud services on Linux are managed using command-line clients.  
Once configured, they can synchronize files automatically or through scheduled jobs.
