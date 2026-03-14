# SSH Setup Between Arch Desktop and ThinkPad T480

Date: 2026-03-14

## Goal

Allow remote access to my Arch Linux desktop from my ThinkPad T480 using SSH.

This allows me to control the desktop remotely and recover the system if the terminal or desktop environment stops working.

## Problem

Initially I could not connect from the T480 to the desktop because the SSH server was not running.

## Steps Taken

Installed the OpenSSH package on the Arch desktop.

Command used:

sudo pacman -S openssh

Enabled the SSH service so it starts automatically at boot:

sudo systemctl enable sshd

Started the SSH service:

sudo systemctl start sshd

## Finding the Desktop IP Address

To determine the IP address of the Arch desktop I used:

hostname -I

This returned the local network IP address.

## Connecting from the ThinkPad

From the T480 I connected using:

ssh kqesr@192.168.x.x

After entering the password I was able to access the Arch desktop remotely.

The terminal prompt changed to:

[kqesr@archpc ~]$

## Result

SSH now works between my ThinkPad T480 and my Arch Linux desktop.

This allows remote access and provides a recovery method if the desktop terminal stops working.

## Lesson Learned

SSH is a powerful tool for remote system administration and troubleshooting.
