# SSH Setup Between Arch Desktop and ThinkPad T480

Date: 2026-03-14

## Goal

Allow remote access to my Arch Linux desktop from my ThinkPad T480 using SSH.

This allows me to control the desktop remotely and recover the system if the terminal or desktop environment breaks.

## Problem

Initially SSH connections failed because the SSH server was not running on the desktop system.

## Steps Taken

Installed the OpenSSH package.

Command used:

sudo pacman -S openssh

Enabled the SSH service so it starts automatically at boot:

sudo systemctl enable sshd

Started the SSH service:

sudo systemctl start sshd

## Finding the Desktop IP Address

To determine the IP address of the Arch desktop, I used:

hostname -I

Example output:

192.168.1.xxx

## Connecting from the ThinkPad

From the T480 I connected using:

ssh kqesr@192.168.1.xxx

After entering the password, I was able to access the Arch desktop remotely.

The terminal prompt changed to:

[kqesr@archpc ~]$

## Result

I can now remotely access my desktop from the ThinkPad.

This will be useful for troubleshooting if the desktop environment or terminal fails.

## Lesson Learned

SSH is a powerful tool for remote system administration.

Having SSH enabled provides a recovery method if the graphical environment becomes unusable.
