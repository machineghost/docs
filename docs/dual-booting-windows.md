---
title: Dual Booting with Windows
description: Learn how to install Pop!\_OS alongside Windows
---

Dual-booting alongside Windows takes a little more effort than [with a Linux-based OS](/docs/dual-booting) due to some quirks with how Windows does things.

## Fast Startup

Windows 8 and later uses a "Fast Startup" setting which prevents Windows from fully shutting down and allowing other OSes to use the disk. Before you can properly dual boot with Windows, you must disable this setting in Windows.

In your Windows install, open Control Panel and head to "Power Options". Select "Choose what the power buttons do", select "Change settings that are currently unavailable", then disable the "fast startup" setting. Note that Windows updates may occasionally turn this setting back on without asking, so if you are unable to boot into Pop!\_OS, check this setting first.

## Create Partitions

To dual boot Pop!\_OS alongside Windows, use the "Customize Partitions…" option when selecting a drive.

![Customize Partitions](/images/dual-booting/customize.png)

Use the "Modify Partitions…" button to open GParted, then select the wanted drive in the top-right of GParted.

![Modify Partitions](/images/dual-booting/modify.png)

Resize the desired partition down to make room for a Pop!\_OS partition. If your device is in EFI mode, create a new 512 MB FAT32 partition at the beginning of the unused space to be used as a Boot (/boot/efi) partition. Create a 4 GB swap partition at the end of the unused space. Create a partition from the the remaining space to be used as Root (/).

When you're ready, select the "Apply All Operations" icon at the end of the toolbar. Once the process is complete, close the GParted window and the installer will update with your changes.

![Apply](/images/dual-booting/gparted-apply.png)

## Choose Partitions

Select the new FAT32 partition, choose "Use partition", and select "Use as Boot (/boot/efi)". Select the new partition you created for the root, choose "Use partition", and select "Use as Root (/)". Select the new Swap partition, choose "Use partition", and select "Use as Swap".

![EFI](/images/dual-booting/efi.png)

## Erase and Install

Once you have your partitions selected, select the red "Erase and Install" button. This will apply your changes and begin the installation. When you restart your device after installing, it should automatically boot into Pop!\_OS where you can set up your user. Note that on BIOS installs, the Pop!\_OS entry may read "Ubuntu". To boot your other OS:

- If your device is in EFI mode, use your device's built-in boot menu.
- If your device is in BIOS mode, a menu will automatically appear when powering on.

Choose your previous OS with the arrow keys, then press Enter.
