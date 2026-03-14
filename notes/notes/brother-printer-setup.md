# Brother Printer Setup on Arch Linux

Date: 2026-03-14

## Goal

Set up my Brother multifunction printer on my Arch Linux workstation so I could print documents.

## Problem

The printer was not automatically recognized with the correct driver.  
CUPS detected the printer on the network but did not list the correct Brother driver.

## Steps Taken

1. Verified that the printer was visible on the network.
2. Installed printing utilities and drivers.
3. Used CUPS to search for available printers.
4. Attempted to add the printer through the web interface.

Commands used during troubleshooting:

sudo pacman -S cups
sudo systemctl enable cups
sudo systemctl start cups

Then opened the CUPS interface in the browser:

http://localhost:631

## Observations

CUPS detected the printer, but the correct Brother driver was not listed initially.

This required trying additional driver packages and confirming the printer model.

## Solution

After installing the appropriate driver and adding the printer through the CUPS interface, the printer appeared in the system and printing worked normally.

## Lesson Learned

Linux printing is managed through CUPS, and sometimes additional drivers must be installed for specific printer models.  
It is important to verify the printer model and driver compatibility when configuring printers on Linux systems.
