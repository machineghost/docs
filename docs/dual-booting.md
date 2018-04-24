---
title: Dual Booting
description: Learn how to dual boot Pop!_OS alongside another OS
---

To dual boot Pop!_OS alongside another OS, use the "Customize Partitions…" option when selecting a drive.

## Create a partition

If you already have an available partition that you want to erase and replace with Pop!_OS, skip to the next section.

If you don't have an available partition, you can create one using the "Modify Partitions…" button to open GParted. Select the correct drive in the top-right of GParted, then right-click the desired partition and select "Resize/Move". Resize the partition down to make room for a Pop!_OS partition, then select the "Resize/Move" button. Right-click the new "unallocated" space and select "New". Choose the filesystem you want (if unsure, keep the default ext4), then select the "Add" button.

When you're ready, select the "Apply All Operations" icon at the end of the toolbar. Once the process is complete, close the GParted window and the installer will update with your changes.

## Choose a partition

Select the partition on which you want to install Pop!_OS. Choose "Use partition" and select "Use as Root (/)". On EFI installs, you must also choose a Boot (/boot/efi) partition. One should exist from your other OS; choose it, and do not format it.

## Windows Caveats

Windows 8 and later uses a "Fast Startup" setting which prevents Windows from fully shutting down and allowing other OSes to use the disk. Before you can properly dual boot with Windows, you must [disable this setting in Windows](https://superuser.com/a/1152002/457793).
