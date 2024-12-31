# Automation-Script-For-ParrotOS-Installation
This is an automated script for installing ParrotOS in your computer as the sole OS. It is a modified program from the WSL version.

The key changes will focus on the following:

**Partitioning Configuration:** 

Ensure the preseed file configures the entire disk _(/dev/sda)_ for installation without leaving other OS remnants.

_partman-auto/choose_recipe select atomic_: Ensures the installer wipes the disk and uses a default partitioning scheme.

**Error Handling:** 

Enhance checks for USB device existence and ISO validity.

Added an explicit mount and unmount mechanism to handle the preseed file placement.

**Mount Points:** 

Configured _mount_point_ dynamically instead of hardcoding paths.

Adjust USB mounting and preseed placement for better portability even if it has no prior file system structure.

**Usage Notes:**

Replace _/dev/sda_ in the preseed file if the target installation disk has a different identifier.

Run this script with _sudo_ privileges to avoid permission issues.
