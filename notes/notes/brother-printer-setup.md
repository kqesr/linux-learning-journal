# Brother Printer Setup on Arch Linux

Date: 2026-03-14

## Goal

Set up my Brother multifunction printer so I could print from my Arch Linux desktop.

## Problem

The printer appeared on the network but the correct driver was not automatically available in the system.

This meant I could see the printer but printing did not work properly.

## Steps Taken

Installed and enabled the CUPS printing system.

Commands used:

sudo pacman -S cups
sudo systemctl enable cups
sudo systemctl start cups

Opened the CUPS web interface in the browser:

http://localhost:631

From there I attempted to add the printer.

## Observations

The printer was detected by CUPS but the correct Brother driver was not listed initially.

This required trying different driver options.

## Solution

After installing the correct driver and adding the printer through CUPS, the printer appeared in the system and printing worked.

## Lesson Learned

Printing on Linux is usually handled by CUPS.

Sometimes additional drivers are required depending on the printer model.
